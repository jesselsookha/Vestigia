# Guide A — Living Examples
## Annotated Records Across Disciplines

---

## How to Read These Examples

The examples in this document are not finished reports or polished documents.

They are **snapshots of work in progress** — the kind of entries a student might write during a project, in real time, without knowing exactly where things will lead. Each one is deliberately imperfect. Real records are imperfect. That is what makes them honest.

Each example contains three layers:

◆ **The Living Record** — what a student might actually write, at the time  
◇ **Individual and Group Perspective** — how the same entry serves both the individual and the team  
◆ **Annotated Commentary** — how the entry maps to the five Guide A categories, to subject deliverables, and to assessment expectations

Read these examples to understand the *practice*, not to copy the *content*. Your project is different. Your discipline may be different. The habit is the same.

!!! note "These are illustrative, not prescriptive"
    The five-category structure (Direction, Decision, Work Performed, Problem, Reflection) appears explicitly in these examples to make the mapping visible. In your own records, you do not need to use these headings. A single flowing entry that covers a decision, a problem, and a reflection is entirely appropriate. The categories are lenses, not mandatory sections.

---

## A Note on Group Projects

Many final-year projects are collaborative. Vestigia is designed for this reality.

Your individual record and your group project are not in conflict. In professional practice, engineers keep personal notebooks. Developers keep personal notes. Teams produce shared deliverables. Both exist simultaneously.

Your individual Vestigia record:

◆ documents your thinking, your decisions, your contribution  
◇ protects your reflection from being vague or generic  
◆ prepares you for individual assessment components, interviews, and showcases

At the same time, a group where members keep good individual records produces better shared outcomes — clearer decisions, less repeated discussion, more grounded progress. The examples below show both perspectives explicitly.

---

## Example 1 — Engineering Project
### Mechanical / Electrical / Systems Design

**Project context:** Design and prototype a low-cost water-level monitoring system for a rural reservoir. The system must operate without submerged components and transmit data remotely.

---

**Living Record — Week 3**

*Date: 12 March*  
*Focus: Sensor selection under environmental constraints*

**Direction and Intention**

Initial goal is to use an ultrasonic sensor for non-contact water-level measurement. This avoids submerged electronics and reduces long-term maintenance risk. It aligns with the safety requirements discussed with the client last week.

**Decision and Trade-off**

Chose ultrasonic sensor over pressure-based and float-mechanism alternatives. Ultrasonic preferred because it requires no contact with water. Known risk accepted: ultrasonic readings are sensitive to surface agitation and mist. Pressure sensor was the second option — more accurate in turbulent conditions, but requires waterproofed submerged housing, which contradicts the brief.

**Work Performed**

Reviewed datasheets for three ultrasonic sensors within the project budget. Calculated expected measurement range for the reservoir dimensions. Conducted bench tests at 0.5m, 1m, and 2m distances in still conditions.

**Problem / Failure**

Readings became unstable when surface agitation was introduced during simulation testing. The sensor returned inconsistent values with variance above acceptable threshold. This was not anticipated in early planning.

**Reflection in Motion**

This exposed an assumption error. I assumed stable surface conditions because the reservoir is described as "calm" — but I never validated this at different times of day or under wind. I need to test under more realistic conditions before committing to this sensor.

If I were restarting the sensor selection process, I would define environmental validation criteria before evaluating technology options.

---

**Individual and Group Perspective**

*As an individual record:*

◆ Demonstrates engineering judgement under constraint  
◆ Documents why this sensor was chosen — not just that it was  
◆ Provides honest evidence of an untested assumption  
◆ Prepares specific material for design justification and risk analysis sections

*Within a group project:*

◇ Prevents revisiting the sensor decision in future meetings  
◇ Explains reasoning to teammates who were not part of this test  
◇ Feeds directly into shared design documentation  
◇ Supports consistent risk register entries

---

**Annotated Commentary**

*Mapping to Guide A categories:* This entry covers all five categories in a single session. Direction establishes the goal and constraint. The decision is documented with alternatives and an accepted trade-off. Work performed is specific and verifiable. The failure is recorded honestly, without hedging. Reflection identifies the assumption error precisely — and proposes a better approach for next time.

*Subject and assessment alignment:* This entry type directly supports design justification sections in project proposals and reports; risk analysis and constraints documentation; supervisor meeting preparation with specific evidence to discuss; WIL evidence of professional engineering reasoning; and individual reflection components grounded in a real experience.

---

## Example 2 — Computer Science / IT Project
### Full-Stack Software Development

**Project context:** Build a full-stack task-management application for a small business client. The system includes a REST API backend, a web-based frontend, and a mobile companion app. The team is working in two-week Agile sprints. The client is involved in sprint reviews.

---

**Living Record — Sprint 2, Week 1**

*Date: 27 March*  
*Focus: Authentication architecture decision*

**Direction and Intention**

We need a secure authentication mechanism that works across both the web frontend and the mobile app. The client's requirement is that users can log in once and access both surfaces. Originally planned to build a custom JWT-based system.

