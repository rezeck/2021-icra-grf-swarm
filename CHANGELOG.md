# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] — 2026-04-09

### Summary

First stable release of the open-source implementation associated with the IEEE ICRA 2021 paper *Flocking–Segregative Swarming Behaviors using Gibbs Random Fields* (Rezeck, Assunção, Chaimowicz). This version is intended for reproducibility, comparison against bundled baselines, and use as a reference implementation of the proposed Gibbs random field (GRF) controller with Metropolis–Hastings sampling.

### Included software

- **`grf_swarm`** — Proposed GRF-based segregation (`grf_swarm_node`, `grf_swarm_nav` for analysis scenarios).
- **`grad_swarm`** — Gradient-based potential (local minima comparison).
- **`pso_swarm`** — PSO-based heterogeneous swarm segregation (Inácio et al., 2019).
- **`min_swarm`** — Minimalistic segregation (Mitrano et al., 2019).
- **`vgs_swarm`** — Differential-potential baseline with global positional knowledge (Santos et al., 2020).

Shared launch parameters (`robots`, `groups`, `world`, `sensing`, `seed`, `log`, `gui`, `iterations`) support fair cross-method experiments.

### Documentation and distribution

- **`docs/`** — Project page for GitHub Pages (usage, parameters, baselines, replication protocol, video embed).
- **`Dockerfile`** and **`docker-compose.yml`** — ROS Melodic environment for building and running demos (headless or GUI profile).
- **`paper/`** — Camera-ready PDF of the ICRA 2021 paper (filename may vary by checkout).

### Notes

- Target platform: **ROS Melodic** on Ubuntu 18.04 (or equivalent container).
- The PSO package build no longer references a non-existent `pso_swarm_generate_messages_cpp` target (CMake fix for clean `catkin_make`).

[`1.0.0`]: https://github.com/verlab/2021-icra-grf-swarm/releases/tag/v1.0.0
