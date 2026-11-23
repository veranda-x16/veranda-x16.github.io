# veranda-x16.github.io

The website of [Veranda](https://github.com/veranda-x16/veranda), a
GEOS-style desktop for the Commander X16: https://veranda-x16.github.io

This repository holds only the workflow that builds and deploys the site
(`.github/workflows/pages.yml`). The site's generator is in Veranda's
repository, `tools/site/build.py` (Python, standard library only): it
reads the manual and the screenshots from Veranda's `docs/manual` and
the releases from GitHub, and writes plain HTML and CSS.

It rebuilds when a release is published, every day, and on a push here.
To build it on a PC:

    git clone https://github.com/veranda-x16/veranda
    python3 veranda/tools/site/build.py --api --out site
    python3 -m http.server -d site

MIT licence, Copyright (c) 2026 Marcin Spoczynski.
