# PROPFlow AI — Project Context

## Project Name

PROPFlow AI

## Project Description

AI-Powered Real Estate CRM, Property Sales & Customer Management Platform.

PROPFlow AI is an enterprise-style Salesforce portfolio project designed to demonstrate Salesforce Administration, Development, Architecture, AI, Integration, Testing, and DevOps.

The complete project scope represents approximately 75 days of learning/building compressed into 10 intensive development days.

The 10-day schedule is a build acceleration plan, not a claim of 75 days of mastery.

---

# Project Objective

Build a realistic Salesforce platform for real-estate organizations that manages the complete customer journey:

Lead
→ Lead Qualification
→ Lead Conversion
→ Account + Contact
→ Property Requirement
→ Property Recommendation
→ Site Visit
→ Opportunity
→ Booking
→ Payment
→ Customer Support

---

# Project Principles

1. Do not fake Salesforce functionality.
2. Verify Salesforce edition, license, permission, and product requirements before claiming a feature works.
3. Clearly distinguish:
   - Working implementation
   - Prototype
   - Architecture demonstration
   - Product/license dependency
   - Future implementation
4. Do not hardcode Salesforce record IDs.
5. Never hardcode credentials or secrets.
6. Avoid SOQL inside loops.
7. Avoid DML inside loops.
8. Build bulkified Apex.
9. Keep triggers thin.
10. Prefer Flow when Flow is appropriate.
11. Prefer Apex when code complexity, transaction control, or advanced logic requires Apex.
12. Use secure Apex with appropriate sharing and CRUD/FLS considerations.
13. Use meaningful Git commits.
14. Document important architecture decisions.
15. Write meaningful tests rather than chasing code coverage.

---

# Salesforce Org

Org Type:

Developer Edition

Salesforce CLI Alias:

PROPFlowDev

Current authentication status:

Connected

---

# Development Environment

Operating System:

macOS

Salesforce CLI:

@salesforce/cli/2.148.3

Architecture:

darwin-arm64

Node:

v24.18.0

IDE:

Visual Studio Code

Version Control:

Git

Repository:

PROPFlow-AI-Salesforce

GitHub:

Remote repository configured as origin

Primary Branch:

main

---

# Current Day

Day 1

Status:

DAY 1 IN PROGRESS

---

# Day 1 Objective

Establish the technical foundation for PROPFlow AI:

- Salesforce DX project
- Git repository
- GitHub repository
- Professional project structure
- Initial Salesforce architecture
- Initial data model
- Core custom objects
- Project context documentation

---

# Salesforce DX Project Structure

Current project contains:

- force-app
- scripts
- tests
- docs
- config
- .vscode
- Salesforce DX configuration

Documentation folders:

- docs/architecture
- docs/salesforce
- docs/development
- docs/integration
- docs/ai
- docs/devops
- docs/progress

---

# Standard Salesforce Objects

PROPFlow AI will use Salesforce standard objects where appropriate.

Planned standard objects:

- Lead
- Account
- Contact
- Opportunity
- Campaign
- Case
- Task
- Event

---

# Custom Objects

The following custom objects have been created:

## Property

API Name:

Property__c

Purpose:

Stores real-estate properties/projects.

---

## Property Unit

API Name:

Property_Unit__c

Purpose:

Stores individual units belonging to a property.

---

## Property Requirement

API Name:

Property_Requirement__c

Purpose:

Stores customer property preferences and requirements.

---

## Site Visit

API Name:

Site_Visit__c

Purpose:

Stores customer property visit appointments and outcomes.

---

## Booking

API Name:

Booking__c

Purpose:

Represents a property/unit booking transaction associated with a sales opportunity.

---

## Payment

API Name:

Payment__c

Purpose:

Stores booking-related payment information.

---

## Commission

API Name:

Commission__c

Purpose:

Stores salesperson/agent commission information.

---

## Integration Log

API Name:

Integration_Log__c

Purpose:

Stores integration events, errors, statuses, and operational information.

---

# Record Naming Strategy

Property:

PROP-{0000}

Property Unit:

