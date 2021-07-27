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


## Reference Implementation


## Roadmap

* Explainability
* Drift


## History

The OMI is founded by [Modzy](https://modzy.com) is a commercial ModelOps platform designed to run any kind of machine learning and artifical intelligence model in production, at scale, with enterprise grade security, governance, and compliance. The design of the Open Model Interface grew out of Modzy's internal research and development to provide a common spec that would support all kinds of models, both present and future, with first-class support for emerging capabilities like drift detection, explainability, and adversarial defense.
