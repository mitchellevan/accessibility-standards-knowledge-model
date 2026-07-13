## General principles

All knowledge in ASKM should be clearly attributed to its provenance.

Most of the knowledge here should derive from outside sources.

Where an author of ASKM has added their own knowledge, that knowledge should also be attributed.

The subject matter of ASKM is accessibility evaluation. Remember: evaluations are only predictions of what real-world users will experience. True accessibility is the quality of user experiences, not the results of expert evaluations.

## Identifiers of source fragments

Identifier numbering MUST meet these goals:

1. Each identifier is unique within the source.
2. When a source fragment is not numbered in the source, the sort order of its identifier matches the sequence in the source.

Identifier numbering SHOULD meet these goals:

3. When a source fragment is numbered in the source, that number is recognizable in the identifier. (Exception: a secondary numbering system, such as tables or figures, should be ignored in the identifiers if it would break the sequence.)
4. When a source fragment is numbered in the source, the sort order of its identifier matches the sequence in the source. (Goal 3 is more important than goal 2.)

How:

* Fragments not numbered in the source document get "_" before the numbering in the identifier.
* When a fragment is numbered in the source document but a sub-fragment is not numbered, a "_" separates these two parts of the identifier.
* Skip a table of contents that's the same as the document itself.
* Use "0" for items before the source numbering starts.
* Use "99" or "999" for items after the source numbering ends.
* When a paragraph is followed by a related list, a best practice is to provide a paragraph number that encompasses both the paragraph and the list. This allows shorthand like "paragraph 3" and "paragraph 4" to match the identifiers, even with intervening lists. See EN 301 549 for an example.
* When a fragment has notes (inline, footnotes, or endnotes), usually number them with the fragment they belong to.
* But a glossary for a whole document would be better numbered on its own, even if cross-referenced like notes. It's a judgment call.

Potential limitations:

* If any source has an unnumbered fragment followed by a fragment numbered 0, then a different approach will be needed.

## Names of source fragments

* In general, err on the side of more verbatim quotes, fewer paraphrases. This makes it simpler for model authors to cite unnamed fragments, easier for model users to follow the citation to the original, and leans into the model's goal of source attribution.
* "Reserved" fragments help explain the identifier numbering hierarchy. They might be cited in the future.