After a stand-up this morning, the team flagged that custom token handling could create security vulnerabilities we are not equipped to audit. This needs a decision before we build further.

**Decision and Trade-off**

Chose to adopt OAuth 2.0 via a third-party authentication provider. Rejected custom JWT implementation — too much risk, insufficient security expertise in the team to audit it properly. OAuth reduces our implementation burden and externalises security responsibility.

Trade-off accepted: less control over the authentication flow; some user experience constraints introduced by the provider's consent screen.

This was my recommendation after reviewing the options overnight. The team agreed in the stand-up.

**Work Performed**

Integrated OAuth provider into the Node.js backend. Implemented token storage and refresh handling in the React Native frontend. Updated the user schema in MongoDB to accommodate OAuth user identifiers. Tested login flow on both web and mobile clients.

**Problem / Failure**

Access tokens expired silently on the mobile client. Users were not prompted to re-authenticate — requests simply failed without explanation. Traced the cause to a misconfigured refresh token handler that was not re-issuing tokens correctly after expiry on mobile.

This caused approximately three hours of debugging and a delay in sprint demo preparation.

**Reflection in Motion**

I assumed the token lifecycle on the backend and the frontend client would synchronise automatically once the OAuth provider was integrated. This was wrong. The mobile client manages token expiry differently from the web client, and I had not accounted for this in my implementation plan.

Next time I integrate an auth provider across multiple clients, I will test token expiry on each surface independently before integration testing.

---

**Individual and Group Perspective**

*As an individual record:*

◆ Documents the recommendation and the reasoning behind it — not just the outcome  
◆ Records a concrete technical failure with a traced cause  
◆ Demonstrates ownership of a decision that affected the whole sprint  
◆ Provides specific material for technical report sections and interview responses about authentication, security trade-offs, and Agile decision-making

*Within the team:*

◇ Explains the OAuth adoption to teammates who were not part of the overnight research  
◇ Documents the refresh token bug so it is not rediscovered later  
◇ Provides a clear account of why the sprint demo was delayed  
◇ Supports accurate sprint retrospective entries

---

**Annotated Commentary**

*Mapping to Guide A categories:* The direction entry captures the client requirement and the emerging concern before the decision is made — establishing context that the decision entry depends on. The decision entry is specific about the alternative, the reasoning, and the accepted trade-off. The work performed entry is individual: "my recommendation," not "we decided." The failure entry traces the bug to its root cause rather than just describing the symptom. The reflection identifies the specific assumption that failed, and proposes a concrete habit change.

*Subject and assessment alignment:* This entry type supports architecture and design justification in technical reports; security and risk documentation; sprint retrospective records; WIL evidence of Agile practice and professional decision-making; and individual reflection components that demonstrate technical growth and self-awareness.

---

## Example 3 — Education Project
### Programme Design and Intervention

**Project context:** Design, pilot, and evaluate a digital literacy intervention for Grade 8 learners at a partner school. The programme involves six weekly sessions delivered by the student team.

---

**Living Record — Week 4 (post-session 2)**

*Date: 14 April*  
*Focus: Unexpected learner response — revising session design*

**Direction and Intention**

The original session plan assumed learners would arrive with some familiarity with basic device navigation. Assessments and informal conversations during session 1 suggested this was not the case for roughly a third of the group.

After discussion with my supervisor on Tuesday, we agreed to revise sessions 3 and 4 to include a foundational device orientation component before moving to the planned content. This changes the scope of what we can cover in six sessions.

**Decision and Trade-off**

Decided to deprioritise the social media critical analysis component (originally planned for session 4) and replace it with extended device orientation in session 3, folding critical analysis into a shorter component in session 5.

The trade-off: less depth on critical analysis than originally planned. The justification: foundational access matters more than advanced content for learners who cannot yet navigate the device confidently.

**Work Performed**

Redesigned the session 3 plan. Prepared differentiated activity sheets for learners at different familiarity levels. Shared the revised plan with my supervisor and with the school coordinator for feedback.

**Problem / Failure**

Session 2 ran significantly over time because I had not accounted for the pace differential between faster and slower learners during a hands-on activity. Several learners finished early and became disruptive; others were still working when time ran out.

I managed this poorly in the moment — I did not have an extension activity ready for early finishers.

**Reflection in Motion**

My lesson plan assumed a more uniform pace than exists in this group. In future sessions, I need to design for pace variation from the start — a core activity, a consolidation activity for on-pace learners, and an extension task for early finishers.

This is something I have read about in teacher education literature but have not had to apply in practice until now. The gap between knowing something theoretically and knowing it in the room is significant.

---

**Individual and Group Perspective**

*As an individual record:*

◆ Documents a significant pedagogical realisation grounded in direct observation  
◆ Records a decision to revise the programme with clear reasoning  
◆ Captures an honest failure in classroom management at the time it happened  
◆ Provides strong material for reflective teaching journals, WIL records, and education portfolio entries

