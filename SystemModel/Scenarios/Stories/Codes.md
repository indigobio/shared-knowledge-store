---
roles:
  - Builder
  - Operator
theme:
  - Develop
  - Production
usability-dimension:
  - Efficient
  - Effective
workstream:
  - lab-assay-workflow
  - review-workflow
page-state:
  - discovery
  - definition
season:
---

### Free Text:
Dropdown support in the Code field should have an option to exclude "free text" editing. To support ASCENT methods in the field where this may be already available be in use. 

Over time, we could perform usage analytics to determine if we can remove the "free-text" option all together.

### 
Several clients have requested us to continue the enhancement of the disposition options, in particular, the Code and Decision fields, building on the customizable Decision terms and pre-populated Code list with the scrollable dropdown which have been provided in Series 4 as already better than Series 3:

- Decision to be definable by sample type (e.g. Standard and QC samples are rarely set to Repeat; Exclude is overloaded in an operator's perspective as excluding from a curve versus excluding a result from being emitted).
    
- subset by decision (e.g. a Code which goes with Repeat could be different than a code which goes with Accept, and a superset list of all codes could get cumbersome)
    
- subset by sample type (e.g. a Code for a QC sample could be different than a code for an Unknown, and a superset list of all codes could get cumbersome)
    
- subset by rule type (e.g. only certain Codes should be allowed for a certain flag)
    
- multiple Code values (e.g. click multi-select; use a 'pill' to show multiple Codes)
    
- show code as "PC - possible carryover" in the dropdown, but only put "PC" in the Code field; then build up the list using multi-select
    

provide option to disallow manual entry; provide means by which a missing code is not allowed

provide mechanism to allow multiple pre-defined codes to be entered. as one possible approach, specify that a custom Code must consist of an "abbreviation" and a "definition"; selection is made in the dropdown of "abbreviation-definition", but after selection, what remains is only the "abbrevation" (e.g. a small rounded button, displaying the abbreviation). at this point, the Code field would allow a second dropdown operation, and so on. any existing "abbreviation" 'button' could have a little 'x' icon, so that it could be removed.

Allow auto-analysis to set both the decision and a code.


Next Steps:
* [ ] Find out the story behind multi-select concepts