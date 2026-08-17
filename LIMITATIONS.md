# Limitations

## Dataset limitations

The inspected trial metadata contained:

- `start_time`
- `stop_time`
- `move_onset_time`
- `split`

No explicit movement-direction, target, or behavioral class label was available in the inspected trial table.

Therefore, supervised movement-decoding accuracy was not calculated or claimed.

## Temporal drift limitation

The early-versus-late comparison represents temporal representational change within a recording.

It should not be interpreted as direct evidence of:

- neurodegeneration
- pathological circuit deterioration
- disease progression
- electrode failure
- clinical impairment

A longitudinal multi-session dataset would be required to make stronger claims about neural drift or degeneration.

## Neural manifold limitation

PCA captures variance in the observed population activity but does not necessarily correspond to biologically meaningful neural dimensions.

Manifold geometry can also depend on preprocessing choices, feature selection, and temporal window definitions.

## Statistical limitation

The reported statistical results describe movement-related changes in this dataset. Statistical significance does not by itself establish biological or clinical significance.

## Future validation

Future work should evaluate:

1. Cross-session neural recordings
2. Explicit behavioral labels
3. Decoder transfer across sessions
4. Procrustes manifold alignment
5. Canonical Correlation Analysis (CCA)
6. Longitudinal recordings
7. Drift-robust decoder performance

These extensions would allow the framework to move from descriptive population analysis toward experimentally validated **drift-resilient neural decoding**.
