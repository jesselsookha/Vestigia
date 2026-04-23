# Guide A — Living Examples
## Annotated Records Across Disciplines

---

## Ⅰ — How to Read These Examples

The examples below are not finished reports or polished documents.

They are **snapshots of work in progress** — the kind of entries a student might
write during a project, in real time, without knowing exactly where things will lead.

Each example contains three layers:

◆ **The Living Record** — what a student might actually write  
◇ **Individual and Group Perspective** — how the same entry supports both  
◆ **Annotated Commentary** — how this maps to Guide A sections, subject deliverables,
and assessment expectations

Read these examples to understand the *practice*, not to copy the *content*.

Your project is different. Your discipline may be different. The habit is the same.

---

## Ⅱ — A Note on Group Projects

Many final-year projects are collaborative. Vestigia is designed for this reality.

Your individual record and your group project are not in conflict.

In professional practice, engineers keep personal notebooks. Developers keep
personal notes. Teams produce shared deliverables. Both exist simultaneously.

Your individual Vestigia record:

◆ documents your thinking, your decisions, your contribution  
◇ protects your reflection from being vague or generic  
◆ prepares you for individual assessment components, interviews, and showcases

At the same time, a group where members keep good individual records produces
better shared outcomes — clearer decisions, less repeated discussion, more
grounded progress.

The examples below show both perspectives explicitly.

---

## Ⅲ — Example Ⅰ: Engineering Project
### Mechanical / Electrical / Systems Design

**Project Context**

Design and prototype a low-cost water-level monitoring system for a rural reservoir.
The system must operate without submerged components and transmit data remotely.

---

### Living Record — Week 3

**Date:** 12 March  
**Focus:** Sensor selection under environmental constraints

---

**Direction and Intention**

Initial goal is to use an ultrasonic sensor for non-contact water-level measurement.
This avoids submerged electronics and reduces long-term maintenance risk. It aligns
with the safety requirements discussed with the client last week.

---

**Decision and Trade-off**

- Chose ultrasonic sensor over pressure-based and float-mechanism alternatives  
- Ultrasonic preferred because it requires no contact with water  
- Known risk accepted: ultrasonic readings are sensitive to surface agitation and mist  
- Pressure sensor was the second option — more accurate in turbulent conditions,
  but requires waterproofed submerged housing

---

**Work Performed**

- Reviewed datasheets for three ultrasonic sensors within the project budget  
- Calculated expected measurement range for the reservoir dimensions  
- Conducted bench tests at 0.5m, 1m, and 2m distances in still conditions

---

**Problem / Failure**

Readings became unstable when surface agitation was introduced during simulation testing.
The sensor returned inconsistent values with variance above acceptable threshold.
This was not anticipated in early planning.

---

**Reflection in Motion**

This exposed an assumption error. I assumed stable surface conditions because
the reservoir is described as "calm" — but I never validated this at different
times of day or under wind. I need to test under more realistic conditions
before committing to this sensor.

If I were restarting the sensor selection process, I would define environmental
validation criteria before evaluating technology options.

---

### Individual and Group Perspective

**As an individual record:**

◆ Demonstrates engineering judgement under constraint  
◆ Documents why this sensor was chosen — not just that it was  
◆ Provides honest evidence of an untested assumption  
◆ Prepares specific material for design justification and risk analysis sections

**Within a group project:**

◇ Prevents revisiting the sensor decision in future meetings  
◇ Explains reasoning to teammates who were not part of this test  
◇ Feeds directly into shared design documentation  
◇ Supports consistent risk register entries

---

### Annotated Commentary

**Mapping to Guide A Sections**

- Direction and Intention → Section Ⅲ.Ⅰ  
- Decision and Trade-off → Section Ⅲ.Ⅱ  
- Work Performed → Section Ⅲ.Ⅲ  
- Problem / Failure → Section Ⅲ.Ⅳ  
- Reflection in Motion → Section Ⅲ.Ⅴ

**Subject and Assessment Alignment**

This entry type directly supports:

◆ design justification sections in project proposals and reports  
◇ risk analysis and constraints documentation  
◆ supervisor meeting preparation — specific evidence to discuss  
◇ WIL evidence of professional engineering reasoning  
◆ individual reflection components — a real experience, not a reconstructed one

---

## Ⅳ — Example Ⅱ: Computer Science / IT Project
### Full-Stack Software Development

**Project Context**

Build a full-stack task-management application for a small business client.
The system includes a REST API backend, a web-based frontend, and a mobile companion app.

The team is working in two-week Agile sprints. The client is involved in sprint reviews.

---

### Living Record — Sprint 2, Week 1

**Date:** 27 March  
**Focus:** Authentication architecture decision

---

**Direction and Intention**

We need a secure authentication mechanism that works across both the web frontend
and the mobile app. The client's requirement is that users can log in once
and access both surfaces. Originally planned to build a custom JWT-based system.

After a stand-up this morning, the team flagged that custom token handling could
create security vulnerabilities we are not equipped to audit. This needs a decision.

---

**Decision and Trade-off**

