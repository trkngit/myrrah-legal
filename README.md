# Myrrah legal

The published privacy policy, served at
<https://trkngit.github.io/myrrah-legal/>.

This repository is public so that an app store reviewer can open the
policy without a GitHub account. It holds nothing else.

## Do not edit index.md here

The source of truth is `docs/PRIVACY.md` in the application repository,
where a CI gate holds the signup consent text to this policy. A change
made here instead would pass that gate while the published document and
the app disagreed, which is the one failure this split introduces.

To update: change `docs/PRIVACY.md` there, then regenerate `index.md`
from it. The only transformation is that GitHub callout syntax
(`> [!NOTE]`) becomes a bold lead-in, because the Jekyll renderer that
serves this page does not understand it.
