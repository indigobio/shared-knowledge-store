Goal: Find a path to get TuneViz smoothly deployed for internal use cases. Candidate use cases are:

* assay config updates
	* Takeaways
		* Customers may only want to update 1 of N compounds to piece meal problems. Hypothesis: Because burden of proof of changing all is too high.
	* Problems
		* Getting data into the test site
		* Assay name collisions
		* Finding relevant test data
		* All or nothing SSC push approach adds indigo management burden.
* series 3 to 4 conversions
* new logo customers

Raw Notes from discussions with Joe Ervin. 
April 2025
#### Assay Config Updates

Updating an assay might be an easier lift than series3 to 4 update. It might give use more immediate feedback. Clients are already using the product and are already sold on it. We are trying to solve a specific assay. Examples: People in S4 that still haven't adopted Dynamic RT bias. Reason: Its a heavy lift to put new things in. 
```
We can empower CommOps with tooling to aid in assay config updates by showing the resultant numbers are within tolerance but we can reduce flagging by x%.
```
Having the tune/vis tool lowers the lift weight for CommOps. 
###### Current state:
Import to test site,  make adjustments, run batches, put together a report, show flags are still behaving accordingly. Somethings the changer can approve, sometimes its some other person/team.

Customers want to opt in for specific cases. Eg. Assay has 72 compounds they want to change only 1 to a new feature.

Anecdote: CHOP has changes that are a year old they can't make because they can't its a burden to update
###### Stumbling blocks:
Make a settings change in ACER and reupload the batch to the test site. Sometimes we do it as part of a support ticket using ASCENT batch copy.

Site Specific Content can be a tripping hazard if they have other things in flight. For some customers the test site gets overloaded with changes. Examples: CHOP - were building an assay, they needed a new result file and new set of rules. They discovered a production assay result issue that needed a production rule change. They had to alter this rule and test it with the assay. To deploy SSC to production it has to go to the test site. **Barrier: Deployments are all or none changes.** "Its a bit of a process"

```
Stumbling Blocks:
* Moving data to test sites
* All or nothing SSC deployments
```

Frequency may be lower than conversion. It doesn't show up as a project its a support ticket. It flies under the radar in CommOps process. 

Process of validation in the laboratory. Validation reports might be have a specific format due to convention or SOP. In that case they do the heavy lifting on this. Indigo helps provide the information to fill the proof. This could be a correlation / comparison study. Screenshots before and after and comparison tool. 

###### Design Transfer
CHOP has a very specific report and validation to Dr Master. Sign off and approve. Once filed they'll deploy to a production site. Then IQ to ensure that production site install is matches what was on test. This is the only lab Joe knows hows to do. 

May require SOP or work instructions and training. All on client side. Sometimes we help provide info to help build training/WI.

In other cases same person will deploy to production and approval marking in ascent is enough of an audit trail for them. 
###### Finding data
Change comes from a support ticket. If they have problem with a specific result they do the before and after of a feature. ProdSpecialists then look up data that is similar to prove that something didn't break. Work is on use to dig through the PDR. Sometimes clients will find other data. 

Uses Power BI or manually looking around data. Does not use PDR. Had never seen it.
He uses "Copy Batch to Site" to move data. Disadvantage if they are using different assays on production site and test.
If so, he does raw batch files. If so, he will upload the data as "test data" in an assay. He also looks at the raw data in the data systems.
![[Pasted image 20250423113700.png]]

#### S4 to S4 Updates
Moving from 3 to 4 always downloads the raw data.
PreReq: He has Instrument Client and the ChopTest Site with a "test poll" directory. It monitors. 
1. Download zip
2. Extract .zip
	1. contans raw data, csv sequence, and additional ascent files.
3. As long as the test site has the same name and instrument as in production
4. Copy/paste folder into test poll folder. 

S3 to S4 Updates
* Same as S4 to S4. With new PreReq: Assay has to be set up.
* Setup the Assay in Series 4. More:
	* RT settings
	* Peak Threshold setttings
	* Advanced settings
	* Trace options (he never uses this)
	* Labeling/naming chromatograms
* Run the converter
* Manually configure naming differences
* Modify additional settings
* Start tuning loop.
	* does the tuning work well enough if the standard peak isn't right. Once its resonabley integrating standards wlel then tune.
* "I have yet to have one that looks just like S3". Our way to calculate in S4 is different enough to know its."
* He uploads the batch to the site and then pulls the test data in. 
	* Focus on the lower calibrator to set the thresholds. 
	* Make sure its picking my internal standards.
	* He runs the data with the test batch enabled. 
	* A big reason I do the step of making sure my standards are being integrated properly is the tuner currently doesn't mess with things like smoothing, trace widths, etc that are sometimes needed to get the peaks to integrate properly. I'd rather just make sure my known references are good before running it.

#### Interview Questions
- [ ] How many are in flight?
- [x] What is the overall process?
- [x] Who puts together the report
- [ ] What are the barriers conversion?
- [x] Show me how you find data for a conversion...
- [x] Show me how you get data out for S4 import...
- [ ] Will prod specialists need to show this to customers? How do you envision the visualizations getting pushed out?