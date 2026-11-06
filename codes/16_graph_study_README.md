# Notebook 16: graph topology and E/I neuronal dynamics

Open `16_fhn_ei_graph_topology.ipynb` in Jupyter and select a Python kernel with NumPy, SciPy, pandas, Matplotlib, NetworkX and IPython. The saved notebook already contains executed results. `16_fhn_ei_graph_topology.html` is a static reading copy.

To reproduce, run all cells from the directory containing the notebook. Earlier notebooks are not runtime dependencies. Results are written under `results/fhn_ei_graph_topology/`; rerunning replaces that notebook's results. Keep a copy of the supplied results when comparing environments or parameter changes.

The experiment uses 36 nodes, nine explicit graph realizations, two 18E/18I assignments, two initial phase fields, a recipient coefficient budget of 0.08, and four additional bipartition-aligned controls. There are 40 main/supplementary trajectories, plus selected accuracy and longer-window runs. Generation, state initialization, simulation, measurement and validation code are in the notebook.

`summary.json` records the actual kernel package versions and numerical tolerances. Seeded graph generation may vary by NetworkX version: the saved `adjacency_*.csv` matrices are the definitive realized graphs for this executed result. Matrix rows/columns use node order 0–35. To use an archived matrix instead of regenerating a graph in a modified experiment, construct it with `nx.from_numpy_array(pd.read_csv(path).to_numpy())` before building conductance matrices. The corresponding `conductance_*.csv` files record directed recipient/source coefficients.

Inspect `graph_structure.csv`, `source_exposure.csv`, `initial_states.csv`, `condition_metrics.csv`, `node_metrics.csv`, `component_metrics.csv`, `spike_events.csv`, `window_sensitivity.csv` and `validation_checks.csv` for quantitative evidence. Graph seed 401 in G(n,m) has one isolated node; it is retained. Component diagnostics resolve this draw rather than treating it as a connected graph. The early window audit uses the same event support as the main run.

These finite graph draws, assignments and observation windows are an exploratory comparison, not a graph-ensemble estimate or a proof of asymptotic stability. Equal coefficient budgets do not equalize actual synaptic currents. All model units are dimensionless.
