# Myrrah legal

The published privacy policy and child safety standards, served at
<https://trkngit.github.io/myrrah-legal/> and
<https://trkngit.github.io/myrrah-legal/child-safety.html>.

This repository is public so that an app store reviewer can open both
documents without a GitHub account. It holds nothing else.

## Do not edit the pages here

The source of truth for `index.md` is `docs/PRIVACY.md` in the
application repository, where a CI gate holds the signup consent text to
this policy. A change made here instead would pass that gate while the
published document and the app disagreed, which is the one failure this
split introduces. The source of truth for `child-safety.md` is
`docs/CHILD-SAFETY.md` in the same repository.

To update: change the source there, then regenerate the page here from
it. The only transformation is that GitHub callout syntax (`> [!NOTE]`)
becomes a bold lead-in, because the Jekyll renderer that serves these
pages does not understand it.
