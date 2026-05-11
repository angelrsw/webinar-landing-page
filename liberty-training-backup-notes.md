# liberty-training-backup-copy.html — Backup Notes

**Created:** 2026-04-28
**Source file:** wp-injectable.html (last delivered version, 98,794 bytes)
**Live WP page modified date:** 2026-04-24T11:03:23

## Known deltas between this backup and the LIVE WP version

The live WP page (~102KB inside `[vc_raw_html]`) is ~3.7KB larger than this
backup. The difference is CSS that was appended during the 2026-04-28 session:

1. Mobile hero stacking fix (resets forced grid placement on `.hero-grid` children below 960px)
2. Hide theme bullet dots inside `#webinar-lp` lists (override `li::before { content: '•' }`)
3. Center the `#contactModal` dialog with full-viewport backdrop

If you need to restore exactly to the live state from this backup, either:
- Re-paste this file into WPBakery raw HTML and re-apply the three CSS blocks
  documented in the 2026-04-28 chat (mobile hero / bullets / modal), OR
- Pull the current state via WP REST API:
  `GET /wp-json/wp/v2/pages/13093?context=edit&_fields=content`
  (decode: base64 → URL-decode the inner `[vc_raw_html]` payload).

## Restoration procedure

1. Edit page 13093 in WP admin (Classic Editor + WPBakery)
2. Open the Raw HTML element
3. Replace the contents entirely with this file's contents
4. Re-apply the documented CSS deltas
5. Update
