# SyntheticDataTool: Requirements Specification
 
## Background:

Fake and Synthetic data has the potential in the NHS to increase innovation through access to realistic but private data, speed up development by providing a test set of data, and enable the generation of datasets that address underlying known biases in data collection.
 
### Problem Statement:

Many fake data generation tools exist but none are in regular use across the NHS.  This may be due to required time investment to build in NHS specifics or lack of confidence in the outputs.
Need for useful and easy to generate test data in different formats for developers is not being met.

Some examples of current alternatives:

R:

[synthpop](https://www.synthpop.org.uk/index.html)

[simPop](https://github.com/statistikat/simPop)

[sms](https://cran.r-project.org/web/packages/sms/index.html)


Python: 

[SDV](https://sdv.dev/)

[Faker](https://faker.readthedocs.io/en/master/)

[Gretel Synthetics](https://github.com/gretelai/gretel-synthetics)


Healthcare:

[simhospital](google/simhospital)

[Synthea](https://github.com/synthetichealth/synthea)

[Synthetic LS data](https://calls.ac.uk/guides-resources/synthetic-ls-data/)

### Aim and Objectives:

**The solution should look to:**

1. Support fast generation of fake data from metadata or user set profiles

2. Embed API connections to current ONS geography and NHS organisation structures

3. Connect with healthcare standards (e.g. FHIR) to produce data in CSV format as well as also other common healthcare formats relevant to the NHS

4. Use existing metrics and tools to support the correction of known bias in the data
 
### Brief Overview of Proposed Solution:

A library that would support NHS specific use cases of creating fake data from scratch (i.e. not generating from real data but using metadata and profiles to populate).   The outputs should be available in a range of formats including (but not limited to) CSV and FHIR to enable onward use of the data for both analysis and development.  A small suite of visualisations would be required to clearly show what the fake data looks like in terms of variable correlations and distributions.  Further, it would be useful to have a latent space representation to highlight outliers and off-manifold observations within the data.  A possible extension would be to have a feature to correct for known bias in the data which would use an equity metric on a single variable to positively skew the data.
 
### Non-Functional Requirements (NFR):

NFR
Specification
Security
Open Source Distribution
Responsiveness
Generation of <5000 data points in under 30s.  Generation of ~1 million data points in under 180s.
Scalability
1 user
Internationalisation
Python
Cross-platform
N/A
Compliance
Not Stated
Accessibility
Not Stated

 
### Features and Scenarios:

**Feature:**  Intuitive ingestion of metadata and profiles

**Feature:**  Fast generation of fake data aligned to user set profiles 

**Feature:** CSV and FHIR output formats for generated data (other formats to be added)

**Feature:** visualisation of variable profiles

**Feature:** visualisation of variable correlations

**Extension:**  visualisation of latent space

**Feature:**  able to generate tabular structured data including numerical and categorical

**Extension:**  able to generate short and long-form text data as a variable

**Extension:**  ability to debias/reskew data based on user definition of equity of a single variable
