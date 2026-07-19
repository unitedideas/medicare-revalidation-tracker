# Medicare Revalidation Tracker

A free, source-aware spreadsheet and workflow template for credentialing, provider-enrollment, medical-billing, and provider-operations teams tracking a known roster of Medicare NPIs.

[Download the CSV template](https://github.com/unitedideas/medicare-revalidation-tracker/releases/latest/download/medicare-revalidation-tracker.csv), preview the [version-controlled source](./medicare-revalidation-tracker.csv), or [create your own copy of this repository](https://github.com/new?template_name=medicare-revalidation-tracker&template_owner=unitedideas). The CSV opens in Excel, Numbers, or Google Sheets.

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

## Preview an automated check

This repository includes a manual GitHub workflow built on `unitedideas/medicare-revalidation-action@v1` that produces a current, source-dated JSON artifact. Its default preview checks two disclosed public demonstration NPIs without an account, token, Apify run, or charge:

1. Create your own repository from this template.
2. Open **Actions → Check Medicare revalidation roster → Run workflow**.
3. Leave **preview** selected and run it.
4. Download `medicare-revalidation-demo` from the completed workflow run.

To check your own 1–100 NPI roster, add an Apify API token as the repository secret `APIFY_TOKEN`, select **roster**, and enter the NPIs. The workflow refuses invalid NPI check digits and an insufficient hard charge cap before starting a paid run. A complete run costs **$0.01 per returned NPI plus buyer-paid Apify platform usage** and fulfills the JSON automatically.

## Important boundary

The public CMS list reports an established revalidation due date or `TBD`. It does not prove that a revalidation was submitted, received, approved, or completed. Verify live application status through PECOS and the responsible Medicare Administrative Contractor.

Do not store protected health information, passwords, PECOS credentials, or private enrollment documents in this template.

## One-time operations dashboard

If the team wants an owned queue without a subscription, the [Medicare Revalidation Operations Dashboard](https://actablesite.com/api/medicare-revalidation-dashboard-referral?source=github_tracker_readme) is **$12 once**. The downloaded HTML file checks up to 100 known NPIs against the current public CMS list, keeps owners and next actions in the buyer's browser, and exports source-dated CSV and calendar files. It is not live PECOS status and should not contain patient data, passwords, credentials, or private enrollment documents.

## Automatic alternative

If nobody reliably owns the recurring source check, [Medicare Roster Watch](https://actablesite.com/api/medicare-roster-watch-referral?source=github_tracker_readme) monitors up to 20 known NPIs against public CMS revalidation and pending-enrollment sources for **$9 per month**. It sends one dated baseline and then email only when a watched public record changes or reaches a due-date reminder stage. Stripe handles renewal and cancellation; monitoring activates automatically after a successful checkout with a valid roster.

## Official sources

- [CMS Medicare Revalidation List](https://data.cms.gov/tools/medicare-revalidation-list)
- [CMS Revalidation Due Date List dataset](https://data.cms.gov/provider-characteristics/medicare-provider-supplier-enrollment/revalidation-due-date-list)
- [CMS revalidation guidance](https://www.cms.gov/medicare/enrollment-renewal/providers-suppliers/revalidations)

ActableSite is not CMS or a Medicare Administrative Contractor. This template is an operations aid, not legal, billing, credentialing, or enrollment advice.

## License

MIT. See [LICENSE](./LICENSE).
