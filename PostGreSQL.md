# Allgemeines
- [Confluence Seite zu PostGreSQL]([PostgreSQL - PaaS - DATEV Engineers](https://confluence.datev.de/display/PAAS/PostgreSQL))
- [PostGreSQL Desaster Recovery Anleitung]([Disaster Recovery (PostgreSQL) - PaaS - DATEV Engineers](https://confluence.datev.de/pages/viewpage.action?pageId=54449696#DisasterRecovery(PostgreSQL)-BestPractice))
- freies objektrelationales Datenbankmanagementsystem. 
- ist weitgehend konform mit dem SQL-Standard
- Open-Source
- Ab 80% Speicherauslastung der DB droht Ausfall der DB bzw. Ausfälle beim Speichern der Daten!!! Deshalb maximal bis 70% Speicher belegen, danach wird eine größere Instanz benötigt!!!
- Das Admin-Team von CF spielt automatisiert Minor-Updates für PostGreSQL innerhalb einer Major-Version ein. Zuerst werden DEV-Stages aktualisiert, dann QS und am Schluß PROD. Updates werden per Cloud-Blog angekündigt. Updates können bei Bedarf für einige Tage verschoben werden oder auf bestimmte Zeiten gelegt werden.
- Update-Ausnahme: Im Fall kritischer Sicherheitslücken werden Updates zwangsweise auf alle Serviceinstanzen ausgerollt.
- Es gibt für PostGreSQL ein Management Dashboard für die Administration.

# Backup & Restore
## Backup
- Backups werden verschlüsselt und komprimiert im S3 abgelegt und sind Serviceinstanz-spezifisch. Es werden immer Vollsicherungen erstellt. Ein Point in Time-Restore ist standardmäßig nicht möglich. Während eines Backups kann das System weiter verwendet werden. Täglich werden nach einem festen Zeitplan Backups angelegt. Jedes Backup ist ein Dump. Alle Änderungen nach Beginn des Backups sind nicht im Backup enthalten.
- Seit 01/2024 ist es versuchsweise möglich, ein Continuous Archiving zu provisionieren, wodurch ein Point in Time Restore möglich ist.
- Es existiert ein Splug-Alert, falls auf PROD ein Backup alter als 30 Stunden ist.
- Backups werden auf DEV und QS 7 Tage aufgewahrt, auf PROD 28 Tage - gilt auch für gelöschte Instanzen.
- Backups lassen sich über das Management Dashboard anlegen.
- Backups können aus dem Management Dashboard herunter geladen werden.
- Vor manuellen Änderungen muss ein zusätzliches Backup erstellt werden!!!!

## Restore
- **Vor einem Restore muss die App gestoppt werden**
- Nach einem Restore kann es notwendig sein, die App erneut an die DB zu binden.
- Eine Nacharbeit nach dem Restore kann mehrere Minuten dauern und das System ist dann nicht verwendbar.
- Ein Restore kann über das MAnagement Dashboard angestoßen werden
