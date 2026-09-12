# Profile design and maintenance

The profile pairs a Bhutan-inspired orbital header with readable project descriptions, an animated "questions" terminal, and a contribution snake. Text and project links remain native Markdown so they stay readable on small screens and usable with assistive technology; every decorative SVG duplicates its message as plain text nearby.

## Assets

- `assets/earth-night-header.svg`: the top banner — a satellite drifts along an orbital trail above Earth's night side, with an occasional shooting star. Respects reduced motion (animation is disabled, and the meteor is hidden, when the viewer's OS requests it).
- `assets/learning-terminal.svg`: an animated terminal that types out the three questions from "Questions I'm exploring." Purely decorative — the same three questions are listed as plain Markdown directly below it. Adapts to light/dark and respects reduced motion.
- `assets/pulse-active.svg`: a small pulsing dot used as a bullet marker next to the three areas in "What I'm spending time on," signaling that all three are current, active focus areas (not a claim about any one project's status).
- The contribution snake is generated daily by `.github/workflows/contribution-snake.yml` and published to the `output` branch. Its two images support light and dark themes; that animation is Platane/snk's own and isn't guaranteed to respect reduced motion.

All custom graphics (header, terminal, pulse dot) use local, hand-written SVG — no external fonts, scripts, or image-generation services — and animate with plain CSS/SMIL inside the SVG file, which is what lets them animate at all inside a GitHub-rendered `<img>`.

## Keeping the profile useful

Update the three selected projects when stronger work becomes available. Describe what each project does and what it demonstrates; avoid unverified performance claims. Update the learning paragraph, the terminal's three questions, and the plain-text "Questions I'm exploring" list together when your interests change — they're meant to stay in sync.

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

Preview at desktop and phone widths, in both color schemes. Check SVG parsing, image loading, project links, reduced-motion behavior (browser/OS setting for "reduce motion"), the terminal's text against the plain-text list below it, and the contribution workflow after changes. A local Markdown preview approximates GitHub styling; the published GitHub page is the final rendering authority.
