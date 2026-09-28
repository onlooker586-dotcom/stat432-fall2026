---
name: stat432-plot-format
description: Improve the formatting of statistical plots produced for STAT 432 homework. Apply only when the user explicitly asks to polish, restyle, or improve a homework figure. Do not change the underlying data, axes, or the statistical content; only adjust visual presentation.
---

# STAT 432 Plot Formatting
Use these rules when restyling a homework figure in Python (matplotlib). Keep the data, variables, and statistical message unchanged.
## Canvas and margins
- Figure size: 7 inches wide by 4.5 inches tall by default; never wider than 9.
- Use tight layout / minimal margins; leave enough room for axis labels and the legend without clipping.
## Titles and labels
- Every plot has a short, descriptive title (sentence case, no trailing period).
- Both axes have explicit labels with units or variable names; never leave bare `x` / `y` labels.
- Legends have a short title and sit inside the plot area when possible, otherwise outside without covering the data.
## Colors and lines
- Use a colorblind-friendly palette (e.g. darkorange, deepskyblue, black, seagreen, crimson). Avoid pure red/green pairs.
- Distinguish multiple curves by both color and marker (e.g. `o-`, `s-`).
- Grid lines are light gray, thin, and behind the data.
## Text and typography
- Axis tick labels and legend text are at least 10 pt; title at least 12 pt.
- Use LaTeX-style math in labels where appropriate (e.g. $\hat\beta$, $k$, $n$).
## What not to change
- Do not add 3D effects, shadows, or decorative backgrounds.
- Do not rescale data, change axis limits to hide outliers, or alter the statistical message.