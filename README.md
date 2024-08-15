# Network analysis for Communal Narcissism, Dark Triad and WHO-related traits before and furin the COVID pandemics.

This repository contains three notebooks:
1. Communal Narcissism vs Knowledge traits (done);
1. WHO traits (done);
1. Dark Triad vs Gender traits (in progress)

The computations and plots are done closely as in [Yu, J., Mahendran, R. COVID-19 lockdown has altered the dynamics between affective symptoms and social isolation among older adults: results from a longitudinal network analysis. Sci Rep 11, 14739 (2021)](https://www.nature.com/articles/s41598-021-94301-6).

The following is being calculated/plotted:
1. perform paired sample t-test;
1. compute [Cohen's d - effect size value](https://en.wikipedia.org/wiki/Effect_size#Cohen's_d);
1. plot the change in time (with mean trajectories);
1. compute partial correlation networks and basic networks' metrics;
1. plot the networks (with only signifcant changes as edges - uncorrected p<0.05);
1. plot correlogram for average absolute edge values between and within questionnaires;
1. plot heatmaps of partial correlations;
1. plot basic graphs' metrics for particular measurements at different times to easily observe change (or lack of thereof);
1. compute and show in correlation matrix the Pearson's correlation of considered variables;
1. plot graphs' nodal strength centrality;
1. plot networks' bridge strength centrality (doesn't apply to WHO)

The Cohen's d values - the difference between two means divided by a standard deviation for the data, are calculated given below formula:<br>
$d = \frac{\bar{x}_1 - \bar{x}_2}{s}$
, where s is [pooled variance](https://en.wikipedia.org/wiki/Pooled_variance):<br>
$s = \sqrt{\frac{(n_1 - 1)s^2_1 + (n_2 - 1)s^2_2}{n_1 + n_2 - 2}}$
<br>
and where $s^2 = \frac{1}{n  - 1}\sum_{i=1}^{n}(x_i - \bar{x})^2$<br>
A positive d indicates that the first mean is higher. In contrast, a negative d indicates that the second mean is higher. A lower Cohen's d indicates the necessity of larger sample sizes, and vice versa - [Wikipedia](https://en.wikipedia.org/wiki/Effect_size#Cohen's_d)

In calculating the partial correlation, I'll use the inverse of a variance–covariance matrix described in _[Epskamp, S., & Fried, E. I. (2018). A tutorial on regularized partial correlation networks. Psychological Methods, 23(4), 617–634.](https://eiko-fried.com/wp-content/uploads/Epskamp-Fried-2018-Tutorial-partial-corr.pdf)_