# BPMN Process Modeling Assignment

## Overview

This repository contains BPMN process models created using **Camunda Modeler**.

The assignment consists of three business process scenarios:

1. Employee Leave Approval
2. Online Purchase Order Processing
3. IT Service Request

The models are created using the basic BPMN building blocks required for the assignment:

* Start Event
* Tasks
* Exclusive Gateways
* Sequence Flows
* End Events

---

## Scenario 1: Employee Leave Approval

This process models how an employee's leave request is handled by the HR system.

The system checks the employee's leave balance. If sufficient leave is available, the request is sent to the manager for approval. Based on the manager's decision, the system either updates the leave balance and sends an approval notification or sends a rejection notification.

If there is insufficient leave balance, the system sends an insufficient-balance notification.

**Folder:** `Scenario-1-Employee-Leave/`

**BPMN Model:** `employee_leave_approval.bpmn`

---

## Scenario 2: Online Purchase Order Processing

This process models the processing of an online customer order.

The system first checks product availability. If the product is unavailable, the customer receives an out-of-stock notification and the process ends.

If the product is available, payment is processed. A successful payment leads to order confirmation, product preparation, shipment, and a shipping confirmation. If payment fails, the customer receives a payment-failure notification and the process ends.

**Folder:** `Scenario-2-Online-Purchase/`

**BPMN Model:** `online_purchase_order.bpmn`

---

## Scenario 3: IT Service Request

This process models how an employee's IT support request is handled.

The help desk registers the request and checks the problem severity. Low-severity problems are assigned to a support technician, while high-severity problems are assigned to a senior technician.

The technician investigates the problem. If it can be resolved internally, the technician fixes it. Otherwise, the problem is escalated to an external service provider.

Afterward, the help desk updates the request status and sends a resolution notification to the employee.

**Folder:** `Scenario-3-IT-Service/`

**BPMN Model:** `it_service_request.bpmn`

---

## BPMN Elements Used

| BPMN Element      | Purpose                                           |
| ----------------- | ------------------------------------------------- |
| Start Event       | Indicates the beginning of the process            |
| Task              | Represents an activity or action                  |
| Exclusive Gateway | Represents a decision with alternative paths      |
| Sequence Flow     | Connects BPMN elements and shows the process flow |
| End Event         | Indicates the completion of a process path        |

---

## Tool Used

**Camunda Modeler**

All BPMN diagrams are created and saved as `.bpmn` files so that they can be opened and evaluated using Camunda Modeler.

---

## Repository Structure

```text
BPMN-Process-Modeling/
│
├── README.md
│
├── Scenario-1-Employee-Leave/
│   ├── employee_leave_approval.bpmn
│   └── explanation.md
│
├── Scenario-2-Online-Purchase/
│   ├── online_purchase_order.bpmn
│   └── explanation.md
│
└── Scenario-3-IT-Service/
    ├── it_service_request.bpmn
    └── explanation.md
```

---

## Verification

The BPMN models are checked to ensure that:

* The process starts with a Start Event.
* All activities are represented using Tasks.
* Decision points use Exclusive Gateways.
* Alternative process paths are clearly represented.
* Sequence Flows correctly connect the process elements.
* Every process path reaches an End Event.
* The diagrams are readable and logically correct.
* The `.bpmn` files can be opened in Camunda Modeler.
