# Hasura-on-Render

This repo is for use with [Render](http://render.com) to create a basic 
[Hasura GraphQL Engine](http://hasura.com) deployment.

This will create a database named ``hasura``, create a web service named 
``hasura`` from the latest Hasura GraphQL Engine docker image, and points 
the web service at the database. You'll then be able to access the Hasura 
Console from the public web.

## How to use

To get started, fork this repository so that it is in your own Github namespace.

### With Render YAML (easiest)

From within the Render Dashboard, choose to create from YAML and select this repository. 

### Manually

From within the Render Dashboard, create a database named ``hasura``. Copy 
the Internal Connection String. Create a web service named ``hasura`` based 
on this repository. Upon creation of the web service, create the following 
two environment variables:
 - name: ``HASURA_GRAPHQL_DATABASE_URL`` value: the Internal Connection String 
(or database URL) of the newly created database
 - name: ``HASURA_GRAPHQL_ENABLE_CONSOLE`` value: ``true``
