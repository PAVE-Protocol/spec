# PAVE Capabilities and Availability

PAVE is a proprietary protocol developed by FRUIT to make human judgment callable by AI and agentic systems.

PAVE defines how human judgment can be represented, discovered, and consulted within existing AI workflows while preserving attribution, authorization, provenance, and human authority.

Its architecture and foundational capabilities have been established. FRUIT continues to advance PAVE implementations and integrations across enterprise and agentic environments.

Organizations interested in implementing PAVE can work directly with FRUIT to evaluate their requirements, configure an appropriate integration, and establish the necessary technical and licensing arrangements.

## Protocol architecture

PAVE provides an architecture for incorporating represented human judgment into existing AI systems without requiring organizations to replace their models, applications, or decision-making processes.

The architecture includes:

- **PAVE Core:** Defines and processes judgment representations, including Registry and Runtime responsibilities.
- **PAVE Agent:** Connects external applications and workflows to PAVE Core through supported interfaces and orchestration.
- **GHI records:** Structured representations of human knowledge used as source material for developing judgment capabilities.
- **Lenses:** Derived representations of human judgment that can be consulted within defined decision contexts.
- **Registry:** Supports discovery and inspection of permitted judgment resource information.
- **Runtime:** Applies supported judgment representations within their authorized scope.
- **Human Judgment MCP:** Provides an MCP-first integration path for connecting compatible AI systems to PAVE.

These components establish how human judgment can participate in automated workflows while maintaining boundaries between consultation, decision-making, and action.

See [Architecture](architecture.md) for a detailed explanation of PAVE's components and integration patterns.

## Core capabilities

PAVE defines several capabilities that support the use of human judgment within AI and agentic systems.

### Judgment representation

Human knowledge and judgment can be structured into representations associated with specific decision contexts.

A Lens provides a way for supported elements of that judgment to be consulted by an AI system without requiring the human contributor to personally evaluate every recurring decision.

Representations have defined scope and require appropriate review, evaluation, and authorization before use.

### Resource discovery and inspection

PAVE supports an architecture in which authorized applications and agents can discover available judgment resources and inspect permitted information about their scope, purpose, and supported operations.

Discovery identifies candidate resources. It does not automatically establish their relevance or authorize consultation.

Inspection provides permitted metadata without automatically exposing private human-source records or underlying representations.

### Judgment consultation

A connected application can request the application of a supported Lens within an authorized decision context.

The resulting contribution can inform an assessment, recommendation, or next step within the surrounding workflow.

Permission to consult a Lens is separate from permission to act on its contribution.

The application or organization retains its existing decision-making and action controls.

### Attribution and provenance

PAVE maintains a distinction between a judgment contribution, its human source, and the representation through which that judgment is made available.

Attribution identifies the human source of a contribution.

Provenance connects the representation to its source and derivation.

Neither implies that the contributor personally reviewed or approved every decision informed by the Lens.

### Authorization and scope

Consultation is governed by the applicable permissions, supported operations, and evaluated scope of the judgment resource.

A resource may be appropriate for one decision context without being suitable for another.

Requests outside supported or authorized conditions require appropriate handling, which may include direct human review.

### Integration with existing workflows

PAVE is designed to participate in existing applications, policies, and agentic workflows.

Organizations can explicitly configure when judgment consultation occurs, which resources may be used, and how the resulting contribution affects the workflow.

This approach does not require an AI agent to independently discover PAVE or determine when human judgment is needed.

Autonomous discovery and selection are separate integration capabilities that depend on the connected agent's tools, permissions, and supported operations.

## Enterprise implementation

Organizations can work with FRUIT to evaluate and implement PAVE within their own technical environments.

PAVE's architecture accommodates different integration arrangements based on an organization's infrastructure, security, data-handling, and operational requirements.

Potential arrangements include:

| Integration arrangement | Description |
| --- | --- |
| **Internal** | Licensed judgment services operate within an organization-controlled environment. |
| **External** | An application consults an authorized external judgment service using approved inputs and permitted outputs. |
| **Hybrid** | Internal applications and data-handling processes work with selected internal or external judgment services. |

