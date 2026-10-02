# Buildora — Product Requirements Document

**Status:** Draft  
**Product:** Buildora  
**Version:** 1.2  
**Source:** Product direction inferred from the supplied reference screens and a role-flow benchmark of Unstop, reviewed October 2026

## 1. Product summary

Buildora is a career and innovation platform for students, early-career talent, mentors, employers, universities, and challenge organizers. It brings together skill-building, portfolio evidence, internships and jobs, hackathons, mentorship, and partner programs in one account.

The product promise is: **learn useful skills, build visible proof of work, and turn it into real opportunities.**

Buildora will launch for three learner segments at the same time: college students, recent graduates, and career switchers. The platform will collect segment, education/experience level, target role, and career goal during onboarding so that discovery, learning plans, and guidance are relevant without splitting the product into separate marketplaces.

The reference screens show a broad destination. This PRD separates the public acquisition experience from the authenticated learner product and the organizer/employer workflows required to make the marketplace work.

## 2. Problem and opportunity

Early-career talent often has learning content, event listings, job boards, and portfolios spread across disconnected products. That makes it difficult to find credible opportunities, demonstrate capability, receive guidance, and track progress.

Employers, universities, and sponsors need a dependable way to reach relevant emerging talent, run challenges, assess candidates, and measure outcomes. They currently assemble this through separate event, recruiting, and community tools.

Buildora creates a single, evidence-based path from learning to participation to hiring. Its signature partner program connects learners to NGO-defined, real-world problems: learners compete or build solutions, then can apply for related NGO internships that add verified impact experience to their profiles.

## 3. Goals

1. Help learners discover and successfully participate in relevant hackathons, internships, jobs, courses, and mentoring.
2. Help learners build a trustworthy skills and project profile that improves applications and recruiter discovery.
3. Give organizers and NGOs the tools to publish, operate, and measure credible challenges that lead to talent and impact outcomes.
4. Give employers a streamlined way to publish roles, review applicants, and hire emerging talent.
5. Establish recurring revenue through participant and organizer subscriptions, while supporting partnerships and sponsorships.



## 4. Non-goals for the initial release

- Replacing a full university learning-management system.
- Building a general social network or chat application.
- Supporting payroll, employment contracts, or direct stipend disbursement.
- Building a general-purpose video-conferencing service.
- Operating an unrestricted course marketplace with third-party payouts.



## 5. Users and jobs to be done


| User                           | Primary need                                                                   | Key outcomes                                                                                       |
| ------------------------------ | ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| Learner / participant          | Find credible ways to learn, build, and advance                                | Register for events, apply for roles, complete learning, show projects, get mentored               |
| Job seeker                     | Convert skills and project work into interviews                                | Create profile, discover roles, apply, track status, practice interviews                           |
| Hackathon organizer            | Run an engaging, measurable event                                              | Create event, manage registrations, teams, submissions, judges, results                            |
| Employer / recruiter           | Hire relevant early-career talent efficiently                                  | Post role, review qualified profiles, shortlist, interview, hire                                   |
| University / ecosystem partner | Create pathways and engage a student community                                 | Co-brand programs, refer students, view aggregate outcomes                                         |
| NGO partner                    | Turn a real community need into a responsible challenge and internship pathway | Publish vetted problem statements, evaluate solutions, offer eligible internships, document impact |
| Mentor / judge                 | Support and evaluate participants                                              | Publish availability, schedule sessions, score projects, provide feedback                          |
| Platform administrator         | Maintain quality and trust                                                     | Moderate listings and content, manage users, resolve reports, view platform health                 |




## 6. Product scope and requirements



### 6.1 Identity, onboarding, and profile

Users can sign up with email/password or Google, GitHub, and LinkedIn. The system must verify email addresses and provide password reset and persistent login options.

On first sign-in, Buildora must collect role, location, education or experience level, interests, skill tags, career goals, and availability. Users may select more than one role, with one active workspace at a time.

