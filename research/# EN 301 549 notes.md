# EN 301 549 notes

## Things to research and document

* For 9.7: browser settings that could be in scope for "user preference settings". Do they include settings in the underlying OS that the browser honors?

## How I researched this

Converted the docx to Google Docs
Copied text from the editor.
Pasted into Visual Studio Code.
Compared the 2025-11 and 2026-06 docs.

## Changes from version 2025-11 to 2026-06

Editorial: applicability to assistive technologies

Informative, substantive: some cross-references to other documents clarified and corrected

Terms added

* caller identification
* destination address
* height in CSSpx
* lipspeaking
* physical height
* relay service invocation functions
* x-height

Terms edited

* documented accessibility feature
* documented platform accessibility feature
* operable part
* secondary user (of relay service)

Terms removed

* RTT capabilities

Term renamed

* stationary hardware ICT → stationary ICT

4.2 clauses have new preconditions.

Editorial:

* 4.2.2 Usage with limited vision: Note 5
* 4.2.8 Usage with limited reach

Substantive:

* 4.2.10 Usage with limited cognition, language or learning
  * New precondition (almost always met)
  * New Note 6 (clarity matching my expectation)
* 4.2.11 Privacy: substantive edit

5.1.3.2	Auditory output delivery including speech

* New Note 6, clarity matching my expectation

5.1.3.4	Speech output user control

* Fixed typo in Note 1

5.1.4 Functionality closed to text enlargement

* Note 1 edited
* Note 4 added

5.10.2	Accessible content creation

* minor typo fixed

6.0.2	Communication client

6.0.4	System connecting to another communication system

6.0.5	System with roaming visiting client

6.0.6	Client in emergency communications

6.0.7	Emergency communications 

6.0.8	System with roaming visiting client in an emergency

6.0.9	System with client in emergency visiting another country

6.2.2.2	Active communicator indication

6.2.2.4	Presentation of relative time order of text

6.2.2.5	Review of RTT communication contents

6.2.4	RTT responsiveness

6.2.5	Adding and erasing of RTT input

6.2.6	Processing rate of RTT

6.2.7	Character representation

6.2.9	RTT media establishment and use

and

6.5.1	General (informative)

* editorial

6.1.1	Voice communication interoperability

and

6.2.10	RTT interoperability

- source numbering

6.5.6	Indication of all active communication participants

- Renamed and substantive edits

7.2.1	Audio description playback

- editorial

7.3	User control of audiovisual accessibility features

- substantive edit: "and deactivation"

8.3 Stationary ICT

- major changes, TODO review in detail

8.3.14 Installation instructions

- substantive changes

8.4.3	Keys, tickets and cards

- substantive edit: cards are no longer limited to fare cards

8.8	Contrast on hardware

- substantive edit: changed "protrude or vice versa" to "tactilely discernible"


9.1.2.2	Subtitles (pre-recorded)

9.1.2.4	Subtitles (live)

- added note about "subtitle" vs "caption"

9.7	User preferences for web pages

- notable editorial
- cross-reference to 12.3 for the user agent documentation
- clarifies that the user agent is the platform

10.1.4.13	Content on hover or focus

- typo fixed

10.2.4.5	Multiple ways (Void)

- clarification agrees with my understanding

10.3.2.3	Consistent navigation

- word substitution provides substantive clarity

10.3.2.4	Consistent identification

- typo fixed

10.7	User preferences for non-web documents

- notable editorial, including removal of "reflow" as an example (though this does not mean reflow is or is not in scope)
- cross-reference to 12.3 for the user agent documentation
- clarifies that the user agent is the platform

11.1.4.13	Content on hover or focus

- fixed substantive typo that would have conflicted with WCAG
- now the precondition is not quite the same as the WCAG exception, but that's okay, the WCAG exception takes care of the rest.

11.6.1	User control of accessibility features

- Clarification agrees with my understanding, and gives a clue that settings of the underlying platform should pass through user agents to apply to documents. Rationale: when a browser supports an OS setting, it sounds to me like an accessibility feature of both the browser and the OS.
- Added cross-reference to 12.3 for the platform documentation

11.6.2	No disruption of accessibility features

- Editorial agrees with my understanding.
- Added cross-reference to 12.3 for the platform documentation

11.7	User preferences

- Removed "that users have set",  it clearer that system presets would also be in scope.
- Added an essential exception
- Added cross-reference to 12.3 for the platform documentation
- Clarified that the OS is usually the platform.

12.3	Accessibility and compatibility features

- Precondition: tightened from "information about the ICT" to "documentation about the use of the ICT"
- Expectation: removed "any accessibility provisions that are not met"; other editorial agrees with my understanding.

12.5	Electronic program guide display

- editorial does not change the meaning

13.1.1	General (informative)

- Edits, not sure if they're substantive.

13.1.2	Relay service access — *sub-clauses*

- Skimmed. Appears mainly to be editorial aligning with ES 202 975 and EN 303 919.

Annex C

- Edits throughout. Most minor; some substantive typo fixes; some matching meaningful changes in the technical requirements.

C.11.7 User preferences

- Possible issue: "essential" in the requirement sounds different from "fundamental" in the conformance test.

C.12.3	Accessibility and compatibility features

- Possible issue: the conformance test omits the requirement to provide information about support services relevant to accessibility.
