Let's talk about these firewalls

around our EC2 instances.

So we briefly configured one in the previous lecture

but security groups yet again, are going to be fundamental

into doing network security in the AWS cloud.

They will control how the traffic is allowed

into and out of your EC2 instances.

Security groups are going to be very easy,

they only contain allow rules,

so we can say what is allowed to go in and to go out,

and security groups can have rules

that reference either by IP addresses,

so, where your computer is from

or by other security groups,

so as we'll see, security groups can reference each other.

So here, let's take an example,

we are on our computer, so we are on the public internet

and we're trying to access our EC2 instance

from our computer.

We are going to create a security group

around our EC2 instance,

that is the firewall that is around it

and then this security group is going to have rules.

And these rules are going to say

whether or not some inbound traffic,

so from the outside into the EC2 instance is allowed,

and also if the EC2 instance

can perform some outbound traffic.

So to talk from where it is into the internet.

Now let's do a deeper dive, right?

Security groups are a firewall on our EC2 instances

and they're going to regulate access to ports.

They're going to see the authorized IP ranges.

Would it be on IPv4 or IPv6?

These are the two kinds of IP on the internet,

and this is going to control the inbound network.

So from the outside to the instance

and the other network from the instance to the outside,

and when we look at security group rules,

they will look just like this.

So they will be the type, the protocol,

so TCP, the port allowing it,

so where the traffic can go through on the instance

and the source which represents an IP address range

and 0.0 0.0/0 means everything

and this here means just one IP.

So you're not expected to know

how to properly configure a security group

for the (indistinct) exam, but they're so important,

so I wanna talk about them.

Now, let's look at the diagram, right?

So we have our EC2 instance

and it has one security group allow attached to it

that has inbound rules and outbound rules.

So I've separated them onto this diagram.

So our computer is going to be authorized on say port 22.

So the traffic can go through from our computer

to the EC2 instance,

but someone else's computer, that's not using my IP address

because they don't live where I live,

then if they're trying to access our EC2 instance

they will not get through it

because the firewall is going to block it

and it will be a timeout.

Then for the outbound rules by default,

our EC2 instance for any security group

is going to be by default allowing any traffic out of it.

So our EC2 instance,

if it tries to access a website and initiate a connection

it is going to be allowed by the security group.

So this is the basics of how the firewall works.

Now good to know,

what do you need to know with security groups?

Well, they can be attached to multiple instances, okay?

There's not a one to one relationship

between security group and instances

and actually an instance

can have multiple security groups too.

Security groups are locked down to a region

/VPC combination, okay?

So if you switch to another region,

you have to create a new security group

or if you create another VPC

and we'll see what VPCs are in the like later lecture,

well, you have to recreate the security groups.

The security groups live outside the EC2.

So as I said, if the traffic is blocked

the EC2 instance won't even see it.

Okay, it's not like an application running on EC2

it's really a firewall outside your EC2 instance.

To be honest, and that's just an advice to you

from developer to developer

but it's good to maintain one separate security group

just for SSH access,

usually SSH access is the most complicated thing

and you really wanna make sure that one is done correctly.

So I usually separate my security group

for SSH access separately.

If your application is not accessible, so timeout,

so we saw this in the last lecture,

then it is a security group issue.

Okay, so if you try to connect to any port

and you computer just hangs and waits and waits

that's probably a security group issue,

but if you receive a connection refused error,

okay, you actually get a response and connection refused,

then the security group actually worked,

the traffic went through and the application was errored

or it wasn't launched or something like this.

So this is what you would get

if you get a connection refused.

By default, all inbound traffic is blocked

and all outbound traffic is authorized, okay?

Now there is a small advanced feature

that I really, really like, and I think it's perfect

if you start using load balancers

and we'll see this in the next lecture as well,

which is how to reference security groups

from other security groups.

So let me explain things.

So we have an EC2 instance, and it has a security group,

what I call group number one,

and the inbound rules is basically saying,

I'm authorizing security group number one inbound

and security group number two.

So, why would we even do this?

Well, if we launch another EC2 instance

and it has security group two attached to it,

well, by using the security group (indistinct) rule

that we just set up,

we basically allow our EC2 instance

to go connect straight through on the port we decided

onto our first EC2 instance.

Similarly, if we have another EC2 instance

with a security group one attached,

while we've also authorized this one

to communicate straight back to our instances.

And so regardless of the IP of our EC2 instances

because they have the right security group attached to them

they're able to communicate straight through

to other instances.

And that's awesome because it doesn't make you think

about IPs all the time.

And if you have another EC2 instance

maybe with security group number three attached to it,

well, because it group number three

wasn't authorized in the inbound rules

of security group number one,

then it's being denied and things don't work.

So that's a bit of an advanced feature

but we'll see it when we'll deal load balancers

'cause it's quite a common pattern.

I just want you to know about it,

again just remember this diagram

and by now you should be really, really good

at security groups and understand them correctly.

Now going into the exam, what ports you need to know?

Well, we need to know something called SSH

or Secure Shell and we're going to see this

in the very next lectures.

This is the port 22.

And this allows you to login to an EC2 instance on Linux.

You have port 21 for FTP or File Transfer Protocol

which is used to upload files into a file share.

And you have SFTP, which is also using port 22, why?

Well, because we're going to upload file

but this time using SSH

because it's going to be a Secure File Transfer Protocol.

Then we have port 80 for HTTP

and we've been using it in the previous lecture.

This is to access unsecured websites.

And you've seen this whenever you go on the internet

and you enter HTTP:// and then the address of the website.

And you've seen it most likely a lot more like this,

you've seen HTTPS, which is to access secured websites

which are the standard nowadays.

And for HTTPS, it is port 443.

Finally, the last port you need to remember

is 3389 for RDP, or the Remote Desktop Protocol

which is the port that's used

to log into a windows instance, okay?

So 22 is SSH for Linux instance

but 3389 is RDP for a windows instance.

Now this is all the theory about security groups.

I will see you in the next lecture for some practice.