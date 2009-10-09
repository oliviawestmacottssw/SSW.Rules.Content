---
type: rule
title: The application – Do you make the app do the work?
uri: the-application--do-you-make-the-app-do-the-work
created: 2009-10-07T00:01:45.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 

```
Dear Mr Northwind, 

Before installing your application, you need to 
run this script by 
first opening up SQL Management Studio. 
Open the attached script, point it to Northwind and 
execute the script. 

Let me know if you have any issues... 
We worked very hard on this release. 

I hope you’re happy with it. 

Regards, 
Eric Phan
```

Figure: Bad example - run SQL scripts manually 

```
Hi Mr. Northwind, 

Please run the attached Northwind_v5.exe. 

Click Run when the prompt appears. 

Regards,
Eric Phan
```

Figure: Better example - run SQL scripts using another package 

```
Dear Mr Northwind, 

When you run the Northwind v1.0 (Rich Client) it will 
automatically upgrade the database for you. 

Just make sure you have dbo permissions: 
Let me know if you run into any issues, 
otherwise have a great day. 

Regards, 
Eric Phan
```

Figure: Best example - run SQL scripts in the application ![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/UsingSQLDeployControl.png) Figure: Deploy SQL scripts by the application itself 
 We have a tool called [SQL Deploy](http&#58;//www.ssw.com.au/ssw/SQLDeploy) can do this.    
