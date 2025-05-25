---
roles:
  - Compliance Officer
  - Lab Leader
theme:
  - Audit
  - Production
workstream:
  - lab-assay-workflow
---
As a [[Lab Leader]] or [[Compliance Officer]], I need the system to track actions and create an exportable reports to use as artifacts to maintain regulatory compliance.

Regulations:
* Each state has their own regulations. NY is the most stringent. FDA's now paused LDT push had planned to accept NY's LDTs because the regulations were similar.
* CAP Clinical
* CAP FDT (forensic drug test)
	* https://documents-cloud.cap.org/appsuite/learning/LAP/TLTM/resources/standards/FDTstandards.pdf
	* https://www.cap.org/laboratory-improvement/accreditation/inspection-tools-and-training
	
On what...
* Users
* Methods
	* [[Traceable changes]] 
* Batches
	*
* Samples
	*  [[Generate sample-target report (Litigation, Clinical)]]
* Quality Controls
* Outputs

#### AQ Supporting Features:
* Chat
* Batch Audit Log (html)
* Batch Archive (.pdf)
* Assay Settings Comparison Report (.html)
* Assay Settings (.csv, .html)

A-Ha
* Users
	* AQ-16
	* AQ-369
* QC
	* AQ-292 [[QC Monitoring]]
* Lab
	* AQ-23
* Batch
	* AQ-35
	* AQ-121
	* AQ-322
	* AQ-253
* Assay
	* AQ-98
	* AQ-151 [[Assay Audit Artifacts]]
* AQ-267 [[Data Findability]]
* Environment
	* AQ-337
	* AQ-118
	* AQ-98