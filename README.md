# NOC Data Study Challenge 2023

This repository contains codes and sample notebooks for downloading and processing the DSG.

## Motivation
Mesoscale eddies are ubiquitous in the global ocean and are a key identifier of global warming. Being able to track and detect eddies is therefore crucial to physical oceanographers in order to  accurately model our changing oceans. However, detecting eddies is non-trivial and current methods are floored. In particular sea surface height (SSH) maps in which eddies leave an identifiable trace, have been shown to be poor at resolving eddies causing aliasing and distortion. Further, model-based eddy identification algorithms which use rule-based systems are sensitive to both noise and artificats in the SSH field. Therefore, improvements to eddy detection workflows are needed.

## Challenge
We propose 2 potential challenges:
1. **SSH Mapping** - How can we accuratley map SSH onto a high-resolution grid given a set of sparse satellite observations using machine learning?

2. **Eddy Identification** - How can we effectively detect eddies given a SSH map using machine learning?

For more details please see the [challenge long description].

## Model Data
Given a lack of a high resolution ground truth, in order to evaluate the quality of SSH mapping and eddy identification algorithms we will use the [eNATL60 North Atlantic ocean simulation](https://github.com/ocean-next/eNATL60).

## Observations
We generate SSH observations by interpolating the eNATL60 model onto real satellite tracks. The SSH observations include tracks from SARAL/Altika, Jason 3, H2B, Sentinel3A, and Sentinel3B altimeter data. This nadir altimeters constellation was operating during the 20200901-20210630 period.

## Challenge Data
The SSH reconstructions are assessed over the period from 2020-09-01 to 2010-06-30. We suggest using the first month for testing, the second data for validation and the remaining 7 months for training. We also use a subset of the North Atlantic near the GulfStream for computational reasons (If there is demand we can potentially increase the size of the domain).
 
## Quick start
You can follow the quickstart guide in [this notebook](https://github.com/ocean-data-challenges/2020a_SSH_mapping_NATL60/blob/master/quickstart.ipynb).


## Acknowledgement

The structure of this data challenge was to a large extent inspired by [WeatherBench](https://github.com/pangeo-data/WeatherBench) and [Ocean Data Challenges](https://github.com/ocean-data-challenges/2021a_SSH_mapping_OSE).
