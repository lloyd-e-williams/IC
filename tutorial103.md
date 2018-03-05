---
layout: post
title:  "Tutorial 103: REST to File Integration"
date:   2018-02-04 19:34:21 -0500
categories: oic tutorial 
typora-copy-images-to: /images/tutorial103
---
This tutorial explains how to create an integration that will use the REST adapter to accept a request that will trigger the File adapter to write a file. You will write a file to an on-premise system so the file adapter has been configured to use an agent.  

From the designer menu, choose **Integrations**. Click on the **Create** button to start creating a new integration:

![Screen Shot 2018-03-05 at 7.59.50 AM](./images/tutorial103/Screen Shot 2018-03-05 at 7.59.50 AM.png)

Choose the **Style: Template with Pattern: Map Data**

![Screen Shot 2018-03-05 at 8.02.54 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.02.54 AM.png)

Name the Integration:  `REST to File Integtration <your initials>`

The identifier and version number are automatically populated. Optionally, supply a description.

Supply the Package Name `<your initials>_WORKSHOP`as shown in the picture

![Screen Shot 2018-03-05 at 8.06.38 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.06.38 AM.png)

Click the **Create** button.

The integration has been created. Click the **Save** button to save the work so far. 

![Screen Shot 2018-03-05 at 8.09.23 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.09.23 AM.png)

Now, you will work on the integration. 

Type your initials in the connections search box on the right to find the connections that you previously created.

![Screen Shot 2018-03-05 at 8.11.58 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.11.58 AM.png)

Choose the `Local REST <your initials>` connection.

![Screen Shot 2018-03-05 at 8.15.03 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.15.03 AM.png)

A wizard will appear to allow you to start configuring the REST interface. 

Call the endpoint **`WritePersonToFile`**

Provide a description for the endpoint.

The endpoint's relative resource URI is: `/log/person`

Select `POST`as the action that the endpoint performs.

Check the box: `Configure a request payload for this endpoint` 

Verify that your configuration matches the screenshot below before clicking next. 

![Screen Shot 2018-03-05 at 8.25.55 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.25.55 AM.png)

Based upon your selections the wizard will take you to the next confguration screen. You will only need to complete some of the configuration items listed down the left hand side of the wizard.



The percentage completion indicator should change to 100%. Click on the **Save** button.

Then click the **Close** button.

The integration is now ready to activate.