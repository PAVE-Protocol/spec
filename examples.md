# PAVE Examples

AI agents can evaluate options, recommend actions, and execute tasks across industries. But many decisions involve tradeoffs that depend on human experience, context, and judgment.

PAVE is designed to make that judgment accessible within existing AI workflows.

The following examples illustrate how organizations could use PAVE to consult relevant human judgment without transferring decision-making authority away from the people and organizations responsible for the outcome.

These are proposed integration scenarios, not claims of deployed implementations.

## Procurement: Weighing price against supplier risk

An enterprise procurement agent is evaluating suppliers for a time-sensitive order.

One supplier offers a significantly lower price, making it the most attractive option based on cost. However, its delivery history raises concerns about reliability. Choosing the cheaper supplier could save money, but a missed delivery could disrupt operations.

The organization has configured its procurement workflow to consult human judgment when a supplier-continuity exception occurs.

### Where human judgment contributes

Leena is an illustrative procurement expert with experience managing supplier relationships and operational risk.

She understands that the lowest-priced supplier isn't always the best choice. A minor price difference may be insignificant compared with the cost of a production interruption, while a supplier with occasional delays may still be appropriate when alternative inventory is available.

A **Lens** representing Leena's judgment could help the procurement agent evaluate these tradeoffs within a defined and evaluated scope.

### How PAVE participates

1. The procurement agent assembles supplier options, pricing, delivery records, and the identified continuity risk.
2. The organization's procurement policy triggers a request for relevant human judgment.
3. The application selects a configured procurement Lens or discovers permitted candidates.
4. The application inspects the selected Lens's scope and permitted uses before requesting consultation.
5. The Lens contributes an assessment of the relevant tradeoffs, which informs the agent's recommendation.
6. The organization's purchasing controls determine whether the recommended order can proceed.

This workflow is explicitly configured. It does not require the agent to independently discover PAVE or decide when human judgment is necessary.

### Decision boundary

The Lens contributes procurement judgment. It does not authorize the purchase.

Missing evidence, circumstances outside the Lens's evaluated scope, or purchasing commitments beyond delegated authority require fresh review.

Attribution connects the contribution to Leena without implying that she personally reviewed or approved the order.

---

## Creative evaluation: Choosing between competing ideas

A creative team uses AI agents to develop several concepts for a film.

The concepts are evaluated by model judges considering originality, narrative meaning, and production feasibility.

The results are inconclusive.

One concept is easier and less expensive to produce. Another is more original but requires a more ambitious production approach.

The models can compare the concepts against their evaluation criteria, but the final recommendation depends on how those criteria should be weighed.

### Where human judgment contributes

An experienced film director may recognize that an unconventional concept has greater narrative potential despite its production challenges.

An editorial specialist might identify weaknesses in a concept that appears compelling on paper but lacks a coherent emotional arc.

A Lens could represent either person's judgment within a defined creative decision context.

The expertise need not come from the person commissioning the work. An organization could consult authorized judgment from another qualified contributor when that perspective is relevant to the decision.

### How PAVE participates

1. The decision owner establishes the creative brief, evaluation criteria, and conditions requiring additional judgment.
2. AI agents generate concepts, and model judges evaluate them.
3. Conflicting assessments or another configured condition triggers a request for human judgment.
4. The workflow selects an appropriate Lens and inspects its scope and permitted uses.
5. The Lens contributes judgment about the competing creative considerations.
6. The contribution informs the recommendation, while the authorized creative decision-maker determines how to proceed.

Human judgment could also contribute earlier in the process, when evaluation criteria are being developed.

For example, a director's Lens might help identify which narrative qualities deserve greater weight before concepts are evaluated. Any resulting criteria would still require approval from the decision owner.

### Decision boundary

A Lens can contribute a creative perspective without automatically resolving disagreement or determining which concept should be produced.

The workflow must preserve material disagreement and route unresolved questions to direct human review when required.

Consulting a Lens does not mean its source personally reviewed, selected, or approved the final concept.

---

