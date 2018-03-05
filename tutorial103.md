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

Since  you didn't check the box to add any request parameters, the wizard moves ahead to configuring the request which we did indicate we wanted to do when we checked the request payload box on the previous screen.

Choose the radio button **JSON Sample** so you can supply a sample request format using JSON (Java Script Object Notation). Also select **JSON** as the type of payload  you want the endpoint to receive. 

Click on the link called `<<<< inline >>>>` after enter sample JSON to supply a sample format.

![Screen Shot 2018-03-05 at 8.33.38 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.33.38 AM.png)

Copy and paste the following text in the box that pops-up:

{  "PersonId" : "300000157866799",  "Name" : "Lloyd"  }

Then click the **OK** button.

![Screen Shot 2018-03-05 at 8.41.20 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.41.20 AM.png)

Choose **Next** to move to the next configuation item in the wizard.

Since no more configuration is required, the wizard shows the **Summary** tab.

![Screen Shot 2018-03-05 at 8.46.13 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.46.13 AM.png)

Click **Done**

The integration is not finished yet, but click on the **Save** button to save the work you have done so far.

![Screen Shot 2018-03-05 at 8.47.39 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.47.39 AM.png)



Notice that the percentage completion indicator has increased but it is not yet at 100% since we have not configured a connection to invoke.

Drag the **File <your initials>** connection to the right hand side on top of **Drag and Drop an Invoke** 

A wizard will pop-up allowing you to configure the file adapter connection. 

Call the endpoint **LogPersonToFile**

Leave the default options: 

Yes - define a schema for this endpoint and 

Create a new schema from a CSV file

![Screen Shot 2018-03-05 at 8.51.41 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.51.41 AM.png)

Click the **Next** button to move to the next section of the configuration wizard.

Specify the Output Directory: `/data/tutorial103`

*Note: This is a directory on the computer where the agent is running since this adapter is configured to use an agent.* 

Specify a File Name Pattern: `<your initials>_Person_%SEQ%.txt`

![Screen Shot 2018-03-05 at 8.57.36 AM](images/tutorial103/Screen Shot 2018-03-05 at 8.57.36 AM.png)

Then click the **Next** button.

Create a file on your own computer that is called **PersonId.csv** with the following two lines of content. 

`PersonId,Name`
`300000157866789,Lloyd`

Click on the **Browse… button and choose the file that you created. 

Enter the Record Name: `Person`

Enter the Recordset Name: `People`

![Screen Shot 2018-03-05 at 9.09.56 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.09.56 AM.png)

Notice that the fields PersonId and Name were populated as Mandatory and the type format String was set.  We will leave these defaults, but in the future you could change as needed. 

Click the **Next** button. The wizard moves to the summary section. 

![Screen Shot 2018-03-05 at 9.15.07 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.15.07 AM.png)

Then click the **Done** button.  

Notice that the integration updates and the percentage completion updates. Click the **Save** button.

![Screen Shot 2018-03-05 at 9.15.53 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.15.53 AM.png)

You will find in the middle an icon linking the two connections called **Click Below to Create Map**

Click that icon to start to create a mapping. Click the **+ icon** to create a new mapping. 

![Screen Shot 2018-03-05 at 9.18.27 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.18.27 AM.png)

A mapping wizard will appear. Drag from the `PersonId` in the source to the `PersonId` under `People/Person`. 

![Screen Shot 2018-03-05 at 9.20.52 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.20.52 AM.png)

![Screen Shot 2018-03-05 at 9.22.33 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.22.33 AM.png)

Do the same for the `Name` field.

![Screen Shot 2018-03-05 at 9.25.18 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.25.18 AM.png)

Then click the **Validate** button and then the **Close** button.

![Screen Shot 2018-03-05 at 9.26.59 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.26.59 AM.png)

Click the **Save** button. Notice the completion percentage is not yet at 100%. This is because we need to configure the tracking option. Choose the menu next to the Last Saved field. 

![Screen Shot 2018-03-05 at 9.29.42 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.29.42 AM.png)



Choose **Tracking**

![Screen Shot 2018-03-05 at 9.31.10 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.31.10 AM.png)

Drag the `PersonId` from the left to the tracking field. 

![Screen Shot 2018-03-05 at 9.32.09 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.32.09 AM.png)

Drag the `Name` to the second tracking field.

![Screen Shot 2018-03-05 at 9.32.17 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.32.17 AM.png)

Click **Save**

![Screen Shot 2018-03-05 at 9.36.33 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.36.33 AM.png)

Notice that the the integration is now at 100% and ready to activate. Click **Close**

Notice that there is an actions menu associated with this integration. 

![Screen Shot 2018-03-05 at 9.39.47 AM](images/tutorial103/Screen Shot 2018-03-05 at 9.39.47 AM.png)

You can activate from this menu or use switch button to activate the integration. 

A pop-up box will appear to allow you to configure some options for the activation. 

![Screen Shot 2018-03-05 at 10.05.45 AM](images/tutorial103/Screen Shot 2018-03-05 at 10.05.45 AM.png)

Uncheck the box to contribute to the recommendations engine. 

Check the box to **Enable Tracing** and **Include payload**

In a production environment, you may not want to enable tracing if you have sensitive information that you do not want appearing in the logs, but for development of the integrations it's good to do until you are sure that your integration is working as expected. It will make debugging any problems much easier. 

A message appears showing that the integration is activating.

![Screen Shot 2018-03-05 at 10.09.27 AM](images/tutorial103/Screen Shot 2018-03-05 at 10.09.27 AM.png)

You will need to click on the **Refresh** icon to see if the integation has finished activating. 

![Screen Shot 2018-03-05 at 10.10.54 AM](images/tutorial103/Screen Shot 2018-03-05 at 10.10.54 AM.png)

Then you can click on the link provided to see the metadata related to the integration. A new tab should open in your browser which contains all the details about this integration including the Endpoint URL, the Swagger definition and the resource details including a sample of the request. 

![Screen Shot 2018-03-05 at 10.13.21 AM](images/tutorial103/Screen Shot 2018-03-05 at 10.13.21 AM.png)The integration is now ready to run. It's best to use a tool for testing REST interfaces (for example Postman or SOAP-UI) to test the interface. In this tutorial, we will use Postman which is available as a stand-alone install or a Chrome browser plug-in. 

If you don't already have a tool that you are very comfortable using, you should download and install Postman from: https://www.getpostman.com/apps



