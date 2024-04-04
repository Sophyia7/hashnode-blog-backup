---
title: "Cloud Computing Explained"
seoDescription: "Get a clear understanding of cloud computing with this guide! Learn about different types of cloud models, CapEx & OpEx, and shared responsibility model. "
datePublished: Thu Apr 04 2024 10:31:15 GMT+0000 (Coordinated Universal Time)
cuid: clul3jyfs000108laeiez98hv
slug: cloud-computing-explained
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1712226235428/d6dbb0ca-70e6-447d-86f1-5e6ffdf5e518.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1712226295223/1f5bd5b0-96cf-4cbd-a5e5-b58361d7ac9f.png
tags: cloud, cloud-computing, hashnode

---

Have you ever wondered what cloud computing is? Or why do companies need cloud engineers to ensure the public uses their applications?

I was curious, too, and started taking the [Azure Learning path](https://learn.microsoft.com/en-us/collections/31gup6jr1ej0r/?wt.mc_id=studentamb_200507) on the Microsoft Learn platform. Every week, I'll share my key takeaways from the week's learnings, hoping that it may inspire others to learn alongside me. 

Today, let's discuss cloud computing! 

# What is Cloud Computing?

![](https://lh7-us.googleusercontent.com/X1gNHBmREm_Lr5Z-R4euauSoFohgxY6GUNtP9QN-_d7vugWBwDyuHXEm3NY95ldGhJCRTH7irVloybL92Muq64RlcA2rrK9i8yPfXZaT0Ba2TCyF8lJJyWzWURub-H9pMnb_YtfTLzSYCIz_lduA0Es align="left")

Cloud computing is all about delivering computing services such as compute power, storage, databases, networks, etc., over the internet for users to access and scale their applications without needing a local or physical infrastructure. 

By using cloud computing, users can save costs. Unlike maintaining a physical infrastructure, cloud computing allows users to pay solely for their use. This reduces the need for upfront investments and ongoing maintenance costs, making it an attractive option for users who need a resource allocation.

## Shared Responsibility Model

In cloud computing, the shared responsibility model is a framework that divides the responsibilities between cloud service providers and consumers(users). It ensures both parties have set roles and expectations, creating a collaborative and efficient cloud computing environment.

Under the shared responsibility model, the cloud provider manages the underlying infrastructure, including the physical data center, network, and host. It includes providing security measures, maintaining hardware and software, and ensuring the availability and performance of cloud services.

On the other hand, the consumer(user) is responsible for managing the cloud services' data, database, and security controls. The consumer also ensures the compliance of applications with regulatory requirements.

Then, we have what we call a *service model*, which is selected by the consumer and determines the level of control and responsibility of the cloud infrastructure.  

For instance, in a Platform as a Service (PaaS) model, the provider manages the operating system, network controls, and infrastructure, while the consumer focuses on deploying and managing applications.

The shared responsibility model enables cloud providers to offer scalable and reliable services while allowing consumers to maintain control over their data and applications. It fosters a cost-efficient collaborative partnership where both parties work together to ensure the success and security of the cloud-based solution.

  
  

# Cloud Models

![](https://lh7-us.googleusercontent.com/foWX7bLMz6n7mSLr4EE8fTZl4Oy-3rz3bGK1iTRIjNtDBl3gIVCoXKCDBfALDqBXB7zynYq1LytLZKp6JcQ-Sv-xIyu2WIWe0LOQtfQF26O9oCEe0TblZSdcF6KOCWafHT1rBwIOy3KPBuO77ZTMFeo align="left")

Cloud models are tiers of how users consume and deploy cloud computing services based on their requirements, needs, level of control, etc. In cloud models, there are three tiers: **Private, Public,** and **Hybrid**. 

### Private Model

Private models are primarily used by a single entity or organization. The internal IT team of the organization has control over the model and its usage. These models cost more because startups and funded companies often use them. Additionally, all services are purchased upfront, even if they are not immediately required, and the IT team assumes the role of a cloud provider. It's important to note that private models can provide enhanced security and customization, making them a suitable choice for organizations with specific data privacy and control requirements.

### Public Model

Public models are the cost-effective options third-party cloud providers like [AWS](https://aws.amazon.com/what-is-aws/), [Azure](https://azure.microsoft.com/en-us), and [GCP](https://cloud.google.com/) offer. These models are ideal for hobbyists, students, and developers working on personal or small-scale projects. Unlike private models, users do not need to purchase all the cloud services the provider provides. Instead, they pay only for the resources they use, making public models a flexible and budget-friendly choice. It's important to note that while public models provide a lower-cost alternative, they may have specific limitations compared to Private models regarding features, customization, and control.

### Hybrid Model

The hybrid cloud model seamlessly blends the features of private and public cloud models, addressing specific organizational needs and preferences. It combines the public cloud's scalability and cost-efficiency with the private cloud's security and control, offering a flexible and secure computing environment. By leveraging the advantages of both models, organizations can optimize their IT infrastructure, enhance security measures, and ensure compliance with regulatory requirements.  

# Capital & Operational Expenditure  

![](https://lh7-us.googleusercontent.com/T9Bn1cYjscx5SPCfwqotr3oWRpYkpjI0acCiUfkQe_El5k02JxagbrqHdjG7fPv9hdi9dVhiJMwg2EdFey-N731GNpPSR02HnP1YISQUKhjqRnGlpDQyW-tUkVLH6iO0-lGHbWBI1h9qxmoK27J0cEc align="left")

When comparing cloud models, there are two types of expenses or costs to consider:

### Capital Expenditure (CapEx)

This cloud cost model is a one-time payment to acquire the necessary resources and services. It includes purchasing software licenses for the private cloud, investing in hardware infrastructure, setting up servers and cooling systems to support the cloud environment, and leasing land for self-managed cloud installations. This upfront investment provides ownership and control over the cloud resources, allowing organizations to control the cloud to their specific needs and requirements.

The CapEx is most suited for companies and organizations using many cloud resources and will scale their applications soon. Here are some advantages of choosing CapEx as a large company:

* Companies that commit to the capital expenditure strategy save costs in the future by bulk purchasing resources.  This may lead to a lower total cost of ownership despite the huge upfront investment. 
    
* Companies with total control and ownership over their hardware and infrastructure can easily customize it to fit their needs and preferences for smoother integration or maximize the compatibility of their cloud ecosystem. 
    
* Companies choosing the capital expenditure approach can safely secure sensitive data in their data centers rather than third-party data centers. They control the encryption standards and the [auditable trails](https://www.investopedia.com/terms/a/audittrail.asp#:~:text=Key%20Takeaways%201%20An%20audit%20trail%20is%20a,suspected%20fraud%20or%20illegal%20financial%20activity.%20More%20items). 
    
* Companies with proprietary infrastructure can easily scale their applications and innovate them in a way their IT team sees fit.  
    

### Operational Expenditure (OpEx)

The OpEx cloud cost model involves the continuous spending on cloud resources over time. It operates similarly to a pay-as-you-go option, where users only pay for the resources they use. This cost model is commonly associated with cloud computing, allowing users to scale their resource consumption based on their actual usage.

In the OpEx, there are some advantages of choosing this over the CapEx model, such as:

* Users do not need to pay an upfront fee,
    
* Users can pay for only the resources they use, 
    
* Users do not need to pay or be concerned about infrastructure maintenance and 
    
* Users can choose when to stop paying for a resource or service. 
    

# Conclusion

To conclude, cloud computing is an easy way to deploy your hobby projects or a small-scale project without considering maintenance costs or buying a data center. Thanks to the cloud providers, you can quickly deploy your to-do app or README generator app and make it accessible for anyone to try and give feedback. 

Did I miss any term? Or did I miss any key takeaway on cloud computing? Please share it in the comments.