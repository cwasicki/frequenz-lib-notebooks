# Tooling Library for Notebooks Release Notes

## Summary

<!-- Here goes a general summary of what this release is about -->

## Upgrading

<!-- Here goes notes on how to upgrade from previous versions, including deprecations and what they should be replaced with -->

## New Features

- Adding wind data to data fetching.
- Add day ahead prices fetching.
- Add `plot_power` to the asset optimization plotly visualizations. It stacks each component on the consumption line in the passive sign convention, so the top of the stack meets the grid line unless the components fail to account for the metered exchange. Unlike `plot_power_flow`, production is not clipped, so a PV system drawing power stays visible.
- `init_microgrid_data` accepts several dotenv files, so shared API URLs can live apart from per-microgrid credentials. Files are loaded in order and override earlier ones, so the most specific file goes last. `~` in a path is now expanded, and a file that loads nothing is reported.
- `init_microgrid_data` reads credentials from `API_AUTH_KEY`/`API_SIGN_SECRET`, falling back to `API_KEY`/`API_SECRET`. Both halves must come from the same pair, so a key and a secret cannot be taken from different files.

## Bug Fixes

- `init_microgrid_data` no longer keeps the credentials of a previously loaded dotenv file. Switching microgrid in a running notebook kernel used to reuse the first microgrid's key and assets URL.
