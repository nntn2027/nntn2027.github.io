# Interplay between Neural and Tensor Networks 2027

Website for the workshop **Interplay between Neural and Tensor Networks**,
held at the Institute of Physics, Chinese Academy of Sciences, Beijing, **August 2–6, 2027**.

**Organizers:** Miles Stoudenmire, Xavier Waintal, Lei Wang, Yantao Wu, Tao Xiang
(local organizers: Lei Wang, Yantao Wu, Tao Xiang — IOP, CAS).

Previous edition: [Grenoble, July 2026](https://quantalps.univ-grenoble-alpes.fr/interplay-between-neural-and-tensor-networks-1704684.kjsp?RH=1616089847905).

## Repository layout

```
launch.sh             Start a local preview server
docs/                 The static site (plain HTML/CSS, no build step)
  index.html          Home: about, key information, previous edition
  speakers.html       Invited speakers
  program.html        Schedule
  venue.html          Location, maps, travel
  accommodation.html  Hotels
  visa.html           Visa / entry policies for China
  organizers.html     Organizing committee, contact
  assets/style.css    All styling (colors defined in :root at the top)
  assets/hero.svg     Banner image (tensor network ↔ neural network)
  assets/main.js      Mobile menu toggle
  .nojekyll           Tells GitHub Pages to serve files as-is
```

## Preview locally

```bash
./launch.sh
# or: cd docs && python3 -m http.server 8000
```

Then open <http://localhost:8000>. Stop with `Ctrl+C`.

## Editing

- **Text:** edit the corresponding `.html` file in `docs/`.
- **Speakers:** `speakers.html` contains a commented template block; copy it into the
  `<div class="people">` grid for each speaker.
- **Photos:** put images in `docs/assets/img/` and replace an initials avatar with
  `<img class="avatar" src="assets/img/name.jpg" alt="Full Name">`.
- **Navigation:** the menu is repeated in every page; when adding or removing a page,
  update the `<ul class="nav-links">` block in each `.html` file.

## Deploying to GitHub Pages

The site lives in `docs/`, which GitHub Pages can serve directly:

1. Push the repository to GitHub.
2. Go to **Settings → Pages → Build and deployment**.
3. Set **Source: Deploy from a branch**, **Branch: `main`**, **Folder: `/docs`**, and save.

The site is published at <https://nntn2027.github.io/> and updates on every push to `main`.
