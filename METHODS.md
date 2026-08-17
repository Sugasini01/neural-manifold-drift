# Methods

## 1. Dataset Inspection

The NWB dataset was inspected to identify trial timing, neural unit metadata, spike times, observation intervals, and electrode information.

The dataset contained:

- 574 trials
- 137 neural units
- 0.7-second trial duration
- Movement onset at 0.25 seconds

## 2. Movement Alignment

Spike activity was aligned to movement onset using a window from:

**−0.20 seconds to +0.45 seconds**

A bin size of **10 ms** was used, producing **65 temporal bins** per trial.

The resulting neural activity tensor had dimensions:

**574 trials × 137 neurons × 65 time bins**

## 3. Population Firing Dynamics

Mean firing rates were calculated before and after movement onset.

Pre-movement activity was compared with post-movement activity to characterize population-level movement responses.

## 4. Neuron-Level Response Analysis

For each neuron, pre- and post-movement firing rates were compared.

Neurons were categorized as increasing or decreasing their firing rate following movement onset.

## 5. Statistical Testing

Statistical significance was evaluated at the neuron level.

Multiple-comparison correction was performed using the False Discovery Rate (FDR), with:

**FDR < 0.05**

## 6. Trial-Level Neural Representation

A trial × neuron population representation was constructed from movement-aligned neural activity.

This produced a matrix of:

**574 trials × 137 neurons**

## 7. Neural Manifold Construction

Principal Component Analysis (PCA) was applied to reduce the dimensionality of the population representation.

The first three principal components explained:

**12.47% of total variance**

The first ten dimensions explained:

**25.94% of total variance**

## 8. Temporal Representational Analysis

Trials were divided into two temporal groups:

- Early trials: 287
- Late trials: 287

Population representations were compared using:

- Centroid distance
- Population correlation
- Representational similarity analysis (RSA)

## 9. Reproducibility

All computational analysis was performed using Python-based scientific computing tools.

The accompanying Jupyter/Colab notebook contains the analysis workflow and outputs.

## 10. Scope

This analysis evaluates temporal changes in neural population representations.

It does not establish neurodegeneration, clinical impairment, or device-level BCI performance.

Future work will evaluate cross-session recordings and explicit behavioral labels to test drift-resilient neural decoding.
