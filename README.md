# MediCloud Hospital Patient Appointment Automation System

An automated Cloud RPA workflow built using UiPath Studio to streamline patient appointment management, token generation, database updates, and email notifications for MediCloud Hospital.


## 🚀 About The Project
The **MediCloud Hospital Patient Appointment Automation System** is designed to eliminate manual administrative overhead in handling hospital appointments. By leveraging UiPath Cloud Orchestrator and Cloud Entities, the bot automatically processes patient records, assigns appointments, updates statuses, and sends customized confirmation or rescheduling emails.



## ⚠️ Problem Statement
Previously, the hospital management department handled patient appointment records manually via cloud entities. Staff members had to individually:
* Review appointment record statuses.
* Manually verify patient details and assign token numbers.
* Dispatch separate hospital email notifications for new bookings or reschedules.

This manual procedure was repetitive, time-consuming, and prone to administrative delays in delivering critical patient updates.



## 💡 Solution Workflow
The developed UiPath Cloud RPA solution automates the end-to-end appointment lifecycle:
1. **Data Retrieval:** Automatically queries patient records from the cloud data service (`PatientAppointments` entity scope).
2. **Iterative Processing:** Parses through records using a `For Each` loop.
3. **Status Validation & Logging:** Evaluates appointment statuses using conditional logic (`If` activity) and logs execution details.
4. **Automated Communications:** 
   * **New Bookings:** Updates record status and instantly dispatches an automated appointment confirmation email with assigned token details.
   * **Rescheduling:** Handles notice dispatches for updated schedules.
5. **Record Maintenance:** Automatically cleans up processed records from the active queue using `Delete Entity Record`.



## 🛠️ Tech Stack & Tools
* **RPA Platform:** UiPath Studio Cloud (Cross-platform compatibility)
* **Cloud Orchestration:** UiPath Cloud Orchestrator (Serverless execution)
* **Data Storage:** UiPath Cloud Data Service / Cloud Entities (`PatientAppointments`)
* **Integrations:** Gmail Integration (for automated patient emails)
* **Version Control:** Git & GitHub



## ⚙️ Workflow Implementation, Variables, & Activities

### Activities Used:
* **Query Entity Records:** Fetches patient appointment entries from the cloud entity scope.
* **For Each (`currentPatientAppointments`):** Iterates sequentially through retrieved patient appointment records.
* **Log Message:** Logs tracking information for auditing.
* **If:** Routes execution based on appointment status (`"new"` condition).
* **Update Entity Record:** Updates status fields inside the cloud database.
* **Send Email:** Dispatches dynamic booking confirmation or rescheduling notices.
* **Delete Entity Record:** Purges processed entries from the active pipeline.

### Key Variables:
* `outputRecords`: Holds raw tabular/entity data fetched from the cloud source.
* `currentPatientAppointments`: Stores the current patient's record during loop iteration.
* `PatientName`: Captures the name of the patient dynamically.
* `Email`: Stores the recipient patient's email address.
* `TokenNumber`: Holds the assigned appointment token code.
* `AppointmentDate`: Stores the scheduled date and timestamp.
* `DoctorName`: Captures the assigned doctor's name.



## ☁️ Deployment & GitHub
* **Deployment:** Published and deployed successfully to UiPath Cloud Orchestrator under `My Workspace/CIA 3 PROJECT MEDIFLOW CLOUD` (v1.0.0) with successful serverless test job executions.
* **Version Control:** Project source code version-controlled and pushed to GitHub for release management and backup.




* **Class:** 3BCA B
* **Registration Number:** 25215133
* **Institution:** CHRIST (Deemed to be University)
