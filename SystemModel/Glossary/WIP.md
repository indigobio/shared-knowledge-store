
This is a file of unprocessed, uncurated definitions.

TRI
SNR - Signal to noise ratio Ours is different than others. Capture that intent.
IBF - list of samples that are part of a run. Run list

* ORDER - Orders represent the request for a test result to be provided for a particular sample ID. A sample may require more than one result to be generated before the order can be satisfied. Order information originates from LIS information or from operator input.
	* When anorder is created, it is in the Ordered state. After preparing, it is in the Prepared state. After measuring and assessing, it is in the Measured and then Assessed state. Once the user reviews the order, it is in the Reviewed state. Once the order is certified by the user, it is in the Certified state. Anorder can bemarkedasclosedorasarerunbytheuser. If marked as closed, the order will be in the Closed state where it will remain until another order for the same test and sample ID is created. If marked as rerun the current order is closed and then a new one is created in the Ordered state.
* Order status - The order status is separate from the test status and one order may have multiple tests recorded against it before being satisfied.
* Test status - The order status is separate from the test status and one order may have multiple tests recorded against it before being satisfied.
* Prepared Samples
* test result - A test result is the fully assessed result including any monoclonal observations as described in the design inputs, the trace and peak data, along with the full provenance of how the test was performed.
* Raw data
* Data Analysis Pipeline
* Measurements
* Users
* Roles
* Samples
* Reagents
* Quality control certificates - are barcodes associated with one or more reagent barcodes
* audit records
* sample - Each sample is required to have a unique barcode that represents a specific aliquot of a patient who is undergoing the lab test.
* labware
* MALDI plates
* lot numbers 
* aliquot
* Results - Results are the outcomes of a test for a particular patient sample that have been approved by a reviewer. They can consist of qualitative or quantitative outcomes as well as any comments. 
* Tecan
	* run- an instance of invoking a Tecan run definition via a Tecan method or script 
	* run definition- a named procedure that can be invoked on the instrument via a method or script
	* maintenance run- a run with the objective of tuning or cleaning the instrument to keep its performance within specification
	* preparation run- a run with the objective of preparing samples for a lab test (e.g. multiple myeloma) of which the Exent IQ system supports
	* method- Tecan FluentControl concept for a top-level, runnable procedure that then invokes one or more scripts
	* script- Tecan FluentControl concept for a procedure that invokes instrument commands or other scripts*
* pending work
	* Orders that have not yet been prepared 
	* Prepared plates that have not been read by the mass spectrometer 
	* Results that are not yet reviewed 
	* Reviewed results that are not yet released
- Model
	- Assay
		- Revisions
			- Revision
				- Assay Settings
					- Target
				- Methods
					- Prep
					- Acquisition
		- Assay Stats
	- Sample Set (Batch, Calibration Set, etc)
		- Target
			- Set Stats
	- Sample
		- Target Result
			- Measurements
				- Measurement - Trace
					- Features (Derived Measurements?)
						- Values - Dictionary
						- Peaks
							- Peak
								- Names/Labels
								- ...
								- Estimated
									- RT
									- Area
								- Modeled
									- Type
									- RT
									- Area
									- ...
						- Traces
							- Trace
								- Names/Labels (ie.Baseline)
				- Measurement - Dictionary
					- Source - LIS/File/etc
				- Measurement - Target Ref
				- Measurement - Ref
			- Annotations/Observations
		- Model 2
			- Measurement
				- Labels
				- Type - Trace, Dictionary
				- Direct/Derived?
				- Sample
				- Features - Measurements from Features
					- Values
					- Peaks
					- Traces





* ![[Pasted image 20250331074307.png]]