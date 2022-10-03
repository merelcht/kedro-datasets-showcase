# Introducing changes to Kedro Datasets

> TLDR; Datasets are moving into a separate package called "kedro-datasets"

### Introduction
Datasets are Kedro's way of dealing with input and output in a data pipeline. They are python classes and all implementations of [the `AbstractDataSet`](https://kedro.readthedocs.io/en/stable/kedro.io.AbstractDataSet.html#kedro.io.AbstractDataSet). [Kedro supports many datasets](https://kedro.readthedocs.io/en/stable/kedro.extras.datasets.html) out of the box to allow you to process data of different formats, such as Pandas, Plotly, and Spark.

Datasets are an important part of Kedro, but at the same time it is a component that does not fit with the rest of the framework from a software architecture perspective. Datasets are currently packaged under the "extras" directory, which already indicates it is extra functionality that can be used with the Kedro framework. Some of the reasons why datasets do not fit with the Kedro framework are:
- The Kedro framework has a different breaking change velocity from the datasets: the datasets are less stable and need to be updated more frequently
- The framework does not need datasets to function

This is why we will be moving the datasets into a separate package, called `kedro-datasets`. Moving `kedro.extras.datasets` from the framework is a breaking change, therefore we will introduce this change in stages:
1. Make a separate `kedro-datasets` package and alias everything in `kedro.extras.datasets` to that new package
2. Remove `kedro.extras.datasets` from the core Kedro package when we ship Kedro `0.19.0`


### What is the change?
Datasets will be removed from the core Kedro package into a separate package called `kedro-datasets`. This means that in the future users will need to install both `kedro` and `kedro-datasets` to leverage all functionality.
Moreover, any dataset contributions need to be added to the new repository.

### Why are we doing this?
The main reason for moving datasets to its own repository is because the rest of Kedro framework has a different breaking change velocity from the datasets. In the past this caused the following issues:
- It was not possible to add support for Python 3.9 and 3.10 to Kedro framework in a non-breaking version, because of breaking changes those python versions introduced to some of the dataset dependencies
- Adding support for newer versions of the datasets was held back by the need for more conservative versioning of the framework
- For users this often meant maintaining workarounds to make old versions of Kedro work with other tools

Moving datasets into its own package means that Kedro becomes more modular, making it easier for users to upgrade an application using Kedro in production gradually by upgrading only the `kedro-datasets` version in its requirements rather
 than modifying the entire template. To be able to use the latest version of the full framework, users will have to migrate the template eventually, but being able to upgrade datasets much faster than they are able to do 
 now will be an improvement for production maintenance.

### How will your new workflow look?
Once datasets are moved to the new repository and removed from the core Kedro package, users will need to change a couple of things to use the framework and datasets as before:
1. In addition to installing kedro, users will need to install kedro-datasets by running: `pip install kedro-datasets`
2. To install a specific dataset, users will need to run `pip install kedro-datasets[SomeDataSet]` instead of `pip install kedro[SomeDataSet]`
3. Use `import kedro-datasets` instead of `import kedro.extras.datasets` to import datasets into code
4. Make any dataset updates and contributions to the new kedro-datasets repository instead of the core kedro one

### Find out more!
You can follow any `kedro-datasets` developments and more on [our Github repository](https://github.com/kedro-org/kedro/). 

We are very excited about the release of this structure in Kedro 0.19.0. We believe that it will enhance the experience of using Kedro and allow you to keep your packages up to date more easily.

If you have any question or feedback, please do let us know by [raising a Github issue](https://github.com/kedro-org/kedro/issues/new/choose).