The onboarding flow must include paths for college students, recent graduates, and career switchers. It must ask for the learner’s current situation, desired role/industry, prior education or work experience, and transition timeline. Recommendations must use these signals, but no eligible learner may be excluded from an opportunity solely because of segment; eligibility remains controlled by each opportunity’s published rules.

Each learner profile must support:

- Name, avatar, location, education, bio, and public visibility choice.
- Skills with level, evidence, and verification state.
- Projects with description, links, media, team members, technologies, and related hackathon.
- Resume upload/export, certificates, application history, saved opportunities, and activity timeline.
- Privacy controls for recruiter discovery and profile sharing.



### 6.2 Opportunity discovery and applications

Buildora must provide searchable, filterable directories for hackathons, internships, and jobs. Results must support keyword search, category or domain, skills, location/remote status, duration, team format, stipend or compensation range, eligibility, registration state, and date.

Each opportunity detail page must show an overview, organizer/employer, requirements, skills, schedule, benefits, FAQs, and a clear primary action.

For internships and jobs, users must be able to apply using their Buildora profile and resume, answer employer-defined questions, save a draft, withdraw where allowed, and receive application-status updates. Employers must be able to configure eligibility questions, review submissions, and move candidates through configurable stages.

**Launch sourcing model:** employers and organizers create and manage opportunities directly in Buildora. All applications and registrations occur natively in Buildora; there will be no syndicated job feed or external apply redirect at launch. ATS import/export and inbound syndication may be considered after the direct marketplace has sufficient supply and moderation capacity.

### 6.3 Hackathons and challenges

Organizers must be able to create an event with title, brand assets, problem statements, eligibility, format, dates, prize details, judging rubric, mentors, judges, registration cap, team rules, and communications.

Participants must be able to register, form or join a team, choose a problem statement, access resources, submit a project before deadline, and view results. A submission must include project name, description, repository or demo links, presentation assets, team members, and optional media.

**Launch format decision:** Buildora must support online, in-person, and hybrid events, with individual and team participation. An event may define a location/venue, capacity, attendance/check-in process, team-size range, team formation deadline, remote collaboration guidance, and per-round participation mode. Hybrid events must allow an organizer to distinguish remote and onsite attendance while maintaining one participant and scoring record.

Judges must receive assigned submissions, score each rubric criterion, leave feedback, and submit a final score. The organizer must be able to finalize rankings, publish winners, and export event data.

**First organizer release: competition and assessment scope.** The core modes are hackathons and NGO innovation challenges, case/project competitions, timed quizzes, and technical screening assessments. A competition may use registration, one or more timed assessments, a project/case submission, and a live presentation or interview round. Workshops, webinars, conferences, cultural events, festivals, and scholarships use the same registration and communications foundation but do not require bespoke competition logic in the first release.

The initial assessment set must include:

- Timed multiple-choice and multiple-select questions, including aptitude, domain knowledge, and situational-judgment questions.
- Timed coding problems with language selection, test cases, automatic scoring, and a manual review queue for edge cases.
- Case, design, and project submissions evaluated with a published rubric; accepted formats include text, file, URL, repository, demo, and presentation.
- Live presentation, interview, and jury rounds with scheduling, structured scorecards, and manual shortlist decisions.

Baseline integrity controls are required from launch: verified email and phone; declared eligibility; server-authoritative timers; one active attempt per configured attempt; randomized question and option order where suitable; question-pool variants; submission timestamps and receipts; duplicate-attempt prevention; audit logs for participant and organizer actions; and manual review/disqualification with a stated reason. Coding and project submissions must support plagiarism/similarity signals, repository-history review, and judge escalation. Buildora must record device, IP, tab-focus, and connection events only when disclosed in the event terms and privacy notice, and must treat them as review signals rather than automatic guilt. Webcam/ID proctoring, browser lockdown, and AI behavioral proctoring are deferred until a privacy, accessibility, and false-positive review is complete; high-stakes assessments can use a live follow-up verification round in the meantime.

### 6.4 Skills, resources, and learning paths

The Skills area provides structured course tracks, individual courses, practical lessons, and completion certificates. Course catalog filtering must support category, difficulty, duration, and skill.

