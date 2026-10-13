# PAVE Terminology

This page defines the concepts and technical terms used throughout the PAVE documentation.

## Core concepts

### Callable Human Judgment (CHJ)

Human-derived judgment represented so a system can request its application within a defined scope.

Callable Human Judgment is the broader [FRUIT concept](https://byfruit.io/what-is-callable-human-judgment/). PAVE provides the protocol behind it.

### PAVE

**Perspective Asset Valuation and Exchange Protocol.** FRUIT's proprietary protocol for making human judgment callable by AI agents.

### Generative Human Intelligence (GHI)

Within PAVE, Generative Human Intelligence (GHI) describes structured representations of human expertise across three dimensions:

- **Perspective:** how a person notices and interprets situations.
- **Judgment:** how a person weighs considerations and makes decisions.
- **Interpretive knowledge:** frameworks, principles, and transferable patterns developed through experience.

GHI is a technical term used in PAVE's source representations. Callable Human Judgment (CHJ) describes the broader concept of making represented judgment available for consultation.

### GHI record

A structured representation of human knowledge used as source material for deriving a Lens.

### Lens

A representation derived from human knowledge and judgment, intended to apply supported elements of that judgment within a defined decision context.

A Lens retains a connection to its human source. It does not represent every aspect of that person or guarantee the decision they would make in an unfamiliar situation.

### Source record and Lens

A GHI record and a Lens serve different purposes: the record holds structured source knowledge; the Lens is the derived representation intended for application.

Providing a model with a biography, conversation history, or knowledge record lets it infer how someone might reason. PAVE introduces transformations between source knowledge and the judgment capability a workflow consults, so the source, derivation, and resulting behavior can be evaluated separately.

### Scope

The boundaries within which a judgment representation is intended, evaluated, or authorized for use.

These boundaries may cover the decision context, supported inputs, permitted purposes, and callers. Evaluated scope and permission to use a resource must both be considered before consultation.

## Resources and operations

### Resource

An identified judgment resource within a host's scope. Its identity allows a workflow to select or reference it.

### Host

A system that makes supported PAVE operations and judgment resources available to authorized callers.

### Descriptor

Metadata describing a resource or the operations a host supports. A descriptor does not provide the underlying Lens or permission to execute it.

### Judgment capability

The represented human contribution that a workflow intends to consult, such as an expert's approach to evaluating supplier risk.

### Interface capability

An operation supported by a host or interface, such as discovery or inspection. Support for an interface operation does not establish that a particular judgment resource can be invoked.

### Discovery

Finding candidate resources within the scope visible to a caller. Discovery does not establish relevance or permission to use a resource.

### Inspection

Retrieving permitted metadata about a selected resource, including its context and limitations.

### Invocation

Requesting the application of a judgment resource. A request requires supported operations, an available runtime, and authorization for the intended use.

### Execution

The actual application of supported judgment by the runtime. Sending an invocation request does not, by itself, establish completed execution.

## Components and integration

### PAVE Core

The layer responsible for PAVE's judgment representations and processing, including Registry and Runtime responsibilities.

### PAVE Agent

The interface and orchestration layer connecting external workflows to PAVE Core.

### Registry

The Core responsibility for discovery and inspection of permitted resource metadata.

### Runtime

The Core responsibility for applying supported judgment representations within their authorized scope.

### Human Judgment MCP

PAVE's MCP-first integration path for connecting compatible workflows through PAVE Agent to PAVE Core.

### Lens creation

The process of developing a Lens from human knowledge and judgment for a defined decision context.

It includes capturing source material, preparing candidate representations, defining their scope, and supporting human review before authorized use.

Elicitation is one method for gathering human knowledge during this process.

### Configured consultation

A workflow explicitly defines when to consult PAVE, how to select a resource, and how to handle its contribution. It does not require a model to independently recognize the need for judgment.

### Autonomous discovery and selection

An agent independently identifies a need for external judgment and selects a relevant resource using its available tools, instructions, and permissions.

This is an optional interaction pattern, separate from configured consultation.

## Authority and source relationships

### Adoption

A person's affirmation that specific material represents their judgment within a stated scope.

Reviewing candidate material or expressing adoption intent does not, by itself, complete formal authorization for use.

### Permission to consult

Authorization for a caller to request a judgment resource's application for a specified purpose and under defined conditions.

### Permission to act

Authority to take a downstream action. The surrounding workflow retains its own decision and action controls.

Permission to consult a Lens does not grant permission to act on its contribution.

### Attribution

Identification of the human source of a judgment contribution.

Attribution does not, by itself, establish consent, compensation, endorsement, or responsibility for a final action.

### Provenance

The relationship between a representation, its source, and its derivation.

The provenance information available to a caller depends on permitted access. A reference does not automatically expose private source records.

### Direct human review

A person participates directly in reviewing a particular decision or unresolved case.

Consulting a Lens applies represented judgment within its limits. It does not mean the source person reviewed or endorsed that particular result.

### Review request

A request for further review when a consultation cannot proceed or conclude under the applicable scope and authority.

A review request is distinct from a completed judgment result and an integration failure.

## Relationship to UDIF

[UDIF — Universal Data Interchange Format](https://github.com/Universal-Data-Interchange-Format/udif) provides an open format for portable data and context.

UDIF and PAVE are separate technologies with distinct purposes, ownership, and licensing.

- **UDIF** is personally owned and independently maintained by Angela Benton. Its Apache License 2.0 materials can be used under that license.
- **PAVE** is proprietary technology owned by FRUIT Holdings, Inc.

Using UDIF's published GHI interchange schema does not, by itself, require a PAVE agreement or provide an executable PAVE Lens.

Use of UDIF is not, by itself, an implementation of PAVE.

## Further reading

- [Architecture](architecture.md) — how components, operations, and permissions fit together.
- [Examples](examples.md) — proposed applications of represented judgment.
- [Licensing](licensing.md) — access, material permissions, and contributor rights.
- [Publication history](history.md) — earlier schemas and retired materials.