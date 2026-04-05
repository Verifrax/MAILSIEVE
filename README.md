# MAILSIEVE

Command-line discovery tool for finding publicly listed business email addresses from domain lists with resumable execution, rate discipline, and inspectable outputs.

## Status

- Repository role: operational discovery tool only
- Repository class: standalone operator tooling
- Public host ownership: none
- Deployment model: local CLI and repository workflow surface
- License: Apache License Version 2.0

## What this repository is

MAILSIEVE is a bounded collection utility for:

- reading domain lists
- crawling public web pages politely
- extracting candidate business email addresses
- preserving resumability across long runs
- producing reviewable output and logs

## What this repository is not

MAILSIEVE is not:

- a proof system
- a verifier
- an authority service
- a governance surface
- a compliance engine
- an identity system
- a guarantee of validity, ownership, consent, deliverability, or permission

MAILSIEVE discovers public contact data candidates.
It does not convert them into verified truth.

## Operational boundary

Inputs:

- domain lists
- public web pages reachable from those domains
- operator-selected rate and concurrency settings

Outputs:

- candidate email address rows
- processed-domain state
- crawl logs for operator review
- diagnostic output

## Repository surfaces

Current repository files include:

- `mailsieve.mjs`
- `batch-run.sh`
- `reset-hard.sh`
- `extract_emails.py`
- `domains.txt`
- `domains.clean.txt`

## Reader contract

A reader landing here should be able to answer immediately:

1. What does MAILSIEVE do? Public email discovery from domains.
2. What does it not do? It does not verify or authorize anything.
3. Does it own a public product host? No.
4. Are outputs self-authenticating? No.

## Contributing

A contribution here is wrong if it:

- upgrades discovery language into verification language
- implies legality, consent, or authority from collection output
- adds deployment or package claims not backed by repository metadata
- turns logs into claimed proof

## License

Apache License Version 2.0. See `LICENSE`.
