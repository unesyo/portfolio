# Initial Issue Backlog

These issue outlines are prepared for project planning. Before opening them on
GitHub, confirm scope, dependencies, and acceptance criteria.

## Add CV Upload Support

Accept a PDF or DOCX CV, validate file type and size, and make the document
available to the extraction workflow. Include clear error states and document
the privacy behavior.

## Add LinkedIn Profile Parser

Define a compliant, user-authorized LinkedIn ingestion approach. Document
platform constraints and convert supported profile data into the shared
portfolio model.

## Add AI Extraction Service

Create a provider-independent extraction interface that converts supported
input into structured profile data, including uncertainty and validation
errors.

## Add Portfolio JSON Schema

Define a versioned schema for identity, bio, experience, projects, skills,
education, and links. Include example fixtures and validation.

## Add Theme Selector

Allow a user to choose between supported portfolio themes while preserving the
same structured profile content.

## Add Preview Mode

Render a portfolio draft before export and allow the user to review all content
and links.

## Add Tests and CI

Choose the initial test strategy, add checks for the current static site and
future data model, and run them in continuous integration.
