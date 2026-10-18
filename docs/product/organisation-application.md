# Organisation Application Form

**Status:** Product requirement agreed  
**Scope:** First version of Konnekt Lite  
**Decision:** Organisation creation requires platform administrator approval.

## Purpose

Collect enough structured information for an authorised Konnekt Lite platform administrator to review an organisation application. Keep the form approachable, make address information searchable, and avoid exposing private organisation details publicly by default.

## Applicant and organisation details

| Field | Required | Notes |
| --- | --- | --- |
| Applicant's full name | Yes | The person submitting the application. |
| Applicant's role/title | Yes | For example, owner, principal, director, or HR manager. |
| Organisation name | Yes | The name the organisation operates under. |
| Organisation type | Yes | School or business for the initial release. |
| Organisation contact email | Yes | Validate format. |
| Organisation contact phone | Yes | Store in a consistent format where possible; support international country codes. |
| Website URL | No | Validate as a URL when provided. |

## Physical address

Each component must have its own input and database field. Do not store the entire address only as one free-text value.

| Field | Required | Notes |
| --- | --- | --- |
| Street address | Yes | Building/house number and street name. |
| Address line 2 | No | Suite, floor, block, or other additional details. |
| Area / neighbourhood | Yes | Neighbourhood, district, or local area. |
| City / town | Yes | City or town. |
| State / province | Yes | State, province, or equivalent administrative area. |
| Postal code | No | Not every location uses one. |
| Country | Yes | Default the form to Nigeria initially, but do not hard-code the data model to Nigeria only. |
| Nearby landmark / directions | No | Helpful directions for locating the organisation. |

### Address form guidance

- Use separate, clearly labelled text inputs.
- Show examples in placeholders without treating them as submitted values.
- Make the required fields clear and validate them on both client and server.
- Preserve the individual address components in storage; a formatted address may be composed for display when needed.
- Do not publish the address on a public digital ID by default.

## Website and social media

These are optional. An organisation may submit none, one, or several.

| Field | Required | Notes |
| --- | --- | --- |
| Website URL | No | Separate URL field. |
| Facebook page URL | No | Separate URL field. |
| Instagram profile URL | No | Separate URL field. |
| LinkedIn page URL | No | Separate URL field. |
| Other social platform | No | Platform name, paired with its URL. Support multiple entries later if justified. |

Validate URLs when present. Do not require an organisation to have a website or social media presence to apply.

## Application and approval workflow

1. An individual registers for a personal account.
2. The individual submits an organisation application.
3. The application is assigned a pending status and enters the platform administrator's review queue.
4. Only a user with an explicit platform-administrator permission can approve or reject the application.
5. An organisation administrator cannot approve their own application and cannot review applications belonging to other organisations.
6. On approval, the organisation workspace becomes active and the approved applicant is assigned the organisation-owner/administrator role according to the access-control design.
7. On rejection, record the decision and reviewer. A reason or message may be included so the applicant can understand the outcome.
8. Keep an auditable record of status changes, reviewer, and timestamps.

Suggested initial statuses: `pending`, `approved`, `rejected`. If resubmission is supported, define whether rejected applications can be edited and resubmitted before implementing that flow.

## Privacy and access control

- Application details are visible only to the applicant as appropriate and authorised platform administrators during review.
- After approval, organisation details are available to that organisation's authorised administrators.
- Website and social links are not automatically public merely because they were supplied on the application form.
- Address, applicant contact details, and review notes must not appear on public digital IDs unless a separate, explicit visibility setting permits it.
- Enforce organisation-level data isolation on the server and in database access patterns; hiding a UI element is not an access-control measure.
- Keep platform-administrator privileges separate from organisation-administrator privileges.

## Acceptance criteria

- [ ] Organisation type can be selected as School or Business.
- [ ] Every address component listed above has its own field.
- [ ] Website and social media fields are optional and independently editable.
- [ ] Applications cannot be activated until an authorised platform administrator approves them.
- [ ] Organisation administrators cannot approve applications or access another organisation's private records.
- [ ] Required fields and provided URLs are validated on the server.
- [ ] Application status changes are auditable.
- [ ] Private address and contact details are not publicly exposed by default.

## Implementation note

This document records the agreed product behaviour. It does not claim the form, schema, authentication, or approval workflow has already been implemented. Database tables and application code should be designed after the core user journeys and permission boundaries are reviewed.
