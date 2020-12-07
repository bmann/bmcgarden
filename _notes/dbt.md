---
title: DBT
---
Data Build Tool
> a command line tool that enables data analysts and engineers to transform data in their warehouses more effectively. Today, dbt has ~850 companies using it in production, including companies like Casper, Seatgeek, and Wistia. -- [What, exactly, is dbt?, Tristan Handy, Oct 2017](https://blog.getdbt.com/what--exactly--is-dbt-/)

From the same article:

> dbt code is a combination of SQL and <a href="http://jinja.pocoo.org/">Jinja</a>, a common templating language used in the Python ecosystem. ref() is a function that dbt gives to users within their Jinja context to reference other data models. ref() does two things:
> 
> 1. It interpolates itself into the raw SQL as the appropriate schema.table for the supplied model.
> 2. It automatically builds a DAG of all of the models in a given dbt project.
> 
> Both of these are core to the way that dbt operates. Because dbt is interpolating the locations of all of the models it generates, it allows users to easily create dev and prod environments and seamlessly transition between the two. And because dbt natively understands the dependencies between all models, it can do powerful things like run models in dependency order, parallelize model builds, and run arbitrary subgraphs defined in its model selection syntax.