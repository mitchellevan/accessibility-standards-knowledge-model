<div ai-disclosure="ai-assisted" ai-assisted-percent="60"> <!-- I outlined the description of Stage 1 and Stage 2; AI drafted; I reviewed and edited. -->

## Stage 1: convert "relationship observations" into structured data

I consider this stage completed in commit `ec069c1`.

## Stage 2: YAML readiness for data

To make the model ready for larger-scale data entry:

1. YAML files pass parsing validation.
1. The examples have consistent shapes.
1. Five to ten meaningfully different knowledge relationships fit without awkward workarounds.
1. Uncertainties in the knowledge content are represented explicitly rather than forced into premature categories.
1. YAML files pass schema validation.
1. A small prototype program produces useful comparison views, read-only.
1. YAML files pass additional validation for usefulness, such as checking for broken cross-references.

The goal at this stage is to make the model stable enough to replicate, not perfect. I expect the model to continue evolving in smaller ways as it grows to accommodate more sources.

This stage could be characterized as example-driven schema development.

</div>
<div ai-disclosure="human-only">

## Backlog

Normative vs. informative
* Mark normative vs. informative fragments.
* Decide how these become normative vs. informative expectations.
* Do documents differ in the weight carried by normative vs. informative? E.g., necessary for conformance (where conformance is the result), or necessary for compliance (where it's a legal or policy document), or maybe something else.

Establish all identifiers for each key source document.
* So ASKM-internal references won't churn.
* This can be done manually or with utility code (q.v.).

Develop a utility to extract fragment stubs from a document.
* Start with EN 301 549.
  * Argument for: Its PDF format would otherwise make manual copy-and-paste laborious.
  * Argument for: Future revisions are expected, more frequently than some other standards.
* Would other source documents benefit from an extraction utility?
  * Argument for: Transparency (a basic principle of the ASKM endeavor). Any human-judgment decisions, e.g. about what should be considered the name of a fragment, can be documented with the utility.
  * TBD: relative effort
* Results of the extraction will include information determined by the source, with little or no per-fragment judgment necessary: identifier, name, URI. These elements will constitute the fragment stub in the model.
* Reminder: respect copyright.

## Ice box

Change from YAML to a different format for the system of record? Defer this indefinitely; only if YAML becomes too limiting.

I thought about this idea: "when" and "then" instead of "applicability_conditions" and "expectations"? I didn't change it (as of 2026-08-03) because it's easier to refer to labels that are nouns. This idea might be worth revisiting for an app.

</div>