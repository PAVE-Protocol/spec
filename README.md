# PAVE

PAVE is a protocol that gives AI and agentic systems a way to call on human judgment and authority when needed.

As software becomes more capable of acting on behalf of people and organizations, the question is no longer only what a system can do. It is also where human judgment matters, whose judgment is being represented, what authority accompanies it and how those contributions remain attributable to the people they came from.

PAVE is being developed to make those relationships legible within machine workflows.

A system can request represented human judgment within a defined scope. Permission to consult that judgment and permission to act remain separate. Attribution and provenance preserve the relationship between a represented contribution and its human source.

FRUIT calls the broader concept [Callable Human Judgment](https://byfruit.io/what-is-callable-human-judgment/).

PAVE is developed by [FRUIT](https://byfruit.io). Invented by [Angela Benton](https://angelabenton.com). PAVE intellectual property is owned by **FRUIT Holdings, Inc.**.

## Current status

PAVE is under active development.

This repository documents PAVE's public architecture, specification status and intended operation. Descriptions of invocation, execution or integrations do not by themselves indicate that those capabilities are publicly available or production-ready.

PAVE Core and PAVE Agent are private engineering repositories.

The complete current architecture is maintained separately from this public repository. Earlier public schemas document prior work and should not be treated as the complete current architecture. See [Specification Status](./spec/README.md).

This repository is not a production SDK or a self-service runtime. The applications described below express the intended integration model; specific capabilities and availability must be established for each implementation.

Evaluation priorities include fidelity to the represented judgment, preservation of source attribution, traceability of use, behavior at scope boundaries, and the operational effect on agent workflows. Suitability and performance are evaluated within the scope of each implementation and use case.

## About this repository

PAVE is proprietary technology developed by FRUIT.

This repository makes selected technical materials publicly available so PAVE's architecture, boundaries and development can be understood and referenced. It does not contain the complete PAVE implementation.

Public availability of these materials does not make PAVE open source. The [PAVE Public Materials License](./LICENSE) governs use of the materials in this repository. Uses outside those permissions require a separate written agreement with FRUIT.

Earlier schema materials and accompanying notes have been retired from the current branch. This repository does not disclose the complete proprietary methodology for eliciting, extracting, and transforming human judgment into executable representations. Detailed methods and implementation materials are maintained separately.

## Why agents need human judgment

Agentic systems can retrieve information, generate alternatives, coordinate tools, and execute tasks. As they take on more consequential workflows, they also encounter decisions whose quality depends on how competing considerations are weighed.

For example, an experienced operator may recognize when a favorable price conceals unacceptable delivery risk. A technical leader may know when an architectural compromise is justified and when it creates an obligation the organization cannot sustain. A researcher may distinguish an interesting result from evidence strong enough to support a conclusion.

That judgment develops through decisions, consequences, and experience. Making it available to agents requires more than access to the same information.

PAVE addresses this need by developing a way to represent and apply specific human judgment through a programmatic interface. Its purpose is to let agents draw on identifiable, authorized judgment capabilities at the point where a workflow requires them, while retaining attribution to the human whose judgment is being applied.

## Human participation in agentic systems

PAVE is built on the thesis that greater agent autonomy should expand the ways humans can participate and contribute to automated work. A person's judgment can remain an identifiable contribution even when that person is not present for each application of it.

This matters because the ability to automate a workflow and the expertise needed to guide its decisions are distinct contributions. As agents take on more work, people need mechanisms through which their judgment can participate under defined terms, with its origin and use remaining visible.

PAVE's intended model connects three elements:

- **Attribution:** identify the human whose judgment a capability represents and preserve that connection when the capability is applied.
- **Authorization:** define who may invoke the capability, for which purposes, and under what conditions.
- **Economic participation:** support licensing arrangements through which contributors can receive value from authorized use of their judgment.

Attribution has two levels: identifying the human source of a Lens and recording when that Lens contributes to a particular workflow or decision. Preserving that connection from source through use is an architectural objective. The extent of attribution and usage recording available in an integration must be established for that implementation.

The purpose is to make human contribution identifiable, governable, and economically recognizable within agentic systems. Attribution identifies the source of represented judgment; it does not by itself establish consent, payment, endorsement of an output, or responsibility for an agent's final action.

## Beyond contextual personalization

Giving an LLM a person's biography, conversation history, or knowledge record can help it generate responses informed by that material. In that arrangement, the model still infers how the person might reason.

PAVE's architecture introduces one or more transformations between the human knowledge and the capability used in execution.

A **GHI record** represents structured human knowledge. A **Lens** is a derived representation intended to apply supported elements of that judgment to a defined decision context while retaining a connection to its human source. The distinction allows the source record, the transformation, and the resulting behavior to be examined separately, with attribution linking the derived capability to the contributor.

The objective is to make the basis for applying judgment explicit and evaluable, rather than leaving it entirely to a model's interpretation of descriptive context. A Lens does not represent every aspect of a person or guarantee the decision that person would make in an unfamiliar situation.

## Applying judgment at scale

Human-in-the-loop review brings direct human attention to a decision. When every recurring decision requires that attention, throughput and response time depend on reviewer capacity and availability.

PAVE is designed to reduce that dependence for decisions within a supported scope. In the intended model, a defined judgment capability can be invoked repeatedly across authorized agent workflows, while people remain responsible for its scope, evaluation, revision, and the decisions requiring direct review.

This creates a different allocation of human effort:

| Human contribution | Intended role within a PAVE-enabled workflow |
| --- | --- |
| Establish the judgment to be represented | Define the basis for a reusable capability. |
| Evaluate its fidelity and limits | Determine where its application is appropriate. |
| Authorize its use | Set the permitted applications and access arrangements. |
| Remain attributable as its source | Preserve recognition of the human contribution as the capability is reused. |
| Review exceptions and new situations | Address cases beyond the supported representation. |
| Revise it as experience develops | Keep the capability aligned with the judgment it represents. |

The intended benefit is broader access to attributable human judgment without requiring the source expert to participate synchronously in every invocation. That benefit depends on demonstrated fidelity, reliable execution, and appropriate integration with the surrounding system's controls.

## Intended applications

The following examples illustrate the kinds of integrations PAVE is being developed to support. They are not announcements of deployed products.

| Agent workflow | Judgment capability | Example boundary for human review |
| --- | --- | --- |
| **Procurement** | Apply an operator's framework for weighing cost, reliability, delivery risk, and supplier exceptions. | A new supplier situation outside the framework's evaluated scope. |
| **Product and engineering** | Apply a technical leader's approach to prioritization and architectural tradeoffs. | A consequential commitment requiring fresh strategic judgment. |
| **Customer resolution** | Apply a service leader's framework for selecting proportionate remedies. | An unusual case or a remedy beyond the application's delegated authority. |
| **Research and analysis** | Apply an expert's framework for assessing evidence and identifying unresolved gaps. | Conflicting evidence that the represented framework cannot adequately resolve. |

In a procurement integration, for example, an agent could assemble supplier options and relevant evidence, invoke an authorized Lens as part of its evaluation, and use the result to inform a recommendation. Under the intended attribution model, the workflow would record which Lens contributed and retain the connection to the human whose judgment it represents. The surrounding application would retain responsibility for purchasing authority, execution controls, and escalation.

## Technical terminology: Generative Human Intelligence

GHI remains a technical term in PAVE's source representations and engineering materials. It does not replace Callable Human Judgment as the broader concept described above. Earlier public schemas are historical material, not current implementation guidance.

PAVE organizes **Generative Human Intelligence (GHI)** into three related types:

- **Perspective:** how a person notices and interprets situations.
- **Judgment:** how a person weighs considerations and makes decisions.
- **Interpretive knowledge:** the frameworks, principles, and transferable patterns developed through experience.

These provide a foundation for representing human expertise as an asset whose application can be attributed, authorized, evaluated, and licensed.

## Relationship to UDIF

[UDIF — Universal Data Interchange Format](https://github.com/Universal-Data-Interchange-Format/udif) provides an open format for portable data and context. PAVE develops the proprietary capabilities for representing and applying human judgment.

UDIF can be adopted independently under Apache License 2.0. Using its published GHI interchange schema does not itself require a PAVE commercial license or provide an executable PAVE Lens.

UDIF remains personally owned and independently maintained by Angela Benton. PAVE is owned by FRUIT Holdings, Inc. Their technical relationship does not combine their ownership or licensing terms.

## Ownership and licensing

**Angela Benton** is PAVE's inventor. **[FRUIT Holdings, Inc.](https://byfruit.io)** owns the PAVE protocol intellectual property.

Ownership of the protocol is separate from rights in an individual's source material and judgment records. An integration must address permission to use that material as well as permission to use PAVE, including applicable attribution requirements and any contributor compensation arrangements.

PAVE is proprietary. The [PAVE Public Materials License](./LICENSE) defines the limited permissions for these materials. Its limits apply to both commercial and non-commercial uses of the materials; uses outside those permissions require a separate written agreement with FRUIT. Public access does not constitute an open-source license.

For commercial licensing, evaluation, and integration inquiries, contact [hello@byfruit.io](mailto:hello@byfruit.io) or visit [FRUIT](https://byfruit.io). Documentation feedback and general technical questions are welcome through [GitHub issues](https://github.com/PAVE-Protocol/spec/issues).

## Publication provenance

This repository is the public PAVE specification-status and overview destination.
The historical notice in spec/README.md is preserved from the approved source
surface, with an added context note. Its reference to earlier Git history describes
the source repository at the time that notice was written, not the history published here.

This repository intentionally contains only the approved current surface and sanitized
specification history. Retired material was excluded from its history. This does not
erase, retract, or change any prior public availability in the source repository.
No access to the Core repository is required to read this overview, status, or license.