These arrangements describe architectural options rather than universally available deployment packages.

The appropriate implementation is established with FRUIT based on the organization's requirements, supported capabilities, and applicable agreements.

### Integration approach

An enterprise implementation typically involves:

1. **Identifying the workflow:** Determine which decisions or processes would benefit from access to represented human judgment.
2. **Defining the judgment requirement:** Establish the relevant expertise, decision context, and scope of consultation.
3. **Selecting judgment resources:** Identify appropriate Lenses or determine what representations need to be developed.
4. **Establishing technical integration:** Determine the interfaces, operations, infrastructure, and deployment arrangements required.
5. **Defining permissions:** Establish authorized callers, permitted uses, contributor rights, and action boundaries.
6. **Validating the workflow:** Evaluate judgment fidelity, authorization, response handling, and integration behavior before operational use.

FRUIT works with prospective adopters to determine the appropriate scope and technical requirements for each engagement.

## Integration interfaces

PAVE's primary integration direction is MCP-first through **Human Judgment MCP**, connecting compatible applications and agents through PAVE Agent to PAVE Core.

Specialized adapters may support additional enterprise platforms, applications, and workflow requirements.

The conceptual integration path is:

**Existing application → Human Judgment MCP or adapter → PAVE Agent → PAVE Core**

Interface compatibility, resource discovery, and judgment execution are distinct capabilities.

Support for a particular interface does not automatically establish that a specific judgment resource is available or executable.

Supported operations and integration requirements are confirmed for each implementation.

## Evaluation and validation

PAVE implementations are evaluated within the context of the judgment resources and workflows they support.

Evaluation may include:

- **Judgment fidelity:** Whether a Lens faithfully represents the relevant human judgment within its defined scope.
- **Resource suitability:** Whether the selected judgment resource is appropriate for the decision context.
- **Authorization:** Whether consultation respects permissions, supported purposes, and applicable conditions.
- **Attribution and provenance:** Whether the contribution maintains the required connection to its human source and derivation.
- **Workflow behavior:** Whether the application correctly handles completed consultations, review requests, and integration failures.
- **Decision quality:** Whether the contribution improves the relevant decision process when evaluated against an appropriate baseline.

Successful technical consultation does not, by itself, establish that a decision outcome has improved.

Validation requirements are determined by the use case, operating environment, and applicable organizational requirements.

## Availability and access

PAVE's public architecture, terminology, and illustrative applications are documented in this repository.

Detailed technical specifications, implementations, and services are available through arrangements with FRUIT.

Organizations interested in evaluating, integrating, or implementing PAVE can engage FRUIT to establish:

- The proposed use case and technical requirements.
- Relevant judgment resources and their permitted scope.
- Supported interfaces and implementation arrangements.
- Contributor authorization and applicable usage rights.
- Evaluation, validation, and deployment requirements.
- Licensing and commercial terms.

Access and supported functionality are determined for each engagement.

The [examples](examples.md) in this repository illustrate potential applications across industries. They do not establish that every integration has been deployed or that specific decision outcomes have been validated.

## Documentation

| Document | Description |
| --- | --- |
| [Overview](README.md) | What PAVE is and why human judgment matters. |
| [Architecture](architecture.md) | Protocol components, integration patterns, and authority boundaries. |
| [Terminology](terminology.md) | Core concepts and technical definitions. |
| [Examples](examples.md) | Illustrative applications across industries. |
| [Specification](spec/README.md) | Public architecture and access to detailed technical specifications. |
| [Licensing](licensing.md) | Public materials, implementation rights, and contributor rights. |

## Contact

To discuss evaluating, integrating, or licensing PAVE, contact [hello@byfruit.io](mailto:hello@byfruit.io).

PAVE was invented by [Angela Benton](https://angelabenton.com) and is proprietary technology owned by **FRUIT Holdings, Inc.**

Public repository materials are governed by the [PAVE Public Materials License](LICENSE).