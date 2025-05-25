---
roles: 
  - Builder
theme:
  - Develop
usability-dimension:
  - Effective
workstream:
  - processing-assessment
page-state:
  - discovery
season-target:
---

![[Pasted image 20250509111611.png]]

The system can sometimes generate peak processing results that are clearly wrong. This leads to user distrust. Examples are:
* long tails
* nessie situation
* step function peak
* oscillating peak

We need a way to flag using an intrinsic (not custom rules) rule to ensure the end user knows that we don't think its okay and is not acceptable.

This lives at the data quality core flag level.

Ideas:
* No visualization
* Flag to an action
* Not reportable
* Show raw data (smoothing may have been the problem)