# Walnut Automatic Calendar
## Product Design Specification — v0.2

**Status:** Concept brief / agent handoff  
**Canonical visual references:** [`design/light-ivory.png`](design/light-ivory.png) and [`design/dark-charcoal.png`](design/dark-charcoal.png). These are concept renders, not verified mechanical designs.  
**Primary objective:** Create a beautiful, non-electronic-display desk calendar that automatically shows the current weekday, month, and day of month.

## 1. Product vision
A timeless, architectural desk object rather than a tech gadget. A compact, solid-looking dark walnut enclosure with softly rounded edges and three inset date windows available in warm ivory or matte charcoal. The user sees only today's date. The mechanism is hidden, movement is unobtrusive, and no screen, LEDs, exposed gears, or adjacent dates are visible.

**Example display:** `MON   NOV   09` (illustrative only; automatically tracks actual date).

## 2. Visual direction — preserve
- **Form:** Low, horizontal, monolithic rectangular block; gently radiused corners and edges; restrained proportions.
- **Material appearance:** Rich medium-to-dark walnut with visible natural grain, satin/matte finish, no glossy plastic appearance.
- **Face:** Three separate, evenly aligned recessed rectangular windows; subtly rounded inner corners; walnut dividers between windows.
- **Display colorways:** (1) **Light / Ivory**: warm matte ivory panels with dark espresso/near-black lettering; (2) **Dark / Charcoal**: deep matte charcoal panels with warm ivory lettering. Same walnut enclosure for both.
- **Typography — locked direction:** **Modern Contrast**, a clean, bold geometric sans-serif, consistent across both colorways. Medium-bold to bold weight, centered text, generous clear shapes; not serif, italic, stencil, dot-matrix, or digital seven-segment. Exact font family remains to be selected after physical legibility and fabrication testing.
- **Shared design:** Both colorways use identical window proportions, letterforms, font weights, layout and mechanism. Color/finish is the only intended variant. No labels, logos, icons, or ornamental markings on the front.
- **Layout:** Weekday on left, month in middle, numeric date on right. Only the active values visible; no glimpses of neighboring characters or dates.
- **Overall mood:** Quiet, premium, minimal, warm, furniture-like. Not industrial, steampunk, retro train-station signage, or visibly electronic.

## 3. Target envelope (provisional)
- Approximately **9 in wide × 3.5 in high × 3 in deep** (229 × 89 × 76 mm).
- Desktop-first, stable on a flat surface; discreet non-slip feet.
- Dimensions may change to accommodate a robust mechanism; preserve the compact horizontal silhouette.
- Wall mounting is a possible future variant, not a v1 requirement.

## 4. Functional requirements
**Must have**
1. Automatically display the correct **weekday, month, and day of month**.
2. Change date daily without manual flipping, rotating, or resetting under normal operation.
3. Handle 28/29/30/31-day months, leap years, and weekday progression correctly.
4. Use **physical printed/painted/mechanical elements** to display the date. No LCD, OLED, e-ink, or projected date display.
5. Hide moving parts and adjacent dates from normal front viewing angles.
6. Maintain alignment and readability after repeated date changes.
7. Provide a straightforward way to set/correct the date and recover after power loss.

**Strong preferences**
- Quiet operation; clicking or flapping noise is not a goal.
- No always-on illumination or status lights visible on the front.
- No visible cable from the front; discreet rear or underside connection acceptable.
- Replaceable/serviceable mechanism and accessible setup controls, concealed from the front.

**Optional / future**
- Battery-powered operation with long battery life.
- Automatic time synchronization; timezone and daylight-saving setup.
- Full weekday names instead of three-letter abbreviations.
- Alternate woods, sizes, or wall-mounted variants. Typography changes require explicit design approval.

## 5. Mechanism — intentionally open
Potential approaches include enclosed rotating drums/wheels, individual digit wheels, sliding cards/tiles, or other motor-driven physical indicators. **Do not assume three full-size drums will fit**: a 31-position date drum may be too large for the desired enclosure. A single visually unified date window can conceal two separately driven digit mechanisms.

Agents should compare concepts by overall size, visual quality, reliability, noise, cost, ease of fabrication, and calibration. No specific mechanism is approved yet.

## 6. Electronics and control — implementation-neutral
A microcontroller, clock source, sensors, and motors may be used internally. Electronics are allowed for timekeeping and motion control, **not as the visible date display**. A prototype may use USB power; a battery-backup clock or other recovery scheme should avoid date drift or loss of settings. Provide a manual setting/calibration workflow.

## 7. Suggested prototype strategy
**Phase A — feasibility:** Demonstrate one mechanically changing field behind an opaque window with no adjacent values visible. Measure noise, alignment, and depth.

**Phase B — complete display:** Integrate weekday, month, and date, including month-end transitions and leap-year logic. Validate restart/recovery behavior.

**Phase C — aesthetic prototype:** Build the walnut-look enclosure (e.g., veneer over fabricated structure), test both ivory and charcoal display surfaces with identical Modern Contrast typography; refine window edges and physical print quality.

**Phase D — finished object:** Improve serviceability, power routing, repeatability, material finish, and long-term reliability.

## 8. Acceptance criteria
- From typical desk-viewing distance, reads cleanly as **one walnut object with three matching date windows (ivory or charcoal)**.
- No other dates, moving parts, electronics, or labels visible on the front.
- Displays weekday/month/date correctly across month-end, year-end, and leap-day tests.
- Changes automatically on schedule, without a daily user action.
- Mechanism stays aligned and does not visibly jam over extended cycle testing.
- Appearance remains faithful to the two canonical renders, including the identical Modern Contrast typography, even if the internals differ.

## 9. Open decisions for later agents
- Exact physical indicator mechanism and drive train.
- One combined date assembly versus separate tens/ones mechanisms.
- Exact geometric sans-serif font selection, window dimensions, and final enclosure depth (font style is fixed).
- Solid walnut versus walnut veneer over structural shell.
- Power architecture and backup duration.
- Date setting interface, calibration sensing, and noise target.
- Prototype BOM, fabrication plan, CAD, firmware, and cost estimate.

## 10. Agent handoff instruction
> Treat the reference image and sections 1–4 as the design intent. Propose implementation options without changing the visible walnut three-window aesthetic, in both approved ivory and charcoal colorways. Identify physical constraints and tradeoffs explicitly. Do not silently replace the physical display with a digital screen. Begin with a feasibility analysis and one-field proof of concept before committing to a full CAD architecture.

## 11. Visual references and version control
- `design/light-ivory.png` — canonical light colorway, Modern Contrast typography.
- `design/dark-charcoal.png` — canonical dark colorway, **same** Modern Contrast typography.
- Images are aspirational appearance references; they do not prove a feasible mechanism, dimensions, material construction, or manufacturing tolerances.
- Keep both references in the repository and link them in agent briefs. Avoid replacing either with older serif-font concepts.
- When proposing a mechanism, preserve a single clean visible value in each recessed window; adjacent dates and internal hardware must stay hidden.

## 12. Decisions recorded in v0.2
1. Desktop form factor first, wall variant later if desired.
2. Walnut housing and softly rounded architectural block shape approved.
3. Two approved display colorways: light ivory and dark charcoal.
4. **Modern Contrast geometric sans-serif typography approved for both**, replacing the earlier serif direction.
5. Date display remains physical and automatically advancing; mechanism is intentionally unresolved.
