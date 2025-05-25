---
roles: 
  - Builder
theme:
  - Develop
usability-dimension:
  - Efficient
  - Easy to learn
workstream:
  - lab-assay-workflow
page-state:
  - discover
  - definition-design
season-target:

---

commentary about our latest ideas with links to miro or git or figma

## Current State Challenges
1. **Configuring rules** is tedious. It requires a lot of keyboard/mouse interactions:
	1. Select a rule 
	2. Configure rule settings
	3. Enable and configure per-compound rule settings.
	To compensate, frequently customers start with a multi-compound assay, save a copy, and edit the copy. This also has the benefit of propagating compound renaming throughout the rules.
2. **Adding a compound** to an ASCENT method requires configuring the per-compound rule settings for the new compound. 
3. **Scoping a rule** to a *sample type* or *compound type* is tedious. It requires either multiple near-identical rules or a parameterization of a rules.

The people in the lab responsible for rules/assessment configuration may be different than the those responsible for numerical processing configuration. Blending workflows together in the ASCENT method notion make it challenging in this occasional scenario.
## Desired Future State
1. Rules are efficient to configure from scratch. Ability to modify a class of things at the same time, e.g Edit all IS or all analytes
	1. Use case for #trace-relationships 
2. Rules are efficient to configure when adding compounds to an ASCENT method
3. Rules can be scoped CompoundType and SampleType to reduce the number needed. 
	1. CompoundType example: compound X needs a tighter tolerance
	2. SampleType example: IS need a tighter tolerance than unknown
4. Rules can be managed (configured, deployed) lab wide and overwritten at an ASCENT method level to aid with lab level consistency.
## Potential Solution:
* Add an abstraction layer between SSC and ASC to handle Rules to allow configuration of lab level rules.
	* Override per Compound, CompoundType, SampleType, or a combination of them.
* Add scope filter to rules: CompoundType, SampleType
* Improve Rules editor within the ASCENT Method UI
	* To handle global/local override
	* Consider table/grid editing rework, while looking for a larger #ui-pattern