**Launch content decision:** courses, assessments, projects, and completion certificates are proprietary Buildora offerings. Buildora owns the learner experience, instructional quality standard, completion criteria, and credential record. Partner experts may author or co-brand content under contract, but external course links and third-party certificate catalogs are not part of the initial course product.

The Resources hub provides guides, tutorials, videos, templates, and tools. Content must be categorized, searchable, and labeled by format, skill area, difficulty, and estimated effort.

Learning paths must define ordered steps and show learner progress. The initial set should include First-Time Hacker, Product Builder, and AI Innovator pathways. Completion can add profile evidence and unlock a certificate or badge when the relevant requirements are met.

### 6.5 Career preparation and mentorship

Career tools must include role-based mock tests, interview-practice questions, portfolio prompts, and a resume checklist. Results should provide a score, recommended topics, and a link to relevant learning resources.

Mentorship must let learners browse mentors by expertise, language, availability, and price/free status; request sessions; schedule approved sessions; and leave feedback. Mentors need profiles, availability, session formats, and request management.

### 6.6 Employer hiring workspace

Employers must be able to create an organization profile, invite team members, post and edit jobs or internships, and manage applications in a pipeline.

An employer or organizer may publish only after Buildora verifies the organization and the publishing representative. Required evidence includes: legal organization name, jurisdiction, registration identifier applicable to that jurisdiction (for example, CIN/LLPIN/GSTIN in India where applicable), registered business address, public website, company-domain email verification, authorized representative’s identity/contact details, and confirmation that they are authorized to publish for the organization. Buildora must validate the legal record against an authoritative registry or a manual-review process, verify domain ownership, screen against its trust-and-safety policy, and retain the evidence and reviewer decision. Any material legal-entity or domain change must trigger re-verification.

The application pipeline must support list and detail views, filters, private notes, owner assignment, status changes, interview scheduling links, candidate messaging templates, and CSV export. Employers may search talent profiles only when users have opted in to discovery.

### 6.7 Partnerships

The public partnership flow must explain corporate challenges, university collaborations, sponsorships, and community/mentorship programs. Prospects must be able to submit a partnership inquiry with contact details, organization, partnership type, subject, and message.

An internal partner workflow must capture inquiry status, owner, notes, next action, and conversion outcome. This can initially live in an integrated CRM or a simple admin queue.

### 6.7.1 NGO impact challenge and internship program

NGO partnerships are a launch differentiator. A verified NGO must be able to propose a community problem, publish it as a challenge or hackathon with Buildora support, review learner solutions, and create related internships on the same organization profile. The learner journey must make the connection explicit: **problem statement → challenge participation/project evidence → internship application → verified impact experience**.

Each NGO problem statement requires an impact brief: community context, intended beneficiaries, success measures, constraints, available data/resources, responsible-use rules, intellectual-property terms, judging criteria, and the type of follow-on internship or implementation opportunity, if any. Buildora and the NGO must review problem statements for safety, feasibility, privacy, harmful data collection, and claims that could exploit unpaid participant work. Any internship must state whether it is paid, stipend-supported, or unpaid; duration, supervision, work location, expected hours, learning outcomes, and applicable legal eligibility must be visible before application.

NGO organizations follow the same legal-entity and authorized-representative verification as other publishers, with charity/nonprofit registration evidence where applicable. An NGO internship becomes a verified impact experience after an authorized NGO representative confirms the learner's role, dates, and completed scope. The public profile shows only the learner-approved summary and impact evidence; beneficiaries' personal data, sensitive case material, and private NGO information remain restricted.

### 6.8 Dashboard and engagement

The authenticated dashboard must be personalized and show:

- Recommended opportunities and learning content based on profile and activity.
- Upcoming deadlines, sessions, applications, registrations, and submissions.
- Progress toward active learning paths and skill goals.
- Application, event, and course status at a glance.
- Calls to complete profile, join a campaign, upgrade a plan, or refer a friend.

Users must receive in-product and email notifications for application changes, registration confirmations, upcoming deadlines, mentor activity, feedback, and new matched opportunities. Notification preferences must be configurable.