- Chose to adopt OAuth 2.0 via a third-party authentication provider  
- Rejected custom JWT implementation — too much risk, insufficient security expertise  
- OAuth reduces our implementation burden and externalises security responsibility  
- Trade-off accepted: less control over the authentication flow; some user experience
  constraints introduced by the provider's consent screen

This was my recommendation after reviewing the options. The team agreed.

---

**Work Performed**

- Integrated OAuth provider into the Node.js backend  
- Implemented token storage and refresh handling in the React Native frontend  
- Updated the user schema in MongoDB to accommodate OAuth user identifiers  
- Tested login flow on both web and mobile clients

---

**Problem / Failure**

Access tokens expired silently on the mobile client. Users were not prompted
to re-authenticate — requests simply failed without explanation. Traced the
cause to a misconfigured refresh token handler that was not re-issuing tokens
correctly after expiry on mobile.

This caused approximately three hours of debugging and a delay in the sprint demo preparation.

---

**Reflection in Motion**

I assumed the token lifecycle on the backend and the frontend client would
synchronise automatically once the OAuth provider was integrated. This was wrong.

The mobile client manages token expiry differently from the web client, and
I had not accounted for this. I now understand that OAuth integration is not
"set and forget" — each client surface requires explicit lifecycle management.

I have noted this as a future architecture decision point: document client-specific
auth behaviour at the integration stage, not when problems surface.

---

### Individual and Group Perspective

**As an individual record:**

◆ Documents the architectural decision and the reasoning behind it  
◆ Records the specific problem encountered and how it was diagnosed  
◆ Demonstrates technical problem-solving and honest acknowledgement of a knowledge gap  
◆ Provides material for individual reflection marks and technical interview questions

**Within a group project:**

◇ Explains why OAuth was chosen — prevents the decision being re-examined later  
◇ Gives context to teammates who work on the auth flow in future sprints  
◇ Supports the team's sprint retrospective documentation  
◇ Acts as an onboarding reference if a new team member joins mid-project

---

### Annotated Commentary

**Mapping to Guide A Sections**

- Direction and Intention → Section Ⅲ.Ⅰ  
- Decision and Trade-off → Section Ⅲ.Ⅱ  
- Work Performed → Section Ⅲ.Ⅲ  
- Problem / Failure → Section Ⅲ.Ⅳ  
- Reflection in Motion → Section Ⅲ.Ⅴ

**Subject and Assessment Alignment**

This entry type directly supports:

◆ system design and architecture sections of the technical report  
◇ Agile sprint retrospective documentation  
◆ testing and evaluation write-ups — specific failure with specific resolution  
◇ WIL evidence of real-world development practice and client-facing delivery  
◆ individual reflection components — a specific learning moment, not a general statement  
◇ portfolio and showcase material — this is the kind of decision story employers ask about

---

## Ⅴ — Example Ⅲ: Education Project
### Intervention Design and Evaluation

**Project Context**

Design and implement a structured literacy intervention programme for Grade 4 learners
in a partner school. Evaluate its impact on reading comprehension over six weeks.

This is an individual project conducted as part of a Work-Integrated Learning module.

---

### Living Record — Intervention Design Phase

**Date:** 18 April  
**Focus:** Choosing a teaching strategy

---

**Direction and Intention**

The project goal is to improve reading comprehension scores by a measurable amount
over six sessions. Initial plan was to use structured worksheet-based activities —
predictable, easy to standardise, familiar to learners.

However, my supervisor raised a concern during our check-in today: worksheet-heavy
approaches often limit engagement in learners who already struggle with reading.
I need to reconsider my strategy before the pilot session next week.

---

**Decision and Trade-off**

- Shifted from worksheet-based exercises to collaborative group-reading sessions  
- Group reading allows for peer modelling — stronger readers support weaker ones  
- Trade-off: harder to control pacing; individual assessment becomes more complex  
- Worksheets are still used, but as a consolidation activity after group work, not as
  the primary mode

---

**Work Performed**

- Observed two literacy lessons at the partner school to understand classroom dynamics  
- Reviewed three recent papers on collaborative reading strategies  
- Developed structured session plan for the first intervention — including role
  allocations for group reading activities  
- Submitted revised intervention plan to supervisor for sign-off

---

**Problem / Challenge**

During the pilot session, a small number of learners dominated group discussions.
Quieter learners were not contributing meaningfully, which contradicted the
engagement objective.

---

**Reflection in Motion**

I assumed that placing learners in groups would distribute participation naturally.
It did not.

This revealed that structured collaboration requires explicit role design —
it is not enough to group people and expect equity. I will introduce role rotation
in the next session: each learner takes a different role (reader, summariser,
questioner) to ensure distributed participation.

This also changes how I define "engagement" in my evaluation framework.
Participation frequency is now an additional metric alongside comprehension scores.

---

### Individual and Group Perspective

**As an individual record:**

◆ Documents pedagogical reasoning — not just what was done, but why  
◆ Captures a specific classroom observation and its direct consequence  
◆ Demonstrates ethical awareness — equity of participation matters  
◆ Provides specific, honest material for reflective practice assessments

