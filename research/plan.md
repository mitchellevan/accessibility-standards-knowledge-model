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

Move the backlog, the icebox, and some of the inline TODOs into GitHub issues.

Cite W3C's permissive copyright notices.

Split language_of_parts YAML file into its source documents.

Normative vs. informative
* Mark normative vs. informative fragments.
* Decide how these become normative vs. informative expectations.
* Do documents differ in the weight carried by normative vs. informative? E.g., necessary for conformance (where conformance is the result), or necessary for compliance (where it's a legal or policy document), or maybe something else.

Write a playbook for adding a source document. Here are initial thoughts. I'll iterate and refine the playbook with each new document I add.
* Start a file in "docs/sources" folder where I can gather notes.
* Summarize why I'm using this document at all.
* Check the copyright policy for the document, to see if copyright allows more than fair use.
* Add an entry in source_documents.yaml, alphabetized by short-name or name.
* If it's not already in archive.org, add it.
* Record the archive.org link in source_documents.yaml.
* Start a file in the "source_documents" folder.
* (Continue with fragments.)

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

Align with EARL. For conceptual and programmatic compatibility. https://www.w3.org/WAI/standards-guidelines/earl/
* Classify ASKM objects as `earl:TestCriterion`, `earl:TestRequirement`, and `earl:TestCase`.
* When summarizing a whole source documents, describe which kinds of `earl` objects it contains.
* Refer to names and descriptions as `dct:title` and `dct:description`, or gloss those classes.
* Don't overload terms that mean something different in EARL, such as `subject`.

Publish a stable URL for objects in ASKM.
* This would help others cite ASKM, including for example an EARL report.
* TBD whether ASKM itself could be used as a test suite, in the EARL sense. It's not a primary goal of ASKM, but it could be a secondary result.
* Step 1: write or generate IDs for objects.
* Step 2: create a website generator for objects.

Publish an API for reading the ASKM data.

## Ice box

Ask publishers for permission to copy, where it would go beyond fair use and be of value to users of the model.

Change from YAML to a different format for the system of record? Defer this indefinitely; only if YAML becomes too limiting.

I thought about this idea: "when" and "then" instead of "applicability_conditions" and "expectations"? I didn't change it (as of 2026-08-03) because it's easier to refer to labels that are nouns. This idea might be worth revisiting for an app.

</div>