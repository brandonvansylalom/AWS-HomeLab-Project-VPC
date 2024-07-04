<h1>AWS Project - Creating and deploying a VPC and EC2 Instance on AWS</h1>

<h2>Description</h2>
This is another entry-level/beginner friendly exploring virtual private cloud (VPC) technologies, specifically in AWS. A VPC is a logically isolated network that would operate similarly to a traditional network like in a standard data center, with the benefits of having a highly scalable architecture in addition to having segregrated resources to specific users. Additionally, I will deploy a basic EC2 instance on the VPC as well.
  
<h2>Lab walk-through/details:</h2>

<p align="center">

<b> Starting at the VPC dashboard:

- <b> Signed in to the AWS management console and search for VPC.

<img src="https://imgur.com/TlsA4dw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<b> Creating the VPC:
- <b> Select Create VPC
- <b> Choose VPC only
- <b> Name the VPC
- <b> Set a default IPV4 CIDR of 10.0.0.0/24
- <b> No IPV6
- <b> Defaults for everything else

<img src="https://imgur.com/egG0JIg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After creating the VPC, the VPC dashboard on the left hand side will have information on the routing tables, subnets, Internet gateways, and more, which can be reviewed or modified as needed/desired.

<img src="https://imgur.com/krKhnEx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<b> Launching an EC2 Instance on the VPC:
- <b> Search EC2 on the Services/search bar on the management console.
- <b> Find Launch Instance.
- <b> Select the Amazon Linux AMI for the image/OS (keeping it cheap and free under the free tier for project and labbing purposes).
- <b> By default, AWS selects and has options enabled with the Free Tier thresholds.
- <b> On Network Settings, select the VPC that was created earlier.
- <b> Created a Subnet
- <b> Left storage settings at default
- <b> Added Tags (VansylalomWebServer), which will help identify the instance once launched
- <b> For Security Groups, left it at default via the wizard creation. This allows you to connect to the instance and any other IP's to connect (indicated by the 0.0.0.0/0) via SSH. Typically not advisable in a real production environment but safe for labs/projects, as a in real setting, you'd authorize only certain IP addresses to access your instance.

<img src="https://imgur.com/7KyS5er.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/0jPPUbX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/qIpXoci.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/JVQ0wkm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<b> Key pair establishment before launching the instance:
- <b> Find the key pair section.
- <b> Select Create New Key pair.
- <b> Label it as master1. 
- <b> Afterwards, create it. It'll download a key to your workstation (downloads) that must be kept somewhere safe, accessible and memorable to access the instance. If you do not remember or have your key pair, you can't access the instance and may have to delete it.
- <b> When done, review all previous steps if needed and revise as needed. Launch your instance.

<img src="https://imgur.com/S0LztNi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/mCiAQrN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<b> Reviewing the Instance/details
- <b> Instance should now be available to view and running.
- <b> Make sure to stop/delete the instance to prevent undesired billing.

<img src="https://imgur.com/elhco3X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
