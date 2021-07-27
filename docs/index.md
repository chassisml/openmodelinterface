# Introduction

![OMI logo](images/omi-logo.png){: style="width:500px" }

The Open Model Interface (OMI) proposes a spec for _multi-purpose_ OCI-compatible container images for Machine Learning models.

We believe that ML teams should be able to build reusable, DevOps-ready container images for interoperable consumption by multiple platforms to avoid being locked in to any one platform.


## Key points

* Models are baked into the container image, not downloaded at runtime
* Model serving framework can be switched at runtime by environment variable
* Pre- and post-processing logic can be shipped with the container image
* Spec includes recommendations around model management for reproducibility & provenance
* First reference implementation of OMI is available, Apache 2 licensed, at [Chassis](https://chassis.ml)


## Model Baking

Including the model files in the container image itself is better than downloading them at runtime because it makes the model images self-contained, adheres to DevOps best practice, improves reproducibility and reliability.

In particular, some systems download a model from, say, an MLflow server when the server starts up. This relies on the MLflow server being online, which makes the MLflow server a critical part of your production infrastructure. As MLflow servers are often managed by ML teams, this is undesirable, and can result in downtime for your ML services if your MLflow server is unavailable when your model containers restart or scale up.

In terms of reproducibility, baking models into containers is better because your CI/CD system can record the exact version of the container that was running at any given time, and so you can trace a specific inference result to the exact model that was running in production at that moment, and then trace it (see "Origin tags" in the spec) back to the exact model that trained it.


## Build once, run many

By creating images that are "multi-purpose", you can avoid lock-in from a specific runtime platform. Instead, your ML teams can build container images that work in a variety of different platforms.

See the spec to see exactly how runtime configuration of the exposed interface works.


## Reference Implementation

The first reference implementation of the OMI is available today, under the Apache 2 license, at [Chassis.ml](https://chassis.ml).
There you can try a test drive of the reference implementation to play with it today.


## Roadmap

* Support for other runtimes: Sagemaker, Algorithmia, etc
* Ingest models from sources other than MLflow
* Explainability support
* Drift support


## History

The OMI is founded by [Modzy](https://modzy.com) is a commercial ModelOps platform designed to run any kind of machine learning and artifical intelligence model in production, at scale, with enterprise grade security, governance, and compliance. The design of the Open Model Interface grew out of Modzy's internal research and development to provide a common spec that would support all kinds of models, both present and future, with first-class support for emerging capabilities like drift detection, explainability, and adversarial defense.
