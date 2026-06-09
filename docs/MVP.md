# Minimum Viable Product

## Goal

The MVP should let a user provide professional profile information and receive
an editable, responsive portfolio draft generated from structured data.

## User Inputs

The MVP should support at least one complete input path first, then expand to:

1. **CV upload:** a PDF or DOCX supplied by the user.
2. **LinkedIn input:** a LinkedIn URL or user-authorized profile export,
   implemented in accordance with applicable platform rules.
3. **Manual form:** information entered directly by the user.

## AI Processing

The extraction service should identify, normalize, and structure relevant
career information. AI-generated suggestions must remain reviewable and
editable before publication.

## Extracted Data

- name;
- professional title;
- short biography;
- work experience;
- projects;
- skills;
- education;
- professional and social links.

## Output

The MVP output is a responsive web portfolio generated from structured profile
data. The user should be able to review the content before exporting or
publishing it.

## User Flow

```text
Choose input method
  -> Provide profile information
  -> Extract and structure data
  -> Review missing or uncertain fields
  -> Generate portfolio
  -> Edit and preview
  -> Export or publish
```

## MVP Limits

- Extraction may require user corrections.
- Only a small number of document formats and themes will be supported.
- LinkedIn support may be limited to user-authorized data or exports.
- Complex layouts and advanced customization are out of scope.
- The first version may generate only static output.
- The MVP should not publish content without explicit user confirmation.

## Success Criteria

- A user can complete an end-to-end flow using a supported input method.
- Core profile fields are converted into a documented structured format.
- The generated portfolio is readable and responsive.
- The user can correct extracted information before publication.
- The project can be run locally with documented steps.
- Contributors can understand the architecture and add a new input, field, or
  theme without rewriting the whole application.
