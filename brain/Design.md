# Design.md

## Vibe
Dark, premium, data-forward. Echoes Manthan's navy + gold look so it feels native to the event, but dashboards must stay readable.

## Color tokens
| Token | Hex | Use |
|---|---|---|
| --bg | #0A111A | page background |
| --surface | #0F1823 | cards |
| --border | #243042 | hairlines |
| --gold | #E8A83A | primary accent, CTAs, highlights |
| --cream | #F2E8D5 | headings, key text |
| --text | #C9CFD6 | body |
| --muted | #7C8794 | secondary |
| --success | #3DDC97 | normal / good |
| --warn | #F5B942 | warning |
| --danger | #FF5C5C | anomaly / alert |
| --forecast | #5BC0EB | predicted line |
(Adjust if PS has a brand/sector feel, e.g. green for agri, blue for health.)

## Typography
- Headings: Playfair Display (serif, 600–700)
- Body/UI: Inter or Manrope (400–600)
- Numbers/labels: JetBrains Mono, uppercase, letter-spacing 0.15em for small labels
- Scale: 12 / 14 / 16 / 20 / 28 / 40; line-height 1.5 body

## Layout
- 8px spacing grid, max width 1280, cards radius 12, 1px border, subtle shadow
- Top bar: logo, status pill (LIVE/REPLAY), time range
- Row 1: 4 KPI cards. Row 2: main chart (2/3) + alerts (1/3). Row 3: insights/explain.
- Mobile: stack, charts full width

## Chart rules
Actual = cream/white solid; Predicted = --forecast dashed; Confidence = 15% opacity band; Anomaly = red dot with tooltip; animate gently (≤300ms).

## UX must-haves
Live indicator pulse, skeleton loaders, friendly errors, tooltips with units, empty states, keyboard-friendly, contrast ≥ 4.5:1, one clear primary action per screen.

## Don't
More than 2 fonts + mono, rainbow charts, tiny text <12px, heavy animations that hurt the demo.
