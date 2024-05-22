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
##### B/G Env. Creation has 3 steps, which take approximately 45 to 50 mins, 
###### Creating a read replica of the source

###### Db engine version upgrade
###### Configure backups

Note:

Above observation of B/G creation time is tested with one table with 103,250 records.
If any of the above steps fail, b/g deployment tries to fix the issue.
![](https://github.com/KHawaldar/poc/blob/master/images/failed_to_apply.png)

Before upgrading the MySQL 8.0 version, it checks the prepatch compatibility.
These are the checks it will carry before upgrading to 8
{code}
1) Usage of old temporal type
No issues found.

2) Usage of db objects with names conflicting with new reserved keywords
No issues found.

3) Usage of utf8mb3 charset
The following objects use the utf8mb3 character set. It is recommended to convert them to use utf8mb4 instead, for improved Unicode support.
More Information:
https://dev.mysql.com/doc/refman/8.0/en/charset-unicode-utf8mb3.html

mysql - schema's default character set: utf8


4) Table names in the mysql schema conflicting with new tables in 8.0
No issues found.

5) Partitioned tables using engines with non native partitioning
No issues found.

6) Foreign key constraint names longer than 64 characters
No issues found.

7) Usage of obsolete MAXDB sql_mode flag
No issues found.

8) Usage of obsolete sql_mode flags
No issues found.

9) ENUM/SET column definitions containing elements longer than 255 characters
No issues found.

10) Usage of partitioned tables in shared tablespaces
No issues found.

11) Circular directory references in tablespace data file paths
No issues found.

12) Usage of removed functions
No issues found.

13) Usage of removed GROUP BY ASC/DESC syntax
No issues found.

14) Removed system variables for error logging to the system log configuration
No issues found.

15) Removed system variables
No issues found.

16) System variables with new default values
No issues found.

17) Schema inconsistencies resulting from file removal or corruption
No issues found.

18) Issues reported by 'check table x for upgrade' command
No issues found.

19) The definer column for mysql.events cannot be null or blank.
No issues found.

20) Tables with dangling FULLTEXT index reference
No issues found.

21) Routines with deprecated keywords in definition
No issues found.

22) DB instance must have enough free disk space
No issues found.

23) Creating indexes larger than 767 bytes on tables with redundant row format might cause the tables to be inaccessible.
No issues found.

24) The tables with redundant row format can't have an index larger than 767 bytes.
No issues found.

25) Column definition mismatch between InnoDB Data Dictionary and actual table definition.
No issues found.

{code}

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
