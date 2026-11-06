# Neuronal Modeling

Python and Jupyter notebooks studying single-neuron dynamics and coupled neuronal networks.

## Contents

- `codes/`: numbered notebooks, existing HTML exports, study notes, saved results, and existing study bundles.
- `codes/results/`: simulation tables, figures, summaries, and numerical validation records.
- The root model catalog and HTML export are preserved separately from the later catalog in `codes/`. These copies differ.

## Notebook sequence

- [01 · Neuronal model catalog](codes/01_neuronal_model_catalog.ipynb)
- [02 · Single-neuron theta/QIF dynamics](codes/02_theta_qif_single_neuron.ipynb)
- [03 · Hopf normal forms: onset, bistability, and switching](codes/03_hopf_single_neuron.ipynb)
- [04 · FitzHugh–Nagumo: recovery, excitability, and slow–fast oscillations](codes/04_fitzhugh_nagumo_single_neuron.ipynb)
- [05 · Hindmarsh–Rose: slow adaptation and bursting](codes/05_hindmarsh_rose_single_neuron.ipynb)
- [06 · Leaky integrate-and-fire (LIF): integration, threshold, and reset](codes/06_lif_single_neuron.ipynb)
- [07 · Exponential integrate-and-fire (EIF): intrinsic onset and numerical cutoff](codes/07_eif_single_neuron.ipynb)
- [08 · Two diffusively coupled FitzHugh–Nagumo neurons](codes/08_fhn_coupled_pair.ipynb)
- [09 · FHN square lattice: four nearest neighbors](codes/09_fhn_nearest_neighbor_lattice.ipynb)
- [10 · Distance-weighted FHN lattice coupling](codes/10_fhn_distance_weighted_lattice.ipynb)
- [11 · FHN synaptic pairs: excitatory and inhibitory source types](codes/11_fhn_excitatory_inhibitory_pairs.ipynb)
- [12 · Excitatory/inhibitory FHN lattice with homogeneous controls](codes/12_fhn_excitatory_inhibitory_lattice.ipynb)
- [13 · E/I fraction and strength ratio: two conductance protocols](codes/13_fhn_ei_fraction_strength.ipynb)
- [14 · Spatial E/I arrangement at fixed fraction and strengths](codes/14_fhn_ei_spatial_arrangement.ipynb)
- [15 · Distance-weighted E/I synapses and boundary conditions](codes/15_fhn_ei_distance_boundaries.ipynb)
- [16 · Graph topology and E/I neuronal dynamics](codes/16_fhn_ei_graph_topology.ipynb)
- [17 · Degree-preserving rewiring and E/I contact controls](codes/17_fhn_ei_degree_rewiring.ipynb)
- [18 · Degree, network size and coupling-strength sweeps](codes/18_fhn_ei_degree_size_strength.ipynb)

## Running the notebooks

Use a Python environment with the dependencies in `requirements.txt`. Launch JupyterLab from `codes/` so relative result paths resolve there. Open notebooks in numerical order. Existing notebook outputs are preserved.

```sh
python -m pip install -r requirements.txt
cd codes
jupyter lab
```

The dependency list was inferred from notebook imports; it is not a pinned or newly tested environment. Network and parameter sweeps may be computationally expensive.

## Provenance and scope

Imported from the local Neuronal Modeling project on 2026-11-06. Notebook contents and existing study outputs were copied without modification. The notebooks were not rerun as part of this repository import. HTML exports and ZIP bundles are existing snapshots and may predate subsequent notebook edits.

Reference books, downloaded research papers, event materials, temporary files, and notebook checkpoints remain outside this repository.

## Scientific interpretation

Results apply to the models, graph conventions, coupling protocols, solver tolerances, seeds, and observation windows specified in each notebook. Numerical validation records are evidence for those computations; finite-window phase measurements do not establish a universal network law.
