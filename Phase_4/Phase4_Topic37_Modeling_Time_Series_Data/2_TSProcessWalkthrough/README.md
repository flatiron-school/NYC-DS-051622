# Time Series: Modeling Process Walkthrough

Main goal here is to step through a time-series problem, making use of cross-validation and of the modeling algorithms from `statsmodels`.

## Learning Goals

- Build time-series models with `statsmodels`
- Cross-validate time-series models

# Lesson Materials

- [Jupyter Notebook: Example Modeling](example_modeling.ipynb)

## Lesson Plan

### Introduction (5 Mins)

This lecture is somewhat like the classificaton workflow lessons in that the goal is just to model workflow, this time of a time series problem. That said, the idea of using AIC to assess models is new. Also there are some concepts in the Level-Up sections that should be new, like ACF and PACF.

### Prep Gun Data and Split with `TimeSeriesSplit` (10 Mins)

Most of this was done in a previous lecture, but the new form of splitting is worth going over. The code illustrates how the splits are made.

### Build and Assess a Baseline Model Using 1 Lag (5 Mins)

This simply uses `train.shift()` to build a FSM.

### Starting with an AR Model (15 Mins)

Building, validating, assessing AR models. Here we also introduce AIC as an assessment tool. The main thing to remember is that AIC is really only useful in *comparing* multiple models (lower scores are better). Small differences in scores between models won't be statistically significant.

### Trying a MA Model (10 Mins)

Building, validating, assessing MA models.

### Both Together: ARMA (10 Mins)

Including both terms produces the best model. Natural question here of **how many terms of each type** to include. This points to ACF and PACF, which are in the Level-Ups. In a nutshell: Check the PACF plot to find how far back betas are statistically significant (outside of the shaded CI region), and use that number of AR terms. A similar inspection of the ACF tells you how many MA terms to use.

### Conclusion (5 Mins)

If have either:

- a seasonal component or
- exogenous variables

we can train a `SARIMAX` model. There's a Level-Up section on this as well.