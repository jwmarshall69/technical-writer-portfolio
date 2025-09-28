# Sample — Release Notes

## 2025‑08‑12

- Added `GET /items/{id}` filters (`status`, `ownerId`)
- Deprecated `GET /legacy-items`
- Fixed 429 retry headers in Sandbox

**Upgrade notes**: Migrate to `/items` with `status=active` by 2025‑12‑01
