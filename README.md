# Introduction

This repository contains CSV files and codeplugs for programming AnyTone radios, specifically AnyTone 878-series HT handsets.  May also work for other AnyTone models or clones, but YMMV.

The data within the CSVs are tailored for my own personal usage habits and geographical repeaters that are of interest to me; however, these CSVs may be useful for building out your own codeplug.  Input format is based around [K7ABD](https://github.com/K7ABD)'s handy [anytone-config-builder](https://github.com/K7ABD/anytone-config-builder), which is a set of Perl scripts which greatly simplify the process of creating the appropriate CSVs for import into the AnyTone CPS software.

## Directories

- **codeplugs** - contains exported codeplugs from the AnyTone CPS software.  Basically the output of all the CSVs once the CSVs have been imported into the CPS software, and what will be written to the radio.
- **csv** - contains raw CSV data to be manipulated.

### CSV Directories

- **input** - contains input CSVs.  These will be processed by `anytone-config-builder.pl`.
- **output** - contains CSV files ready for import into AnyTone CPS.
- **export** - future use

### How to process

Processing the CSVs is as simple as running `anytone-config-builder.pl` on them once you have them the way you want them.  See the [anytone-config-builder](https://github.com/K7ABD/anytone-config-builder) for more details.

**Example**:
  ./anytone-config-builder.pl --analog-csv=csv/input/analog.csv --digital-others-csv=csv/input/digital-others.csv --digital-repeaters-csv=csv/input/digital-repeaters.csv --talkgroups-csv=csv/input/talkgroups.csv --output-directory=csv/output