**For collaborative research projects:**

◇ Aligns team members on the rationale for intervention design choices  
◇ Documents classroom adaptations so evaluation consistency is maintained  
◇ Provides shared reference for ethical reflection requirements

---

### Annotated Commentary

**Mapping to Guide A Sections**

- Direction and Intention → Section Ⅲ.Ⅰ  
- Decision and Trade-off → Section Ⅲ.Ⅱ  
- Work Performed → Section Ⅲ.Ⅲ  
- Problem / Challenge → Section Ⅲ.Ⅳ  
- Reflection in Motion → Section Ⅲ.Ⅴ

**Subject and Assessment Alignment**

This entry type directly supports:

◆ methodology and intervention design sections of the project report  
◇ reflective journal requirements — specific, grounded, not generic  
◆ WIL or practicum documentation — evidence of professional and ethical reasoning  
◇ evaluation framework development — the reflection directly revises the metrics  
◆ supervisor meeting preparation — concrete observations and decisions to discuss

---

## Ⅵ — Example Ⅳ: IT-Adjacent Project
### UX Design and Marketing Strategy

**Project Context**

Develop a user-centred marketing strategy and interactive UI prototype for a mobile
fitness application. The project is part of an IT degree with a UX and digital
marketing specialisation.

The team includes a UX designer, a front-end developer, and a marketing strategist.
This record belongs to the marketing strategist.

---

### Living Record — Research and Ideation Phase

**Date:** 6 May  
**Focus:** Understanding why users do not convert from free trial to paid subscription

---

**Direction and Intention**

The primary project goal is to increase onboarding conversion — moving users from the
free trial to a paid subscription. My initial assumption was that poor usability was
the main barrier. If the app was easier to use, more people would stay.

After analysing three competitor apps this week, that assumption feels incomplete.

---

**Decision and Trade-off**

- Shifted focus from usability improvements to motivational UX patterns  
- Specifically: gamification elements and visible progress feedback  
- The insight was that usability is table stakes — users expect it; it does not
  motivate them to pay  
- Trade-off: motivational UX is harder to evaluate quantitatively in the timeframe;
  impact on conversion cannot be directly proven within the project scope

---

**Work Performed**

- Conducted six user interviews with current free-trial users  
- Developed three distinct user personas from interview findings  
- Sketched wireframes for a revised onboarding sequence  
- Mapped the customer journey from first open to subscription prompt

---

**Problem / Failure**

Early prototype testers understood the features clearly but lacked motivation to
engage with the subscription prompt. They described the app as "useful but not
something I'd pay for." This response was consistent across four of the six testers.

---

**Reflection in Motion**

This shifted my thinking significantly. The problem is not that users do not
understand the product. The problem is that they do not perceive enough value
to justify paying for it.

This is a messaging and positioning challenge as much as a design challenge.
Marketing strategy and UX cannot be designed independently — they need to work
from the same premise about what value this product actually delivers.

I need to revisit the value proposition before we finalise either the campaign
messaging or the UI prototype.

---

### Individual and Group Perspective

**As an individual record:**

◆ Documents the strategic shift and the insight that triggered it  
◆ Records the specific user research finding — "useful but not something I'd pay for"  
◆ Demonstrates user-centred thinking and honest response to research findings  
◆ Provides strong material for portfolio write-ups and UX/marketing interviews

**Within the design and marketing team:**

◇ Aligns the team on the revised value proposition before further work  
◇ Explains why certain personas were prioritised  
◇ Prevents UX and marketing from diverging on the core message  
◇ Supports coherent branding and campaign consistency across team deliverables

---

### Annotated Commentary

**Mapping to Guide A Sections**

- Direction and Intention → Section Ⅲ.Ⅰ  
- Decision and Trade-off → Section Ⅲ.Ⅱ  
- Work Performed → Section Ⅲ.Ⅲ  
- Problem / Failure → Section Ⅲ.Ⅳ  
- Reflection in Motion → Section Ⅲ.Ⅴ

**Subject and Assessment Alignment**

This entry type directly supports:

◆ research methodology sections — user interviews as a design input  
◇ marketing strategy justification — why this approach, not another  
◆ UX documentation — persona development grounded in real findings  
◇ WIL evidence of professional practice — client-facing research and iteration  
◆ individual portfolio and showcase — a clear story of strategic thinking  
◇ reflective assessment components — a genuine shift in understanding, not a summary

---

## Ⅶ — What These Examples Demonstrate

Across all four disciplines and project types, Vestigia records do the same work:

◆ they make thinking visible — not just outcomes  
◇ they document decisions at the moment they are made  
◆ they capture the honest version of what happened  
◇ they connect individual effort to collective deliverables  
◆ they prepare you for the questions you will face in reports, presentations, and interviews

The tools differ. The client types differ. The problems differ.

The recording habit is the same.

---

*These examples are starting points for understanding the practice.  
They are not templates. Do not copy the structure and fill in your details.  
Your project has its own story. Record it.*
