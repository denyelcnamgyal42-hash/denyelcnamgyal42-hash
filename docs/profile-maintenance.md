# Profile design and maintenance

The profile pairs a space-themed header with readable project descriptions and a contribution snake. Text and project links remain native Markdown so they stay readable on small screens and usable with assistive technology; every decorative SVG duplicates its message as plain text nearby.

There are **three** complete sets of decorative animated assets in `assets/`. Only one set is wired into `README.md` at a time — the other two stay in the repo, unused, so you can switch by changing a handful of `<img src>` paths rather than digging through git history.

## Active set: "orbit" (ringed planet / nebula / orbital arcs)

The most fully "space" of the three: soft nebula clouds, a layered starfield, a ringed planet at the frame's edge with a small probe that continuously orbits it (via an SVG motion path), and occasional meteors. Dividers, questions, and workbench use matching low orbital-arc paths (not straight lines) with a soft blue glow-pulse at each waypoint, echoing the header's orbit.

- `assets/header-orbit.svg`: the top banner.
- `assets/divider-orbit.svg`: a dotted rule with a small glowing comet traveling along it.
- `assets/questions-orbit.svg`: three points on a low arc, each glow-pulsing in turn, with the matching question from "Questions I'm exploring" printed underneath.
- `assets/workbench-orbit.svg`: six points on a low arc (Python, PyTorch, FastAPI, Docker, Linux, Git), each glow-pulsing in turn.
- `assets/pulse-star.svg`: a small twinkling 4-point star, used as a bullet marker next to the three areas in "What I'm spending time on."

## Kept but inactive

Two earlier designs are still in the repo, fully working, in case you want to switch back:

**"constellation / flowing path"** — line-art Himalayan ridge + dipper-style constellation, dashed lines that continuously flow, amber accent: `header-constellation.svg`, `divider-path.svg`, `questions-path.svg`, `workbench-path.svg`, `pulse-node.svg`.

**"orbital / terminal"** (the original) — a satellite drifting over Earth's night side, a typing terminal, glowing chip highlights, teal accent: `earth-night-header.svg`, `learning-terminal.svg`, `section-divider.svg`, `workbench-strip.svg`, `pulse-active.svg`.

**To switch sets:** in `README.md`, swap all six `<img src>` values (header, divider ×2, questions, workbench, pulse-dot ×3) to the other set's filenames, and update each `alt` text to match — the three sets describe themselves differently. `git log -p -- README.md` shows each past swap if you want exact wording to copy.

## Shared conventions (all three sets)

- The contribution snake is generated daily by `.github/workflows/contribution-snake.yml` and published to the `output` branch. Its two images support light and dark themes; that animation is Platane/snk's own and isn't guaranteed to respect reduced motion.
- All custom graphics use local, hand-written SVG — no external fonts, scripts, or image-generation services — and animate with plain CSS (plus one SMIL `animateMotion` for the orbiting probe) inside the SVG file, which is what lets them animate at all inside a GitHub-rendered `<img>`.
- Every custom SVG respects `prefers-reduced-motion` (animation is disabled rather than just slowed — the orbiting probe and meteor are hidden outright) and adapts colors to `prefers-color-scheme` where it renders on the page background (the headers are an intentional exception — always dark, like a hero image).
- Every decorative SVG has a plain-Markdown equivalent nearby — the questions/tools graphics duplicate the "Questions I'm exploring" list and the "Python, PyTorch, ..." sentence — so nothing is lost if the SVG fails to load or animation is off.

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