### 6.9 Plans and entitlements

Buildora supports participant and organizer plans. The participant subscription should launch only after the proprietary learning catalog, preparation tools, and job-match signals are reliable enough to provide recurring value.


| Plan family                                                 | Indicative entitlement                                                                                                                                                                                                                                                                                                                                  |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Participant Free                                            | Full profile, opportunity discovery, saved opportunities, normal applications/registrations, selected resources, and basic practice. No applicant-ranking or application-access advantage is sold.                                                                                                                                                      |
| Buildora Pro (recommended initial participant subscription) | Unlimited proprietary courses, projects, learning paths, and Buildora certificates; advanced role/skill-gap and application-match insights; premium practice and AI resume/profile/application feedback subject to fair-use limits; advanced search; templates; exclusive group career sessions; and a limited monthly mock-interview or mentor credit. |
| Career Coaching add-on                                      | Paid human mentorship or additional mock interviews sold as a separate credit/package, with transparent cancellation and refund terms. This avoids making high variable-cost coaching an unlimited subscription promise.                                                                                                                                |
| Organizer Pro                                               | Hackathon creation, event pages, participant data, standard reporting                                                                                                                                                                                                                                                                                   |
| Organizer Premium                                           | Advanced analytics, participant matching, dedicated support, integrations, promoted reach                                                                                                                                                                                                                                                               |


Buildora Pro must be offered monthly and annually, with a time-limited trial or introductory offer only where legally permitted. Pricing, tax, billing cadence, cancellations, invoices, and entitlement enforcement must be handled by a payment provider. The exact plan prices shown in the references are marketing placeholders until commercial approval.

Paid membership may improve a learner’s preparation and decision-making, but must never guarantee an interview, placement, event selection, employer response, or a higher ranking in an employer’s hiring workflow. Any employer-visible signal, such as a “strong match,” must be derived from published role requirements and transparent candidate evidence rather than payment status.

### 6.10 Public site, content, and trust

The public site must provide conversion pages for Hackathons, Internships, Skills, Careers, Growth/Plans, Resources, News, and Partnerships. It must include clear CTAs, responsive layouts, accessible navigation, legal pages, and contact/support routes.

The News section must support searchable, categorized posts, pagination, newsletter subscription, and an editorial workflow with draft, review, publish, and archive states.

Administrators must be able to moderate user-generated content, approve organizations and listings, suspend accounts, manage taxonomy, and handle abuse reports. Audit logs are required for administrator actions and sensitive workflow changes.

### 6.10.1 Credential and outcome verification

Buildora must distinguish a learner’s **self-declared** skills from evidence-backed **verified** skills. A skill becomes verified only when it is linked to one or more accepted evidence sources:

- A Buildora assessment passed at the assessment’s published proficiency threshold.
- A proprietary Buildora course/project completed with required graded work.
- An approved external credential whose issuer, credential ID, and validity can be checked.
- A reviewed project demonstrating the skill, with ownership and work evidence.

Project verification requires: creator attestation; a repository, live demo, or securely shared artifact; an intelligible project description; technologies/skills claimed; and evidence of the learner’s contribution. For team projects, each contributor’s role must be stated. Buildora should use automated plagiarism/similarity checks where feasible and send flagged or high-impact projects to review. A hackathon project may earn verified status after a valid submission and organizer/judge confirmation, but participation alone does not verify every skill tag.

Each Buildora certificate must be created only after its published completion rules are met. It must include a unique credential ID, learner name, course/path and version, issue date, issuer, and a public verification page that can confirm current validity without exposing unnecessary learner data. Revoked, expired, or superseded credentials must retain a visible status.

A placement outcome has three states: **candidate-reported**, **offer accepted**, and **started/verified placement**. Buildora may mark an offer as accepted when the employer’s authorized user records it or the candidate provides acceptable evidence. It may mark a placement as started/verified only after employer confirmation from the verified organization or appropriately minimized evidence of start date. Documents containing compensation, government IDs, or other sensitive data must not be publicly displayed; access must be limited, encrypted, retained only as long as necessary, and logged.

