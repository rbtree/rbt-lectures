---

### Introduction to Amazon Web Services for Developers
#### Srđan Marković, CTO, Red Black Tree d.o.o. 

---

### How it seamed from my perspective? Developers [Monkey Dance](http://knowyourmeme.com/memes/steve-ballmer-monkey-dance)

![YouTube Video](https://www.youtube.com/embed/V-FkalybggA)

<span style="font-size:0.6em; color:gray">* at Microsoft's 25th Anniversary event in September 2000.</span>

---

### A New Paradigm

#### What is an Application?

- *"Is a computer program designed to perform a group of coordinated functions, tasks, or activities for the benefit of the user (sitting by the computer)"* <!-- .element: class="fragment" -->
- With the introduction of the World Wide Web a new paradigm emerged <!-- .element: class="fragment" -->

+++

### A New Paradigm

#### The Web Application <!-- .element: class="fragment" -->

- Software applications now run on a different computers, continents away <!-- .element: class="fragment" -->
- User access them via HTTP protocol and interract with them through their Web Browser <!-- .element: class="fragment" -->

--- 

### An Example (part 1)

- e.g. Milica, starting a new Web Startup <!-- .element: class="fragment" -->
- developed a shiny new Web App <!-- .element: class="fragment" -->
- running from a web server in her closet <!-- .element: class="fragment" -->
- her Web App is so amazing, getting thousands of users each day <!-- .element: class="fragment" -->
- Milica realises that the server in the closet is not going to work out so well for her <!-- .element: class="fragment" -->
- it's getting hot, stinking the clothes in the wardrobe, starting to run slowly <!-- .element: class="fragment" -->
- all that is hurting her business <!-- .element: class="fragment" -->

+++

### An Example (part 1)

- Milica reaches out to her friend Miloš, and he suggests setting up a server in the Hosting Company <!-- .element: class="fragment" -->
- Milica now has to deal with a long bureaucratic process to provision a new server box <!-- .element: class="fragment" -->
- due to a high running costs of the hardware and services, the server box is shared with many other small companies <!-- .element: class="fragment" -->

+++

### An Example (part 1)

- Milica needs to raise money from an investor (e.g. Tamara) <!-- .element: class="fragment" -->
- but there's still a huge risk with the "guesstimate" of resource needs <!-- .element: class="fragment" -->
- and it all takes a lot of time and money, while Milica's business still can't generate profit <!-- .element: class="fragment" -->

+++

### An Example (part 1)

- a new Cloud Company appears, provides an easy way to setup an account, create elastic infrastructure and start running services instantly <!-- .element: class="fragment" -->
- and all that for a cheap money at the end of the month, only for what's been used <!-- .element: class="fragment" -->
- Milica expands her business easily, both virtually and geographically, being able to go global and conquer the World :) <!-- .element: class="fragment" -->

---

### Back to [Monkey Dance](http://knowyourmeme.com/memes/steve-ballmer-monkey-dance)

Setting up a server required a significant investment of intellectual capital:

- Servers
- Connectivity
- Cooling
- Networking Hardware
- Cabling
- Storage
- Expertise
- Security
- Facilities

+++ 

#### Imagine all the challenges