## Cybersecurity: Fixing a vulnerability without creating another risk

An AI security agent identifies a vulnerability in a production system and recommends deploying a software patch.

The patch could reduce exposure to an attack, but applying it immediately might also interrupt a critical service.

The organization must weigh the security risk against the operational consequences of the proposed response.

Its security workflow is configured to consult relevant human judgment when a proposed action involves a significant tradeoff.

### Where human judgment contributes

An experienced security leader understands that addressing a vulnerability isn't always as simple as deploying the available patch.

Depending on the circumstances, temporarily isolating an affected component, applying an alternative mitigation, or scheduling a controlled deployment may be more appropriate.

A Lens representing that leader's judgment could help an AI system weigh exploitability, system exposure, available mitigations, and operational consequences.

### How PAVE participates

1. The security agent assembles the vulnerability finding, affected systems, supporting evidence, and proposed response.
2. A configured risk threshold triggers consultation of relevant human judgment.
3. The workflow selects an authorized security Lens within its evaluated scope.
4. The Lens contributes judgment about the risks and tradeoffs associated with the available responses.
5. The contribution informs the recommended priority, mitigation strategy, or need for further investigation.
6. Existing security and change-management controls determine the authorized response.

### Decision boundary

The Lens does not authorize the deployment of a patch, the isolation of a system, or the acceptance of residual security risk.

Those decisions remain subject to the organization's existing authority and change-management controls.

Uncertain evidence, unfamiliar system behavior, or responses beyond delegated authority require direct review.

Consultation does not establish that a vulnerability is exploitable or that a proposed fix is safe to deploy.

---

## Customer service: Handling an exception fairly

A customer requests a refund after the standard return window has expired.

Ordinarily, the request would be denied under the company's return policy. However, the customer's account history shows several delivery problems and previous unsuccessful attempts to resolve the issue.

The usual policy does not fully address the circumstances.

The organization's customer service workflow is configured to consult relevant human judgment when certain exceptions arise.

### Where human judgment contributes

An experienced customer service leader understands that applying a policy consistently doesn't always mean applying it identically in every situation.

The leader might consider the customer's history, the company's responsibility for earlier problems, the remedies already offered, and whether an exception would be proportionate.

A Lens representing that judgment could help an AI service agent assess the circumstances and recommend an appropriate resolution.

### How PAVE participates

1. The service agent gathers the customer's case history, previous remedies, and applicable policy constraints.
2. The exception triggers consultation of an authorized customer service Lens.
3. The Lens contributes judgment about the relevant circumstances and possible remedies.
4. The agent uses that contribution to prepare a recommendation and identify unresolved questions.
5. The workflow checks the proposed remedy against company policy and delegated limits.
6. An authorized agent or human reviewer approves the action.

### Decision boundary

Consulting a Lens does not override company policy or increase the service agent's authority to issue refunds.

Disputed facts, remedies outside delegated limits, or circumstances beyond the Lens's evaluated scope require direct review.

The organization remains responsible for the resolution.

---

## Credit: Evaluating an application with conflicting indicators

A financial institution uses an AI-supported workflow to evaluate a credit application.

The applicant meets several standard criteria, but the available financial information presents conflicting indicators about repayment capacity.

An automated assessment identifies the inconsistency and routes the application for additional consideration.

The institution has configured its workflow to consult relevant human judgment within its permitted assessment process.

### Where human judgment contributes

An experienced credit specialist may recognize that conflicting financial indicators require a closer examination of the evidence rather than an immediate approval or denial.

For example, the specialist might identify missing financial information, inconsistencies that warrant verification, or circumstances requiring additional assessment under the institution's established criteria.

A Lens representing that judgment could help the workflow determine which questions need further investigation.

### How PAVE participates

1. The application assembles permitted financial information, assessment results, and the reason for exception review.
2. A configured rule triggers consultation of an appropriate credit Lens.
3. The workflow verifies that the requested consultation is within the resource's authorized and evaluated scope.
4. The Lens contributes judgment about the conflicting evidence and identifies areas requiring further assessment.
5. The institution applies its lending policies and applicable requirements.
6. The authorized decision process determines the outcome and any required explanation.