### 6.11 College and community workspace

Buildora must treat colleges and student communities as distribution partners as well as opportunity providers. At launch, verified college staff receive a dedicated college workspace with a verified institution profile, staff roles, student-community pages, event publishing, and aggregate participation and outcomes reporting.

Authorized placement staff must be able to publish campus-restricted opportunities, set student eligibility rules, nominate or import an eligible cohort, track applications and selections, and export outcome reports. Student clubs and festival committees must be able to use an organization workspace with constrained permissions to run events.

### 6.12 Configurable competition engine

Hackathons are one competition format. The platform must also support case competitions, quizzes, assessments, workshops, webinars, conferences, cultural events, college festivals, scholarships, and campaign challenges without a separate build for each.

An organizer must define an ordered sequence of rounds. Each round has an opening/closing window, eligibility or advancement rule, instructions, contact owner, attachments, and one or more execution modes:

- Registration form or profile-based eligibility check.
- Timed quiz or assessment with question bank, randomization, attempt policy, proctoring/integrity settings, and result thresholds.
- File, URL, repository, video, presentation, or free-text submission.
- External event/assessment link with attendance or completion import.
- Live interview, presentation, or jury evaluation with scheduling and scorecards.
- Manual shortlist, leaderboard, waitlist, or disqualification decision.

The system must preserve a timestamped participant history across every round, send deadline and advancement notifications, prevent late or duplicate submissions according to configured rules, allow organizer overrides with an audit trail, and publish only the results authorized by the organizer. Participants need a single event page that makes their current round, required action, schedule, and status unambiguous.

### 6.13 Assessments and interview operations

Buildora must provide an assessment service usable both as standalone preparation and as a selection round. It needs question banks organized by role, skill, difficulty, and organization; timed tests; coding or case-based prompts where applicable; invitations; candidate identity checks; attempt rules; auto-scoring where feasible; manual evaluation queues; score reports; and candidate feedback controls.

For mock and employer interviews, Buildora must support interview templates, availability collection, calendar/video links, interviewer assignment, structured scorecards, private notes, recommendation outcomes, and candidate feedback. Employer workflows must allow assessment and interview results to feed the application pipeline without manual re-entry.

### 6.14 Organization and brand workspace

Every verified employer, university, organizer, and partner must have a public organization page with its description, logo, verified status, open opportunities, past programs, relevant resources, and contact or follow actions. The page may show participant reviews and interview experiences only after moderation and where the contributor has consented.

Organization administrators must have tiered roles: owner, billing administrator, hiring manager, event manager, evaluator, content editor, analyst, and read-only viewer. Permissions must be scoped to the organization and, where relevant, an individual opportunity.

The organization workspace must allow teams to build an audience before recruiting: publish branded challenges, content, events, talent communities, and opt-in campaigns; collect consented leads; and measure reach, registrations, engagement, qualified applications, interview conversion, and hires. This provides a coherent Buildora equivalent of a source → screen → assess → interview → hire workflow.

### 6.15 Mentor marketplace operations

Mentor onboarding must include an application, professional experience and expertise, public bio, social/professional links, services, session format and duration, price, availability, payout details, and acceptance of mentor standards. Profiles remain private until approved by Buildora.

Mentors need a dashboard for bookings, schedule overrides, session history, payouts, ratings, learner feedback, and the ability to pause availability. Learners must see total price, taxes, cancellation terms, and refund terms before booking. Buildora processes payments through its payment provider and must collect required payout/KYC and tax information before a mentor can receive money. It must authorize or collect the learner payment at booking, release the mentor payout after recorded completion or expiry of the dispute window, and support platform-managed refunds, partial refunds, no-show handling, receipts, and payout reconciliation. Buildora must define a transparent marketplace fee, payout schedule, dispute process, and local regulatory/tax operating model before paid sessions open.

### 6.16 Community advocacy and retention

The ambassador program is not a launch growth channel. Buildora may run small, voluntary campus cohorts after the core marketplace is operating, with applications, onboarding, campaign materials, task proof, and staff approval. Recognition may include a public badge, verified volunteer certificate, recommendation letter where earned, learning access, or event access. It must not promise cash, commission, cash-equivalent rewards, employment, or placement benefits.

