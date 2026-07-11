(Stub)

Here's where I will write my prose observations of how standards relate to each other.

I might call them "accessibility sources" which can include standards, regulations, and test procedures. But if I say "standards" it might be shorthand for those other things.

## Relationships

**Relationships** among standards, focusing on Section 508, EN 301 549, and WCAG. Examples:

* Including WCAG by reference. Except for some ICT types for some criteria.
* Clauses in two standards say the same thing.
* Clauses in two standards are similar or overlapping.

Also relations among clauses within one standard, e.g.

* Failing a test gets reported into two clauses: WCAG, software interoperability.

TBD: define "tests" as a thing? Or something more abstract than "tests", like the "requirement" part of a clause?

Similarities and differences can be:

* By definition or in practice
* Based on normative or informative text

## Applicability

A clause can apply to technology x...

* By definition
* In practice
* Theoretically, if examples exist

I also want to distinguish between an absence of relationship (e.g., not yet analyzed) and a negative relationship. Possible formulations that the model could offer:

* Negative relationship: Clause x does not apply to hardware.
* Negative relationship: Clause x does not apply to any other technologies, other than the ones listed in the model.
* Absence of relationship: Clause x applies to web content, but the model does not say anything about whether clause x does or does not apply to other technologies.

Clauses can inherit their applicability from ancestor clauses.

## The structure of standards (sources) and their clauses

We could think of a standard or source as just a large clause, the top-level ancestor of all of its constituent clauses.

## Technologies

"Technology" can be:

* A technology type defined by the standard, such as web, non-web software, non-web document, hardware
* A sub-type of another technology
* Orthogonal to other technologies, such as video player
* A ["content technology" as defined in WCAG](https://www.w3.org/TR/WCAG/#dfn-technologies)

## "Applicability" vs. "precondition"

"Applicability" and "precondition" are quite similar concepts. Open question: are they even different things?

Applicability is useful because it's common for two clauses to differ mainly by what technology they apply to, and otherwise they require the same or similar things.

## Rationales

A little or a lot of judgment is necessary to describe relationships. Judgment of things such as:

* Applicability "in practice"
* Equating or contrasting two requirements when their written formulations are different.

I'll start with just a prose "rationale" for each relationship. Over time these rationales might develop more formal structure of their own, such as:

* A reusable rationale formulation, as an object in the model
* Categories of the character of the rationale
* Confidence levels
* Internal-to-the-model or external-to-the model

## What should we call clauses and sources?

Possibilities:

* Clause — No. This would be confusing because the EN has numbered things that are clauses, and other things such as definitions and notes that are not clauses.
* Source
* Reference
* Guideline

## First attempt at relationship mapping

This is a first attempt at mapping one expectation to several source documents. This attempt is to see how the ontology works in a real example.

This example: "language of parts" applied to non-web.

* WCAG → 3.1.2 Language of Parts https://www.w3.org/TR/WCAG22/#language-of-parts
  * Expectation: programmatically determined human language identifier, which enables correct speech output pronunciation, and can be tested indirectly by a screen reader. (Paraphrased)
* WCAG2ICT → A_3.26: "3.1.2 Language of Parts — Depends upon language information in a programmatically determinable form intended to drive correct pronunciation. Where another mechanism achieves correct pronunciation for ICT with closed functionality, such as self-voicing, the intent of this success criterion would be met."
  * Expectation: correct pronunciation. (Paraphrased.)
* EN 301 549 v4 → 5.1.3.14 Spoken languages
  * Expectation: the human language of speech output is the same as the human language of the visual content. (Paraphrased.)
* BIK BITV-Test (App): no test.
  * Rationale of source document name: https://bitvtest.de/tests-und-beratung/bik-bitv-test-app
  * Source document URI: https://bitvtest.de/pruefverfahren/bitv-20-app
  * Source document retrieved: 2026-07-10
  * My comments: Omission of a language-of-parts guideline is correct. The scope of the "BIK BITV-Test (App)" source document is the BITV requirements that apply to mobile apps, based on EN 301 549 version 3.2.1. (https://bitvtest.de/tests-und-beratung/bik-bitv-test-app). The referenced EN document does not contain a guideline for language of parts in open non-web software. (TODO link to EN 301 549 v3.2.1)
* BIK BITV-Test + WCAG 2.2 (App):
  * Rationale of source document name: https://bitvtest.de/tests-und-beratung/bik-bitv-test-app
  * Source document URI: https://bitvtest.de/pruefverfahren/bitv-20-plus-app
  * Source document retrieved: 2026-07-10
  * My comments: Same as for language-of-parts for BIK BITV-Test (App).
* WCAG2ICT-Test (App) (BIK)
  * Rationale of source document name: The name listed here plus "(BIK)" for context. https://bitvtest.de/tests-und-beratung/bik-bitv-test-app
  * Source document URI: https://bitvtest.de/pruefverfahren/bitv-20-app
  * Source document retrieved: 2026-07-10
  * My comments: Omission of a language-of-parts guideline is incorrect. The scope of the "WCAG2ICT-Test (App) (BIK)" source document is the WCAG requirements that apply to mobile apps, based on WCAG2ICT. (https://bitvtest.de/tests-und-beratung/bik-bitv-test-app). However, WCAG2ICT does provide such guidance. https://www.w3.org/TR/wcag2ict/#language-of-parts
* EAA
  * Source document URI: https://eur-lex.europa.eu/eli/dir/2019/882
  * EAA Annex I(I)(2)(a) "do so via more than one sensory channel; this shall include providing alternatives to vision, auditory, speech and tactile elements"
  * EAA Annex I(I)(2)(o)(i) Self-service terminals: "provide for text-to-speech technology"
  * Rationale: EN 301 549 v4 maps its clause 5.1.3.14 "Spoken languages" Table ZB.2 to the aforementioned EAA source fragments (provisions).
* VPAT 2.5Rev TODO
* ACAA TODO
