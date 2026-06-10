# instabooth-admin

Git-synced admin data for the Instabooth multi-event setup.

## Layout

- `booth.json` — booth-global settings (cameras, GPIO, admin password, secrets)
- `events.json` — event registry (id, name, status, data_path, template_id)
- `active-event.json` — pointer to the currently active event's data folder
- `templates/{template-id}/` — reusable event templates (config + userdata assets)

## Event data

Per-event runtime data (media, database, cache) lives in `../instabooth-data/events/{event-id}/` and is **not** tracked in this repo.

## Statuses

`draft` → `published` → `active` ↔ `pause` → `done` → `archive` → `deleted`
