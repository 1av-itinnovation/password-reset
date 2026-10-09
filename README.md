# 1AV Password Reset Request

Online form for 1Aviation Groundhandling Services, Corp. employees who cannot sign in and need their password reset by the IT Department.

**Live page:** https://1av-itinnovation.github.io/password-reset/

## What it does

1. The employee fills in the form (Employee Number, ESS Username, Mobile Number, Personal Email Address, Reason for Request).
2. The request is sent to the 1AV IT Department and placed in the queue for processing.
3. The employee sees a confirmation with a reference number.
4. The IT Department sends updates to the mobile number and personal email address provided.

The form is available in English and Filipino and works on phones, tablets and computers.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole website: page, styles, logo and script in one file |
| `.github/workflows/deploy.yml` | Publishes the site and connects the form to the IT Department's request queue |
| `README.md` | This document |

## Maintenance

- **Wording:** all labels and messages are in the `TEXT` block near the top of the script in `index.html`, under `en` (English) and `fil` (Filipino).
- **Settings:** the `CONFIG` block in the same script holds the validation rules (for example, the employee number format).
- **Publishing:** every change committed to the `main` branch is published automatically by the workflow in `.github/workflows/deploy.yml`. Progress is shown in the **Actions** tab, and changes go live a minute or two after the run finishes.
- **Connection address:** stored as the repository secret `ALERT_WEBHOOK_URL` and inserted at publish time. It is never written in the repository files. After changing the secret, re-run the workflow from the **Actions** tab.

## Security

- The form never asks for a password. The IT Department will never ask an employee for their current password.
- Every request is verified by the IT Department before a password is reset.
- Do not add credentials, internal addresses or employee data to this repository. It is public.

## Ownership

Developed and maintained by **1AV IT Innovation**, Information Technology Department, 1Aviation Groundhandling Services, Corp.

For concerns about this page, contact the 1AV IT Department.
