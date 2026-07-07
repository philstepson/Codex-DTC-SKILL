# Nexus DTC Execute Navigation

## Browser And Auth

Use the user's authenticated in-app browser session. Do not automate credentials or MFA. If the session expires, ask the user to reauthenticate and continue from the same app context.

Use the in-app browser control skill and `node_repl` browser API when available. After connecting, inspect the selected tab and verify the current URL, page title, focused engagement, visible rows, and open drawers.

## Known Pages And Surfaces

- Page `647`: Execute Engagement focused engagement listing.
- Page `187`: Edit Engagement drawer. Use generated links from page 647; the drawer iframe is safer than direct URL construction.
- Page `44`: Select Account Opportunity or Revenue Lines drawer.
- Page `352`: Engagement Progress drawer.
- Page `69`: Update Engagement Results / milestone log drawer.
- Page `188`: Engagement Artifacts drawer.

## Focused Engagement Pattern

Use the app-generated URL when possible. If the user provides an engagement ID and the row is not focused, one focused navigation attempt is acceptable:

```text
https://<host>/ords/f?p=303:647:<session>:::647:P647_TRX_ENG_ID_FOCUS:<engagement_id>
```

Verify after navigation:

- `Engagement: ... (Id: <engagement_id>)` appears.
- The report shows `1 - 1 of 1`.
- The intended account name is present.

If the page falls back to many rows, use the app filter/search UI or refocus once. Do not loop through guessed URL variants.

## APEX Drawer Handling

Prefer clicking generated links in the row. After a drawer opens, inspect the iframe title:

- `Edit Engagement`
- `Select Account Opportunity or Revenue Lines`
- `Engagement Progress`
- `Update Engagement Results`
- `Engagement Artifacts`

Interact inside the iframe with frame locators. Do not click broad, repeated links without narrowing by href/title/text and confirming count.

## Verification After Writes

After clicking `Save`, `Apply Changes`, or `Add`, read the drawer or main page for explicit signals:

- success message such as `Row updated`
- updated audit fields
- changed linked opportunities
- changed heat/status/progress
- changed last updated by/on

Close the drawer and re-read the main engagement row. Summarize only app-visible results.
