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

## The structure of standards (sources) and their clauses.

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
