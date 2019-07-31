# UNGP method service - guide
Guidance and documentation for the UN Global Platform method service.

# UN Global Working Group - Big Data 
The UN Global Working Group on Big Data was created in 2014 for Official Statistics and the Sustainable Development Goals (SDGs) to explore the potential of new technologies and data sources. As part of the Working Group, we are developing the UN Global Platform for Data, Services and Applications. 

The best way to browse the services provided by the platform is in the marketplace:
https://marketplace.officialstatistics.org/

If you are working on new data science applications or exciting data sources that can benefit the global community, do get in touch. These are not limited to what the statistical community has traditionally explored, but include, for example:
- satellite imagery and indicators of pollution, water coverage, etc.
- transport statistics using internet-of-things (IoT) 
- private / public data partnerships on data sources such as social media, retail, employment

# methods.officialstatistics.org
We are partnering with Algorithmia to provide a methods & algorithms service. The aim of this service is for data scientists and statisticians around the world to be able to publish their statistical methods, algorithms and machine learning models, so that they can be reused at a global scale. 

Is the method service what you need? Check this short 50 second video about how to deploy and publish a machine learning model:
https://www.youtube.com/watch?v=-sW8E8psQI4

The service allows you to:
- write methods / algorithms (pretty much anything that you can turn into a callable function) using your own IDE or the one provided by us
- execute methods / algorithms remotely - all the algorithms are published as APIs and can be called using your credentials from anywhere
- publish methods / algorithms - you can publish algorithms with their documentation, versioning, etc. - Algorithmia does do the versioning, dependency management, compilation, scaling and API deployment for you
- share and document - you can document the algorithms on-site, as well as discuss them and share them

# how to get started

Once you have an account, we suggest you start by visiting the Algorithmia learning center:
https://learn.algorithmia.com/
Remember that, when using the method service, you must replace any references to algorithmia.com by  methods.officialstatistics.org (for example, this is the domain under which you publish methods)

We strongly recommend you start by deploying the standard "hello world" algorithm and making changes to it. Can you change its behaviour? Can you publish and version it? Can you make enough changes as to feel compelled to change the interface to it?

The main activities that you will want to do are to develop and publish algorithms using your favoured languages, deploying machine learning models, as well as making this work easier by integrating the method service with your prefered tools (Jupyter Notebooks, data storage buckets and git). These activities are covered in the documentation below.

The most important user guides are:
- How to use your particular client / programming language, as well as set up data
https://methods.officialstatistics.org/developers/clients

- How to connect data sources such as dropbox, buckets by AWS, Azure and Google, as well as database sources
https://methods.officialstatistics.org/developers/data

- How to deploy machine learning models
https://methods.officialstatistics.org/developers/model-deployment

- How to integrate the method service / algorithmia with Jupyter Notebooks
https://blog.algorithmia.com/from-jupyter-notebook-to-fully-scalable-model-now-a-reality/

# advanced functionality

To make the best use of algorithms in the method service, the patterns used are based around RESTful API calls (see documentation on how to design microservices such as https://medium.com/platform-engineer/microservices-design-guide-eca0b799a7e8 ). This means that the algorithms do not store a state. The design principles to build good algorithms focus on simple, reusable and composable functionality. For example, each algorithm should carry out one function well, and these algorithms can later be reused to build more complex algorithms (published separately).

To make the most of calling algorithms in the method service, you might want to keep in mind:

- How to use asynchronous call patterns from your favoured language such as...
... Python https://realpython.com/async-io-python/
... R https://cran.r-project.org/web/packages/promises/vignettes/intro.html

- How to use and deploy event listeners
https://methods.officialstatistics.org/developers/integrations/event_listeners


# looking for testers
You can explore the site at 
https://methods.officialstatistics.org 

and if you are a government (any UN government) data scientist / statistician, do ask for a user account at methods@officialstatistics.org 
