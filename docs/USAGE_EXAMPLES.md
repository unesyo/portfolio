# Usage Examples

The repository is currently a static personal portfolio and a reference for the
future product. The scenarios below clearly separate current behavior from
planned behavior.

## View the Current Portfolio

Status: **Currently available**

```bash
python -m http.server 8000
```

Open `http://localhost:8000` to view the existing portfolio.

## Generate a Portfolio from a CV

Status: **Planned**

1. Upload a supported PDF or DOCX CV.
2. Review the extracted name, title, bio, experience, projects, skills,
   education, and links.
3. Correct missing or uncertain fields.
4. Generate a portfolio draft.

## Generate a Portfolio from LinkedIn

Status: **Planned**

1. Provide a LinkedIn URL or user-authorized profile export.
2. Confirm that the user has permission to process the provided data.
3. Review extracted profile information.
4. Generate a portfolio draft.

Implementation must comply with applicable LinkedIn platform rules and should
prefer user-authorized data access.

## Modify Generated Sections

Status: **Planned**

After generation, the user will be able to edit text, reorder supported
sections, remove content, and approve AI suggestions before publication.

## Choose a Theme

Status: **Planned**

The user will select from a small set of responsive themes. The same structured
profile data will be reusable across themes.

## Publish or Export a Portfolio

Status: **Planned**

The first export target should be a downloadable static website. Later options
may include direct deployment integrations with supported hosting providers.
