# Swedish legal baseline

Use this reference to select the applicable regime and describe its relationship to technical standards. It is a maintained review aid, not a substitute for the current legal text. The sources below were checked on 2026-09-10.

## DOS-lagen: offentlig digital service

Primary law: [Lag (2018:1937) om tillgänglighet till digital offentlig service](https://www.riksdagen.se/sv/dokument-och-lagar/dokument/svensk-forfattningssamling/lag-20181937-om-tillganglighet-till-digital_sfs-2018-1937/) (DOS-lagen).

Potential scope includes state and municipal authorities, municipal or regional assemblies, publicly governed bodies, specified publicly financed private actors, and certain education providers. Read the current definitions and exclusions before concluding that an actor or content is covered.

For digital service under the actor's control, section 10 requires compliance with technical requirements issued under the law. Third-party-controlled service is subject to a "so far as possible" duty under section 11. The law includes limited content exclusions and an "unreasonably burdensome" exception; neither should be inferred from code alone.

Public actors must also provide an accessibility statement with a feedback/request function. A person can request access to certain excluded content, and accessibility feedback must be answered as soon as possible.

Digg states that its requirements correspond to Annex A of EN 301 549 V3.2.1 (2021-03). For web content this relies largely on WCAG 2.1 Level AA but includes requirements beyond WCAG. Use the exact currently incorporated version for a legal mapping. WCAG 2.2 can be reported separately as recommended best practice, not automatically as a DOS-lagen violation.

Official guidance:

- [Digg: Digital offentlig service ska vara tillgänglig](https://www.digg.se/kunskap-och-stod/regler-och-rekommendationer/regler-och-rekommendationer/digital-offentlig-service-ska-vara-tillganglig)
- [Digg: WCAG 2.1 AA och EN 301 549 Annex A](https://www.digg.se/kunskap-och-stod/regler-och-rekommendationer/regler-och-rekommendationer/pa-webbriktlinjer-finns-lagkrav-och-rekommendationer)

## LPTT: e-handel för konsumenter

Primary law: [Lag (2023:254) om vissa produkters och tjänsters tillgänglighet](https://www.riksdagen.se/sv/dokument-och-lagar/dokument/svensk-forfattningssamling/lag-2023254-om-vissa-produkters-och-tjansters_sfs-2023-254/) (LPTT). It entered into force on 28 June 2025.

An e-commerce service is, in summary, a remotely supplied website or mobile service provided electronically at a consumer's individual request for the purpose of concluding a consumer contract. Do not automatically apply this classification to purely B2B sites, informational catalogues with no consumer-contract purpose, or unrelated internal software.

The law covers in-scope consumer e-commerce services and requires ongoing conformity. It also requires information describing how the service meets accessibility requirements. Applicable transitional provisions exclude some pre-28-June-2025 prerecorded media, documents, and unchanged archives, and allow limited continuation of specified earlier products or contracts. Check the exact provision before relying on it.

Services supplied by a microenterprise are exempt under section 10. The statutory definition uses fewer than ten employees and annual turnover or annual balance-sheet total not exceeding EUR 2 million. Treat this as a scope fact requiring evidence, not an assumption. This service exemption does not erase possible product-related responsibilities or make accessibility unnecessary as best practice.

Requirements may also be disapplied where compliance would fundamentally alter the service or impose a disproportionate burden. Such reliance generally requires a documented, reasoned assessment and notification; a code reviewer should flag the issue for legal review rather than decide it.

[Post- och telestyrelsens föreskrifter (PTSFS 2024:6) om vissa tjänsters tillgänglighet](https://pts.se/regelbibliotek/foreskrifter-om-vissa-tjansters-tillganglighet/) require e-commerce services to meet the general service requirements and, specifically, to:

- reproduce available accessibility information about products and services sold
- make identification, security, and payment functions perceivable, operable, understandable, and robust when part of the service
- provide identification methods, electronic signatures, and payment services that satisfy those four principles

The general service rules also address accessible websites/apps, accessible usage and accessibility information, interoperability/testing information, and support services.

Current PTS guidance says EN 301 549 V3.2.1 covers much of the functional requirements and can guide implementation while relevant standards are updated. It recommends WCAG 2.2 additionally. Do not present either as a complete one-to-one legal safe harbor without verifying the current EU harmonized-standard status.

Official guidance and regulation:

- [PTS: Lagen om vissa produkters och tjänsters tillgänglighet](https://pts.se/digital-inkludering/lagen-om-vissa-produkters-och-tjansters-tillganglighet/)
- [PTS: Tillgänglighetskrav](https://pts.se/digital-inkludering/lagkrav/introduktion-till-tillganglighetsdirektivet/tillganglighetskrav/)
- [PTS: Branschspecifika krav för e-handel](https://pts.se/digital-inkludering/lagkrav/introduktion-till-tillganglighetsdirektivet/branschspecifika-krav/)
- [Post- och telestyrelsens föreskrifter (PTSFS 2024:6) om vissa tjänsters tillgänglighet](https://pts.se/regelbibliotek/foreskrifter-om-vissa-tjansters-tillganglighet/)

## When both may apply

Analyze each regime independently. A public actor can be subject to DOS-lagen while a consumer-facing transaction also falls within LPTT. Report overlapping duties once, with both legal bases, and preserve any differences in scope, documentation, exceptions, and enforcement.
