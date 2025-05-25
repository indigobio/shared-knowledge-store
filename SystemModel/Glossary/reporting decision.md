---
aliases:
  - reporting category
  - routing
  - reporting
  - reporting decisions
tags:
  - domain
  - indigo
---
*noun.* The user supplied disposition of a determination. The values may be used to create specific document outputs useful outside of ASCENT (e.g. a file listing all samples marked for Repeat which can be fed back to the instrument)

Default reporting decisions:
* **accept**. Selecting a specific reporting category, commonly used to indicate a decision based on observed flag values. These selection will drive the determination to "go to green" and render all flags in italics.  Accepting a determination is considered part of the disposition that may be used by another tool after ASCENT. Agreeing to the R^2 flag would be an example.
* **exclude**. Selecting **Exclude** is commonly used to indicate a decision based on observed flag values. This selection will drive the determination to “go to green” and render all flags in italics (as indicative of their non-relevance, since the decision has been made on suitability for use).
* **include**. When a batch is first made Ready to Review, all determinations will be set to **Include**. A determination with no flags be in a “green”, indicating it is resolved; a determination with at least one flag will be in a “blue” state, indicating it needs review.
* **repeat**. Selecting **Repeat** is commonly used to indicate a decision based on observed flag values. This selection will drive the determination to “go to green” and render all flags in italics (as indicative of their non-relevance, since the decision has been made on suitability for use).
