# Portfolio And Resume

A static website containing a portfolio page and a resume page, built with HTML, CSS, and JavaScript. Portfolio content is loaded from `data.json`; no build step or package installation is required.

## Live pages

Assuming GitHub Pages is enabled for this repository, the expected URLs are:

- [Portfolio](https://mithun1st.github.io/mh/portfolio.html)
- [Resume](https://mithun1st.github.io/mh/resume.html)

## Run locally

From the project directory, start a local web server:

```sh
http.server 8000
```

Open [http://localhost:8000/portfolio.html](http://localhost:8000/portfolio.html). The page must be served over HTTP so it can fetch `data.json`.

## Update portfolio content

Edit `data.json` to add, change, or remove content:

- `personal_information`: name, photo, professional title, contact details, social links, and location
- `summary`: profile summary
- `projects`: project name, dates, role, optional URL, description, and image paths
- `work_experience`: company, job title, dates, and description
- `skills`: skill groups and their items
- `achievements`: name, associated information, result, and optional URL

`education` and `languages` are also stored in the JSON file but are not currently displayed on the portfolio page.

Use dates in `YYYY-MM-DD` format. Set an ongoing item's `end` to `null` to display “Now”. Project image paths are relative to the project directory and should point to files under `assets/`. A project name is linked when its `url` is provided.

Keep `data.json` valid JSON: use double quotes for strings, commas between fields and items, and no trailing commas. The page content and presentation are separate: edit `data.json` for portfolio information and `portfolio.html` for layout, styles, or fixed interface labels.

## Files

- `data.json` — portfolio content
- `portfolio.html` — portfolio page, styles, and rendering logic
- `resume.html` — separate resume page
- `assets/` — profile photo and project images