- e.g. cloning hard drives manually to setup more servers (1 to 2 to 4 to 8 to 8 to 8 to 8) <!-- .element: class="fragment" -->
- alternative was a very limited Web Hosting (e.g. CPanel with cgi-bin, PHP, MySQL, FTP access) <!-- .element: class="fragment" -->
- or expensive and complicated Server Housing (together with all the "horror stories") <!-- .element: class="fragment" -->
- can you feel the [pain](http://stackoverflow.com/a/1732454/819694)? <!-- .element: class="fragment" -->

---

### What is the "Cloud" 

#### The Buzz-word of the century <!-- .element: class="fragment" -->

- service oriented architecture <!-- .element: class="fragment" -->
- the infrastructure service for the World <!-- .element: class="fragment" -->
- elastic computing <!-- .element: class="fragment" -->
- storage in the Cloud <!-- .element: class="fragment" -->
- security and compliance <!-- .element: class="fragment" -->
- pricing and availability (going from *"high upfront costs"* to *"no upfront and usage-based costs for each month"*) <!-- .element: class="fragment" -->

+++

### What is the "Cloud" 

#### Developers building systems with changed mindset <!-- .element: class="fragment" -->

- from *"assume reliable infrastructure"* to *"expect infrastructure failure"* <!-- .element: class="fragment" -->
- take a moment to think about the difference as a [Developer](http://knowyourmeme.com/memes/steve-ballmer-monkey-dance) <!-- .element: class="fragment" -->
- can you feel the [relief](http://knowyourmeme.com/memes/feels-good)? <!-- .element: class="fragment" -->

---

### AWS History

- 2002 AWS born out of their own need to support [amazon.com](https://amazon.com) expansion <!-- .element: class="fragment" -->
- 2003 engineer Chris Pinkham started trying to build an *"infrastructure service for the world"* <!-- .element: class="fragment" -->
- pitched to Jeff Bezos, wrote paper with another engineer Benjamin Black <!-- .element: class="fragment" -->
- 2004 AWS launched their first service (SQS) <!-- .element: class="fragment" -->
- 2006 Jeff Bezos talked about EC2 and S3 <!-- .element: class="fragment" -->
- 2007 Gazda and I attended [Microsoft Sinergija 07](http://knowyourmeme.com/memes/steve-ballmer-monkey-dance) in Novi Sad (completely irrelevant) <!-- .element: class="fragment" -->

--- 

### Back to the Example (part 2)

#### Here's what Milica would need to invest to start running her Web App before Cloud <!-- .element: class="fragment" -->

- $ server for Web App <!-- .element: class="fragment" -->
- $ probably another Server for Database <!-- .element: class="fragment" -->
- $ network hardware and cables <!-- .element: class="fragment" -->
- $$ probably a dedicated room <!-- .element: class="fragment" -->
- $ high-speed Internet connection <!-- .element: class="fragment" -->
- Milica (and her investor Tamara) would need to cash upfront $$$$$$ <!-- .element: class="fragment" -->
- and all that before earning a single $ from her business <!-- .element: class="fragment" -->

+++

### Back to the Example (part 2)

#### Here's what Milica would need to invest upfront to run her Web App on AWS <!-- .element: class="fragment" -->

- nothing <!-- .element: class="fragment" -->
- we've already mentioned AWS's pricing, going from *"high upfront costs"* to *"no upfront and usage-based costs for each month"* <!-- .element: class="fragment" -->

+++ 

### Demo (part 1)

#### [Amazon Web Services Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html)

+++ 

### Back to the Example (part 3)

- let's imagine Milica's application becomes wildly popular <!-- .element: class="fragment" -->
- her best friends (Martina and Nemanja) share it Facebook, Instagram, Pinterest, Snapchat <!-- .element: class="fragment" -->

+++ 

### Back to the Example (part 3)

- eventually, [Zorannah](http://www.pulsonline.rs/puls-poznatih/njeno-carstvo-ovde-zivi-najpoznatija-srpska-blogerka/rh5s0ns) hears about it and writes a blog post <!-- .element: class="fragment" -->
- everyone goes mad and wants a piece of Milica's Web App <!-- .element: class="fragment" -->
- poor server becomes a solid heat and noise generating appliance <!-- .element: class="fragment" -->

+++ 

### Back to the Example (part 3)

- buying a new server takes a lot of time, Milica risks to make [Zorannah](http://www.pulsonline.rs/puls-poznatih/njeno-carstvo-ovde-zivi-najpoznatija-srpska-blogerka/rh5s0ns) change her mind and write another blog post! <!-- .element: class="fragment" -->
- even provisioning a new server in a big Hosting Company takes time <!-- .element: class="fragment" -->

+++

### Back to the Example (part 3)

- with AWS Elastic Compute Cloud, Milica can scale her infrastructure almost instantly, while still paying only what she uses <!-- .element: class="fragment" -->
- eventually, Milica's Web App becomes popular in China - no problem, AWS has a Region in Asia, too <!-- .element: class="fragment" -->

---

### How's AWS organized

- Regions <!-- .element: class="fragment" -->
- Availability Zones (AZ) <!-- .element: class="fragment" -->
- Edge Locations (DNS, Services) <!-- .element: class="fragment" -->

+++

### How's AWS organized

- "Pods" in secret locations, controlled physical access, best in class datacenter security, video surveillance <!-- .element: class="fragment" -->
- hardware refresh cycle to avoid component failure <!-- .element: class="fragment" -->
- always-on monitoring system <!-- .element: class="fragment" -->
- security certifications and compliance (including some "**ISO 27001** standard") <!-- .element: class="fragment" -->

+++ 

### Demo (part 2)

#### [AWS named as a leader in the Infrastructure as a Service (IaaS) Magic Quadrant report for 6th consecutive year](https://aws.amazon.com/resources/gartner-2016-mq-learn-more/)

+++

### How's AWS organized

- Security Groups, VPC, Direct Connect, VPN Access, Dedicated Server, Import/Export <!-- .element: class="fragment" -->
- Identity and Access Management (IAM) <!-- .element: class="fragment" -->
	- Users, Groups, Roles <!-- .element: class="fragment" -->
	- Access to all AWS resources <!-- .element: class="fragment" -->
	- Multi-Factor Authentication (MFA) <!-- .element: class="fragment" -->
	- API access (AWS CLI, Terraform.io) <!-- .element: class="fragment" -->

---

### Core services of AWS

- Elastic Compute Cloud (EC2) <!-- .element: class="fragment" -->
- Relational Database Service (RDS) <!-- .element: class="fragment" -->
- Simple Storage Service (S3) <!-- .element: class="fragment" -->
- DNS Service (Route 53) <!-- .element: class="fragment" -->

+++

### Back to the Example (part 3)

#### [AWS Demo (part 3)](https://console.aws.amazon.com/console/home)

-- 

### More services of AWS

- Virtual Private Cloud (VPC) <!-- .element: class="fragment" -->
- CDN Service (CloudFront) <!-- .element: class="fragment" -->
- Monitoring (CloudWatch) <!-- .element: class="fragment" -->

+++

### Back to the Example (part 4)

#### [AWS Demo (part 4)](https://console.aws.amazon.com/console/home)

--- 

### All services of AWS

#### [AWS Demo (part 5)](https://aws.amazon.com)

+++

### Back to the Example (not really)

#### Would you like to see more?
 
- My ideas include, but are not limitted to <!-- .element: class="fragment" -->
	- going into more details about characteristics and configuring VPC, NAT Instances and Gateways, ELB, EBS, EFS, Glacier, ElastiCache, Auto Scaling, Security, etc <!-- .element: class="fragment" -->
	- Demoing another more complex real-case scenario (for one of our clients) <!-- .element: class="fragment" -->
	- introducing and going into more details about [AWS Lightsail](https://amazonlightsail.com), [DigitalOcean](https://www.digitalocean.com), [Microsoft Azure](https://azure.microsoft.com), [Google Cloud Platform](https://cloud.google.com), and other Cloud services <!-- .element: class="fragment" -->
	- Demoing AWS CLI and other advanced tools (Terraform.io) <!-- .element: class="fragment" -->
- Feel free to suggest topics for more AWS Lectures (part 2, 3, etc) <!-- .element: class="fragment" -->

---

### Questions?

- Feel free to contact me via email after the Lecture <!-- .element: class="fragment" -->

---

### How it seams now? ["Šta je to programiranje" by Radiša Nedeljković](https://www.youtube.com/watch?v=A7p-VnzkRoI&t=20s)

![YouTube Video](https://www.youtube.com/embed/A7p-VnzkRoI)

<span style="font-size:0.6em; color:gray">* negde u Srbiji, oktobar 2014.</span>
