# Lightweight Feature Planning Process

This process adapts the reusable planning framework for small, low-to-medium risk features developed by a solo builder. It keeps planning quick while ensuring you capture the decisions, risks, and execution steps needed to ship confidently.

## Step 1: Intake Snapshot
Start every feature by completing this shared intake template:

```markdown
**Problem Statement:**
[Describe the problem you are trying to solve, the pain points, and the context. Why is this needed?]

**Proposed Solution (High-Level):**
[Describe your initial vision for the application or system. What should it do?]

**Target Audience:**
[Who will be using this application?]

**Key Constraints and Preferences:**
[List any critical technical constraints (e.g., "must be client-side", "must work offline"), preferred technologies (e.g., "prefer Python", "avoid frameworks"), budgetary constraints (e.g., "must use free services"), or design inspirations.]
```

## Step 2: Scope Check
Clarify the edges of the feature before you dive into implementation. Capture:

- **Must-Have Boundaries:** What has to ship and what is explicitly out of scope.
- **Dependencies / Prereqs:** Libraries, data, configs, or prep work you must line up.
- **Rollout Considerations:** Whether you will use a flag, staged release, or direct deployment.
- **Effort Budget:** How much focused work you are willing to invest and where it fits into your queue.

## Step 3: Solution Sketch
Outline how you intend to build the feature:

- **Approach Summary:** A few sentences describing the planned implementation.
- **Key Changes / Touchpoints:** Files, services, or UI that will change.
- **Risks & Mitigations:** Any concerns (performance, data integrity, UX) and how you will manage them.
- **Test Strategy:** Manual checks, automation, or data validation you need.
- **Reference Links or Notes:** Links to spikes, diagrams, or supporting docs.

## Step 4: Implementation Plan
Break the work into manageable chunks so you know what progress looks like:

- **Milestone 1:**
  - *Goal:*
  - *Expected Output:*
- **Milestone 2:**
  - *Goal:*
  - *Expected Output:*
- **Milestone 3 (optional):**
  - *Goal:*
  - *Expected Output:*
- **Deployment & Follow-Up Tasks:** Feature flags, migrations, cleanup, monitoring, or any post-release actions to handle.

After Step 4 is complete, begin implementation using the plan as your guide.

## Future Considerations
Document any follow-up work you intentionally postpone (stretch goals, refinements, research). Capture:

- **Item:** What you are leaving for later.
- **Reason:** Why it isn’t part of the current delivery.
- **Revisit Trigger:** Condition or moment when you plan to reassess.

Keep this section at the bottom of your plan so future you can see what remains on the horizon.

## Expected Artifacts

Working through the steps yields a single Markdown record containing:

- A completed intake snapshot (Problem, Proposed Solution, Target Audience, Constraints/Preferences).
- Scope check notes detailing boundaries, dependencies, rollout strategy, and effort budget.
- A solution sketch summarizing the approach, touchpoints, risks, mitigations, test plan, and references.
- An implementation plan with milestones, expected outputs, and deployment/follow-up tasks.
- A Future Considerations list capturing postponed items, rationale, and when to revisit.

## LLM Collaboration Guidance

When an LLM participates in the process (e.g., preparing clarifying questions or drafting sections):

- The LLM must ask numbered binary questions (Yes/No or A/B) during any clarification round to tighten scope. Keep each question self-contained and informed by the current artifacts.
- Present trade-offs before requesting a decision. For example: “Option A ships faster but increases app size; Option B is lighter but slower. Do you prefer A?”
- Confirm whether the user wants the LLM to research domain or technical topics before proceeding; only act after approval.

## Usage Tips

- Fill sections iteratively as information becomes clear; refine between working sessions.
- Keep notes brief—aim for high signal, low overhead. Link to deeper notes or code spikes when necessary.
- Revisit the document after delivery to capture lessons learned and update Future Considerations if items ship or are dropped.
