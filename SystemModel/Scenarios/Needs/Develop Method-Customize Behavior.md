---
roles:
  - Builder
theme:
  - Develop
workstream:
  - lab-assay-workflow
  - processing-assessment
  - data
---

As a [[Builder]], I need to:
* configure the behavior of my ASCENT method.
* customize how information is presented to [[Operator]]  as part of the method development process. 

This includes the customization of:
* Numerical Processing Behavior
* Assessment Behavior
	* Create, Edit, Delete, Test
	* Share between methods
	* Management of use with assays
* Design of the Review Experience (UI, reports, etc)
	* Behavior
		* Reprocessing behavior 
		* Decision options
		* Automation options
		* [[Develop Method-Customize Behavior-Quantitation and Calibration Flexibility]]
	* UI
		* Info presented in review & certify workflow
		* Info presented in reports

#### AQ Supporting Features
* Assay Config Interface (chromatogram defn, rules, reports)
* SSC
#### A-Ha
* Numerical Processing
	* AQ-328
	* AQ-367 [[Processing Behavior]]
	* AQ-110 [[Processing Behavior]]
	* AQ-295 Designated reference sample/compound/determination [[Processing Behavior]]
	* AQ-294 Add maximum intensity in trace to processed peak results [[Processing Behavior]]
	* AQ-270 Remove/rename Equable peak model [[Processing Behavior]]
	* AQ-271 TRI - use internal standard to delimit analyte [[Processing Behavior]]
	* AQ-269 Peak integration from calculated baseline [[Processing Behavior]]
	* AQ-247 Quantification options [[Processing Behavior]]
	* ASC-787 Calibration improvements
	* ARQ ONLY
		* AQ-13 Sigmoid processing - reference Ct threshold
		* AQ-259 ARQ OpenArray
* Assessment Behavior
	* AQ-304 [[Rules Usability]]
	* AQ-296 [[Rules Usability]]
	* AQ-298 [[Rules Usability]]
	* AQ-265 [[Rules Usability]]
	* AQ-117 [[Rules Usability]]
	* AQ-116 [[Rules Usability]]
	* AQ-263 [[Rules Scope]] [[SystemModel/Scenarios/Stories/Manual Peak Modification|Manual Peak Modification]]
	* AQ-97 [[Rules Scope]]
	* AQ-26 core-pcr rules in ARQ to be handled as are core-1 and core-2 in ASCENT 
	* AQ-64
	* AQ-165
	* AQ-297 Expose baseline equation values to rules system [[Rules Scope]]
* Calibration
	* AQ-315
* Review Experience
	* AQ-165
	* AQ-361
	* AQ-237
	* AQ-366
	* AQ-112 [[Codes]]
	* AQ-68 [[Codes]]
	* AQ-166 [[Codes]]
	* AQ-288
	* AQ-156 [[QC Monitoring]]
	* AQ-18 Peak Area bar for Calibration and QC perspectives
	* AQ-143 Extend SSC/ASC approach to qualitative results
* Reports
	* AQ-794
	* AQ-169