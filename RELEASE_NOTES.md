# Tooling Library for Notebooks Release Notes

## Summary

<!-- Here goes a general summary of what this release is about -->

## Upgrading

<!-- Here goes notes on how to upgrade from previous versions, including deprecations and what they should be replaced with -->

## New Features

- Adding wind data to data fetching.
- Add day ahead prices fetching.
- Add `plot_power` to the asset optimization plotly visualizations. It stacks each component on the consumption line in the passive sign convention, so the top of the stack meets the grid line unless the components fail to account for the metered exchange. Unlike `plot_power_flow`, production is not clipped, so a PV system drawing power stays visible.

## Bug Fixes

<!-- Here goes notable bug fixes that are worth a special mention or explanation -->