*Within the team delivering the programme:*

◇ Shares the revised session rationale with co-facilitators before session 3  
◇ Alerts the team to the pace differentiation problem so others can prepare extension tasks  
◇ Ensures the programme coordinator understands why the scope changed  
◇ Creates a record that supports programme evaluation at the end of the project

---

**Annotated Commentary**

*Mapping to Guide A categories:* This example shows how a Vestigia record works in a people-centred, practice-based project. Direction captures the revised scope and the reasoning behind it. The decision documents a real trade-off between depth and accessibility. Work performed includes design and stakeholder communication. The failure is recorded with specificity and without evasion. The reflection connects theory to practice explicitly — a marker of genuine educational learning.

*Subject and assessment alignment:* This entry type supports teaching journal and reflective practice assessments; WIL evidence in education and community engagement contexts; programme evaluation and impact documentation; and individual portfolio entries demonstrating adaptive practice and professional growth.

---

## Example 4 — UX / Marketing Project
### Product Strategy and Campaign Design

**Project context:** Develop a go-to-market strategy and campaign for a new consumer subscription product for a small start-up client. The team includes students from UX design, marketing, and business strategy.

---

**Living Record — Week 6**

*Date: 2 May*  
*Focus: User research finding — repositioning required*

**Direction and Intention**

The original value proposition assumed users would pay for the product primarily because of its time-saving features. The marketing strategy and UX flows were both built around this premise.

Following user interviews this week, this assumption needs to be revisited.

**Decision and Trade-off**

Decided to pause the campaign copy development and UX prototype iteration until the value proposition is clarified. This delays deliverables by approximately one week but avoids building further on a premise the research suggests is incorrect.

The trade-off: timeline pressure. The justification: continuing without addressing this would produce campaign materials and a UX that are misaligned with what users actually value.

This decision was mine to make as the research lead. I discussed it with the client before implementing it.

**Work Performed**

Conducted six user interviews using the semi-structured protocol developed in week 4. Synthesised findings into an affinity map. Identified the dominant theme: users found the product useful but did not perceive sufficient value to justify the price point.

Presented findings to the team and client in a working session on Friday.

**Problem / Failure**

Four of the six interviewees said something close to: the product is useful, but it is not something I would pay for. This is not a usability problem. It is a value perception problem.

The original brief assumed the problem was awareness — that users would pay if they understood the product better. The research suggests the problem is positioning — that users understand the product but do not believe it is worth the price.

**Reflection in Motion**

This shifted my thinking significantly. Marketing strategy and UX design cannot be developed independently — they need to work from the same premise about what value this product actually delivers to this user.

I had been treating the research phase as a validation exercise — expecting it to confirm the original strategy. It has instead challenged it. I need to approach the next phase with more openness to what the research is actually saying, rather than looking for confirmation of what I expected to find.

---

**Individual and Group Perspective**

*As an individual record:*

◆ Documents the strategic shift and the research finding that triggered it  
◆ Records specific user research output — not vague impressions, but a consistent theme across four of six interviews  
◆ Demonstrates user-centred thinking and honest response to disconfirming evidence  
◆ Provides strong material for UX case studies, marketing portfolio entries, and interviews about research-led decision-making

*Within the design and marketing team:*

◇ Aligns the team on the revised value proposition before further work diverges  
◇ Explains why deliverables have been paused — with evidence, not just a decision  
◇ Prevents UX and marketing from continuing to develop misaligned outputs  
◇ Supports coherent client communication and transparent project management

---

**Annotated Commentary**

*Mapping to Guide A categories:* This example shows a Vestigia record at a pivotal project moment — where research disconfirms strategy and a decision must be made about what to do with that. Direction captures the original premise and the emerging challenge. The decision is specific about what is being paused and why. Work performed documents the research activity with enough specificity to be credible. The failure entry is honest about what the research actually found — without softening it. The reflection captures a genuine methodological shift in the student's approach to research.

*Subject and assessment alignment:* This entry type supports research methodology sections demonstrating user-centred practice; marketing strategy justification and iteration records; UX documentation showing persona and insight development; WIL evidence of professional client communication and adaptive strategy; and individual portfolio entries demonstrating strategic thinking and research integrity.

---

## What These Examples Demonstrate

Across all four disciplines and project types, Vestigia records do the same work:

◆ they make thinking visible — not just outcomes  
◇ they document decisions at the moment they are made  
◆ they capture the honest version of what happened  
◇ they connect individual effort to collective deliverables  
◆ they prepare you for the questions you will face in reports, presentations, and interviews

The tools differ. The client types differ. The problems differ. The recording habit is the same.

!!! tip "These are starting points"
    These examples are here to make the practice concrete, not to provide a structure to replicate. Your project has its own story. The most valuable Vestigia record you will ever write is the one you write for yourself, about your own work, at the moment it happens.

---

*Guide A is complete. When your project is done and you are ready to present your work professionally, continue to **[Guide B](../guide-b/index.md)**.*