### Decision boundary

The Lens does not independently approve or deny credit, override lending policy, or establish regulatory compliance.

The institution remains responsible for the decision, the permitted use of applicant information, and the basis communicated to the applicant.

Cases involving insufficient evidence, unsupported circumstances, or additional review requirements must follow the institution's established procedures.

---

## Insurance: Evaluating a complex claim

An insurance company receives a claim involving property damage.

The available documentation contains conflicting accounts of the incident, and some evidence needed to determine the cause and extent of the loss is missing.

An AI workflow can organize the documents, identify inconsistencies, and retrieve relevant policy information.

However, deciding which questions to investigate next may require experience interpreting complex claims.

### Where human judgment contributes

An experienced claims specialist may recognize that an apparent inconsistency is not necessarily evidence of a problem with the claim.

The specialist might distinguish between missing documentation that is routine and evidence gaps that materially affect the assessment.

A Lens representing that judgment could help the workflow identify relevant questions, weigh available evidence, and prioritize further investigation within a defined claim context.

### How PAVE participates

1. The application assembles permitted claim documents, relevant policy terms, and unresolved questions.
2. The case meets a configured threshold for judgment consultation.
3. The workflow selects an authorized claims Lens within its evaluated scope.
4. The Lens contributes judgment about the available evidence and areas requiring further investigation.
5. The application requests additional evidence or prepares a recommendation informed by that contribution.
6. The insurer's authorized claims process determines coverage and settlement.

### Decision boundary

The Lens does not change policy terms or independently determine whether a claim should be approved, denied, or settled.

The insurer retains responsibility for interpreting the policy, meeting applicable requirements, and authorizing the outcome.

Disputed facts, insufficient evidence, and circumstances outside the Lens's evaluated scope require direct review.

---

## What these examples have in common

Although the industries and decisions differ, the underlying architecture remains consistent.

In each scenario:

- **An existing workflow identifies a need for judgment.** The organization defines when consultation should occur.
- **A relevant Lens is selected.** The application uses a configured resource or discovers permitted candidates.
- **Scope and permissions govern consultation.** The resource must support the intended decision context and authorized use.
- **Human judgment contributes to the decision.** The Lens informs an assessment, recommendation, or next step.
- **Decision-making authority remains separate.** The organization or authorized decision owner determines whether and how to act.
- **Exceptions can require direct human review.** A Lens does not eliminate the need for people to evaluate unfamiliar or unresolved situations.
- **Attribution preserves the human connection.** The judgment contribution remains connected to its human source without implying personal approval of every resulting decision.

PAVE's role is to make relevant human judgment accessible alongside the models, tools, policies, and people already participating in a workflow.

It does not require organizations to replace their existing AI systems or transfer decision-making authority to PAVE.

## Evaluating a PAVE integration

These examples illustrate possible applications. Whether a particular integration is technically supported or improves decision-making must be established through evaluation.

An evaluation should consider:

- **Judgment fidelity:** Does the Lens faithfully represent the intended human judgment within its evaluated scope?
- **Authorization:** Are consultations restricted to permitted callers, purposes, and conditions?
- **Workflow integration:** Can the connected application correctly select resources, request consultation, and handle the resulting contribution?
- **Review and failure handling:** Does the workflow distinguish completed judgment outcomes from requests for review and integration failures?
- **Decision quality:** Does the contribution improve the relevant decision process when compared with an appropriate baseline?

A successful consultation demonstrates that a judgment resource was used within a workflow. It does not, by itself, establish that the resulting decision was better.

## Next steps

Explore [Architecture](architecture.md) to understand PAVE's components and workflow boundaries, or see [Terminology](terminology.md) for definitions of Lenses, judgment capabilities, authorization, and related concepts.

To discuss evaluating or integrating PAVE, contact [hello@byfruit.io](mailto:hello@byfruit.io).