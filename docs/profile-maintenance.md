# Profile design and maintenance

The profile pairs a Bhutan-inspired orbital header with readable project descriptions, a terminal learning log, and a contribution snake. Text and project links remain native Markdown so they stay readable on small screens and usable with assistive technology.

## Assets

- `assets/banner.svg`: desktop header with orbital motion.
- `assets/banner-mobile.svg`: larger type and a simpler composition for screens up to 600px wide.
- `assets/learning-terminal.svg`: an illustrative learning log with progressive text reveals. It does not display live commands or statistics.
- The contribution snake is generated daily by `.github/workflows/contribution-snake.yml` and published to the `output` branch. Its two images support light and dark themes.

The custom SVGs respect reduced-motion preferences. The third-party contribution snake may continue animating. The terminal also adapts to the viewer's color scheme. All custom graphics use local SVG code without external fonts, scripts, or image services.

## Keeping the profile useful

Update the three selected projects when stronger work becomes available. Describe what each project does and what it demonstrates; avoid unverified performance claims. Update the learning paragraph when your interests change.

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

Preview at desktop and phone widths, in both color schemes. Check SVG parsing, image loading, project links, reduced-motion behavior, and the contribution workflow after changes. A local Markdown preview approximates GitHub styling; the published GitHub page is the final rendering authority.
