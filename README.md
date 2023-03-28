# Axelor Application without git submodules

Ce code est utile dans le cadre de la mission de @patou et @hgwood chez leur client sur le premier semestre 2023. Ce repo peut être archivé au-delà de cette période.

## Building and publishing modules to the local Maven repository

- Checkout `master`
- Follow instructions [here](https://docs.axelor.com/abs/5.0/install/source/windows.html#build-from-source)
- Run `./gradlew publishToMavenLocal`

## Building and running the application without submodules

- Checkout `no-submodules`
- Run `./gradlew build`: this should successfully build a war file in `./build/libs`
- Run `docker compose up`: the app should be available on `http://localhost:8889` after a few minutes

# Original README

> Axelor Open Suite
> ================================
> 
> Axelor Open Suite reduces the complexity and improve responsiveness of business processes. Thanks to its modularity, you can start with few features and  then activate other modules when needed.
> 
> Axelor Open Suite includes the following modules :
> 
> * Customer Relationship Management
> * Sales management
> * Financial and cost management
> * Human Resource Management
> * Project Management
> * Inventory and Supply Chain Management
> * Production Management
> * Multi-company, multi-currency and multi-lingual
> 
> Axelor Open Suite is built on top of [Axelor Open Platform](https://github.com/axelor/axelor-open-platform)
> 
> 
> Installation
> ================================
> 
> To compile and run from source, you will need to clone Axelor Open Suite modules, which is a
> [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) repository, using following commands:
> 
> ```bash
> $ git clone git@github.com:axelor/open-suite-webapp.git
> $ cd open-suite-webapp
> $ git checkout master
> $ git submodule init
> $ git submodule update
> $ git submodule foreach git checkout master
> $ git submodule foreach git pull origin master
> ```
> 
> You can find more detailed [installation instructions](https://docs.axelor.com/abs/5.0/install/index.html) on our documentation.
> 
