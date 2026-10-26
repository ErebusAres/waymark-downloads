# Waymark 0.5.17

- Retires online character profiles, player search, cloud saves and remote usage reporting.
- Removes View online and Website & sync from the desktop app. The native usage timer no longer schedules cloud sync; legacy worker cloud commands are offline stubs and cannot upload data.
- The website remains available for downloads and help. Legacy tracking endpoints return HTTP 410 before parsing uploads, authenticating devices or accessing D1/R2, so older clients stop syncing when they next contact the service.
- Local pet tracking, character progress, collection marks, settings, pins, routes, minimap layout, usage statistics and local backups continue to work. A saved selection of the former cloud settings page returns to General.
- Existing remotely stored records have been preserved and are no longer served as profiles or cloud downloads. This update does not delete stored databases or backups.

App updates still use the signed GitHub release feed. The website and download hosts still handle normal visitor/download requests; the retired tracking API does not read or write tracking storage.
