---
roles:
  - Operator
theme:
  - Production
usability-dimension:
  - Easy to learn
  - Engaging
page-state:
  - design
workstream:
  - review-workflow

season-target:
---
When tables are displayed in the system with configurable display attributes (e.g. sort, column visibility), provide an efficient and usable way to persist this configuration.

This could go multiple implementation paths as the [[Builder]] and [[Operator]] may have different preferences for display.
* persist configuration automatically as part of the signed in user's profile.
* allow [[Builder]] option when configuring an AQ method.

Current belief is this level of display option should be show preference for the Operator.

#ui-pattern about data tables could be abstracted.
#ui-pattern about how to persist data (with user, with browser session, with assay, etc)

## Next Steps
- [ ] Resolve assumption of operator level bias
- [ ] Look for other classes of this work in the UI