UNIT-{0000}

Property Requirement:

REQ-{0000}

Site Visit:

VISIT-{0000}

Booking:

BOOK-{0000}

Payment:

PAY-{0000}

Commission:

COMM-{0000}

Integration Log:

LOG-{0000}

---

# Planned Data Relationships

Initial architecture:

Account
→ Property Requirement

Account
→ Opportunity

Account
→ Booking

Account
→ Case

Contact
→ Property Requirement

Contact
→ Site Visit

Contact
→ Booking

Property
→ Property Unit

Property
→ Site Visit

Property
→ Booking

Property Unit
→ Booking

Opportunity
→ Booking

Booking
→ Payment

These relationships will be implemented deliberately after the initial object foundation.

---

# Important Architecture Decisions

## Opportunity vs Booking

Opportunity represents the sales/deal lifecycle.

Booking represents the actual property/unit reservation or transaction.

They are intentionally separate concepts.

---

# Customer Journey

Lead
→ Qualification
→ Lead Conversion
→ Account + Contact
→ Property Requirement
→ Property Matching
→ Site Visit
→ Opportunity
→ Booking
→ Payment
→ Support

---

# Planned Technical Architecture

Frontend:

Lightning Web Components

↓

Apex Controller

↓

Service Layer

↓

Selector/Data Access Layer

↓

Salesforce Data

---

# Planned Automation Architecture

Use Salesforce Flow for appropriate declarative automation.

Use Apex for:

- Complex transactional logic
- Advanced validation
- Bulk processing
- Integration logic
- Complex business rules
- Asynchronous processing

Triggers should remain thin.

Target architecture:

Trigger
→ Trigger Handler
→ Service Layer
→ Selector Layer

---

# Planned AI Features

1. AI/algorithm-assisted Lead Scoring

Inputs:

- Budget
- Location
- Timeline
- Lead Source
- Engagement
- Activities

Output:

- Score
- Classification
- Reasoning

2. Property Recommendation

Input:

Customer Requirement

Output:

- Ranked properties
- Match percentage
- Match reasoning

3. Opportunity/Deal Risk

Output:

- Low
- Medium
- High

4. Opportunity Summary

AI-assisted concise sales summary.

Salesforce-native AI capabilities will only be implemented where the current Salesforce org and available products/licenses support them.

Agentforce, Data Cloud, Einstein, and other licensed capabilities must be verified before implementation.

---

# Planned Integration Architecture

Salesforce

↓

REST API

↓

External System / Mock Integration

Important concepts:

- HTTP
- JSON
- GET
- POST
- PATCH
- HttpRequest
- HttpResponse
- Named Credentials
- External Credentials
- Authentication
- Error handling

Integration errors will be recorded in:

Integration_Log__c

No credentials or secrets will be stored in source code.

---

# Planned Event Architecture

Platform Event example:

Property_Booking_Created__e

Architecture:

Booking

↓

Platform Event

↓

Subscriber

↓

Processing

Change Data Capture will be taught separately and clearly distinguished from Platform Events.

---

# Planned Security Model

Personas:

- System Administrator
- Sales Manager
- Salesperson
- Property Manager
- Finance User
- Customer Support
- Customer

Security concepts:

- Organization-Wide Defaults
- Role Hierarchy
- Profiles
- Permission Sets
- Permission Set Groups
- CRUD
- Field-Level Security
- Sharing Rules
- Record Ownership
- Apex with sharing
- Apex security
- Security review

Permissions should follow least privilege.

---

# Planned DevOps Architecture

Source control:

Git

Repository:

GitHub

Development:

Salesforce DX

IDE:

VS Code

CI/CD:

GitHub Actions

Analysis:

Salesforce Code Analyzer

Potential Salesforce DevOps Center:

Use if available in the org.

Fallback:

GitHub + Salesforce CLI.

---

# Planned 10-Day Roadmap

## Day 1

Architecture
Salesforce DX
Git/GitHub
Data Model
Custom Objects
ERD Foundation

## Day 2

Security
Profiles
Permission Sets
OWD
Roles
Sharing
Sales Cloud
Service Cloud

