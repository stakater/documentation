## GoCD Abstractions

**![Figure 1: GoCD Abstractions](figures/GoCD-abstractions.png)**

Although it really is a simplification, it tries to convey visually 2 very important and often misunderstood/ignored characteristics of GoCD:

* its 4 built-in powerful abstractions and their relationship: *Tasks* inside *Jobs* inside *Stages* inside *Pipelines*
* the fact that some are executed in parallel (depending on agents availability) while others sequentially:

** Multiple Pipelines run in parallel
** Multiple Stages within a Pipeline run sequentially
** Multiple Jobs within a Stage run in parallel
** Multiple Tasks within a Job run sequentially

## Pipeline Stages

* by default it should be snapshot e.g. 1.1.0-SNAPSHOT;
* identify & set the build number? so, e.g. it will become 1.1.0-21

### Build Stage

* Set new version
* Build (including test)
* Build docker image & publish to docker registry

### Deploy-to-Test-Env Stage

### Deploy-to-Stage-Env Stage

### Publish Stage

* Create release branch in git
* Create tag in git

Approve?

### Promote-to-Prod-Env Stage
