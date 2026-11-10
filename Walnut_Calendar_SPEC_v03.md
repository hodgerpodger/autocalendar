# Walnut Automatic Calendar — Spec v0.3

**The renders are the spec.** If anything below conflicts with them, the renders win.

| Ivory | Charcoal |
|---|---|
| ![Ivory](Walnut_Calendar_Ivory.png) | ![Charcoal](Walnut_Calendar_Charcoal.png) |

**Goal:** a commercial product eventually. First milestone: a working prototype that looks like the renders.

## 1. What it is
- A walnut block with three recessed windows showing **weekday · month · day**, for example `MON · NOV · 09`.
- It updates itself at midnight and never needs flipping or resetting by hand.
- **It must look non-electronic.** The date is shown by printed physical material, with no screen of any kind (LCD, OLED or e-ink). From the front, nothing reveals that there are electronics inside.
- **It shows nothing else:** no time, agenda, weather, app, lights or logo.

## 2. Look (from the renders)
**Looking beautiful is the only hard requirement.** Every dimension below is a rough target estimated from the renders. Change any of them freely if the result looks better or the mechanism needs the room. Judge it on the paper mockup and later prototypes, not on the numbers.

| Item | Estimate |
|---|---|
| Body | ~9" W × ~3.4" H, depth TBD (target ≤ 3.5") |
| Corners/edges | Large soft radius on all edges (~0.4–0.5") |
| Windows | 3, each ~1.5" tall; widths ~2.5" / 2.4" / 2.2" (weekday / month / day) |
| Dividers | ~0.2–0.25" walnut between windows |
| Side margins | ~0.55" walnut to the left/right of the outer windows |
| Window recess | Stepped bevel ~0.1", panel set back below the wood surface, rounded inner corners |
| Cap height | ~0.47" |
| Cover | **None.** Open recess with no glass or acrylic, as shown in the renders |

- **Text:** all uppercase and centred.
  - Weekday, abbreviated to 3 letters: `MON TUE WED THU FRI SAT SUN`
  - Month, abbreviated to 3 letters: `JAN FEB MAR APR MAY JUN JUL AUG SEP OCT NOV DEC`
  - Day, always 2 digits with a leading zero: `01`–`31`
- **Font:** bold geometric sans. The renders look like Montserrat SemiBold/Bold. Candidates: Montserrat, Jost, Outfit (all freely licensed).
- **Colourways:**
  - Ivory: warm matte ivory panel, espresso/near-black text.
  - Charcoal: matte near-black panel, warm ivory text.
  - Walnut, type and layout are identical in both.
- **Day panel:** one seamless panel. **No visible seam between the digits.**
- **Unequal window widths:** the renders show windows getting slightly narrower from left to right. Decide on the paper mockup whether to keep this or make all three equal.

## 3. Mechanism direction
**Roller-blind scroll per window.** A printed film strip winds between two spools and passes flat behind the window, like an old bus destination sign.
- This is the only approach found so far that gives a flat, seamless panel like the renders. Drums are far too big at this window size (a 31-position date drum would be ~15" in diameter), and split-flaps show a seam and are noisy.

| Window | Frames | Strip length (approx.) |
|---|---|---|
| Weekday | 7 | ~11" |
| Month | 12 | ~19" |
| Day | 31 | ~50" (single strip) |

- **Registration:** a printed mark on the film edge for each frame, read by an optical sensor. Alignment is closed-loop, and the device can find its own position again after a power loss.
- **Rewind:** at month-end the day strip rewinds from 31 back to 01 (and the weekday strip from SUN to MON, and so on). This happens at midnight.
- **Colourway:** set entirely by the printed film. One mechanism serves both colourways.
- **Must hold:** the film is flat with no ripple in the window, each frame stops centred within ~0.5 mm, neighbouring frames are never visible at rest, and the drive is quiet enough for a bedroom.

## 4. Electronics (hidden)
- Microcontroller plus a battery-backed real-time clock (e.g. DS3231 with a coin cell). Date logic covers month lengths, leap years and weekdays.
- One drive solution per window: either two motors (one per spool) or one motor with a spring take-up.
- Power from a USB-C port on the back for the prototype. Battery-only power is a candidate for the product.
- Setting the date and calibration use buttons concealed on the back or underside.

## 5. Prototype plan
1. **Paper mockup.** Printed cards in a cheap shell to confirm body size, window sizes, recess, font and both colourways against the renders.
2. **Weekday test rig.** One roller-blind window. Measure flatness, stopping accuracy, noise and depth.
3. **Day window.** The 50" strip, rewind behaviour, and whether spool size fits the depth.
4. **Full mechanism.** All three windows, firmware, and power-loss recovery.
5. **Walnut enclosure.** Build it around the proven mechanism, with a removable back for service.

## 6. Open questions
- Final depth.
- Film material and printing method (ivory text on charcoal needs UV or screen printing).
- Motor type and noise target.
- Solid walnut or veneer.
- Prototype → product cost targets.
