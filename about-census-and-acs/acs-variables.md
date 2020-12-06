# ACS Variables

## ACS Variable Formats

### Summary File

- Variable format: `[Table ID]_[Row Number][Variable Type]`

Example: Variable `B01001_001E` (*Total*) represents the estimate for table `B01001` row number `001`

### Subject Tables

- Variable format: `[Table ID]_[Column Number]_[Row Number][Variable Type]`

Example: Variable `S0101_C02_001E` (*Male!!Total population*) represents the estimate for table `S0101`, column number `02` (*Male*), row number `001`

### Data Profiles

- Variable format: `[Table ID]_[Row Number][Variable Type]`

Example: Variable `DP02_0002PE` (*Family households (families)*) represents the percent estimate for table `DP02` row number `0002`

### Comparison Profiles

Variable format: `[Table ID]_[Data Year]_[Row Number][Variable Type]`

Example: Variable `CP02_2011_2015_002E` (*Family households (families)*) represents the estimate for table `CP02`, data year `2011-2015`, row number `002`

## ACS Variable Types

ACS data contain variables ending in E, EA, M, MA, PE, PM and SS

Variable Type	| Title	| Related Products | Meaning
--------------|-------|------------------|--------
`E`	| Estimate | Summary Files, Subject Tables, Data Profiles, Comparison Profiles |	A numeric representation of the estimate.
`EA` | Estimate Annotation | Subject Tables, Comparison Profiles | A character representation of the estimate. If an Estimate Annotation exists, use this value in place of the Estimate.
`M`	| Margin of Error	| Summary Files, Subject Tables, Data Profiles | A numeric representation of the margin of error.
`MA` | Margin of Error Annotation	| Subject Tables Only	| A character representation of the margin of error. If a Margin of Error Annotation exists, use this value in place of the Margin of Error.
`PE` | Percent Estimate	| Data Profiles Only | An estimate representing a percent of the total.
`PM` | Percent Margin of Error | Data Profiles Only | The Margin of Error for the corresponding Percent Estimate (PE) variable
`SS` | Statistical Significance | Comparison Profiles Only | Returns `*` or `c` representing the Statistical Significance for the corresponding estimate (E) variable. An `*` indicates that the estimate is significantly different (at a 90% confidence level) than the estimate from the most current year. A "c" indicates the estimates for that year and the current year are both controlled; a statistical test is not appropriate.

## ACS Table Prefixes

Table Prefix | Meaning
-------------|--------
`B` | The **Base** table, gives the most detail available on the ACS
`C` | Collapse table
`CP` | Comparison Profiles
`DP` | Data Profiles
`S` | Subject table
