# odoo_data_sync_odoo20

Hasil migrasi suite **odoo_data_sync** (Odoo 13 → Odoo 20).

| Sumber | Target |
|---|---|
| `~/odoo_13/odoo_data_sync/` (branch main, versi 13.0.x) | `~/odoo_20/<modul>/` (versi 20.0.x) |

## Urutan migrasi (sesuai dependensi)
1. `amr_jsonrpc` (fondasi)
2. `amr_data_sync` (core)
3. `amr_data_sync_api`, `amr_data_sync_event`, `amr_data_event`, `amr_data_push`
4. `amr_data_sync_queue`, `amr_data_sync_hr`, `amr_data_sync_resource`

## Dependensi eksternal
- `amr_resource`, `amr_service_client` — perlu repo/versi terpisah
- `queue_job` (OCA) — cek compat Odoo 20; bila belum, refactor ke pattern native
