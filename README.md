# Security Engineer Takehome Exercise

Recommended time: approximately 4 hours

## Part 1

The vc_data directory contains sample data files which simulate a data lake containing documents at two levels of sensitivity

1.  Public: news reports, announcements, press releases, presentations etc that can plausibly be retrieved from any public data source
2.  Confidential: internal or confidential company documents, memos, projections, or presentations that should not be revealed to the public

### Deliverable
A Python script that 
- Analyzes the files to classify data into categories: 'Public', 'Confidential'
- Produces a summary report of the types and numbers of documents and their classifications categories

## Part 2:
Suppose we now have 100x of these kinds of files, being dropped into our data lake AWS S3 bucket on a daily basis by a number of different sources. We also have different machine learning models running on AWS SageMaker being trained on either all data (public + confidential) or purely public data. 

### Deliverable
- A system architecture diagram of an automated system (ideally based on AWS tools) to classify and tag existing and incoming/uploaded files based on sensitivity levels, on some periodic cadence.
- Example IAM role(s)/policies to enforce appropriate security boundaries for ML models
  - allow SageMaker models tagged with confidential to access to all data
  - all other SageMaker models without confidential tag to access only data classified as public
- A brief document with additional recommendations for 
  - prevent/mitigate data breaches
  - addressing internal and external threats to data confidentality and integrity
  - any other recommendations as deemed appropriate
