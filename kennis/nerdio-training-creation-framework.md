---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [l&d, instructional-design, addie, method, certification, course-production]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# The Nerdio training creation framework (Bas's L&D method)

Bas's reusable, repeatable method for taking a certification-level course from concept to certified learning experience. The reusable part is the *process and sequencing*, not any specific course content.

**1. Foundation = ADDIE.** Analyze, Design, Develop, Implement, Evaluate is the backbone.
- Analyze: identify the target audience (who they are, what they know, what they must master) and set the level: 100, 200, or 300.
- Design: define learning goals, choose the mix of text/video/interaction ('multimedia'), define assessments.
- Develop: the production phase, writing/recording/editing/building.
- Implement: publish in the LMS, wire up quizzes, certificates, automation.
- Evaluate: post-launch review of analytics and feedback, continuous improvement.
The **ADDIE document is the architectural blueprint**, owned by a *training architect* (there are multiple), who maps every module, lesson, and subtopic with objectives, delivery formats, and dependencies. It survives multiple reviews before anything proceeds, but stays flexible enough to change mid-flight.

**2. Outline & planning (still inside ADDIE).** Define module/lesson counts, text-vs-visual-vs-multimedia balance, which topics group together, expected learning time per module, and which lessons get quizzes/assignments/labs. Takes days of collaboration between architects, authors, editors, and multimedia designers. 'A solid outline sets the rhythm for everything that follows.'

**3. Kick-off.** Each certification course becomes its own **Asana project** holding every module, lesson, and task. Every task has an owner, deadline, and dependency (some tasks can only start after a prerequisite is finalized). Kick-off finalizes roles (authors, multimedia leads, reviewers, editors, project leads) and the timeline/deadlines. Work becomes cross-functional from here.

**Continuous progress tracking.** A dedicated project owner (deliberately *not* involved in content creation, so focus stays on flow) reviews status weekly: tasks approaching/exceeding deadlines, reassignments/escalations, next action + owner + due date. Asana dashboards keep deadlines, blockers, and dependencies visible.

**4. Writing & content creation.** Authors build text lessons first. Each lesson runs a structured workflow: draft -> review (SME review optional at this stage depending on author knowledge level) -> edit -> final approval, all tracked in Asana, with multiple pairs of eyes before release. Strict editorial/formatting standards: consistent tone and terminology, clear definitions and accurate technical phrasing, proper bullets/callouts, accessible balanced style. Images follow equally strict resolution/colour/branding standards and live in designated repositories. 'Consistency isn't by accident, it's what ensures quality and trust across all courses.'

**5. SME review & copy editing.** Optional SME review validates technical accuracy and relevance ('technical correctness is non-negotiable'). Then copy editors / technical writers review for language, flow, and adherence to the Nerdio editorial style guide, an iterative feedback-loop process.

**5.5. Centralized storage / asset management.** Before multimedia starts, every component goes into a centralized asset structure with its own repository per type: text lessons (version-controlled, naming conventions, revision history), scripts (stored separately so updates don't break video/audio sync), images/screenshots (optimized, shared libraries for reuse), videos/raw footage (strict version control, tagged by topic and duration), audio (narration linked to its script). Lets anyone locate/update/repurpose instantly and prevents duplication or data loss.

**6. Multimedia production.** Script (dialogue, pacing, visual direction) -> record (audio/video, sequential or simultaneous) -> edit (the 'Nerdio polish': remove filler, add transitions, embed graphics, sync) -> render/store (named, uploaded to media library for LMS integration).

**7. LMS assembly.** Assemble text + visuals + video inside the LMS, following the ADDIE blueprint exactly, module by module, lesson by lesson: text lessons with embedded visuals, video lessons, quizzes/checklists/interactive elements, downloadable templates. Multiple reviewers validate structure, navigation, design consistency.

**8. Question pool development.** The pool is the foundation of the certification exam. Each module contributes its own questions covering conceptual and scenario-based topics; questions are categorized by difficulty (easy/medium/hard), tagged by learning objective, and reviewed for accuracy and fairness. Goal: test understanding, not memorization (questions and answer order shuffle each attempt), with balanced coverage.

**9. Final integration & certification setup.** Generate xAPI and SCORM packages for LMS/cross-platform compatibility; design and link badges/certificates to completion triggers; automate certificate issuance; update learning paths. Also assess content reusability (lessons/visuals repurposable for other training, partner enablement, or the Knowledge Base), which Bas often considers before a course even begins.

**10. Testing, launch, continuous improvement.** Test every element (lessons, exams, automations, certificates) for usability, accuracy, accessibility, technical stability. After launch, run an ongoing review cycle: quarterly evaluations, mid-cycle spot checks, continuous monitoring of learner feedback, completion rates, and exam performance, feeding refinements. 'The result is a living system that keeps improving over time.'

**Why it's worth it:** detailed, demanding, time-consuming, but the badge represents hundreds of hours of cross-functional collaboration. 'No secret formula, just hard (team) work, dedication, staying on top of things and doing all that constantly.'

*Link to: nerdio-content skill / ADDIE, voice-profile (Nerdio register), question-pool standards.*

*Bron: Nerdio-content 'Behind the Certificate The Nerdio Training Creation Framework' (Blogs).*

## Verwante notities

- [Bas's ADDIE course-planning method](addie-course-planning-method.md)
- [Bas's ADDIE method for Nerdio course design](addie-method-nerdio-course-design.md)
- [Idea: 30-day Nerdio engineer bootcamp framework](idee-nerdio-30-day-engineer-bootcamp.md)
- [Method: The Learning Pyramid Applied to Technical Training](learning-pyramid-training-method.md)
- [Method: Bas's Nerdio lab-guide template convention](method-nerdio-lab-guide-template.md)
- [How Bas reviews Nerdio L&D content as SME](nme-course-content-review-method.md)
- [Scripting every video first measurably raises quality](position-scripting-raises-video-quality.md)
- [Training Method: Bringing Field Experience Into the Classroom](trainer-method-field-experience-to-classroom.md)
- [Training content must be technically true and honestly named](training-must-be-technically-true.md)
- [Training is a living document that tracks the product, not a frozen deliverable](training-tracks-the-product-not-frozen.md)
- [Webinar Curriculum: The Onboarding Arc](webinar-curriculum-onboarding-arc.md)
