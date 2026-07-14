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

## First attempt at relationship mapping: "language of parts" applied to non-web

This is a first attempt at mapping similar expectations to each other in several source documents. The goal of this attempt is to exercise the ontology.

### (A) Guidelines expecting programmatic characteristics

* WCAG [SC 3.1.2](https://www.w3.org/TR/WCAG22/#language-of-parts) *Language of Parts*
  * Applicability condition: Web. See "WCAG applicability".
  * Expectation: The human language of each phrase is programmatically identified. (Paraphrased)
* WCAG2ICT fragment xxxx 
* EN 301 549 v4:
  * [9.3.1.2](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.00_30/en_301549v040100va.pdf?page=67) *Language of parts*
    * Applicability condition: web
    * Expectation: includes WCAG SC 3.1.2 by reference.
  * [10.3.1.2](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.00_30/en_301549v040100va.pdf?page=82) *Language of parts*
    * Applicability condition: non-web document
    * Expectation: The human language of each phrase is programmatically identified. (Paraphrased)
  * [12.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.00_30/en_301549v040100va.pdf?page=106) Accessibility information about products
    * Applicability condition 1: Web content provides information about a product.
    * Expectation 1: This information in web content meets clause 9 (+- WCAG 2.2).
    * Applicability condition 2: A non-web document provides information about a product.
    * Expectation 2: This information in a non-web document meets clause 10 (+- WCAG 2.2).
    * Applicability condition 2: Non-web software provides information about a product.
    * Expectation 2: This information in non-web software meets clause 11 (+- WCAG 2.2).
      * Remember that clause 11 does not include a language-of-parts guideline for non-web software. See "Non-expectations".
  * [12.2](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.00_30/en_301549v040100va.pdf?page=107) Accessibility information about services
    * Like 12.1: s/product/service/
* EAA
  * EAA Annex I(I)(1)(i-iv) "the information on the use of the product provided on the product itself... shall be accompanied... by accessible information"
  * EAA Annex I(III)(b)(ii) Services: "be presented in an understandable way"
  * TODO more?
  * Rationale: TODO

### (A2) Guidelines expecting programmatic characteristics in content creation

* EN 301 549 v4:
  * 5.10.2 *Accessible content creation*
    * Case a
      * Applicability condition 1: A content creation tool (defined in clause 3.1 *Terms* 'authoring tool') that creates web content.
      * Expectation 1a: The content creation tool enables its users to create web content that meets clause 9 (+- WCAG 2.2), to the extent described in clause 5.10.1.
      * Expectation 1b: s/enables/guides/
    * Case b
      * Applicability condition 2: A content creation tool (defined in clause 3.1 *Terms* 'authoring tool') that creates non-web document content.
      * Expectation 2a: The content creation tool enables its users to create non-web document content that meets clause 10 (+- WCAG 2.2), to the extent described in clause 5.10.1.
      * Expectation 2b: s/enables/guides/
    * Case c
      * Applicability condition 3: A content creation tool (defined in clause 3.1 *Terms* 'authoring tool') that creates non-web software content.
      * Expectation 3a: The content creation tool enables its users to create non-web software content that meets clause 11 (+- WCAG 2.2), to the extent described in clause 5.10.1.
      * Expectation 3b: s/enables/guides/
      * Remember that clause 11 does not include a language-of-parts guideline for non-web software. See "Non-expectations".
  * 5.10.3 *Preservation of accessibility information in transformations*
    * Applicability: a content creation tool (Terms: 'authoring tool') that transforms an input, and the input can contain accessibility information (implied by 'preserved'). ("Accessibility information" needs a de facto definition.)
    * Expectation: the accessibility information is preserved in the output, to the extent described in clause 5.10.1.
      * Rationale: ASKM interprets 5.10.1 "to the extent supported" as meaning the same as 5.10.3 "if mechanisms exist".
    * In context of 5.10.3, "accessibility information" is not limited to info required for clauses 9–11. So 5.10.3 could apply to language-of-parts information in non-web software content as input, depending on its format and technology. And 5.10.3 could expect preservation of language-of-parts information in non-web software content as output, depending on its format and technology.
  * 5.10.4 Repair assistance
    * Applicability: like 5.10.2, and the tool detects failures of 9, 10, or 11
      * Remember that clause 11 does not include a language-of-parts guideline for non-web software. See "Non-expectations".
    * Expectation: inform the user and help them fix the problems (see 5.10.4 and its notes)
  * 5.10.5 *Templates*
    * Applicability: like 5.10.2, and the tool has templates
    * Expectation 1: One or more templates meet the expectations of 5.10.2.
      * Rationale: ASKM interprets 5.10.5 "supports" to mean the same as 5.10.2 "enable and guide".
      * Remember that clause 11 does not include a language-of-parts guideline for non-web software. See "Non-expectations".
    * Expectation 2: Users are accurately informed of at least one template meeting expectation 1.
* EAA TODO

### (B) Guidelines expecting characteristics of speech output

* EN 301 549 v3.2.1 → 5.1.3.14 Spoken languages
  * Applicability condition: "Where speech output is provided as non-visual access to closed functionality"
  * Expectation: The human language of speech output is the same as the human language of the visual content. (Paraphrased; see the source for exceptions.)
* EN 301 549 v4 → 5.1.3.14 Spoken languages
  * Applicability condition: "Where ICT includes closed functionality, and speech output is provided as non-visual access to closed functionality"
  * Expectation: The human language of speech output is the same as the human language of the visual content. (Paraphrased; see the source for exceptions.)
* Relationship between the above:
  * Applicability conditions: Same.
    * Rationale: The phrase is more precise in v4 but conveys the same intent as in v3.2.1.
  * Expectation: Same.
    * Rationale: The words are identical.
* WCAG2ICT fragment A_3.26: "3.1.2 Language of Parts — Depends upon language information in a programmatically determinable form intended to drive correct pronunciation. Where another mechanism achieves correct pronunciation for ICT with closed functionality, such as self-voicing, the intent of this success criterion would be met."
  * Applicability condition: Don't use WCAG; use other accessibility guidelines that apply to closed functionality.
    * Rationale: WCAG2ICT fragment A_3.0: "For non-web software on ICT with closed functionality, those who implement this document (WCAG2ICT) should consider the applicability of individual WCAG 2 success criteria on a criterion-by-criterion basis. Alternate accessibility provisions might be needed to cover the user needs addressed by the following success criteria"
  * Expectation: Pronunciation is correct. (Paraphrased.)
* EAA
  * Source document URI: https://eur-lex.europa.eu/eli/dir/2019/882
  * EAA Annex I(I)(2)(a) "do so via more than one sensory channel; this shall include providing alternatives to vision, auditory, speech and tactile elements"
  * EAA Annex I(I)(2)(o)(i) Self-service terminals: "provide for text-to-speech technology"
  * Rationale: EN 301 549 v4 Table ZB.2 maps its clause 5.1.3.14 "Spoken languages" to the aforementioned EAA source fragments (provisions).

### (C) Relationship between (A) and (B)

* Applicability conditions: Different.
* Expectation: Similar.
* Rationale:
  * According to [Understanding SC 3.1.2](https://www.w3.org/WAI/WCAG22/Understanding/language-of-parts.html), part of the intent is "Screen readers can use the pronunciation rules of the language of the text." (Retrieved 2026-07-12)
  * According to WCAG2ICT fragment A_3.26, the intent of WCAG 3.1.2 is correct pronunciation.

### (D) Non-expectations

* EN 301 549 v3.2.1 clause 11.3.1.2 "Void"
  * Contains a note: Void because "language of parts" would be impossible for software. (Paraphrased.)
* EN 301 549 v4 clause 11.3.1.2 "Language of Parts (Void)"
  * Contains a note: Void because "language of parts" would be impossible for software. (Paraphrased.)
* BIK BITV-Test (App): no test.
  * Source document retrieved: 2026-07-10
  * ASKM comment: Omission of a language-of-parts guideline is consistent with the scope of "BIK BITV-Test (App)". The scope (https://bitvtest.de/tests-und-beratung/bik-bitv-test-app) is the BITV requirements that apply to mobile apps, based on EN 301 549 version 3.2.1 (https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf), which does not contain a guideline for language of parts in open non-web software.
* BIK BITV-Test + WCAG 2.2 (App): no test.
  * Source document retrieved: 2026-07-10
  * ASKM comment: Same as for language-of-parts for BIK BITV-Test (App).
* WCAG2ICT-Test (App) (BIK): no test.
  * Source document retrieved: 2026-07-10
  * ASKM comment: Omission of a language-of-parts guideline is not consistent with the scope of "WCAG2ICT-Test (App) (BIK)". The scope (https://bitvtest.de/tests-und-beratung/bik-bitv-test-app) is the WCAG requirements that apply to mobile apps, based on WCAG2ICT (https://www.w3.org/TR/wcag2ict/#language-of-parts). However, WCAG2ICT does provide such guidance.

### Applicability conditions for WCAG 2 as a whole

WCAG 2 applies to web pages, online and offline documents, and open software applications (those that can interoperate with assistive technology). Some WCAG success criteria apply to closed software.

Rationale:

* WCAG 2 does not have a formal precondition that would limit the applicability of all its success criteria. WCAG 2 and its related documents do describe the kinds of ICT where WCAG 2 is relevant.
  * WCAG Overview fragment _1 [Introduction](https://www.w3.org/WAI/standards-guidelines/wcag/#intro), fragment _1.3 (retrieved 2026-07-12): "WCAG applies to dynamic content, multimedia, web on mobile, and AI web interfaces. WCAG can also be applied to non-web information and communications technologies (ICT) such as native apps, software, and documents, as described in [WCAG2ICT](https://www.w3.org/WAI/standards-guidelines/wcag/non-web-ict/)." The link goes to the source document "WCAG2ICT Overview".
* WCAG 2 is directly relevant to web content. This means HTML web pages and some other kinds of content.
  * WCAG 2.2 fragment _0.1 [Abstract](https://www.w3.org/TR/WCAG22/#abstract), fragment _0.1.1: "Web Content Accessibility Guidelines (WCAG) 2.2 covers a wide range of recommendations for making web content more accessible."
  * WCAG 2.2 fragment _0.1 [Abstract](https://www.w3.org/TR/WCAG22/#abstract), fragment _0.1.2: "WCAG 2.2 success criteria are written as testable statements that are not technology-specific."
  * WCAG 2.2 fragment _0.3.4 [Requirements for WCAG 2.2](https://www.w3.org/TR/WCAG22/#requirements-for-wcag-2-2) links to the source document "Requirements for Web Content Accessibility Guidelines 2.2" (paraphrased name: Requirements for WCAG 2.2).
    * Requirements for WCAG 2.2 fragment 1 [Introduction](https://w3c.github.io/wcag/requirements/22/#introduction), fragment 1_2 (retrieved 2026-07-12): "The underlying goal of WCAG 2.2 requirements are the same as for WCAG 2.0 and WCAG 2.1 – to promote accessibility of Web content."
    * Requirements for WCAG 2.2 fragment 3.1 [Success Criterion Characteristics](https://w3c.github.io/wcag/requirements/22/#success-criterion-characteristics), fragment 3.1_6 (retrieved 2026-07-12): "Success criteria should... Apply to all content across all websites unless preconditions for the application of the success criteria are explicitly identified (e.g. 'except interruptions involving an emergency')."
    * Requirements for WCAG 2.2 fragment 3.1 [Success Criterion Characteristics](https://w3c.github.io/wcag/requirements/22/#success-criterion-characteristics), fragment 3.1_7 (retrieved 2026-07-12): "Success criteria should... Apply across technologies to the greatest extent possible."
  * "Web" is not defined. "Web page" means anything served from a URL and presented in a user agent. "Web content" also relies on a user agent.
    * WCAG 2.2 fragment 6 *Glossary:* [web page](https://www.w3.org/TR/WCAG22/#dfn-web-page-s)
    * WCAG 2.2 fragment 6 *Glossary:* [content](https://www.w3.org/TR/WCAG22/#dfn-content)
  * "Technologies" means web content technologies.
    * WCAG 2.2 fragment 6 *Glossary:* [technology](https://www.w3.org/TR/WCAG22/#dfn-technologies)
    * [Understanding Techniques for WCAG 2.2 Success Criteria](https://www.w3.org/WAI/WCAG22/Understanding/understanding-techniques)
    * [Techniques for WCAG 2.2](https://www.w3.org/WAI/WCAG22/Techniques/) (retrieved 2026-07-15) lists these web content technologies: ARIA, client-side script, CSS, HTML, PDF, server-side script, SMIL, and plain text.
* WCAG 2 can be applied to non-web documents and software, with some exceptions.
  * [WCAG2ICT Overview](https://www.w3.org/WAI/standards-guidelines/wcag/non-web-ict/) fragment _0.0 Summary (retrieved 2026-07-12): "[WCAG2ICT](https://www.w3.org/TR/wcag2ict/)... describes how Web Content Accessibility Guidelines (WCAG) principles, guidelines, and success criteria can be applied to documents, software, and other information and communications technologies (ICT)." The link goes to the source document "Guidance on Applying WCAG 2 to Non-Web Information and Communications Technologies (WCAG2ICT)" (paraphrased name: WCAG2ICT)
  * WCAG2ICT fragment _1 [Abstract](https://www.w3.org/TR/wcag2ict/#abstract) (retrieved 2026-07-12): "This document describes how the Web Content Accessibility Guidelines (WCAG) versions 2.0 [WCAG20], 2.1 [WCAG21], and 2.2 [WCAG22] principles, guidelines, and success criteria can be applied to non-web Information and Communications Technologies (ICT), specifically to non-web documents and software. It provides informative guidance (guidance that is not normative and does not set requirements)."
  * WCAG2ICT fragment _3.2.1 [Interpretation of web terminology in a non-web context](https://w3c.github.io/wcag2ict/#interpretation-of-web-terminology-in-a-non-web-context), fragment _3.2.1.3 (editor's draft retrieved 2026-07-12):
    * "Not all success criteria have been fully adopted in all local standards, regulations, and legislation, and may not be applicable to all technologies. WCAG2ICT has been used in some standards and regulations to determine whether or not to apply certain success criteria. Some standards (for example, Section 508 in the U.S., and EN 301 549 in Europe) do not apply WCAG 2 Success Criteria 2.4.1 Bypass Blocks, 2.4.5 Multiple Ways, 3.2.3 Consistent Navigation, and 3.2.4 Consistent Identification to non-web documents and non-web software. In addition, EN 301 549 does not apply 2.4.2 Page Titled and 3.1.2 Language of Parts to non-web software. In contrast, the U.S. Department of Justice [Guidance to Revisions to ADA Title II Regulation on Accessibility of Web Information and Services of State and Local Government Entities, Appendix D to Part 35, Title 28](https://www.ecfr.gov/current/title-28/chapter-I/part-35/appendix-Appendix%20D%20to%20Part%2035), directs implementers to utilize the guidance in WCAG2ICT to determine the applicability of success criteria and how to apply the requirements to mobile applications. Since WCAG2ICT does not specifically say which criteria can or should apply, those implementing WCAG2ICT should consider the applicability of individual success criteria to non-web documents and non-web software."
  * TODO applied to text-based terminal applications
  * TODO problematic for closed

### Learnings from this example

Overall this was a good exercise. It shows how relationships can work among specific guideline fragments. It also led to ASKM content that will get reused for many fragments (e.g., WCAG 2 applicability as a whole; guidelines for authoring tools).

Each source document should be an object in the model.

Each source fragment should be an object in the model.

Each referral to a source should point to the source's object in the model, not directly to a URL of the source.
* Easier for maintenance
* Prevents ambiguity, e.g. in EN 301 549 where source fragments don't have unique URLs.

It's too time-consuming to write each source fragment manually in each citation, especially when they are not numbered in the source document. These things will help:

* To the extent allowed by copyright, index the whole source document in the model my numbering all major source fragments.
* When drafting content before the cited source fragments have been indexed:
  * Cite a higher-level source, even the whole document, and quote the source.
  * Cite the section by name only (e.g., its heading) when there is no numerical identifier.

For WCAG applied to non-web, I'll need to decide how to cite sources.

* Option: Where ASKM cites a guideline in WCAG2ICT, it should be understood as citing WCAG interpreted by WCAG2ICT.
* Option: Cite both WCAG2ICT and WCAG each time.

Provisional decision: Don't record two contradictory relationships. Instead, each claim (or "statement"? or "assertion"?) in the model (e.g. "relationship" or "is named") should have a rationale. A rationale contains one or more pro arguments, and zero or more con arguments.

There should be a way to indicate a "TODO"-equivalent directly in the model.
* Because there will be so many TODOs it would overwhelm the issue tracker.
* Because even just a "TODO" in the model is a signal to somebody reading the model that there's a potential connection.

Applicability conditions should have a short form to normalize them, making comparison straightforward regardless of different wording.

Open question: how structured are rationales and arguments?
* I feel there should be an enumerated type, with values such such as:
  * "plain reading" with a source object
  * "interpreted reading" with the interpretation and one or more source object
  * "identical text" as evidence of a relationship
* Is "analysis" another thing? A prose explanation, which can have additional rationale.

Open question: how should the model represent "my comments"?

Open question: is this easy enough, lightweight enough? While also being well grounded in evidence?

I'll probably need a way to mark "citation needed", so I can record a more or less established opinion quickly without getting sidetracked on finding exact sources. The "citation needed" can also have a prose comment, like "probably in WCAG2ICT"

The whole model will need to be localizable, while meeting this same language-of-parts requirement.
* Can the default language be English, while allowing any tree or leaf to override the language?
* I'll probably need to mix languages within a text string, such as a comment or rationale. Plan to beat: span element with lang attribute.