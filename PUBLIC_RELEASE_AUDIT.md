# Public Release Audit — MeetingAI Local v2.0.2

This document records the lightweight privacy/static review performed for the GitHub public package.

## Scope

- `meetingai.py`
- embedded/external `MeetingAI_v2.0.2.bundle.zip`
- three public screenshots
- public repository documentation

## Privacy scan

Checked for common accidental disclosures including:

- operating-system user-home and user-profile path patterns;
- email addresses;
- OpenAI-style and GitHub-style API tokens;
- AWS access-key patterns;
- user-specific absolute paths;
- private LAN IPv4 addresses;
- non-example external hosts.

No personal username, email, API key, secret token or user-home path was found in the application source/bundle scan.

Expected public values retained:

- `127.0.0.1` / `0.0.0.0` local service defaults;
- RFC documentation test IPs `192.0.2.10` / `198.51.100.20` used by a PROXY-v2 self-test;
- public package/model mirror hosts;
- `example.com` / `example.invalid` documentation placeholders.

## Screenshots

Public images were renamed to neutral names and re-encoded without EXIF / ICC / comment metadata. Sensitive environment values visible in the original screenshots had already been visually masked before packaging.

## Code integrity

The public root `meetingai.py` is byte-for-byte the same application file as the validated v2.0.2 build. No runtime logic was changed during GitHub packaging.

## Repository safety

`.gitignore` excludes runtime data, secrets, passwords, certificates, logs, meeting audio and generated configuration. This is a guardrail, not a substitute for reviewing `git status` before publishing.
