# RISE-MICCAI Autumn School 2026 Website

Source for the **RISE-MICCAI Autumn School 2026** website
(11–13 November 2026, virtual on Zoom, 13:00–17:00 UTC each day).

The site is a static HTML/CSS/JS page derived from the
[Summer School 2025 template](https://github.com/RISE-MICCAI/Summerschool_website_template)
and is served with GitHub Pages from the `main` branch.

## Structure

```
index.html              Home page: registration, schedule, speakers, FAQ, code of conduct, organisers
pages/program.html      Schedule partial, loaded into #program by js/import.js
css/main.css            Styles
js/                     Navigation, speaker tooltips, program loader
resources/images/       Logos
resources/speakers/     Speaker headshots (<Firstname>.jpg) and bios (<Firstname>.txt)
```

## Editing content

- **Schedule**: edit `pages/program.html`. Each day is a `.day-schedule` block
  containing `.schedule-item` entries. Speaker names use the `.speaker-profile`
  markup so that the bio appears as a hover tooltip.
- **Speakers**: edit the `#speakers` section in `index.html` and drop the
  headshot into `resources/speakers/`. Keep images at roughly 600 px on the
  long edge.
- **Registration links, FAQ, organisers**: edit the matching section in
  `index.html`.

## Open items

- Add the application / registration form link (see the `TODO` in the
  `#registration` section of `index.html`).
- Add Yipei Wang's photo (`resources/speakers/Yipei.jpg`) and bio
  (`resources/speakers/Yipei.txt`, plus the speaker card and tooltip).

## Local preview

Because the schedule is fetched with `fetch()`, open the site through a local
server rather than as a `file://` URL:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## License

MIT
