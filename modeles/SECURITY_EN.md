# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please help us
address it responsibly by following these steps:

1. **Do not publicly disclose the vulnerability.**
2. Contact us directly at
   [opensource@ssi.gouv.fr](mailto:opensource@ssi.gouv.fr) with the following
   details:
   - A clear description of the issue.
   - Steps to reproduce the vulnerability.
   - Any potential impact or exploit scenarios.

## CVE attribution

ANSSI is not a CNA[^CNA] and doesn't allocate CVE identifiers. You can request
one directly from MITRE using
https://mitre.github.io/mitre-cve-roles/cve-id-request/

[^CNA]: CVE numbering authority

## LLM-assisted research

Additionally, **for LLM-assisted research** (code assistant, genAI etc.), if
the tool seems to discover a vulnerability, we ask you to:
- indicate explicitely that LLM tools were used and precise which tools (model,
  version) and for which usages (vulnerability research, proof of concept,
  report writing etc.)
- confirm the vulnerability is real considering the threat model and real world
  usage of the project;
- provide a proof of concept exploit;
- provide a tested patch proposal fixing the vulnerability, without regression
  and including a unit test validating the approach.

Code assistant tools make those steps very easy so make sure to check them
personally before sending a report.

Thank you for helping us keep this project secure!
