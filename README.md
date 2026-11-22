# AKONDO GLOBAL WORLD — Vercel Website Package

An English-only, responsive website for international visa enquiries, invitation enquiries, air-ticket enquiries, and work-related interest from skilled and non-skilled applicants. All requests are manually reviewed by the owner. The site does not promise visas, jobs, invitations, or tickets.

## Included workflow

1. Applicant chooses one of three services and submits contact details, destination country, category, and enquiry details.
2. The request is emailed to `akondaglobal@gmail.com` only.
3. The owner receives secure, time-limited APPROVE and DECLINE links by email.
4. APPROVE sends a private, 72-hour upload link to the applicant's email. DECLINE sends a polite rejection email and no upload link.
5. The applicant uploads PDF/JPG/PNG/WEBP files (maximum combined size 3 MB). The files are forwarded as email attachments to `akondaglobal@gmail.com`; the applicant receives confirmation.
6. The website does not use its own database. Temporary upload processing and email provider processing still occur; providers may process/log data according to their policies.

## Deploy to Vercel

1. Extract this ZIP on your computer, or upload its contents to a new GitHub repository.
2. In Vercel, choose **Add New → Project** and import that GitHub repository. Vercel will install `formidable` from `package.json`.
3. In Vercel Project Settings → Environment Variables, add all values below. Do not commit secrets to GitHub.
4. Redeploy after setting the variables.
5. Submit a test enquiry using your own email. Confirm the enquiry arrives, test APPROVE and DECLINE, and test document upload with dummy files before using real customer documents.

### Required environment variables

- `OWNER_EMAIL` = `akondaglobal@gmail.com`
- `SITE_URL` = your full deployed Vercel URL, e.g. `https://your-project.vercel.app`
- `RESEND_API_KEY` = your Resend API key
- `RESEND_FROM` = a sender address on a domain verified in Resend, e.g. `AKONDO GLOBAL WORLD <no-reply@your-verified-domain.com>`
- `APPROVAL_SECRET` = a long random secret of at least 32 characters

Email cannot be sent until you create/configure the Resend account, verify a sender domain, and add the variables. A normal Gmail address cannot be used as the sender unless supported and verified by the provider; keep `OWNER_EMAIL` as the destination inbox.

## Company details displayed

- Brand: AKONDO GLOBAL WORLD
- Primary application inbox: `akondaglobal@gmail.com`
- Phone: `01797528560`
- WhatsApp: `01355952967`
- Additional contact email: `akondatravels4@gmail.com` (displayed as a contact only; application details go to the primary inbox)
- License reference: `TRAD/DNCC/027476/2023`
- Address transcribed from supplied document: Ch-80/A, BTI Premier Plaza, Level 02, Office 77, North Badda, Dhaka-1212, Bangladesh

The old document's business name is not displayed. The license number is shown as a reference, not a claim that the document licenses the new brand. Verify the number/address against the original document before publishing.

## Important limits and security notes

- The current code is prepared for deployment but has not been tested against your Resend account because no API key or verified sender domain was provided.
- Vercel and the email provider may process request data and logs. The site has no own database, but no third-party-retention guarantee can be made.
- Upload links expire after 72 hours. The link may be reused until expiry because this no-database version cannot persist a one-time-use flag.
- Keep passport files private; use dummy documents for testing and delete received files when no longer needed.
- The site is English-only and has no pricing, fee, or payment feature.
