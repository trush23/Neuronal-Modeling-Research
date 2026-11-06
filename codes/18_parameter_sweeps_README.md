# Notebook 18: degree, size and coupling-strength sweeps

Open `18_fhn_ei_degree_size_strength.ipynb` in Jupyter with a Python kernel containing NumPy, SciPy, pandas, Matplotlib, NetworkX and IPython. The delivered notebook contains executed results; `18_fhn_ei_degree_size_strength.html` is the static reading copy. Earlier notebooks are not runtime dependencies.

Run all cells from the directory containing the notebook. Outputs are written under `results/fhn_ei_degree_size_strength/`; rerunning replaces that notebook's outputs. Preserve the supplied bundle before changing parameters or software versions. `summary.json` records the actual kernel versions and numerical settings. Exact seeded graph generation may vary by NetworkX version; frozen adjacency and conductance CSVs define the delivered realizations.

Three experiments are separated:

- Degree: N=36, k=4/8/12, fixed recipient coefficient budget B=0.08 versus fixed contact coefficient g=0.02. These conventions coincide at k=4; at larger k the latter increases total strength to gk.
- Size: N=18/36/72, k=4, B=0.08. Density changes with N. Each size has an exact half E/I assignment generated with seed 301; assignments are not nested across sizes.
- Strength: N=36, k=4, B=0/0.04/0.08/0.16. The same graphs, source labels and phase fields are retained at each strength.

Each graph specification has a ring and random regular draws seeded 601/602, with phase seeds 11/29. There are 15 graphs and 78 design labels. Exact matches in node count, source assignment, phase seed and complete conductance matrix reuse a single main trajectory; `design_to_run.csv` records the reuse. Shared controls are not additional independent replicates. Two graph draws and two phase fields do not support a graph-ensemble estimate or confidence intervals.

Read `graph_structure.csv`, `coefficient_audit.csv`, `node_source_contacts.csv`, `source_assignments.csv`, `initial_states.csv`, `condition_metrics.csv`, `unique_run_metrics.csv`, `node_metrics.csv`, `spike_events.csv`, `coupling_convention_contrasts.csv`, `numerical_audits.csv`, `window_sensitivity.csv` and `validation_checks.csv` for the evidence. Matrix node order is 0 through N-1; rows of G are recipients and columns are sources. The continuous FHN model and gate parameters use dimensionless units.

At zero coupling, local cancellation fraction C is undefined (NaN), not zero; uncoupled phase order is checked against the initial phase-phasor magnitude. The same 1000-unit trajectory supplies early-window event support in the longer-window audit, so extending integration does not alter early phase coverage. Independent Radau and tighter DOP853 checks cover two selected extremes, not every trajectory. Longer windows do not prove convergence or stable attractors.

The notebook records figure alternative text in output metadata; the delivered standalone HTML retains descriptive image alternatives. Saved PNGs allow direct figure inspection without executing the notebook. This is the requested finite degree/size/strength stage, not a full factorial study or universal scaling law.
