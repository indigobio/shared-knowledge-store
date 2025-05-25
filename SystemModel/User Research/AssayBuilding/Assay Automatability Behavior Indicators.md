2025-04-09
Answers provided by Joe Erwin, Persona Type: [[Product Specialist]]
#### Summary
Well-Behaved Traits
* Consistent retention time (RT): Especially when other peaks don't interfere within the RT window.
* Reliable ion ratios and peak shapes.
* Quality control (QC) metrics: Consistent area, response, RT, and shape across batches.
* Stable internal standard (ISTD) behavior: Predictable area, RT, and low bias, provided no interfering peaks exist.
Poorly Behaved Traits
* High RT variance that coincides with nearby interferences, making it hard to isolate correct peaks.
* High ion ratio variance or inconsistent QC measures.
* Frequent manual interventions in native systems, often indicating Ascent incompatibility.
* Shenanigans (e.g., changing ISTDs on-the-fly) used to make curves/QCs pass.
* Bias in ISTDs often linked to drift and problematic peak identification.
Automation Readiness Indicators
* Low reliance on manual integration.
* Use of consistent and compliant workflows.
* Willingness to improve assays (e.g., add ISTDs, validate system suitability).
* Onsite expertise in chromatography/mass spectrometry is present.
Practical Takeaways
* Labs need to trust Ascent to deliver results at their current quality levels—or better.
* Pushback is common, especially among smaller or less regulated labs, when Ascent prevents legacy “workarounds.”
* Open and honest communication about limitations and areas of improvement is key.
* Success depends not just on technical readiness, but also cultural and process adaptability.

#### Raw Interview
**Questions:**
- What characteristics of a compound/assay make it better or worse behaved?  Such as?
    - RT variance across all the batches even with predictions (wide cluster)
    - High ion ratio variance ranges
    - Prevalence of splits or clusters?
    - QC consistency in: area, response, RT, shape, etc?
    - if IS - consistency in: variance offset from other IS compounds, consistency of area, RT, shape, …
- What other factors do you look at when score a lab for “automatability”?

**Answers:**
Basically I look for:  

1. Can the results be released with a minimum of user intervention;
2. Can the required user interventions be done in a reasonable way in Ascent;
3. Can we reliably discern correct from incorrect peaks.

RT variance is really only an issue when there are other candidate peaks that fall within the RT window of the target peak that can't be reliably excluded by thresholds or other means.

If they do a lot of manual integration to normally get things to pass in their native system, chances are it won't work well in Ascent; manual integration in Ascent is typically much more time consuming than in the native system, not necessarily a bad thing, but it does punish labs/users that rely on it to reduce rework.

If they have to put eyes on a compound because it doesn't behave well (weird peak shape, clusters or have close interferences that can't be reliably integrated because of variance, etc) that's not necessarily a deal breaker, but I do always let them know so they can judge if having to review all of those will offset any potential savings on other compounds, or if we need to do a rule to flag it appropriately.

Some interventions do not work well in Ascent; case-in-point is changing ISTDs on-the-fly to make a curve or QC pass. Or uploading multiple curves to choose one from. I see those as red flags for problems in going live in Ascent.

ISTD RT consistency is not so much an issue IF there are not any interfering peaks that can be confused with the real one. Large Bias values can be a red flag; the larger the bias, the more independent drift they tend to have, thus the larger the variance that has to be accounted for in the windows and more likely we can run into issues with interferences.

In the end, when we're trying to get labs to go live they have to trust that Ascent is going to do the job as well as they do for the vast majority of their results. That's usually a bit of an uphill slog, either because they need to be convinced it will be just as stringent on quality (Cleveland, UW, Lurie, etc) or they're going to save money (most of the small strip-mall type labs).

For the latter, if the rerun rate goes up because they can't do the same shenanigans they do today to get things to pass, they put up a lot of resistance and we run into a failure to launch. It doesn't matter if the stuff they're doing isn't really defensible or has been dinged by regulators in the past at other labs, until they've been caught in an audit.

If I see indications of shenanigans, I try to sus out how dependent they are on them and how receptive they are to possible improvements. We've managed to bring along several labs by encouraging them to just add more ISTDs, perform basic system suitability before running the full batch, and make other minor changes to better control their assay.

For the ones who are not open to improvements, I try to be very honest about the limitations of what they should expect. Sometimes the resistance can come from a lack of available expertise onsite; for example with National, they used a consultant to develop their assay but then it was run by med-techs with no real knowledge of chromatography or mass spec; it was just another analyzer to them. That lack of expertise onsite can sometimes be a red flag that go-live or maintenance will be challenging, because they may not be able to maintain sufficient control over the analytical process.

Anyways, sorry for the rather lengthy book here! Hopefully this is helpful. In all cases I leave it up to the customer/others to decide what they want to do, but I try to give an honest and fair assessment based on my experience.