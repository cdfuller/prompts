# The Reusable Project Planning Process

This process guides the development of a project from an initial idea to a complete plan, documented in three distinct Markdown artifacts: The **PRD** (What/Why), the **TSD** (How), and the **Roadmap** (Milestones/Sequence).

## 0\. Initial Intake (The Project Brief)

To begin a new project, the user should provide the initial information using the following template:

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

## 1\. Phase 1: Discovery, Research, and PRD Definition (The "What")

This phase focuses on understanding the domain and defining the product scope.

1.  **Domain Research Strategy:**
      * Analyze the intake brief to identify specialized domain knowledge required (e.g., complex calculations, industry standards, competitive landscape).
      * The LLM proposes specific areas requiring deeper research.
      * **Action:** The LLM asks the user whether the LLM should conduct this research and present findings, or if the user will provide the necessary domain expertise.
2.  **Execute Domain Research:**
      * Based on the strategy, the research is conducted.
      * *Output:* A brief summary of key domain insights, terminology, and potential functional edge cases relevant to the project.
3.  **Clarification Round 1 (Product Focus):**
      * Ask a numbered list of binary (Yes/No or A/B) questions to define the scope and functionality, informed by the domain research.
4.  **Artifact Generation 1:** Generate the **Product Requirements Document (PRD)** in Markdown format.

## 2\. Phase 2: Technical Analysis and TSD Definition (The "How")

This phase focuses on translating the product vision into a technical blueprint.

1.  **Technical Research and Analysis:**
      * Review the PRD and domain insights. Identify technical challenges.
      * **Action:** Conduct research focused on specific technical implementations, algorithms, available libraries, APIs, and architectural patterns suitable for the requirements and constraints.
      * Analyze the trade-offs (performance, cost, complexity, maintainability) between different approaches.
2.  **Clarification Round 2 (Technical Focus):**
      * Ask a numbered list of binary questions focusing on the technology stack.
      * The LLM must present the trade-offs identified during the technical research before asking for the user's decision (e.g., "Approach A is faster but increases app size; Approach B is smaller but slower. Do you prefer A?").
3.  **Artifact Generation 2:** Generate the **Technical Specification Document (TSD)** in Markdown format, including detailed Input/Output examples and technical edge cases.

## 3\. Phase 3: Roadmap and Execution Planning (The "Sequence")

This phase breaks the work into manageable steps.

1.  **Milestone Definition:** Analyze the PRD and TSD and break the project down into sequential, logical steps that deliver incremental value, without assigning calendar dates or durations.
2.  **Artifact Generation 3:** Generate the **Implementation Roadmap** in Markdown format, documenting the ordered milestones and key deliverables with no time-based commitments.
3.  **Handoff:** Confirm all artifacts (PRD, TSD, Roadmap) with the user and ask which Milestone they would like to begin implementing.
