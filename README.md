# an-ai-for-an-eye

This repository contains code for the experiments contained "An AI for an Eye" which is currently under review at CHIIR 2026.

The code expects an OpenRouter API key to be set to `OPENROUTER_API_KEY`.

The main entry point is in `dl-gen.sh` which runs three multimodal generative models against the two digital library interfaces with parameters calibrated from unreleased participant data using `calibrate_params.py`.

From there, heatmaps can be generated using `dl-heatmap.sh`.

To compute AOI hits, use `dl-aois.sh`.


And the following tables can be generated (data, not formatting) using:
- Table 1: Can be determined using `dl-compare-maps.sh`
- Table 2/Table 3: The combination of `dl-aoi-stats.sh`, `dl-aoi-time-stats.sh`, and `dl-fixations-before.sh`. Note that these report more AOIs than the paper as we were space constrained in the paper.
- Table 4: Can be determined using `dl-compare-maps-model.sh`.


`tobii_aoi_to_json.py` is an helper function that converts text-based AOI exports from Tobii into more useful JSON formats which we use throughout the scripts.

`plot_scanpaths.py` is a function that visualizes the individual scan-paths and is the basis script for much of the other work but is not present in the paper directly.