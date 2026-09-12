# Profile design and maintenance

The profile pairs a Bhutan-inspired header with readable project descriptions and a contribution snake. Text and project links remain native Markdown so they stay readable on small screens and usable with assistive technology; every decorative SVG duplicates its message as plain text nearby.

There are two complete sets of decorative animated assets in `assets/`. Only one set is wired into `README.md` at a time — the other stays in the repo, unused, so you can switch back by changing a handful of `<img src>` paths rather than digging through git history.

## Active set: "constellation / flowing path"

A minimal line-art style: dashed lines that continuously flow (like current along a wire) rather than glow or type, gold/amber accent, a hand-drawn mountain ridge and star constellation instead of a literal space scene.

- `assets/header-constellation.svg`: the top banner — a line-art Himalayan ridge and a small dipper-style constellation, both traced in flowing dashed light, with two accent stars that pulse.
- `assets/divider-path.svg`: a thin dashed rule with one small dot continuously traveling along it, used between major sections instead of blank space.
- `assets/questions-path.svg`: three waypoints on a line, each pulsing in turn, with the matching question from "Questions I'm exploring" printed underneath — the visual and the text always show the same three questions.
- `assets/workbench-path.svg`: six waypoints (Python, PyTorch, FastAPI, Docker, Linux, Git) on a line, each pulsing in turn.
- `assets/pulse-node.svg`: a small pulsing amber dot, used as a bullet marker next to the three areas in "What I'm spending time on."

## Kept but inactive: "orbital / terminal"

The earlier design — a satellite drifting over an Earth's-night-side horizon, a typing terminal, and glowing chip highlights, in a teal accent. Nothing in `README.md` currently points at these, but they're fully working if you want them back.

- `assets/earth-night-header.svg`, `assets/learning-terminal.svg`, `assets/section-divider.svg`, `assets/workbench-strip.svg`, `assets/pulse-active.svg`.

**To switch back:** in `README.md`, swap `header-constellation.svg` → `earth-night-header.svg`, `divider-path.svg` → `section-divider.svg` (both occurrences), `questions-path.svg` → `learning-terminal.svg`, `workbench-path.svg` → `workbench-strip.svg`, and `pulse-node.svg` → `pulse-active.svg` (all three occurrences). Update the `alt` text on each `<img>` to match, since the two sets describe themselves differently.

## Shared conventions (apply to both sets)

- The contribution snake is generated daily by `.github/workflows/contribution-snake.yml` and published to the `output` branch. Its two images support light and dark themes; that animation is Platane/snk's own and isn't guaranteed to respect reduced motion.
- All custom graphics use local, hand-written SVG — no external fonts, scripts, or image-generation services — and animate with plain CSS inside the SVG file, which is what lets them animate at all inside a GitHub-rendered `<img>`.
- Every custom SVG respects `prefers-reduced-motion` (animation is disabled rather than just slowed) and adapts colors to `prefers-color-scheme` where it renders on the page background (the headers are an intentional exception — always dark, like a hero image).
- Every decorative SVG has a plain-Markdown equivalent nearby — the terminal/path questions duplicate the "Questions I'm exploring" list, the chip/waypoint strip duplicates the "Python, PyTorch, ..." sentence — so nothing is lost if the SVG fails to load or animation is off.

## Keeping the profile useful

Update the three selected projects when stronger work becomes available. Describe what each project does and what it demonstrates; avoid unverified performance claims. Whichever asset set is active, update its questions/tools graphic and the matching plain-text list together when your interests change — they're meant to stay in sync.

The next useful improvements are in the linked repositories:

1. Pin the three featured projects through GitHub's **Customize your pins** control.
2. Add a short repository description to each project; all three were empty when reviewed.
3. Fill the empty Snake and booking-assistant READMEs with an overview, setup instructions, a screenshot or demo, and limitations.
4. Replace the password lab's chart placeholders with its actual results and explain the experiment settings.

These are recommendations, not changes made to those repositories or your account settings.

## Research and design references

- [GitHub: using your profile to enhance your resume](https://docs.github.com/en/account-and-profile/tutorials/using-your-github-profile-to-enhance-your-resume): project selection and explaining your work.
- [GitHub: pinning items](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/pinning-items-to-your-profile): up to six pinned repositories and gists.
- [Platane/snk](https://github.com/Platane/snk): contribution animation, SVG-only generation, custom palettes, and theme selection.
- [lowlighter/metrics](https://github.com/lowlighter/metrics): evaluated as an optional statistics system. Not added; project evidence is more useful for this profile at its current stage.

## Validation

Preview at desktop and phone widths, in both color schemes. Check SVG parsing, image loading, project links, reduced-motion behavior (browser/OS setting for "reduce motion"), the animated text/labels against their plain-text equivalents, and the contribution workflow after changes. A local Markdown preview approximates GitHub styling; the published GitHub page is the final rendering authority — and only reflects what's been pushed to `main`.
