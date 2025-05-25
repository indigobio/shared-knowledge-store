---
roles: 
theme:
  - Audit
usability-dimension:
  - Effective
  - Efficient
  - Easy to learm
workstream:
  - workflow
page-state:
  - discovery
  - definition
  - design
season-target:
  - season-11
---
#### Next steps
* [ ] iterate on excel prototype. review with Jim / Quest lighthouse partner
* [ ] downselect initiation method by a criteria. Develop the criteria...most usable? ui subsystem we intend to enhance and need to be thinking about an overhaul anyway. review with Tim / Parhkurst / Cody

#### Overview
Provide a mechanism to generate a sample-centric report to be used in a court of law to provide a defensible audit history of sample processing. 

This same report could be utilized by clinical labs to report a per determination basis. Many times a sample may be prepped, processed, and measured on more than what was ordered by the doctor due to lab batch processing efficiency. In this case, they want a simplified report of just what was ordered to go back to the doctor.

The report needs to be capable of documenting the full provenance of a determination. However, it is desirable to offer varying degrees of detail in the report to support legal, doctor usability, or audit scenarios of showing "just enough", with the ability to report more detail if the legal or audit digging ensues.

Report must print well. Paper is status-quo in this space. 

This report serves 2 needs:
* printable proxy for a view they don't have in ASCENT
* provides something procedurally operators can sign
#### Background
###### Current State 
* Cherry pick the right things from the ASCENT's archive pdf
	* calibration
	* QC
	* sample page
	* audit trail reduced that impact the compound
* Screen capture artifacts as needed to support their SOP from the enhanced review
	* compound tab
	* determination with chat open. Archive has similar info as the determination scope, but they like the determination scope because it is more familiar in layout and plot rendering. They have to defend in a court of law and therefore want the familiar artifacts.
	* cal / qc
* Add a cover sheet.

Litigation workflow is a 2nd (or 3rd) pass similar to review. The lens of the workflow is legal and procedural. Forensic cases do not allow the review by exception workflow. Therefore, the current state for this use case is to hand-craft the report described above, print it out, review each page, and wet sign each page to have a proper paper trail. 
###### Q&A

| Question                                                         | Answers                                                                                                                                                                                                             |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| How deep do you traverse the tree for provenance                 | Anything that is linked for rule determination, RT influencing, or quantitation is fully unrolled.                                                                                                                  |
| Do we need larger thumbnails on the report than on audit report. | Maybe. It matters that the presentation of the info is familiar so the user can be confident in a court of law defending this. Currently the audit pdf looks unlike how they review it and does not meet this need. |

#### Concept

##### Season 11 Concept
* Mechanism to locate samples and gesture to create a report on a compound within the sample. User can specify level of detail to include in the report at a block level. Ideas for gesture initiation. Likely can pick one:
	* Mechanisms to locate samples and gesture to create a report. Down select ideas.
	* Extend - Search by sample name -> search box results. compound filter needed
	* Extend - Select from a batch's sample page. compound filter needed.
	* Add - from a determination page. no further filtering needed.
	* Add - New workflow from batch's "select a file to download" workflow
	* Add - New workflow from Operations | Audit
	* From a determination screen
* Report is an Excel file with proper print area and scaling set, affording a simple print to pdf or paper action. 
	* action-item Get validation from Quest on the Excel first solution.
* No cover page - Customer can put that on with their own stylistics.
* Available to all users, not hidden behind a feature flag.

Concept Feedback
* [Sample-Target-Report-iteration0.xlsx](https://indigobio-my.sharepoint.com/:x:/p/rmoschell/ERA63zHFtsNLjQ6Q46wJV9UBGogsOjdbhVLaVo2cOe2qfA?e=eg9vq4)
	* Consider how to format more like screens they are familiar with
	* Consider a mechanism to select more or less detail, coverage in traceability.
	* Filtered audit trail is the right path
	* Flattened assay structure (definitions, options, rules) is in the right direction.
		* Consider how this could be leveraged for assay comparison over time for design continuity.
	* The pain is real. Digging through a 2000+ page .pdf is tedious and error prone.

###### Known technical gaps
* Use use rappel to build a prototype.
	* Today output files don't have access to the audit & assay config.  
	* Today output files don't have access to the mechanism to render plots in the same way as the determination scopes.

##### Future
* Once certified, print a litigation package for all the positives. All analytes, some analytes, only positives, etc.
* Add workflow that forces review of e-sign and certify review of everything. Helps tier 2 forensic labs. #capability
* Add workflows to make "masking" or just what the doctor ordered first class. Helps tier 2 forensic labs. #capability
* Additional customization of reported content.

##### Alternate Ideas
* Report builder style solution
	* Rejection rationale: Not aligned with direction we desire to take AQUA. Reporting needs are vast and the market has plenty of solutions.
	 
#### References
* [[Customer Examples]]
* https://miro.com/app/board/uXjVI8A7Qng=/?share_link_id=386162369524
