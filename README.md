# Methods and Measures

Methods and Measures is a browser-based decision aid within the HCI User Studies Toolkit. It guides researchers and students from study goals to suitable research methods and standardized measures for HCI and UX studies.

## What the tool does

- Provides a guided selection flow based on study purpose, evidence type, sampling strategy, data type, and concepts of interest
- Filters and displays matching methods and measures from an XML-based catalog
- Links to questionnaires, methodological references, and further sources for each matching entry
- Uses the shared visual style of the HCI User Studies Toolkit

## Project structure

- `index.html` contains the page structure, dynamic rendering logic, and filtering behavior
- `methods.xml` contains the decision structure as well as the method and measure entries
- `_css/` contains toolkit and vendor stylesheets
- `_js/` contains vendor JavaScript dependencies used by the page
- `_img/` contains background and logo assets
- `_icons/` contains the icon source package used in the project
- `_fonts/` contains local font files for the shared toolkit styling
- `downloads/` contains referenced questionnaires and supporting PDF resources
- `.nojekyll` ensures GitHub Pages serves the `_css/`, `_js/`, `_img/`, `_icons/`, and `_fonts/` directories correctly

## Local usage

Open `index.html` in a browser or serve the folder through a simple static web server. The page is fully client-side and reads its data from `methods.xml`.

## Deployment note

The published site depends on underscore-prefixed asset folders such as `_css/` and `_js/`. When deploying via GitHub Pages, keep `.nojekyll` in the repository root so these folders are not ignored by Jekyll during site generation.

## Maintaining the catalog

- Add or refine decision nodes in the `<options>` sections of `methods.xml`
- Add or update entries in `<measures>` with stable `id` and `category` values
- Keep option ids and method categories aligned so the filtering logic can match them reliably
- Prefer concise, user-facing wording because the XML content is rendered directly in the interface

## Scope

The tool is intended as a quick orientation aid for HCI research planning. It helps users find an informed starting point, but it does not replace a full literature review or methodological supervision.

## Citation

If you want to adequately cite this work, please refer to [`HCIToolkit.bib`](HCIToolkit.bib) or use the following entry:

```bibtex
@inproceedings{schwind2023a,
    author = {Schwind, Valentin and Resch, Stefan and Sehrt, Jessica},
    title = {The HCI User Studies Toolkit: Supporting Study Designing and Planning for Undergraduates and Novice Researchers in Human-Computer Interaction},
    year = {2023},
    isbn = {978-1-4503-9422-2/23/04},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3544549.3585890},
    doi = {10.1145/3544549.3585890},
    booktitle = {Extended Abstracts of the 2020 CHI Conference on Human Factors in Computing Systems},
    location = {Hamburg, Germany},
    series = {CHI EA '23}
}
```
