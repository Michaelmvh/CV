# Curriculum vitae

This repository publishes the public version of Michael Vanden Heuvel's CV. `CV.pdf` is generated
from a private source repository and should not be edited manually.

## Stable links

- Latest release: <https://github.com/Michaelmvh/CV/releases/latest/download/CV.pdf>
- Current file on `main`: <https://raw.githubusercontent.com/Michaelmvh/CV/main/CV.pdf>

Use the latest-release link when sharing the CV. It automatically redirects to the newest versioned
release. The raw link always serves the file currently committed to `main`, but browser download
behavior may vary.

## Portfolio deployment

After publishing a release, the workflow sends a `cv-published` repository dispatch to
`Michaelmvh/michaelmvh.github.io`. That repository downloads the current `CV.pdf` and deploys it to
`michaelmvh.com`.

The dispatch requires an Actions secret named `PORTFOLIO_DISPATCH_TOKEN`, containing a fine-grained
personal access token restricted to `Michaelmvh/michaelmvh.github.io` with **Contents: Read and write**
permission. If the secret is absent, CV publishing still succeeds and reports that automatic portfolio
deployment is not configured.
