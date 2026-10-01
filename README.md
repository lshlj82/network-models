# Network models: an interactive lab

An interactive web demo of the network models covered in **Lecture 5: Network models**. Build each model, watch it grow link by link, and compare its structure with the properties of real networks: short paths, many triangles, and hubs.

> Created by **Claude Opus 5.5** (Anthropic), based on the lecture slides by **Sang Hoon Lee**.

## Models

| Family | Models |
| --- | --- |
| Random graphs | Erdős–Rényi G(N, L), Gilbert G(N, p) |
| Small worlds | Watts–Strogatz, Newman–Watts |
| Fixed degree sequence | Configuration model |
| Growth and preferential attachment | Barabási–Albert, generalized (non-linear) preferential attachment, attractiveness model, fitness model |
| Adding triangles | Holme–Kim, random walk model |
| Other mechanisms | Rank model, static model (Goh–Kahng–Kim) |

## Features

- **Live parameters**: sliders rebuild the network instantly.
- **Play build**: replays the construction in the order the algorithm creates links or nodes. Nodes outside the largest connected component are faded, so the emergence of the giant component in the ER model is visible.
- **Measured structure**: number of nodes and links, average degree, largest degree, average clustering coefficient, average shortest-path length in the giant component, and giant-component size.
- **Degree distribution**: linear or log–log (log-binned) plots with theory overlays: Poisson for ER, k⁻³ for BA, the target sequence for the configuration model, and predicted exponents for the attractiveness, rank and static models.
- **Visual cues**: rewired shortcuts in the small-world models are drawn in orange; self-loops and multi-edges in the configuration model are drawn in red, with an option to erase them.
- **Experiments**: larger simulations that reproduce figures from the slides, such as the percolation transition, the Watts–Strogatz ℓ(p) and C(p) curves, BA versus random attachment, the winner-takes-all effect for α > 1, and tunable clustering in Holme–Kim.
- **Code snippets**: the matching NetworkX call or a short textbook-style Python sketch for each model.
- Light and dark themes, and a responsive layout for phones.

## Usage

It is a single self-contained file with no build step and no dependencies.

- **Locally**: open `index.html` in a modern browser.
- **GitHub Pages**: push this repository, then go to *Settings → Pages* and serve from the branch root. The demo will be available at `https://<user>.github.io/<repo>/`.

Fonts are loaded from Google Fonts; without a network connection the page falls back to system fonts and works the same.

## Notes

- All networks are generated in the browser with JavaScript implementations of each model. Results vary from sample to sample; use **New sample** to draw another one.
- Path lengths for large networks are estimated from a sample of up to 160 source nodes.
- Literature references shown for each model were added by Claude and should be checked against the original sources before use in teaching materials.

## Credits

- Lecture slides: **Sang Hoon Lee**, Gyeongsang National University.
- Demo: created by **Claude Opus 5.5** (Anthropic).
- Model descriptions follow the lecture and the textbook it draws on, *A First Course in Network Science* by F. Menczer, S. Fortunato and C. A. Davis.
