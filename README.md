# MixEhr — Releases

MixEhr is a set of transition plugins for Resolume Arena: 375 transitions in 16 families, each family one FFGL mixer
you can pick as a layer's blend mode, as the layer transition or as a clip transition, with a Style dropdown and its own controls per style.

This repository hosts the releases of MixEhr. The source code is private. Bug reports are welcome in the [Issues tab](../../issues).

**How-to for new users** (below): [a. What it is](#a-what-it-is) · [b. Download and install](#b-download-and-install) ·
[c. Where it shows up in Arena](#c-where-it-shows-up-in-arena) · [d. Pick a family and a style](#d-pick-a-family-and-a-style) ·
[e. The panel](#e-the-panel) · [f. What the controls do](#f-what-the-controls-do) · [g. Styles that use a file](#g-styles-that-use-a-file) ·
[h. Saving](#h-saving) · [i. The 16 families](#i-the-16-families) · [j. Help and licence](#j-help-and-licence)

**Every style and its controls: [STYLES.md](STYLES.md).**

## a. What it is

16 plugins named **MixEhr &lt;Family&gt;** (MixEhr Slide, MixEhr Wipe, MixEhr 3D …). Each one holds a whole family of
transitions: slides, dissolves, wipes, zooms, 3D flips, glitches, light effects and more. You choose the family where Arena lists
transitions, then choose the look from its **Style** dropdown and shape it with that style's own controls.

## b. Download and install

**[Latest release](../../releases/latest)** — `MixEhr-1.0.0-macOS.zip`. macOS only, universal (Apple Silicon and Intel).
The bundles are signed with a Developer ID and notarised by Apple. Tested in Resolume Arena 7.28.1.

1. Unzip `MixEhr-1.0.0-macOS.zip`. You get a folder `MixEhr` with 16 `.bundle` files and `NOTICES.txt`.
2. Copy the `.bundle` files into `~/Documents/Resolume Arena/Extra Effects/` (create the folder if it is not there).
3. Restart Arena. The plugins appear as **MixEhr <Family>** in the blend mode and transition lists.

You can install only the families you want; each bundle works on its own.

## c. Where it shows up in Arena

Each family appears once in each of Arena's three lists:

- **Clip transition** — the clip's own transition, set in the clip panel's **Transition** tab.
- **Layer transition** — the transition the layer uses when it goes from one clip to the next.
- **Blend mode** — in the layer's blend mode list, next to Arena's own blend modes.

How long a transition takes is set by Arena's own transition duration, as with Arena's built-in transitions.

## d. Pick a family and a style

1. Choose a family (for example **MixEhr Wipe**) as the clip or layer transition.
2. Open its **Style** dropdown and pick a look (for example *Clock Wipe*). All styles are listed in [STYLES.md](STYLES.md).
3. Trigger a clip to see it. Change Style and trigger again to try the next one.

Each style keeps its own settings: switching Style and back leaves your settings where they were.

## e. The panel

At the top of the panel are the controls every style shares: **Style**, **Curve**, **Ends At**, and in some families
**Angle** and **File**. Below them, every style of the family has a **heading row with its name**, followed by that style's own
controls (Columns, Softness, Background …).

Arena shows **all** styles' sections in the panel, whatever Style is picked. Only the section under the heading of the style you
picked does anything; leave the others alone. Scroll to your style's heading to find its controls.

## f. What the controls do

- **Start from the default.** A slider at **0.5**, a switch **off**, a colour with alpha **0** and **Angle 0** give the style's
  own default look.
- **Sliders**: 0.5 is the default; towards 0 is less, towards 1 is more (up to deliberately "too much").
- **Switches**: off is the default; on flips it (Reverse, Vertical, Clockwise …).
- **Colours**: a colour picker whose **alpha** says how much of your colour replaces the style's own. Alpha 0 = the style's own
  colour, alpha 1 = your colour.
- **Curve**: the easing of the motion (Linear, Smooth, Ease In, Ease Out, Ease In Out, Sine, Expo, Quart). Default Smooth.
- **Ends At**: the point in the transition where the new clip is fully reached (0.5–1, default 0.9). Arena ends a transition a
  little before its very end, so the default makes sure you always land exactly on the new clip. Lower it to finish the effect earlier.
- **Angle**: turns the style's direction, in degrees counter-clockwise from its own direction (0 = its default direction). Styles
  without a direction ignore it.
- **Debug Log**: leave off. It writes one line per transition to the macOS log, useful for bug reports.

## g. Styles that use a file

Some styles read a picture from the shared **File** control at the top of the panel:

- **MixEhr Luma** — *Luma Wipe* and *Luma Map Wipe*: a grey-scale picture decides the order in which the screen changes.
- **MixEhr Warp** — *Displacement Map*: a grey-scale picture bends the image.
- **MixEhr Stinger** — the four *Logo* styles use your logo picture; *Stinger Matte* uses a stinger.

Pick a PNG or JPG; a stinger can also be a DXV `.mov`, which then runs along with the transition. With no file chosen these styles
use a built-in grey ramp, so they still work.

## h. Saving

Everything you set (family, Style, every control) is saved with your Arena composition and comes back when you open it again.

## i. The 16 families

| Family | Styles | Family | Styles |
|---|---|---|---|
| MixEhr 3D | 41 | MixEhr Luma | 15 |
| MixEhr Blur | 8 | MixEhr Optical | 8 |
| MixEhr Dissolve | 37 | MixEhr Organic | 11 |
| MixEhr Geometric | 36 | MixEhr Pattern | 21 |
| MixEhr Glitch | 18 | MixEhr SeamWork | 33 |
| MixEhr Light | 21 | MixEhr Slide | 27 |
| MixEhr Stinger | 6 | MixEhr Warp | 39 |
| MixEhr Wipe | 42 | MixEhr Zoom | 12 |

Every style in each family, with its own controls: [STYLES.md](STYLES.md).

## j. Help and licence

Questions and bug reports: the [Issues tab](../../issues). For a bug, say the family, the style and your Arena version.

Free to use; proprietary binaries. See [LICENSE](LICENSE). Third-party notices (gl-transitions MIT attribution and others):
[NOTICES.txt](NOTICES.txt), also inside the zip and inside every bundle.
