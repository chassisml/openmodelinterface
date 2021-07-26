# Introduction

![OMI logo](images/omi-logo.png){: style="width:500px" }

The Open Model Interface proposes a spec for _multi-purpose_ OCI-compatible container images for Machine Learning models.

We believe that ML teams should be able to build DevOps-ready container images for consumption by multiple platforms.


TODO: diagram

## Key points

* Models are baked into the container image, not downloaded at runtime

* Model serving framework can be switched at runtime by environment variable

* Pre- and post-processing logic can be shipped with the container image

* First reference implementation of OMI is available, Apache 2 licensed, at [Chassis](https://chassis.ml)


## Model Baking

TODO: Rationale


## Build once, run many: Runtime Configuration

![](images/chameleon.webp)


## Reference Implementation


## Roadmap

* Explainability
* Drift
