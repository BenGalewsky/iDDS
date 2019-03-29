# Intelligent Data Delivery Service
As outlined in the IRIS-HEP IDDS whitepaper, we see a need in the community 
to have HEP applications decouple processing applications from files in storage.  

The user story here is _“As part of an experiment on the LHC I want to be able to 
prepare the data I want and make it available in the locations I want so I can 
efficiently use my global resources.”_

We propose developing a new component, the intelligent data delivery service 
(IDDS), in support of this use case.  For this, we make the following assumptions:
* This covers central production of datasets, user analysis, and training of machine learning models. 
* We are explicitly interested in the cross-experiment use case.
* “Preparing data you want” involves specifying a set of data, which may be 
individual ROOT files or a dataset.
* Ability to combine logical datasets to create an omnibus input to support a job.
* Ability to create projections and simple filters of the ROOT files that remove 
data that is not required by the user.
* Data will be cached in a location that optimizes the use of global resources.
