# Kedro Datasets move into a separate package

Datasets are Kedro's way of dealing with input and output in a data and machine-learning pipeline. [Kedro supports many datasets](https://kedro.readthedocs.io/en/stable/kedro.extras.datasets.html) out of the box to allow you to process different data formats including Pandas, Plotly, Spark and many more.

In the `0.19.0` release of Kedro we will move datasets from the "extras" directory in Kedro into a separate package, called `kedro-datasets`. This change is one of the initiatives that will bring us closer to a stable release of Kedro 1.0. 
You can expect the `0.19.0` release early next year.

### Why are we doing this?

We want to remove the sources of breaking changes in Kedro to achieve a stable framework. This is why, in Kedro `0.19.0`, we will move datasets into a separate package to reduce breaking changes associated with dataset dependencies. Our primary goal is to enable Kedro users to keep their packages up to date more easily.

In the past, we have faced challenges like not being able to: 
 - [Add Python 3.9 and 3.10 support](https://github.com/kedro-org/kedro/issues?q=is%3Aissue+python+3.9+is%3Aclosed) to the Kedro framework until all of our datasets had released Python 3.9 and 3.10 support. 
 - Provide new, but workflow-breaking, dataset functionality to our users because the Kedro framework has more conservative versioning i.e. on average we ship a breaking release once a year and users would have to wait that long for changes to the datasets.

The benefits to Kedro users of having datasets in a separate package include: 
 - Kedro becomes more modular, making it possible for users to upgrade only the `kedro-datasets` dependency in production rather than modifying the entire template.
- Users can deploy newer datasets with older versions of Kedro and can even use datasets without Kedro. 

### The new Kedro workflow

Once datasets are moved to the new repository and removed from the core Kedro package, users will need to make three changes:
1. In addition to installing Kedro, users will need to install `kedro-datasets` to make use of datasets. Specifically, you will need to run `pip install kedro-datasets[SomeDataSet]` instead of `pip install kedro[SomeDataSet]` to install a dataset.
2. Use `import kedro_datasets` instead of `import kedro.extras.datasets` to import datasets into code.
3. Make any dataset updates and contributions to the new `kedro-datasets` repository instead of the core `kedro` one.

### How we will roll out this breaking change

Moving `kedro.extras.datasets` from the framework into a separate package is a breaking change, therefore we will introduce this change in stages by:

- Making a separate `kedro-datasets` package and having `kedro` instantiate datasets from `kedro-datasets` with higher priority than `kedro.extras.datasets`.
- Removing `kedro.extras.datasets` from the core Kedro package when we ship Kedro `0.19.0`.

### Find out more!
You can follow any `kedro-datasets` developments and more on [our GitHub repository](https://github.com/kedro-org/kedro/issues/1457). 

We are very excited about the release of this structure in Kedro `0.19.0`. 

If you have any questions or feedback, comment on our [existing GitHub issue about this work](https://github.com/kedro-org/kedro/issues/1457) or by [raising a GitHub issue](https://github.com/kedro-org/kedro/issues/new/choose).
