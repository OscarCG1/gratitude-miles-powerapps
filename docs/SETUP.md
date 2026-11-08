# Setup and deployment notes

This is a **source-code portfolio sample**, not a validated deployable Power Apps package.

## Dependencies
- Microsoft Power Apps Canvas App environment
- Microsoft 365 Users connector (`Office365Users`)
- SharePoint lists named `GratitudeNotes` and `GratitudeSettings`

## Source-based data fields
- GratitudeNotes example export: `Title`, `From`, `To`, `Thank you Note`, `SentOn`, `PeriodId`, `IsVisible`. The Power Fx logic expects `To` to be a SharePoint Person record with `Email` and `DisplayName`, rather than plain CSV text.
- GratitudeSettings example export: `CurrentSettings`, `PeriodStart`, `PeriodEnd`, `MaxNotesperPeriod`. Actual SharePoint column types and required values need validation.

## Important limitations
The YAML files are extracted screen and application source only. They are not an importable `.msapp` and cannot be deployed without reconstructing and validating the Power Apps environment and connections. The note submission workflow has not been confirmed end to end.

## Security
The sample data is synthetic. Do not commit employee notes, internal tenant details, production list exports, access tokens or original internal packages. The admin email in source is a placeholder; replace it with appropriate role-based access controls in any real deployment.
