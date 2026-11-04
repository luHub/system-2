# Builder-on

**An open supply network for discovering projects, suppliers, providers, and opportunities to cooperate.**

Builder-on makes productive opportunities visible and helps independent participants find one another.

It is designed to operate with minimal infrastructure: a public Git repository, GitHub Pages, structured JSON records, and pull requests.

> **Open participation without centralized permission.** Any registered supplier or provider may discover an open project and propose cooperation. The project owner remains free to accept or decline. Builder-on makes opportunities visible. Participants decide what happens next.

---

## 1. Why Builder-on?

Many productive projects require a combination of materials, products, services, skills, and coordination.

Finding the right participants can be difficult when information is scattered across separate networks or controlled by centralized platforms.

Builder-on provides a simple, open directory where:

- Projects can publish their goals and requirements.
- Suppliers can describe the products, materials, and resources they offer.
- Providers can describe their services, skills, and capabilities.
- Participants can discover open projects and independently propose involvement.
- Mutually declared relationships can be recorded transparently.

Builder-on does not attempt to manage the project itself. It provides the information and contact channels needed for participants to coordinate independently.

## 2. Design Principles

### Open discovery

Public project, supplier, and provider records can be browsed without requiring an account or platform membership.

### Open participation

Any registered supplier or provider may propose participation in any open project. An invitation from the project owner is not required.

### Independent decisions

Project owners and participants decide whether to cooperate. Builder-on does not approve, assign, or guarantee commercial relationships.

### Minimal infrastructure

The initial implementation uses:

- GitHub repository
- GitHub Pages
- Static HTML
- JSON records
- Pull requests for modifications

No application backend, database, or paid infrastructure is required for the initial version.

### Transparent records

Changes are submitted through pull requests and reviewed before they become part of the public repository.

### Clear responsibility boundaries

Builder-on provides discovery and contact channels. Participants remain responsible for their own negotiations, agreements, transactions, and execution.

## 3. Network Entities

Builder-on uses five core record types.

| Entity | ID format | Purpose |
|---|---|---|
| Project | `BO-P-NNNN` | A productive initiative with goals and requirements |
| Supplier | `BO-S-NNNN` | An organization or individual offering products, materials, or resources |
| Provider | `BO-V-NNNN` | An organization or individual offering services, skills, or execution |
| Participation | `BO-I-NNNN` | A proposal to participate in an open project |
| Relationship | `BO-R-NNNN` | A relationship declared by the relevant participants |

### Projects

A project describes what is being built, developed, or delivered.

A project record may include:

- Name and description
- Status
- Location
- Categories
- Requirements
- Contact information

Projects may be marked as:

`draft` · `open` · `in-progress` · `completed` · `suspended` · `withdrawn`

### Suppliers

A supplier describes products, materials, equipment, or other resources it can provide.

A supplier record may include:

- Name and description
- Categories
- Location
- Capabilities
- Contact information
- Status

### Providers

A provider describes services, expertise, or execution capabilities.

A provider record may include:

- Name and description
- Categories
- Location
- Capabilities
- Contact information
- Status

### Participation

A participation record expresses interest in contributing to a project.

Any registered supplier or provider may submit a proposal for an open project without waiting for an invitation.

A proposal is **not**:

- A contract
- A commitment to deliver
- An exclusive arrangement
- An endorsement by Builder-on
- Evidence that the project owner has accepted

Participation statuses:

`proposed` · `acknowledged` · `discussing` · `accepted` · `declined` · `withdrawn`

Acceptance should only be represented when the relevant parties have independently declared their agreement.

### Relationships

A relationship record describes an association between a project, supplier, and provider.

A relationship is distinct from a unilateral participation proposal. It should only be represented as mutually declared when the relevant parties have confirmed the association.

## 4. Repository Structure

```text
builder-on/
│
├── index.html
│
├── data/
│   ├── projects/
│   ├── suppliers/
│   ├── providers/
│   ├── participation/
│   └── relationships/
│
├── schemas/
│   ├── project.schema.json
│   ├── supplier.schema.json
│   ├── provider.schema.json
│   ├── participation.schema.json
│   └── relationship.schema.json
│
├── templates/
│   ├── project.template.json
│   ├── supplier.template.json
│   ├── provider.template.json
│   ├── participation.template.json
│   └── relationship.template.json
│
├── docs/
│   ├── GOVERNANCE.md
│   ├── PARTICIPATION.md
│   ├── RESPONSIBILITY.md
│   └── CONTRIBUTING.md
│
└── .github/
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```

`index.html` is the static website interface. The JSON files in `data/` are the public source of truth for network records.

## 5. How It Works

```text
Publish a project
       │
       ▼
Project becomes discoverable
       │
       ▼
Supplier or provider finds the project
       │
       ▼
Participant submits a participation proposal
       │
       ▼
Proposal is reviewed and published
       │
       ▼
Project owner and participant contact one another
       │
       ▼
They negotiate independently
       │
       ▼
If mutually agreed, a relationship may be declared
       │
       ▼
Participants execute their work independently
```

Builder-on does not need to be involved in the commercial or operational relationship after providing discovery and contact channels.

## 6. Contributing

All modifications to the public network are submitted through pull requests.

Contributors may propose to:

- Add a project
- Update a project
- Add a supplier
- Add a provider
- Propose participation in an open project
- Update or withdraw a participation proposal
- Add or update a mutually declared relationship

### Contributor declarations

By submitting a record, contributors confirm that:

- They are authorized to submit the information.
- The information is accurate to the best of their knowledge.
- Public contact details are intentionally provided.
- No confidential information is included.
- They understand Builder-on's responsibility boundaries.

### Review

Submissions should be checked for:

- Valid JSON structure
- Correct record type and ID format
- Unique IDs
- Required fields
- Valid statuses
- Existing referenced records
- Open project status for new participation proposals
- Appropriate declarations for accepted participation or relationships
- No unsupported claims of endorsement, acceptance, or certification

A repository maintainer's merge of a pull request is **not** evidence of a commercial agreement between participants.

## 7. Responsibility Boundaries

Builder-on is a discovery and coordination directory.

Builder-on is responsible for:

- Publishing public records
- Maintaining the repository and website
- Reviewing proposed changes
- Providing discovery and contact channels

Participants are responsible for:

- Verifying one another
- Negotiating terms
- Establishing contracts or other agreements
- Payments and financial arrangements
- Delivery, quality, and execution
- Legal and regulatory compliance
- Managing disagreements and disputes

A record in Builder-on does not constitute verification, certification, endorsement, or a guarantee.

## 8. Future Development

The initial version focuses on projects, suppliers, providers, participation, and relationships.

Additional directories may be introduced when useful, including:

- Legal services
- Finance
- Logistics
- Insurance
- Certification
- Technical infrastructure

Future additions should preserve the core principles: open discovery, independent decisions, minimal infrastructure, and clear responsibility boundaries.

## 9. Governing Principle

> **Builder-on makes opportunity visible. Participants decide what happens next.**

Open participation without centralized permission. Any registered supplier or provider may discover an open project and propose cooperation. The project owner remains free to accept or decline.

Builder-on is not the owner of the projects, the participants, or their agreements. It is the open structure through which they can find one another.

## 10. Status

- **Version:** 0.1
- **Implementation:** Static GitHub Pages website
- **Data:** Public JSON records in the repository
- **Modification workflow:** Pull requests
- **Backend:** None
- **Database:** None
- **Paid infrastructure:** None