Referral links may be used for attribution and community measurement, but they do not create a paid reward ledger at launch. Buildora must show voluntary ambassadors what data is tracked, require truthful promotion, and give administrators moderation and removal controls.

## 7. Core user journeys



### Learner: discover to opportunity

1. Signs up and completes profile and interests.
2. Receives recommendations for a learning path and relevant opportunities.
3. Completes learning activities and adds a project or certificate to profile.
4. Registers for a hackathon or applies for an internship/job.
5. Tracks status and receives feedback or interview invitations.
6. Uses outcomes to improve profile and future matching.



### Organizer: create to results

1. Creates or verifies an organization and selects a plan.
2. Creates a hackathon, defines rules, schedule, prizes, team rules, and rubric.
3. Publishes event and monitors registrations.
4. Manages teams, communications, resources, mentors, and submissions.
5. Assigns judges, finalizes scores, publishes results, and reviews analytics.



### College lead or ambassador: activate a campus community

1. A college lead verifies the institution and receives its dedicated workspace.
2. The lead creates campus-restricted programs, manages eligible cohorts, and reviews aggregate outcomes.
3. A voluntary ambassador cohort may promote approved opportunities using supplied materials.
4. An ambassador submits activity proof and can earn non-cash recognition when criteria are met.



### NGO partner: problem to verified impact experience

1. A verified NGO submits an impact brief and a related challenge or hackathon for review.
2. Buildora and the NGO publish the approved program, resources, responsible-use rules, and any related internship.
3. Learners form teams or participate individually, submit work, and receive structured evaluation.
4. The NGO shortlists viable solutions and can invite eligible participants to apply for the internship.
5. After completion, the NGO confirms the learner's role, dates, and scope so Buildora can mark the experience verified.



### Employer: post to hire

1. Creates organization profile and job/internship listing.
2. Defines required skills, eligibility, questions, and process stages.
3. Reviews applications and eligible discoverable talent.
4. Shortlists, schedules interviews, records decisions, and marks hire outcome.
5. Reviews source and conversion metrics.



### Mentor: list to deliver a session

1. Applies, documents expertise, configures services, availability, pricing, and payout details.
2. Receives approval and publishes or shares the mentor profile.
3. Accepts bookings that match available slots and receives the session context.
4. Conducts the session, records attendance, leaves structured feedback, and receives learner feedback.
5. Tracks payout and reputation, then refines availability and services.



## 8. MVP release plan



### Phase 1 — Marketplace foundation

- Authentication and learner profiles.
- Public directories and detail pages for hackathons, internships, and jobs.
- Search, filters, saved opportunities, applications, registration, and status tracking.
- Employer job posting and basic application pipeline.
- Organizer event publishing and participant registration.
- Configurable registration, assessment, submission, presentation, and shortlist rounds for hackathons, NGO challenges, case competitions, quizzes, and technical screening.
- Baseline assessment integrity controls, rubric scoring, judge review, and event audit logs.
- Verified organization profiles and role-based organization access.
- Dedicated verified-college workspace for staff, plus NGO problem briefs, challenge publishing, related internship applications, and verified impact-experience records.
- Admin review of organizations, listings, and reports.
- Public marketing pages, partnership inquiry form, and basic news/resources CMS.



### Phase 2 — Evidence and engagement

- Project portfolio and certificates.
- Courses, resources, learning paths, progress tracking, mock tests, and interview practice.
- Team formation, project submissions, judging, winner publication, and event exports.
- Assessment delivery, interview scheduling/scorecards, and pipeline integration.
- Personalized dashboard, recommendations, and notifications.
- Subscription billing and entitlement controls.



### Phase 3 — Network effects and scale

- Mentorship scheduling and feedback.
- Mentor onboarding, approvals, payouts, and marketplace operations.
- Talent search and richer recruiter workflows.
- Organizer analytics, matching, integrations, and white-label/co-branded events.
- University partner outcomes dashboard, ambassador program, referrals, and SSO.
- Mobile app after web engagement and retention validate the highest-value use cases.



