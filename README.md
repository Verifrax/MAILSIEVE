# MAILSIEVE

![License](https://img.shields.io/badge/license-Apache--2.0-blue)

Command-line discovery tool for publicly listed business email addresses from domains, built for rate-limited collection, resumable execution, and evidence-oriented operator review.

## Status

* Repository role: operational discovery tool only
* Repository class: operator tooling surface
* Public host ownership: none
* Stack position: adjacent operational utility, not a protocol-core repository
* Artifact-chain role: may support operator workflows, but does not define, issue, execute, verify, publish, or register artifact-0005
* Deployment model: local CLI and repository workflow surface
* License: Apache License Version 2.0

## One-sentence role

MAILSIEVE performs bounded, resumable discovery of publicly exposed business email addresses from declared domains while preserving rate discipline, output traceability, and evidence-oriented collection hygiene without becoming a proof surface, verifier, authority issuer, runtime, archive, or intake system.

## What this repository is

MAILSIEVE is an operator-facing discovery utility.

It exists for cases where a user needs to:

* process domain lists
* discover publicly exposed business email addresses
* preserve resumability across long-running collection batches
* keep rate discipline against public websites
* emit append-only result sets
* preserve lightweight collection evidence for later review

This repository is for controlled collection workflows where:

* input is a domain list
* output is a technical discovery result
* evidence of the crawl path matters
* restart safety matters
* rate limiting matters
* non-destructive operator review matters

It is an operational tool, not a truth engine.

## What this repository is not

MAILSIEVE is not:

* the VERIFRAX protocol repository
* an authority issuance surface
* a governed execution runtime
* a proof publication surface
* the public verifier
* the artifact-chain evidence root
* an archive surface
* an intake or applicant-flow surface
* a commercial landing surface
* a compliance system
* an identity system
* a guarantee of email validity, deliverability, ownership, consent, or permission

MAILSIEVE does not:

* prove that a discovered address is current
* prove that a discovered address belongs to a legal entity
* prove consent to contact
* prove business legitimacy
* issue a seal
* record a CORPIFORM receipt
* verify artifact-0005
* replace `https://verify.verifrax.net/`
* publish proof material to `proof.verifrax.net`
* define repository governance

The strongest boundary here is simple:

MAILSIEVE discovers public contact data candidates.
It does not convert them into verified truth.

## Relationship to the Verifrax perimeter

MAILSIEVE is perimeter-adjacent tooling.

It is connected to the broader Verifrax system only as an operational utility that may support research, outreach, collection, or evidence-oriented preparation work.

It is not part of the main authority → execution → verification path.

That main path is:

* `.github` — governance root
* `AUCTORISEAL` — authority issuance/reference
* `CORPIFORM` — governed execution and receipt boundary
* `VERIFRAX` — authored source and evidence-root chain record
* `VERIFRAX-verify` — public verifier
* `proof` — public proof publication
* `SIGILLARIUM` — seal/archive reference

MAILSIEVE sits outside that core chain.

If governance or artifact references ever apply to MAILSIEVE, those references come from the governed org surfaces and evidence root, not from self-assertion in this README.

## Why artifact-0005 must still be named here

Artifact-0005 must remain visible across the repo perimeter so that adjacent tooling does not drift into invented system history.

But MAILSIEVE must describe that relationship correctly.

MAILSIEVE does not:

* create artifact-0005
* execute artifact-0005
* verify artifact-0005
* register artifact-0005
* serve artifact-0005 publicly

MAILSIEVE may only acknowledge that artifact-0005 is the load-bearing chain boundary in the broader Verifrax system and that this repository is downstream or adjacent operational tooling, not the artifact owner.

If MAILSIEVE starts sounding like evidence-root truth, it is already wrong.

## Why the verifier must still be visible here

A perimeter tool should not imply that collection output is self-authenticating.

That is why the public verifier must remain visible even here:

* repository: `VERIFRAX-verify`
* live verifier: `https://verify.verifrax.net/`

Not because MAILSIEVE emits verifier-ready proof objects by default, but because the org perimeter must keep verification separate from collection.

Collection is not verification.
Discovery is not proof.
Evidence logging is not governed receipt generation.

## Public host ownership

MAILSIEVE owns no public Verifrax hostname.

It does not own:

* `api.verifrax.net`
* `proof.verifrax.net`
* `apply.verifrax.net`
* `verify.verifrax.net`
* `auctoriseal.verifrax.net`
* `corpiform.verifrax.net`
* `cicullis.verifrax.net`
* `sigillarium.verifrax.net`
* `docs.verifrax.net`
* `status.verifrax.net`

That absence must be explicit so that no one mistakes this repository for a public product surface.

## Problem this repository solves

MAILSIEVE solves a narrow operational problem:

given a set of domains, how do you discover publicly listed business email addresses in a way that is:

* resumable
* rate-controlled
* append-only in result handling
* evidence-aware
* operator-reviewable

It does not solve:

* contact consent
* legal basis for outreach
* business verification
* identity proof
* authority proof
* artifact verification
* chain registration

## Operational model

The repository’s operational pattern is:

1. read domains from operator input
2. normalize the targets
3. crawl bounded public surfaces politely
4. extract candidate business email addresses
5. append structured results
6. preserve processing state for resume
7. write lightweight evidence logs for later inspection

That is the whole model.

Anything stronger than that should be rejected.

## Core surfaces

The repository currently centers on surfaces such as:

* `domains.txt` or equivalent operator input
* `processed.txt` for resumability
* `results.csv` for append-only collection output
* `logs/evidence.jsonl` or equivalent crawl evidence trail
* shell or Node-based runner surfaces
* rate and concurrency tuning surfaces

Those surfaces are operational convenience and inspection aids.

They are not authoritative records.

## Inputs and outputs

### Inputs

MAILSIEVE consumes:

* domain lists
* public web pages reachable from those domains
* operator-selected concurrency and rate parameters
* local execution environment

### Outputs

MAILSIEVE emits:

* candidate email address rows
* processed-domain state
* evidence-oriented crawl logs
* diagnostic output for operator review

It does not emit:

* proof objects
* governed receipts
* authority objects
* artifact registration records
* verification verdicts
* legal determinations

## Usage boundary

Use MAILSIEVE when you need bounded technical discovery.

Do not use MAILSIEVE as a substitute for:

* human review
* consent analysis
* compliance review
* deliverability testing
* identity verification
* authority validation
* repository governance truth

The limiting case is the important one:

if MAILSIEVE finds `contact@example.com`, that only proves that the tool found a public string matching an email pattern in a collection context.
It does not prove that anyone should rely on it.

## Reliability posture

MAILSIEVE is optimized around collection discipline rather than certainty.

That means it prioritizes:

* restart safety
* controlled fan-out
* rate awareness
* append-only output handling
* evidence logging

It does not promise:

* exhaustive discovery
* perfect extraction
* freshness of every result
* deliverability of discovered addresses
* semantic correctness of every page interpretation

A slow bounded tool with inspectable outputs is better than an aggressive crawler with ambiguous state.


## Verifrax system path labels

The governed Verifrax path that this README must stay compatible with is:

1. `.github` — organization governance and governed repository boundary
2. `AUCTORISEAL` — authority issuance and public authority reference
3. `CORPIFORM` — governed execution and receipt emission
4. `VERIFRAX` — authored protocol, evidence root, and artifact-chain registration boundary
5. `VERIFRAX-SPEC` — derived specification publication surface
6. `VERIFRAX-PROFILES` — deterministic profile-constraint surface
7. `VERIFRAX-SAMPLES` — pinned sample and reproducibility surface
8. `VERIFRAX-verify` — public verification repository and UI boundary
9. `VERIFRAX-DOCS` — explanatory documentation surface
10. `cicullis` — enforcement boundary
11. `proof` — proof publication surface
12. `SIGILLARIUM` — seal and archive reference surface
13. `apply` — intake surface

The live host-label map that must remain explicit and non-contradictory is:

* `https://api.verifrax.net/` — execution surface
* `https://proof.verifrax.net/` — proof publication surface
* `https://auctoriseal.verifrax.net/` — authority issuance and authority reference surface
* `https://corpiform.verifrax.net/` — runtime and receipt reference surface
* `https://cicullis.verifrax.net/` — enforcement reference surface
* `https://verify.verifrax.net/` — public verification surface
* `https://sigillarium.verifrax.net/` — seal and archive reference surface
* `https://apply.verifrax.net/` — intake surface
* `https://docs.verifrax.net/` — documentation surface

This README must remain compatible with `artifact-0005` as the load-bearing authority → execution → verification → evidence boundary without claiming that this repository alone authors, proves, seals, or registers `artifact-0005` unless that role is actually true for this repository.


## Security and misuse boundary

The main risk in this repository is misuse through over-interpretation or abusive collection behavior.

This README must therefore keep three lines hard:

* public data discovery is not permission
* technical evidence is not legal justification
* candidate contact information is not verified identity

A second risk is perimeter drift: turning a collection tool into a fake verifier or fake evidence root by language alone.

That must not happen.

## Canonical related repositories and surfaces

* [`.github`](https://github.com/Verifrax/.github) — governance root
* [`VERIFRAX`](https://github.com/Verifrax/VERIFRAX) — authored source and evidence-root chain record
* [`AUCTORISEAL`](https://github.com/Verifrax/AUCTORISEAL) — authority issuance/reference
* [`CORPIFORM`](https://github.com/Verifrax/CORPIFORM) — governed execution and receipt boundary
* [`VERIFRAX-verify`](https://github.com/Verifrax/VERIFRAX-verify) — public verifier repository
* [`https://verify.verifrax.net/`](https://verify.verifrax.net/) — public verifier surface
* [`proof`](https://github.com/Verifrax/proof) — proof publication surface
* [`SIGILLARIUM`](https://github.com/Verifrax/SIGILLARIUM) — seal/archive reference surface

## CI and governance expectations

If CI exists here, it should prove operational properties only:

* input normalization behavior
* resumability correctness
* append-only result handling
* rate and concurrency guard behavior
* deterministic parsing expectations where applicable

This README must not imply protocol-grade determinism, chain authority, or governed execution unless the repository actually proves those properties.

## Reader contract

A reader landing here must be able to answer immediately:

1. What exactly does MAILSIEVE do?
2. What does it not prove?
3. Does it own any Verifrax public host? No.
4. Is it the verifier? No.
5. Is it part of artifact-0005 proof or registration? No.
6. Where does public verification actually live? `https://verify.verifrax.net/`

If those answers are not obvious, the README is still weak.

## Contributing

A contribution here is wrong if it:

* upgrades discovery language into verification language
* implies consent, legality, or authority from collection output
* implies ownership of a public Verifrax host
* implies artifact-0005 was produced or verified here
* removes the distinction between collection and verification
* removes the distinction between logging and governed receipts
* adds package or deployment claims not backed by repository metadata

## License

Apache License Version 2.0. See `LICENSE`.
