# TowerScreen

Seismic capacity of historical masonry towers by limit analysis. Static site: everything runs in the browser.

- `index.html`: **Screening.** Collapse multiplier from five closed-form failure mechanisms of an isolated tower with a hollow square section.
- `ubla.html`: **Block solver.** Rigid-block upper-bound limit analysis. The tower is made of blocks in running bond with Mohr–Coulomb interfaces (tension cut-off, compression cap). The kinematic linear programme is solved on the user's device by HiGHS compiled to WebAssembly.

Both pages are single self-contained files. They also work offline by double-click.

## Publish with GitHub Pages
1. Create an empty repository on GitHub (Pages is free for public repositories).
2. From this folder:
   ```
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: Settings → Pages → Build and deployment → Source: *Deploy from a branch*, Branch: `main`, folder `/ (root)`.
   The site appears at `https://<user>.github.io/<repo>/`.

## Third-party software
- three.js r160: MIT licence, inlined in both pages.
- highs-js 1.15.4 and HiGHS: MIT licence, inlined in `ubla.html`. See `third-party-licenses/`.

Results are indicative and do not replace a structural assessment.
