
<h1>How to host Static Website on Amazon S3</h1>
Hosting a static website on Amazon S3 (Simple Storage Service) is a popular and cost-effective solution. A static website consists of fixed content like HTML, CSS, JavaScript, images, and videos. With no server-side scripting like PHP or databases.
<h2>INTRODUCTION</h2>
A static website is a type of website that delivers pre-built content to users — typically written in HTML, CSS, and JavaScript — without the need for server-side processing or databases. Unlike dynamic websites that generate content on the fly, static websites serve the same content to every visitor.
One of the most efficient and affordable ways to host a static website is by using Amazon S3 (Simple Storage Service). Amazon S3 is a cloud-based object storage service offered by Amazon Web Services (AWS). It allows users to store and retrieve data at any time, from anywhere on the web. By enabling static website hosting in Amazon S3, you can turn a regular S3 bucket into a web host that delivers your site to users worldwide — without the need to manage any servers. This method is scalable, reliable, and ideal for portfolios, documentation sites, blogs, and simple business websites.
Amazon Route 53 is a scalable and highly available Domain Name System (DNS) web service by AWS. It helps you manage domain names and route traffic to various AWS services, including S3, EC2, CloudFront, and more. Works seamlessly with S3 static website hosting.
<h2>ARCHITECTUAL DIAGRAM</h2>

![static website Architectual design](https://github.com/user-attachments/assets/f0954328-02d2-404e-b3be-e3ad264f7b7c)

<h3>ADVANTAGES OF HOSTING A STATIC WEBSITE ON AN AMAZON S3 BUCKET</h3>
<h5>•	Pay-as-you-go pricing - You only pay for what you use (storage and bandwidth).</h5>
<h5>•	Handles unlimited traffic without any extra configuration.</h5>
<h5>•	S3 provides 99.999999999% (11 9’s) durability for stored objects.</h5>
<h3>PREREQUISITES</h3>
<h5>•	AWS account</h5>



![AWS account Sign in](https://github.com/user-attachments/assets/49b6fb82-8174-4ebc-a040-0c2bba7500ff)



<h2>Here's a step-by-step breakdown of how it works and how to do it:</h2>
<h2>1.	Go to AWS S3 Console</h2>

![Navigate to S3](https://github.com/user-attachments/assets/62447230-c6f3-4a36-8548-b39f7c7e8ee5)

<h2>2.	Click "Create bucket"</h2>
<h5>•	Name the bucket exactly the same as your domain name (my-static-website007) 
NB: Bucket name must be unique</h5>
<h5>•	Choose region</h5>
<h5>•	Uncheck “Block all public access” under permissions</h5>
<h5>•	Acknowledge the warning and proceed</h5>
<h5>•	Proceed to Create Bucket</h5>



![bucket details](https://github.com/user-attachments/assets/e0cf81c2-b2e5-4cac-a65a-46d99bdd7bc1)




<h2>3.	Upload Your Website Files</h2>
<h5>•	Upload the website contents to your S3 bucket including sub-folders.</h5>
<h5>•	Use folders if needed (css, index.html, images etc.,)</h5>


![file uploads](https://github.com/user-attachments/assets/54c1b39b-70b9-42a5-9362-9e376afe9800)


<h2>4.	Click Make Public Read using ACL</h2>
<h5>•	Go to Object</h5>
<h5>•	Select index.html</h5>
<h5>•	Go to Actions, from the dropdown select make public using ACL</h5>


![make public](https://github.com/user-attachments/assets/65149d0a-641f-4127-a342-8cf2be456501)




<h2>5.	Enable Static Website Hosting<h2/>
<h5>•	Go to bucket</h5>
<h5>•	Properties</h5>
<h5>•	Scroll to Static website hosting</h5>
<h5>•	Click Edit</h5>
<h5>•	Choose Enable</h5>
<h5>•	Set:</h5>
<h6>Index document: index.html</h6>
<h6>(Optional) Error document: error.html</h6>
<h5>•	 Click Save changes</h5>
<h5>•	AWS provides a website endpoint URL like: http://my-staticwebsite007.s3-website-us-east-1.amazonaws.com/</h5>

![edit static website](https://github.com/user-attachments/assets/a9aa7d3c-2f10-470e-acb2-aac567d1b514)


<h2>6.	Hosted Static Website</h2>

![Website](https://github.com/user-attachments/assets/f30c29f1-bb9a-43ba-a722-1474f66d45ab)
