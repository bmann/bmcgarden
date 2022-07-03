---
title: TypeSense Showcase Recipe Search
link: https://recipe-search.typesense.org/
git: https://github.com/typesense/showcase-recipe-search
date: 2021-01-10
---
Showcase of using [[TypeSense]] search to search a ~2M recipe data set which is stored as structured data.

From the [Github README](https://github.com/typesense/showcase-recipe-search):

> This search experience is powered by Typesense which is a blazing-fast, open source typo-tolerant search-engine. It is an open source alternative to Algolia and an easier-to-use alternative to ElasticSearch.
> 
> The recipe dataset is from [Glorf/recipenlg](https://github.com/glorf/recipenlg) 🙏!
>
> The dataset is 2.2 GB on disk, with ~2.2 million rows. It took 8 minutes to index this dataset on a 3-node Typesense cluster with 4vCPUs per node and the index was 2.7GB in RAM.
>
> The app was built using the Typesense Adapter for InstantSearch.js and is hosted on S3, with CloudFront for a CDN.
>
> The search backend is powered by a geo-distributed 3-node Typesense cluster running on Typesense Cloud, with nodes in Oregon, Frankfurt and Mumbai.