## Day 3

Property Management
Requirements
Site Visits
Bookings
Payments
Validation Rules
Record Types
Flow Automation

## Day 4

Apex Fundamentals
SOQL
SOSL
DML
Collections
Governor Limits
Bulkification
Service Layer
Selector Layer
Trigger Framework

## Day 5

Advanced Apex
Triggers
Queueable
Batch
Scheduled Apex
Platform Events
CDC
REST Integration
Named Credentials

## Day 6

Lightning Web Components
Property Search
Property Cards
Property Details
Site Visits
Booking
LWC/Apex Communication
LDS
Events

## Day 7

AI
Lead Scoring
Property Matching
Deal Risk
AI Summaries
Agentforce Evaluation

## Day 8

Experience Cloud where supported
Service Cloud
Cases
Knowledge
Customer Journey
Customer-facing LWC fallback

## Day 9

Testing
Test Data Factory
Apex Tests
Bulk Tests
Callout Mocks
LWC Jest
Security Review
Performance Review
Error Handling

## Day 10

GitHub
CI/CD
GitHub Actions
Salesforce Code Analyzer
DevOps Center Concepts
Reports
Dashboards
Documentation
Architecture Diagrams
README
Demo
Portfolio
Interview Preparation
Productization Roadmap

---

# Day 1 Current Status

Completed:

- Salesforce DX project created
- Salesforce CLI verified
- Salesforce org authenticated
- PROPFlowDev alias connected
- Git initialized
- GitHub repository connected
- Main branch configured
- Initial Git commit created
- Professional project directory structure created
- Property__c created
- Property_Unit__c created
- Property_Requirement__c created
- Site_Visit__c created
- Booking__c created
- Payment__c created
- Commission__c created
- Integration_Log__c created
- Initial architecture defined

Remaining Day 1 task:

- Save this project context file
- Commit and push project context
- Final Day 1 verification

---

# Previous Known Salesforce Issue

A previous Salesforce CLI authentication attempt encountered an API-disabled error.

If a similar error occurs again:

1. Capture the exact error.
2. Verify the Salesforce user and permissions.
3. Verify API access.
4. Verify org authentication.
5. Diagnose the actual cause.
6. Do not randomly reinstall or change unrelated configuration.

---

# Current Git State

Initial commit:

chore: initialize PROPFlow AI Salesforce DX project

A second documentation commit will be created after this file is saved.

---

# Future Chat Continuation Rule

If the current ChatGPT conversation reaches its context limit:

Start a new conversation.

Upload:

PROJECT-CONTEXT.md

and any completed:

docs/progress/DAY-XX.md

files.

Then instruct ChatGPT:

"Continue PROPFlow AI from the current documented day. Read the uploaded project context and progress files first. Do not restart completed work."

The project files are the source of truth for implementation state.

---

# Important Development Rule

Never assume a feature works merely because it exists in the overall project architecture.

For every Salesforce feature, verify:

- Org edition
- License
- Permission
- Product availability
- Configuration
- Current Salesforce capabilities

If unavailable:

Document:

1. Why unavailable
2. Required product/license/permission
3. Closest valid alternative
4. Production architecture

---

# Day 1 Status

IN PROGRESS

Next action:

Commit PROJECT-CONTEXT.md and push to GitHub.

Next project phase:

Day 2 — Security + Sales Cloud + Service Cloud

### Known Limitation — Test Users

Two additional internal test users could not be created because the Salesforce Developer Edition has no remaining Salesforce or Salesforce Platform user licenses.

Current license availability:
- Salesforce: 2 total, 2 used, 0 remaining
- Salesforce Platform: 3 total, 3 used, 0 remaining
- Customer Community Login: 5 remaining
- External Apps Login: 20 remaining
- Identity: 10 remaining

The available Community/Identity licenses were not used as substitutes because they do not provide the same capabilities as internal Salesforce users.

Day 2 security configuration was therefore completed using the available administrator context. Additional internal-user testing can be performed later when an appropriate Salesforce/Salesforce Platform license is available.