# Gratitude Miles — Power Apps Recognition App

A Microsoft Power Apps Canvas App prototype for peer-to-peer appreciation in a workplace setting.

## Overview

The application is designed to help employees recognize colleagues through gratitude notes and to highlight top recipients during a configurable recognition period.

## Technology

- Microsoft Power Apps (Canvas App) and Power Fx
- SharePoint Lists (`GratitudeNotes`, `GratitudeSettings`)
- Microsoft 365 Users connector (`Office365Users`)

## What the supplied source demonstrates

- Retrieval of the signed-in user's Microsoft 365 profile
- Loading period dates and note limits from SharePoint settings
- Filtering visible notes by period
- Aggregating notes by recipient and calculating a top-three ranking
- Screen layouts for the home screen and a send-note screen

## Repository contents

- `src/App.pa.yaml` — app startup logic and data collections
- `src/Screen1.pa.yaml` — home screen definition
- `src/scrSendNote.pa.yaml` — send-note screen definition

## Status and limitations

This repository contains reviewable YAML source extracted from a supplied Power Apps source package. It is **not** a standalone runnable web app or a verified deployable Power Apps export. The visible screen source does not establish a complete working note-submission workflow. Running the app requires the appropriate Power Apps environment, SharePoint lists, permissions, and connectors.

## Data model (inferred from Power Fx references)

- `GratitudeSettings`: `PeriodStart`, `PeriodEnd`, `MaxNotesperPeriod`
- `GratitudeNotes`: `SentOn`, `IsVisible`, `To` (person with Email and DisplayName)

Other columns and their types must be verified against the original SharePoint configuration before deployment.

## Security and sharing

Do not commit production SharePoint list exports, tenant identifiers, credentials, employee information, or private recognition notes. The original package is intentionally not included here; review all sources before publishing publicly.

## Future improvements

- Document the full SharePoint schema and setup process
- Implement and test end-to-end note submission
- Add screenshots using synthetic demo data
- Add validation, error handling, and deployment instructions

## Portfolio relevance

Demonstrates low-code application design, Microsoft 365 integration, Power Fx data transformations, and enterprise process improvement.

## Example data and setup

Synthetic CSV examples are in `sample-data/`; see `docs/SETUP.md` for data model, dependencies, and deployment limitations. Original employee data and corporate admin identifiers have been excluded.
