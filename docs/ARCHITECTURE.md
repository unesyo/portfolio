# Architecture Overview

This document describes a simple target architecture for the AI Portfolio
Builder. It is intentionally technology-neutral until the MVP stack is chosen.

## Current Architecture

The repository currently hosts a static portfolio:

```text
Browser -> index.html -> bundled CSS, JavaScript, images, and browser plugins
```

There is no backend API, AI extraction service, storage layer, or portfolio
generation engine yet.

## Target Flow

```text
User input -> AI extraction -> Structured profile data -> Portfolio generator
           -> Editable preview -> Published portfolio
```

## Proposed Components

### Frontend Web App

Collects user input, displays extraction results, allows corrections, selects a
theme, and previews the generated portfolio.

### Backend API

Coordinates uploads, validation, extraction jobs, portfolio generation, and
export requests. It should enforce file limits, validate inputs, and avoid
exposing provider credentials to the browser.

### AI Agent and Extraction Service

Extracts profile fields from supported inputs, identifies uncertainty, and
returns structured data. It should preserve source references where practical
and never publish inferred content without review.

### Structured Profile Model

Provides the stable contract between extraction, editing, and generation. A
versioned JSON schema should describe fields such as identity, experience,
projects, skills, education, and links.

### Portfolio Generation Engine

Transforms validated profile data and a selected theme into a static,
responsive portfolio.

### Templates and Themes

Define presentation separately from profile data. Themes should support common
sections, accessibility, responsive layouts, and safe rendering of user
content.

### Optional Storage

Stores drafts, generated assets, or export jobs only when required. The MVP
should minimize personal data retention and make retention behavior explicit.

### Export and Deployment Layer

Produces a downloadable static bundle and, later, integrations for supported
hosting providers.

## Design Principles

- Keep the profile data model independent from any theme.
- Require user review before publication.
- Treat uploaded documents and profile data as sensitive.
- Validate all generated and user-provided content.
- Start with a modular monolith unless scale requires separation.
- Keep provider-specific AI integrations behind a small interface.

## Initial Technical Decisions to Make

- frontend and backend framework;
- versioned portfolio JSON schema;
- supported document parsers;
- AI provider abstraction and evaluation approach;
- local development and deployment model;
- privacy, retention, and deletion behavior.
