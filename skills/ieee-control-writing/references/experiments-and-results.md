# Experimental setup and results

M04 sentence frames. Select actual facts rather than adopting a protocol from an example. The active profile's M07 owns experimental narrative, M06 owns statistical meaning, and M08 owns display formatting.

## Platform, comparison, and fixed settings

- "The experiments were conducted using [platform] in [environment]."
- "The controller runs at [confirmed update rate]."
- "The [quantity] is measured using [sensor or system]."
- "The proposed method is compared with [baseline] under [conditions]."
- "The gains were tuned for [specified nominal task]."
- "The design parameters are listed in Table [identifier]."
- "The design parameters remain fixed across [specified test set]."
- "Simulation and [specific experiments] use separate parameter sets."

## Purpose and command changes

- "The nominal-condition test evaluates [tracking variables] at [operating point]."
- "The operating-point study evaluates performance over [specified range]."
- "Each trial changes [one command] while keeping [the other] fixed."
- "At [time], the [command] changes from [value] to [value]."

## Repetition, curves, and windows

- "Each [condition] was tested in [number] trials."
- "Figure [identifier] shows representative trials for [cases]."
- "Table [identifier] reports the mean and standard deviation of trial-level [metric]."
- "The evaluation window begins at [event] and ends at [event]."
- "For each trial, the RMSE is evaluated from the command switch to that trial's stopping time."
- "Within each [matched group], all controllers are evaluated over a common window ending at [confirmed rule]."

The last two frames describe different protocols. Choose the documented one, including endpoint conventions; a representative curve does not establish every repetition's window.

## Metrics and numerical comparisons

- "For [sampling scheme], the RMSE is computed as [existing equation]."
- "The maximum per-condition RMSE is the largest RMSE among the tested operating points."
- "The mean [channel] RMSE is [value] for [method] and [value] for [baseline]."
- "At [condition], [method] reduces mean [metric] by [reported percentage]."
- "The mean [first-channel] and [second-channel] RMSE values are [values], respectively."

Include units and comparator when needed. Use supplied percentages or the actual authorized calculation; formatting and rounding follow M08.

## Observations and interpretation

- "At the nominal operating point, [methods] track [commands] with [reported behavior]."
- "The [channel] responses settle within [reported interval]."
- "Across the tested operating points, [method] maintains [reported error range]."
- "As [variable] changes, [metric] changes from [value] to [value]."
- "Both controllers achieve [supported description], while [method] has lower [metric] in [cases]."
- "The main improvement is in [channel], where [metric] decreases by [reported amount]."
- "The difference is statistically significant according to [test and reported result]."

The last sentence requires an actual inferential result; it is not a synonym for a numerical reduction. Mixed results and scope questions follow M02 and M06.

## Captions and notes

- "Representative [responses] for [experiment and conditions]."
- "[Metric] over [defined operating conditions]."
- "Values are the mean and standard deviation of trial-level [metric]; [number] trials were performed for each [group]."
- "Each trial is evaluated over [confirmed window definition]."

Explain symbols, panels, line styles, error bars, and windows as needed. Keep the actual statistics, controller order, and names.
