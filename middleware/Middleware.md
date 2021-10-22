### Notes + Question Answer of Middleware

Three Tier Architecture -

Three-tier architecture, which separates applications into three logical and physical computing tiers, is the predominant software architecture for traditional client-server applications.

Basically the three tier architecture Contains -

1- Presentation Tier

2- Application Tier

3- Data or database tier

The Main benefit of three-tier architecture is that because each tier runs on its own infrastructure, each tier can be developed simultaneously by a separate development team, and can be updated or scaled as needed without impacting the other tiers.

### Tier vs. layer

In discussions of three-tier architecture, *layer* is often used interchangeably – and mistakenly – for *tier*, as in 'presentation layer' or 'business logic layer.' 

They aren't the same. A 'layer' refers to a functional division of the software, but a 'tier' refers to a functional division of the software that runs on infrastructure separate from the other divisions. The Contacts app on your phone, for example, is a *three*-*layer* application, but a *single-tier* application, because all three layers run on your phone.

The difference is important, because layers can't offer the same benefits as tiers.

Workflow Diagram :

![  Architectural pattern for a three-tier application  ](https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/images/image2.png)

**Ques- Do application server only process dynamic pages**

No, It can do both , An application server typically can deliver web content too, but its primary job is to enable interaction between end-user clients and server-side application code—the code representing what is often called *business logic*—to generate and deliver dynamic content, such as transaction results, decision support, or real-time analytics. 

**Ques- What is a web container?**

A **web container** is the component of a web server that interacts with Java servlets. A web container manages the life cycle of servlets; it maps a URL to a particular servlet while ensuring that the requester has relevant access-rights.

**Ques - What are Servlets?**

*Servlets* are the Java programs that run on the Java-enabled web server or application server.

**Ques - Use of Database server?**

Database servers are **used to store and manage databases that are stored on the server** and to provide data access for authorized users

**Ques - What is recovery in Database server?**

taking backup of data at different regions 

**Ques- Deployment Descryptor?**

A deployment descriptor (DD) refers to **a configuration file for an artifact that is deployed to some container/engine**. ... It directs a deployment tool to deploy a module or application with specific container options, security settings and describes specific configuration requirements.

