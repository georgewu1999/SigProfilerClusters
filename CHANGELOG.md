# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.2] - 2025-07-21

### Added
- Integrated `pytest` to ensure correct handling of the `variant_caller` parameter.

### Changed
- Update the standard names for the `variant_caller` parameter
  - Changed `sanger` to `caveman`
  - `TCGA` and `standardVC` have been merged into a more flexible `standard` option.
  - `standard` is now default and parses VAF from 8th and 10th columns of VCF files (`VAF=` or `AF=`).

### Fixed
- Plotting Stability: Added error handling to skip samples that are invalid and proceed with valid ones.
- Resolved a potential index out-of-bounds error in the `plot_hist` function.

## [1.2.1] - 2025-04-02

### Changed
- Add centromere coordinates for mm39 genome.

## [1.2.0] - 2024-02-24

### Changed
- Updated dependencies: Now requires **Pandas >= 2.0.0**, **NumPy >= 2.0.0**, and **Python >= 3.9**.
- Dropped support for **Python 3.8**

## [1.1.3] - 2024-10-31

### Added
- Added support for Variant Allele Frequency (VAF) values from the following variant callers:
  - Sanger
  - TCGA
  - standardVC
  - Mutect2