## 9. Success measures



### North-star metric

**Monthly successful opportunity outcomes:** users who complete a meaningful milestone: accepted application, completed internship/job placement, verified hackathon submission, or completed learning-path credential.

### Supporting metrics


| Area                  | Metrics                                                                                                                                                |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Activation            | Sign-up to completed profile rate; first saved/applied/registered action within 7 days                                                                 |
| Marketplace liquidity | Opportunities per active learner; qualified applications per listing; time to first qualified application                                              |
| Learner outcomes      | Registration-to-submission rate; application-to-interview rate; application-to-placement rate; course/path completion; verified NGO impact experiences |
| Organizer outcomes    | Event publish-to-registration conversion; submission rate; judge completion rate; organizer repeat rate                                                |
| Revenue               | Free-to-paid conversion, monthly recurring revenue, churn, revenue per organizer                                                                       |
| Quality and trust     | Listing-approval SLA, report resolution time, spam/fraud rate, learner and employer satisfaction                                                       |




## 10. Non-functional requirements

- **Responsive and accessible:** Support current desktop and mobile browsers; meet WCAG 2.1 AA for key journeys.
- **Performance:** Public pages should meet Core Web Vitals targets on a mid-tier mobile network. Search results should return within two seconds at p95 under expected load.
- **Security:** Use secure authentication, role-based access controls, encrypted data in transit and at rest, audit logs, rate limits, and OWASP-aligned practices.
- **Privacy:** Collect only needed personal data; provide profile visibility controls, consent for recruiter discovery, account/data deletion workflow, and data-retention policy.
- **Reliability:** Make application, registration, payment, and submission operations idempotent and recoverable; retain timestamped records of status changes.
- **Localization readiness:** Store currency, time zones, dates, and location data in formats that can support expansion beyond India without a redesign.
- **Observability:** Track funnel events, errors, job processing, notification delivery, and operational metrics with role-sensitive data redaction.



## 11. Dependencies and assumptions

- A payment provider is needed for paid plans.
- Email, calendar/video, storage, search, analytics, and CRM providers will be selected during technical design.
- Initial market assumptions are India-focused, based on the reference copy, but the platform should avoid hard-coding a single geography.
- Opportunity legitimacy, organizer verification, and moderation policies are critical launch dependencies.
- Content supply and partner acquisition need operating owners; software alone does not create a healthy opportunity marketplace.



## 12. Risks and mitigations


| Risk                                                              | Mitigation                                                                                                                       |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Low-quality or fraudulent listings                                | Verify organizations, moderate listings, show trust indicators, and offer reporting/escalation                                   |
| Assessment fraud or unreliable scores                             | Apply configurable integrity controls, preserve attempt evidence, review anomalous results, and allow a verified follow-up round |
| NGO challenges create unsafe, extractive, or unimplementable work | Review impact briefs, responsible-use terms, data access, supervision, and internship disclosures before publication             |
| Mentor quality or booking disputes                                | Screen mentors, use clear cancellation/no-show rules, collect two-way feedback, and provide dispute handling                     |
| Learners create incomplete profiles                               | Progressive onboarding, profile completeness guidance, clear benefits, and resume import                                         |
| Few applications or poor candidate fit                            | Matching signals, eligibility clarity, recommendations, and employer feedback loops                                              |
| Hackathon operational failures                                    | Deadline controls, draft/autosave, submission receipts, rubric versioning, and organizer support                                 |
| Too much scope in the first release                               | Ship marketplace and core operational workflows before mentorship, advanced learning, and enterprise features                    |
| Content goes stale                                                | Named content owners, review dates, content analytics, and archive workflows                                                     |




## 13. Resolved product decisions


