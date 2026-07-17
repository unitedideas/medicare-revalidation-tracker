# Medicare Revalidation Tracker

A free, source-aware spreadsheet template for credentialing, provider-enrollment, medical-billing, and provider-operations teams tracking a known roster of Medicare NPIs.

[Download the CSV template](./medicare-revalidation-tracker.csv) or open it in Excel, Numbers, or Google Sheets.

## What it preserves

- NPI, legal name, location, enrollment type, and responsible owner
- Current public CMS due date or `TBD`
- The date and source revision used for the check
- Formula-driven days until due, internal 180-day review date, and attention flag
- Submission target, application ID, last verified status, next check, and notes

The first blank data row contains the formulas. Duplicate that row for the rest of the roster.

## Minimum workflow

1. Start with NPIs your organization already manages.
2. Check each NPI in the official CMS Medicare Revalidation List or the [free bulk lookup](https://actablesite.com/medicare-revalidation-due-date-lookup?utm_source=github&utm_medium=repository&utm_campaign=medicare_revalidation_tracker).
3. Keep every returned enrollment row when one NPI has multiple records.
4. Record the check date and CMS source revision beside the result.
5. Assign an owner and next-check date.

For the full field guide and interpretation rules, see the [Medicare revalidation tracking spreadsheet guide](https://actablesite.com/medicare-revalidation-tracking-spreadsheet?utm_source=github&utm_medium=repository&utm_campaign=medicare_revalidation_tracker).

## Important boundary

The public CMS list reports an established revalidation due date or `TBD`. It does not prove that a revalidation was submitted, received, approved, or completed. Verify live application status through PECOS and the responsible Medicare Administrative Contractor.

Do not store protected health information, passwords, PECOS credentials, or private enrollment documents in this template.

## Automatic alternative

If nobody reliably owns the recurring source check, [Medicare Roster Watch](https://actablesite.com/pending-medicare-roster-watch?utm_source=github&utm_medium=repository&utm_campaign=medicare_revalidation_tracker) monitors up to 20 known NPIs against public CMS revalidation and pending-enrollment sources. It sends one dated baseline and then email only when a watched public record changes.

## Official sources

- [CMS Medicare Revalidation List](https://data.cms.gov/tools/medicare-revalidation-list)
- [CMS Revalidation Due Date List dataset](https://data.cms.gov/provider-characteristics/medicare-provider-supplier-enrollment/revalidation-due-date-list)
- [CMS revalidation guidance](https://www.cms.gov/medicare/enrollment-renewal/providers-suppliers/revalidations)

ActableSite is not CMS or a Medicare Administrative Contractor. This template is an operations aid, not legal, billing, credentialing, or enrollment advice.

## License

MIT. See [LICENSE](./LICENSE).
