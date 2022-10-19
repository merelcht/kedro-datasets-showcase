# Kedro datasets move into a separate package

Datasets are Kedro's way of dealing with input and output in a data and machine-learning pipeline. [Kedro supports numerous datasets](https://kedro.readthedocs.io/en/stable/kedro.extras.datasets.html) out of the box to allow you to process different data formats including Pandas, Plotly, Spark and many more.

In the upcoming `0.19.0` release of Kedro we will move datasets from the "extras" directory in Kedro into a separate package, called `kedro-datasets`. This change is one of the initiatives that will bring us closer to a stable release of Kedro 1.0. 

You can expect the `0.19.0` release early in 2023.

### Why are we doing this?

Our primary goal is to enable Kedro users to keep their packages up to date easily. We want to remove sources of breaking changes and achieve a stable framework. This is why, in Kedro `0.19.0`, we will move datasets into a separate package to reduce breaking changes associated with dataset dependencies. 

In the past, Kedro users were impacted by datasets being part of the Kedro framework in several ways:

 - Users had to wait until all of our dataset dependencies had released Python 3.9 and 3.10 support before the [Kedro framework was compatible with Python 3.9 and 3.10](https://github.com/kedro-org/kedro/issues?q=is%3Aissue+python+3.9+is%3Aclosed).  
 - Users could not get new, but workflow-breaking, dataset functionality frequently, because the Kedro framework has more conservative versioning (on average we ship a breaking release once a year and users had to wait that long for changes to the datasets).

The benefits to Kedro users of having datasets in a separate package include: 

- Kedro becomes more modular, making it possible for users to upgrade only the `kedro-datasets` dependency in production rather than modifying the entire template.
- Users can deploy newer datasets with older versions of Kedro and can even use datasets without Kedro. 

### The new Kedro workflow

Once datasets are moved to the new repository and removed from the core Kedro package in the `0.19.0` release, users will need to make three changes:

1. In addition to installing Kedro, users will need to install `kedro-datasets` to make use of datasets. Specifically, you will need to run `pip install kedro-datasets[SomeDataSet]` instead of `pip install kedro[SomeDataSet]` to install a dataset.
2. Use `import kedro_datasets` instead of `import kedro.extras.datasets` to import the datasets package into code.
3. Make any dataset updates and contributions to the new `kedro-datasets` repository instead of the core `kedro` one.

### How we will roll out this breaking change

Moving `kedro.extras.datasets` from the framework into a separate package is a breaking change, therefore we will introduce it in stages by:

- Making a separate `kedro-datasets` package and having `kedro` instantiate datasets from `kedro-datasets` with higher priority than `kedro.extras.datasets`.
- Removing `kedro.extras.datasets` from the core Kedro package when we ship Kedro `0.19.0`, early in 2023.

### Find out more!
Watch this recording of [the October 2022 Kedro Showcase](https://www.youtube.com/watch?v=MkMWl3jkxAU) to learn more about the changes to datasets, new features in the 0.18.x releases, and community updates.  

We are very excited about the release of this structure in Kedro `0.19.0`. What do you think? If you have any questions or feedback, comment on our [existing GitHub issue about this work](https://github.com/kedro-org/kedro/issues/1457) or by [raising a GitHub issue](https://github.com/kedro-org/kedro/issues/new/choose).
