Let's do a summary

on what we learned for EC2.

So we have created EC2 Instances,

and they were composed of an AMI,

which was defining the operating system.

Then we defined an instance size

where we defined how much CPU power we want,

and how much RAM we want.

We described the storage for our EC2 Instance,

We defined the firewall on our instances

with the security groups,

and finally, a bootstrap script called the EC2 User Data

that was started when the EC2 Instance was started.

So the security groups are attached to EC2 Instances.

And they are a firewall outside of your instance.

And you can define rules to allow which ports

and which API can access your EC2 instance.

For EC2 User Data,

this was a script that we launched

at the first start of an instance

that we used to set up our EC2 instance

to be a web server and say "hello world".

SSH was a way for us to start a terminal

from our computers into our EC2 Instances,

to start issuing commands on port 22.

And once we did it,

we were able to leverage an EC2 Instance role

that was similar to IAM role,

to have our EC2 instance issue commands against IAM.

In terms of the EC2 purchasing options,

we have multiple options you need to know for the exam.

We have On-demand, Spot, Reserved in three flavors

of Standard, Convertible and Scheduled.

We have Dedicated Host and finally Dedicated Instances.

So that's it.

I hope you liked it

and I will see you in the next section.