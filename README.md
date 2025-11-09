# Matrix Build Demo

This repository contains a GitHub Actions workflow that demonstrates a matrix build across OS and Node versions and uploads artifacts for each run.

**Contact**: 22f1001316@ds.study.iitm.ac.in  


## How it works

- The workflow `.github/workflows/matrix-build.yml` runs on push to `main` (and can be triggered manually).
- It uses a matrix of `os` and `node-version` so many jobs run in parallel.
- Each job produces `build/output.txt` with metadata and uploads it as an artifact named `build-76ab456-<os>-v<node-version>`.

## Validation checklist

- [ ] At least 3 matrix jobs succeed (the matrix here creates 9 combinations).
- [ ] Artifacts are visible in the Actions UI with prefix `build-76ab456-`.
- [ ] Each artifact contains non-empty content.
- [ ] The workflow contains a step named `matrix-76ab456`.
