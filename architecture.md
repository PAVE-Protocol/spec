# PAVE architecture

PAVE is designed to bring represented human judgment into existing AI workflows. An application can consult a relevant judgment capability while retaining its own models, orchestration, policies, and action controls.

An enterprise can configure when PAVE should participate, which resources to consult, and how to use the contribution. Autonomous discovery by a general-purpose agent is a separate, optional interaction pattern.

## Components

| Component | Responsibility |
| --- | --- |
| **PAVE Core** | Defines and processes judgment representations, including resource discovery and judgment execution. |
| **PAVE Agent** | Connects external workflows to PAVE Core through interfaces and orchestration. |

Within PAVE Core:

- **Registry** supports discovery and inspection of permitted resource metadata.
- **Runtime** applies supported judgment representations within their authorized scope.

PAVE Agent handles integration with the surrounding workflow. Core remains responsible for the meaning and processing of PAVE judgment representations.

## From human knowledge to a Lens

Before human judgment can be consulted by an AI system, it must be represented in a form the system can use.

PAVE distinguishes the human knowledge captured in a **GHI record** from the **Lens** derived from that material for a specific decision context.

A GHI record holds structured human knowledge. A Lens is a derived representation intended to apply supported elements of that judgment within a defined context.

Three decisions remain distinct:

1. **Adoption:** the person affirms that specific material represents their judgment within a stated scope.
2. **Permission to consult:** authorized callers may request its application for specified purposes.
3. **Permission to act:** the surrounding workflow determines who may act on the contribution.

Reviewing candidate material or expressing adoption intent does not, by itself, complete authorization for use.

See [Terminology](terminology.md) for the source-record and Lens distinction.

## Judgment in a workflow

A conceptual PAVE consultation follows this sequence:

1. **Identify the need.** A configured rule, a person, or an agent determines that relevant judgment should participate.
2. **Select a resource.** The workflow uses a configured resource or discovers candidates within its permitted scope.
3. **Inspect its limits.** The workflow checks available metadata, decision context, and use conditions.
4. **Request consultation.** The request proceeds only when the resource, operation, and intended use are supported and authorized.
5. **Handle the response.** The workflow distinguishes a completed judgment outcome from a request for review or an integration failure.
6. **Decide and act.** The contribution informs the existing decision process under its action controls.

Discovery returns candidates; it does not establish their relevance or authorize their use. Inspection returns permitted metadata, rather than the underlying Lens or private human records.

A request requiring review is not a completed judgment result. An integration failure must be handled as a failure, rather than interpreted as a judgment decision.

## Configured enterprise integration

Organizations can integrate PAVE directly into existing applications, workflows, or policies.

For example, an enterprise could require a procurement agent to consult an authorized Lens whenever a supplier decision meets specified risk conditions.

This approach does not require an AI agent to discover PAVE independently. The organization determines when and how human judgment participates.

The organization defines:

- When consultation is required.
- Which resources or selection criteria apply.
- What inputs may be supplied.
- Who may request consultation and for what purpose.
- How contributions, review requests, and failures affect the workflow.
- Who retains authority for the final action.

For example, a supplier-continuity exception could trigger consultation of a procurement Lens. The contribution would inform the existing recommendation process, while purchasing approval and execution remain with the organization.

This is an illustrative integration pattern. A specific implementation requires agreed access, supported operations, authorized resources, and validation of the connected workflow.

## Optional autonomous discovery

A general-purpose agent could also identify a need for external judgment and select an appropriate resource.

That behavior depends on the agent’s tools, instructions, permissions, resource descriptions, and ability to select relevant judgment. Access to PAVE alone does not establish reliable autonomous selection.

Configured consultation and autonomous selection are separate capabilities. A workflow can use explicit configuration even when autonomous selection is unavailable or unsuitable.

## Integration interfaces

PAVE's integration direction is MCP-first, using the **Model Context Protocol (MCP)** to connect with compatible AI systems.

**Human Judgment MCP** provides the intended interface between external workflows and PAVE Agent, which connects to PAVE Core. Specialized adapters may address additional platform or workflow requirements.

The conceptual connection is:

**Existing application → Human Judgment MCP or adapter → PAVE Agent → PAVE Core**

Interface compatibility is one part of an integration. The connected system must also support the required operations, resource selection, permissions, and response handling.

MCP compatibility alone does not establish support for a particular platform or the availability of judgment execution.

## Authority, attribution, and provenance

PAVE separates resource access from authority to make a downstream decision.

Authentication identifies a caller. Permission to consult determines whether that caller may use a judgment resource for a particular purpose. Action authority remains with the surrounding workflow.

**Attribution** identifies the human source of a contribution. **Provenance** connects the representation to its source and derivation. Neither implies that the source person personally reviewed or endorsed a particular result.

A caller receives only the metadata and outputs permitted for that interaction. Discovery and provenance references do not automatically grant access to private source records or derivation evidence.

## Enterprise operating patterns

PAVE's architecture allows organizations to evaluate different integration arrangements based on their infrastructure, security, and data-handling requirements.

| Pattern | Conceptual arrangement |
| --- | --- |
| **Internal** | The workflow and licensed judgment services operate within an organization-controlled environment. |
| **External** | The workflow sends approved inputs to an authorized external judgment service and receives permitted outputs. |
| **Hybrid** | Internal systems handle data preparation and actions while selected internal or external services provide judgment contributions. |

For each arrangement, the integration must define data transfers, storage, retention, logging, source visibility, output reuse, revocation, and exception handling.

These patterns describe possible arrangements. Deployment options and data-handling commitments must be established for the specific integration.

## Access

Contact [hello@byfruit.io](mailto:hello@byfruit.io) to discuss PAVE evaluation, integration, and licensing.

See [Examples](examples.md) for proposed workflows and [Licensing](licensing.md) for access and contributor rights. Public repository materials are governed by the [PAVE Public Materials License](LICENSE).