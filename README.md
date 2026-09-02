# PROPFlow AI — Salesforce Real Estate CRM

> A Salesforce-based Real Estate CRM for managing properties, property units, customer requirements, bookings, and sales processes.

## 📌 Overview

PROPFlow AI is a Salesforce CRM project designed around a real-estate business use case.

The project focuses on building a realistic Salesforce application using **Salesforce DX, custom objects, security configuration, and declarative automation with Flow**.

The application is being developed incrementally, with future plans to explore Apex, Lightning Web Components, integrations, testing, DevOps, and Salesforce AI capabilities.

---

## 🎯 Project Objectives

PROPFlow is designed to help a real-estate organization:

* Manage properties and individual property units
* Manage customer property requirements
* Track property availability
* Manage property bookings
* Automate property-unit status changes
* Control access based on business roles
* Build a scalable Salesforce DX project structure
* Explore Salesforce development and AI capabilities

---

## 🏗️ Current Application Architecture

```text
                  PROPFlow AI
                       │
        ┌──────────────┼──────────────┐
        │              │              │
     Property      Customer       Property
                    Requirement      Unit
        │                             │
        └──────────────┬──────────────┘
                       │
                    Booking
                       │
                       ▼
              Salesforce Flow
                       │
          ┌────────────┼────────────┐
          │            │            │
       Reserved       Sold       Available
```

---

# 🧩 Salesforce Data Model

The current project includes the following custom objects:

### Property

Represents a real-estate property or project.

### Property Unit

Represents an individual unit associated with a property.

### Property Requirement

Stores customer requirements related to property searches.

### Booking

Represents a customer's booking of a property unit.

---

# ⚙️ Automation

Salesforce Flow is used to automate the property and booking lifecycle.

### Property → Property Unit

When a new Property is created, the automation creates the required Property Unit record and sets its initial status to **Available**.

```text
Property Created
       ↓
Property Unit Created
       ↓
Status = Available
```

### Booking Lifecycle

The project also automates property-unit availability based on booking status.

```text
Booking Created
       ↓
Property Unit = Reserved
       ↓
Booking Confirmed
       ↓
Property Unit = Sold
```

If a booking is cancelled:

```text
Booking Cancelled
       ↓
Property Unit = Available
```

### Implemented Flows

* Create Property Units
* Reserve Property Unit
* Confirm Booking / Sell Unit
* Cancel Booking / Release Unit

These flows have been tested as part of the current implementation.

---

# 🔐 Security & Access Control

The project includes a Salesforce security model based on different business responsibilities.

### Permission Sets

* PROPFlow Sales User
* PROPFlow Sales Manager
* PROPFlow Property Manager
* PROPFlow Finance User
* PROPFlow Support User

### Role Hierarchy

A role hierarchy has been configured to represent sales-management relationships and access.

The project currently demonstrates concepts including:

* Permission Sets
* Role Hierarchy
* Object-level access
* Field-level access
* Record-level security concepts

---

# 🛠️ Salesforce DX

PROPFlow follows a Salesforce DX source-driven project structure.

```text
PROPFlow-AI-Salesforce/
│
├── force-app/
│   └── main/
│       └── default/
│           ├── objects/
│           ├── flows/
│           └── permissionsets/
│
├── config/
├── scripts/
├── .gitignore
├── sfdx-project.json
├── package.json
└── README.md
```

The project is maintained using Git and GitHub so Salesforce metadata can be tracked as source code.

---

# 🔄 Development Workflow

```text
Salesforce Org
      ↕
Salesforce CLI
      ↕
VS Code
      ↕
Salesforce DX Project
      ↕
Git
      ↕
GitHub
```

---

# Development Progress

### Day 1 — Core Data Model

* [x] Salesforce DX project setup
* [x] Property object
* [x] Property Requirement object
* [x] Property Unit object
* [x] Core real-estate data model

### Day 2 — Security

* [x] Permission Sets
* [x] Role hierarchy
* [x] Sales access model
* [x] Property management access
* [x] Finance access
* [x] Support access

### Day 3 — Automation

* [x] Property → Property Unit automation
* [x] Booking → Reserved automation
* [x] Confirmed Booking → Sold automation
* [x] Cancelled Booking → Available automation
* [x] End-to-end Flow testing

### Upcoming Development

* [ ] Apex
* [ ] SOQL
* [ ] Triggers
* [ ] Apex Test Classes
* [ ] Lightning Web Components
* [ ] Reports & Dashboards
* [ ] API / Integration concepts
* [ ] Advanced Salesforce development
* [ ] Salesforce AI capabilities

---

# 📊 Current Status

**Project Status:** 🚧 In Development

### Completed

* Salesforce DX project setup
* Real-estate data model
* Custom objects
* Permission Sets
* Role hierarchy
* Security foundation
* Property Unit automation
* Booking lifecycle automation
* Flow testing

### Currently Working On

**Apex + SOQL + Triggers**

---

# 🎓 Salesforce Concepts Demonstrated

The current implementation demonstrates:

* Salesforce DX
* Custom Objects
* Data Modeling
* Permission Sets
* Role Hierarchy
* Salesforce Security
* Record-Triggered Flow
* Business Process Automation
* Git/GitHub
* Source-driven development

Future development will expand the project toward Salesforce development and AI capabilities.

---

# 👨‍💻 Author

**Ayush Mehunkar**

MCA Student | Salesforce Administration & Development

GitHub: **ayush11-ayu**

---

## 📄 Disclaimer

This is an educational portfolio project created to demonstrate Salesforce administration, automation, development, and source-driven development concepts through a realistic real-estate CRM use case.
