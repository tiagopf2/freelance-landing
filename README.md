# Freelance landing page

A single-file landing page for my freelance work with small businesses.
Visitors pick the problem that applies to them and jump to a section that
covers it, with a real example and a call to action.

Everything lives in `index.html` — markup, styles and script. No build step
and no dependencies, so it loads fast on a phone.

## Editing

Open `index.html` in any editor. Search for `TODO(tiago)` to find the bits
that still need filling in.

## Contact form

Uses Netlify Forms. Netlify parses the HTML at deploy time, spots the
`data-netlify="true"` attribute and wires the form up on its own, so there is
nothing to configure in the markup. Submissions appear under **Forms** in the
Netlify dashboard, and you can turn on email notifications there.

The hidden `bot-field` input is a spam trap. Netlify drops any submission that
has it filled in.

Note that this only works on Netlify hosting. On any other host the form will
not submit.

## Deploying

Netlify, connected to this repo. Import the repo in Netlify, leave the build
command empty and set the publish directory to `.`, since there is nothing to
build.

**Turn on form detection or the contact form will not work.** New Netlify
sites have it switched off, and the form fails silently. In the Netlify UI it
is under Project configuration > Forms > Form detection. Redeploy after
enabling it, then check Forms in the dashboard: the form is registered once
`contact` shows up there.
