# Experimental Writing and Quantitative Results

The frames below are original examples. Populate them only with author-provided facts. Preserve existing experiment identifiers, controller names, plotting conventions, and data. Do not carry a protocol from one paper into another.

## 1. Describe the experimental platform

- "The experiments were conducted using [platform] in [environment]."
- "The controller runs at [confirmed update rate]."
- "The [quantity] is measured using [sensor or system]."

Use the most informative accurate term: pool experiments, flight tests, robot experiments, bench tests, or experimental tests. "Hardware" is appropriate for physical components and hardware-in-the-loop systems; avoid using it as shorthand for an entire experiment when the intended meaning is unclear.

## 2. Introduce comparison controllers and tuning

- "The proposed method is compared with [baseline] under [conditions]."
- "The gains were tuned for [specified nominal task]."
- "The selected design parameters are listed in Table [identifier]."

Describe the actual tuning procedure or setting. Do not claim optimal tuning, exhaustive optimization, identical bandwidths, or universally fair comparisons without supporting facts. Avoid defensive statements about not deliberately weakening a baseline. Let the documented setup and nominal results establish the comparison.

## 3. Explain fixed parameters across operating conditions

- "The same controller design parameters are used at all [specified operating points]."
- "The design parameters remain fixed during the command-switching tests."
- "Simulation and [specific experiments] use separate parameter sets."

Distinguish fixed design parameters from parameter estimates that change online. State the domain over which a parameter set is fixed. Separate simulation and experimental parameter sets do not imply retuning between experimental conditions.

## 4. Give each experiment a clear purpose

- "The nominal-condition test evaluates [tracking variables] at [operating point]."
- "The operating-point study evaluates tracking performance over [specified range or grid]."
- "The command-switching tests evaluate the response to changes in [command]."

Describe what the test measures rather than announcing its outcome before presenting evidence. Keep multiple channels visible when the paper concerns coordinated tracking. Do not narrow a multivariable contribution to its strongest single-channel result merely to simplify the narrative.

## 5. Describe command changes precisely

- "Each trial changes [one command] while keeping [the other command] fixed."
- "At [time], the [command] changes from [value] to [value]."
- "The four cases comprise increases and decreases in [two separately changed commands]."

Do not describe separate single-command changes as simultaneous switching. For depth or position, distinguish an increase in the numerical command from a physical rise or descent. Use the manuscript's sign convention rather than assuming that a larger depth coordinate means upward motion.

## 6. Report repeated trials and representative curves

- "Each [condition] was tested in [number] trials."
- "Figure [identifier] shows representative trials for [cases]."
- "Table [identifier] reports the mean and standard deviation of [trial-level metric]."

Keep representative trajectories distinct from average trajectories and pooled samples. Do not claim independent trials, randomized ordering, or a representative-trial selection rule unless supplied. Identify the unit of repetition: trial, condition, controller, or participant.

## 7. Define the evaluation window

- "The evaluation window begins at [event] and ends at [event]."
- "For each trial, the RMSE is evaluated from the command switch to that trial's stopping time."
- "Within each [confirmed matched group], all controllers are evaluated over a common window ending at [confirmed rule]."

These last two frames describe different protocols. Select only the one that matches the experiment. A window shown for a representative run is not automatically the window for every repetition. State whether windows are trial-specific or shared when that affects the comparison. Preserve endpoint conventions such as a closed start and open end.

## 8. Define metrics without changing their calculation

- "For [specified sampling scheme], the RMSE is computed as [existing equation]."
- "The trial-level RMSE values are summarized across [specified trials]."
- "The maximum per-condition RMSE is the largest RMSE among the tested operating points."

Do not replace time-weighted RMSE with equally weighted sample RMSE, pool trials silently, or invent interpolation and gap-handling procedures. The mean of trial RMSE values is generally not the RMSE of a mean trajectory. A maximum per-condition RMSE is not a maximum instantaneous tracking error.

## 9. Report channel-specific numerical comparisons

- "The mean [channel] RMSE of [method] is [value], compared with [value] for [baseline]."
- "At [condition], [method] reduces the mean [channel] RMSE by [percentage] relative to [baseline]."
- "The mean [first-channel] and [second-channel] RMSE values are [value] and [value], respectively."

Name the channel, statistic, condition, comparator, and units. Use unreduced or unrounded author-provided statistics for percentage calculations when calculation is authorized; otherwise preserve the stated percentages. If only rounded values are available, do not pretend to have access to raw precision. Keep rounding consistent within comparable results.

## 10. Discuss nominal responses

- "At the nominal operating point, [methods] track [commands] with [reported response characteristics]."
- "The [channel] responses settle within [reported interval]."
- "The mean [metric] is [reported relationship] for [methods]."

Use the nominal test to establish actual behavior, not to disparage or praise the tuning process. Do not infer settling time from an RMSE table or assert equivalent performance from visually similar curves without an appropriate basis.

## 11. Discuss an operating-point grid

- "Across the tested operating points, [method] maintains [reported error range or trend]."
- "As [operating variable] moves away from the nominal value, [reported metric] changes from [value] to [value]."
- "The mean and maximum per-condition [channel] RMSE values are [values]."

Compare both the aggregate behavior and the variation among operating points when the data support both. Results on a finite grid support performance across those tested conditions; they do not automatically establish global robustness or behavior outside the tested range. Do not silently narrow an existing claim during language-only editing; raise a substantive scope issue separately.

## 12. Describe unequal improvements across channels

- "Both controllers achieve [supported speed-tracking description], while [method] has a lower mean depth RMSE in [specified cases]."
- "The main improvement is in [channel], where [metric] decreases by [reported amount]."
- "The results show improved [defined tracking objective], with the largest reduction in [specific metric]."

Emphasize the evidence-supported strength without turning a mixed result into dominance in every channel. Do not claim an aggregate improvement unless the stated objective or aggregate measure supports it. "Both have low error" requires an actual basis. Avoid gratuitous self-criticism, but retain findings that materially qualify the main claim.

## 13. Separate descriptive and inferential statements

- Descriptive: "The mean [metric] is lower for [method] in all [specified cases]."
- Quantitative: "The reduction in [metric] is [percentage]."
- Inferential, only if supplied: "The difference is statistically significant according to [test and reported result]."

Prefer a numerical effect over an unqualified "significant improvement." Do not infer statistical significance from mean and standard deviation alone. Standard deviation, standard error, confidence intervals, and min-max ranges are different summaries.

## 14. Write figure captions and table notes

- "Representative [responses] for [experiment and conditions]."
- "[Metric] over [defined operating conditions]."
- "Values are the mean and standard deviation of trial-level [metric]; [number] trials were performed for each [group]."
- "Each trial is evaluated over [confirmed window definition]."

Explain symbols, line styles, panels, error bars, and windows only as needed to interpret the display. State the actual meaning of box boundaries and whiskers rather than assuming a default convention. Use the established controller order and names. For a scalar speed, use "Speed," not "Velocity," unless the plotted quantity is genuinely a velocity component or vector.

This writing skill does not prescribe centered versus left-aligned table notes or a particular font size. Follow the selected venue template. Do not change numerical table bodies, figure content, or layout during a language-only task without authorization.
