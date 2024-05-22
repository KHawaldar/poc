# RDS Migration- Blue/Green Deployment.
* [Knowledge Base](#knowledge-base)
  * [Blue Green Deployment](#blue-green-deployment)
    * [Blue Green Environment Creation](#blue-green-environment-creation)
    * [Switch Over](#switch-over)
      * [Cancel to Switch over](#cancel-to-switch-over)
      * [Proceed to Switch over](#proceed-to-switch-over)
        * [Choose the quiet time to switch over to production env](#choose-the-quiet-time-to-switch-over-to-production-env)
      * [Success Switch over](#success-switch-over)
      * [FAQ on Switch over](#FAQ-on-switch-over)
* [Demo](#demo)
  * [Prerequisite](#prerequisite])
  * [Creating a blue green deployment](#creating-a-blue-green-deployment)
  * [Connecting to green db instance via MySQL workbench in Integration env](#connecting-to-green-db-instance-via-mySQL-workbench-in-integration-env)
  * [Switching a Blue Green deployment](#switching-a-blue-green-deployment)
  * [Check Pods](#check-pods)
  * [Re deploy CloudFormation](#re-deploy-cloudformation)
  
## Knowledge Base

### Blue Green Deployment
#### Step 1: Blue env

![](https://github.com/KHawaldar/poc/blob/master/images/blue-en.png)


#### Step 2: B/G deployment 

![](https://github.com/KHawaldar/poc/blob/master/images/pic3.png)
#### Step 3: Switch over started
![](https://github.com/KHawaldar/poc/blob/master/images/pic.png)
#### Step 4: App connected to greem

![](https://github.com/KHawaldar/poc/blob/master/images/pic1.png)

#### Step 5: B/G deployment success
![](https://github.com/KHawaldar/poc/blob/master/images/green_to_blue.png)

#### Blue Green Environment Creation

#### Switch Over

##### Cancel to Switch over

##### Proceed to Switch over

###### Choose the quiet time to switch over to production env

##### Success Switch over

##### FAQ on Switch over

## Demo

### Prerequisite

### Creating a blue green deployment

### Connecting to green db instance via MySQL workbench in Integration env

### Switching a Blue Green deployment

### Check Pods

### Re deploy CloudFormation
