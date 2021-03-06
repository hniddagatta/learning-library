# Create and Populate Database Tables

## Introduction

This lab will walk you through the steps to create and populate database tables containing customer, account, purchase, and relationship data. You will then run some graph algorithms and queries and visualize the results in subsequent labs.

Estimated Lab Time: 2-3 minutes

### Objectives

In this lab, you will:
* Create and populate database tables
* Run graph algorithms and queries and visualize the results

### Prerequisites

* This lab assumes that you have successfully completed the lab - Setup Oracle Database in Docker

## **STEP 1:** Load the data

1. Connect to the database as "sys" user, and create a user, "customer_360".

    ```
    $ <copy> docker exec -it oracle-db sqlplus sys/Welcome1@localhost:1521/orclpdb1 as sysdba</copy>
    ```

2. At the SQL prompt enter:

    ```
    <copy>
    @/graphs/customer_360/create_user.sql
    EXIT
    </copy>
    ```

3. Connect to the database as the "customer_360" user, and create tables.

    ```
    $ <copy>docker exec -it oracle-db sqlplus customer_360/Welcome1@localhost:1521/orclpdb1</copy>
    ```

4. At the SQL prompt enter:

    ```
    <copy>
    @/graphs/customer_360/create_tables.sql
    EXIT
    </copy>
    ```

You may now proceed to the next lab and create the graph.

## Acknowledgements ##

* **Author** -  Jayant Sharma, Product Manager
* **Contributors** - Ryota Yamanaka
* **Last Updated By/Date** - Anoosha Pilli, Database Product Management, October 2020

## Need Help?
Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/livelabsdiscussions). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.

