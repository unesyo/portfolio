# AI Portfolio Builder

AI Portfolio Builder is an early-stage open source project that aims to turn a
CV, a LinkedIn profile, or manually entered career information into a clear,
professional, and customizable web portfolio.

The repository currently contains a static personal portfolio for Younes EL
HADDAR. That portfolio is being kept as the first reference implementation
while the project evolves into a reusable AI-assisted portfolio builder.

## The Problem

Creating a strong portfolio takes time, design skills, and repeated manual
editing. Many professionals already have the necessary information in a CV or
professional profile, but do not have a simple way to transform it into a
polished web presence.

AI Portfolio Builder is intended to make that process faster while keeping the
user in control of the generated content.

## Vision

The long-term vision is a workflow where a user provides:

- a CV in PDF or DOCX format;
- a LinkedIn URL or user-authorized profile export; or
- profile information through a manual form.

An AI-assisted extraction service will structure the profile data, generate a
portfolio draft, and let the user review, edit, theme, export, and publish it.

## Project Status

Status: **Early-stage / pre-MVP**

Currently available:

- a responsive static personal portfolio;
- sections for biography, experience, projects, skills, education, and links;
- bundled Bootstrap-based styling and third-party UI plugins;
- a reference portfolio that can be served by any static web server.

Planned, but not yet implemented:

- CV upload and parsing;
- LinkedIn URL input and user-authorized data ingestion;
- manual profile form;
- AI profile extraction and recommendations;
- structured portfolio data model;
- editable preview and theme selection;
- export and deployment workflows;
- automated tests and continuous integration.

## Example Usage

The current portfolio can be viewed locally:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

The planned product flow will look like this:

```text
Upload CV -> Review extracted profile -> Choose a theme -> Edit portfolio -> Publish
```

See [docs/USAGE_EXAMPLES.md](docs/USAGE_EXAMPLES.md) for current and planned
usage scenarios.

## Architecture Overview

### Current architecture

```text
index.html
  -> local CSS, JavaScript, images, fonts, and bundled browser plugins
  -> optional external feeds and GitHub activity integrations
```

The current application is a static site. It has no root package manager
manifest, backend, database, build step, or automated test suite.

### Target architecture

```text
User input
  -> AI extraction service
  -> Structured profile data
  -> Portfolio generation engine
  -> Editable preview
  -> Export or published portfolio
```

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for the proposed components
and design principles.

## Installation

No dependency installation is required for the current static portfolio.

```bash
git clone https://github.com/unesyo/portfolio.git
cd portfolio
python -m http.server 8000
```

You can also open `index.html` directly, although serving it locally gives more
consistent browser behavior.

## Development

Edit the static files directly:

- `index.html` contains the current portfolio content;
- `assets/css/` and `assets/scss/` contain styling;
- `assets/js/main.js` initializes the current browser-side integrations;
- `assets/images/` contains portfolio images;
- `docs/` contains the product direction and contributor documentation.

There are currently no repository-level build, test, or lint commands.

## Roadmap

The roadmap progresses from project foundations to a usable MVP, an editing
experience, stronger AI workflows, and mature open source practices.

See [docs/ROADMAP.md](docs/ROADMAP.md) for phases and deliverables.

## Why Open Source?

Professional portfolios should be accessible to people regardless of their
design experience, budget, or preferred hosting platform. Building in the open
makes it possible to:

- keep generated content and career data under user control;
- make extraction and generation behavior transparent;
- support community-built themes, integrations, and deployment targets;
- learn from contributors with different professions and portfolio needs;
- create a reusable foundation rather than a one-off personal site.

## Contributing

Contributions are welcome, especially around the data model, extraction
workflows, accessibility, documentation, themes, and testing.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
The initial implementation backlog is documented in
[docs/ISSUE_BACKLOG.md](docs/ISSUE_BACKLOG.md).

## License

Original project code and documentation are available under the
[MIT License](LICENSE).

The repository also contains third-party theme and plugin assets with their own
licenses and attribution requirements. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
and the license files distributed with those assets before reusing them.