| Decision                            | Direction                                                                                                                                                                                                  |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Initial learner market              | College students, recent graduates, and career switchers, supported through role-aware onboarding and recommendations.                                                                                     |
| Opportunity sourcing                | Direct marketplace only at launch: verified employers/organizers publish and manage opportunities natively; learners apply in Buildora.                                                                    |
| Publisher verification              | Legal entity, authorized representative, organization domain, registry/manual review, and trust-and-safety approval before publishing.                                                                     |
| Hackathon formats                   | Online, in-person, hybrid, individual, and team events all work at launch.                                                                                                                                 |
| Course model                        | Proprietary Buildora content and credentials; partner authorship may be co-branded but does not create an external course catalog.                                                                         |
| Initial participant subscription    | Buildora Pro: unlimited proprietary learning/certificates plus career preparation, insights, and controlled coaching benefits; applications remain free and fairly ranked.                                 |
| Evidence standards                  | Verified skills must be linked to an assessment, completed graded learning, verifiable credential, or reviewed project; placements require employer confirmation or appropriately minimized evidence.      |
| First organizer competition release | Hackathons/NGO challenges, case and project competitions, timed quizzes, and technical screens; registration, timed assessment, submission, presentation/interview, and shortlist rounds are configurable. |
| Assessment integrity                | Identity and eligibility signals, authoritative timers, randomized pools, attempt controls, activity/audit logs, similarity checks, and human review. Intrusive automated proctoring is deferred.          |
| College workspace                   | Verified college staff receive a dedicated workspace at launch for campus programs, cohorts, eligibility, and aggregate outcomes.                                                                          |
| Ambassador program                  | Deferred as a growth channel. Any early cohort is voluntary and can receive only non-cash recognition such as badges, certificates, learning access, or event access.                                      |
| Mentor payments                     | Learners pay through Buildora; Buildora manages collection, refunds, payout release, mentor KYC/payout setup, and reconciliation through a payment provider.                                               |
| NGO differentiation                 | Verified NGOs publish reviewed impact briefs, challenges, and related internships; confirmed work becomes a verified impact experience on the learner profile.                                             |


Technical design must still select payment, payout/KYC, assessment-runner, similarity-detection, notification, and CRM providers.

## 14. Benchmark research notes

The following design inputs were drawn from public Unstop pages in October 2026. They inform Buildora requirements but are not a requirement to copy Unstop’s product, content, pricing, or brand.


| Benchmark observation                                                                                                                                                                        | Buildora product implication                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Unstop presents distinct Talent, Mentor, and Recruiter entry points and offers discovery across jobs, internships, competitions, practice, mentorship, and courses.                          | Maintain role-aware onboarding and dashboards while allowing a user to hold multiple roles.                                  |
| Unstop’s business navigation groups the funnel as brand/engage, source, screen, assess, interview, and hiring automation.                                                                    | Treat employer products as a connected workflow with shared candidate data and conversion reporting.                         |
| Unstop’s public opportunity taxonomy includes challenges, assessments, hackathons, workshops/webinars, conferences, cultural events, college festivals, internships, jobs, and scholarships. | Build a configurable round engine and unified opportunity model rather than an implementation tied only to hackathons.       |
| Unstop’s mentor flow supports approval, services, availability, pricing, booking, feedback, and payouts.                                                                                     | Build mentor marketplace operations, not only a learner-side mentor directory.                                               |
| Unstop’s campus ambassador program uses selection, a task timeline, performance progression, and rewards.                                                                                    | Keep a lightweight, voluntary cohort only after launch; use task proof and non-cash recognition rather than paid incentives. |


Public sources: [Unstop platform home](https://unstop.com/), [Unstop mentor program](https://unstop.com/become-a-mentor/amp), [Unstop mentor FAQs](https://unstop.com/mentor/faqs/amp), and [Unstop Campus Champions](https://campuschampions.unstop.com/).

Subscription benchmark: [LinkedIn Premium Career](https://premium.linkedin.com/careers/compare-plans) packages job-search insights, profile support, networking features, and learning, while [Coursera Plus](https://www.coursera.org/courseraplus/) bundles a broad proprietary/controlled learning catalog and completion credentials. Buildora Pro adopts the useful principle: charge for ongoing preparation, learning, and decision support, while keeping basic discovery and applications available to every qualified learner.