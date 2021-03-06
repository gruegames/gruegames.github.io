---
layout: post
title:  "Setting up AWS for Game Development, Part 1"
date:   2016-09-13 11:31:54 -0700
categories: aws lambda ec2
author: keith
---

So, the first thing you will need to do is create an AWS account. There are plenty of tutorials on how to do that, so I won't go into that here. 

Once your account is created, you are going to want to set up a couple of key things before you start:

1. IAM users with credentials
2. Custom EC2 launch image (called AMIs) 
3. ASG scaling handler

One and two are already covered on the internet as well. But for three, you are left on your own. Why do you need this? Well, if you are a (very) small game studio 
like we are, you don't have the bandwidth to set up every EC2 instance you create for your backend by hand. If you are deploying more dedicated servers because there 
is an influx of traffic, the last thing you want to do is set up every one of them manually.  

To deal with that we've thrown together a AWS Lambda app. [You can find it here.](https://github.com/SeismicGames/lambda_sns_ec2_scaling)

[Here](https://github.com/SeismicGames/lambda_sns_ec2_scaling) is the project with all the steps needed to set up and get started. 

Step 2 will be setting up and using [Terraform](https://www.terraform.io/), so you can start building with EC2 instances.

**UPDATE:** A friend just told me that you can do this with [Cloudwatch Events](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/WhatIsCloudWatchEvents.html) as well. 
I'm not familiar with them so I'll have to take a look. Thanks Brian!

{% include author.html %}
