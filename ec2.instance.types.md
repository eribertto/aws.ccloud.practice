Okay, so now let's talk

about EC2 Instance Types.

So there are different types of EC2 instances

that you can use for different use cases

and they have different types of optimization.

And let's go check out this link

and we'll see we have for now,

seven different types of EC2 instances.

So this website on the AWS website

is what we're interested into.

And as we can see, we have different types of instances.

We have general purpose, compute, optimized,

memory optimize and so on.

And so for each type of instance

we have different families.

And so as we can see this website is going to

be the reference for us to look at Institute Instance types

and know their costs and other specificity.

What I'm going to do though, is just walk you

through a high-level overview of how they work in AWS.

AWS will have the following naming convention.

For example, we'll be talking

about an M five dot two X large type of instance.

What does that mean?

Well, M is going to be called the Instance Class.

Okay. And this is going to be, for example, in this case

a general purpose type of instance,

five is generation of the instance.

So as AWS improves the hardware over time

if we release a new generation of hardware, and so

after M five, if they improve the M type of instance class

then we'll go to M six

and then finally the two X large represented the size

within the instance class.

So, it starts as small and then large

and then two X large four X large and so on.

So it represents the size of the instance,

and the more the size, the more the memory

the more the CPU is going to have on your instance.

So from an exam perspective, what do you need to know?

Well, we'll talk about a few different types

of instance types.

So you have a general purpose

and these are great for diversity of workloads

such as web servers or code repositories.

They will have a good balance

between compute, memory, networking.

And so in this course

we'll be using general purpose instances.

We'll be using the T2 micro

which is the free tier, general purpose type of instance.

On the website that I just showed you

you will see all the different types

of instance that our general purpose

and this is going to evolve over time,

So I won't update this slide.

But you can always refer back

to the AWS website to check what the instances are

in the general purpose type of family.

Then we have compute optimized,

and these are instances are great,

and optimized for compute intensive tasks.

So what requires a high level of processor?

Well, if, for example, it could be

if you're batch processing some data

if you're doing media transcoding

if you need a high-performance web servers

if you're doing high performance, computing is called HPC.

If you're doing machine learning

or if you have a dedicated gaming server.

So all these things are tasks that require a very good CPU

very good compute side.

And so Ec2,

instances do have this kind of particularity

and for now all the computer optimized instances

in EC2, are of the C names.

So C5, C6, and so on.

Next, we have some EC2 instances that are memory optimized

and there are going to be

have a really fast performance for the type

of workloads that will process large datasets in memory.

So memory means RAM.

And so the use cases are this is going to

be high performance for relational or

non-relational databases are mostly going to be

in memory databases,

distributed web-scale cache store.

So for our elastic cache, for example

in memory databases that are optimized

for business intelligence or BI.

And applications performing real-time processing

of big unstructured data.

So in terms of the names for the memory optimized instances

there's going to be the R series because R stands for RAM

but there's also going to be X one high memory and Z one,

but again, you don't have to remember the name

of the instances, but good to know at a high level.

Okay. And finally we'll have storage optimized instances.

They're great when you are accessing a lot

of data sets on the local storage.

And so the use cases for storage optimized instances

are going to be high-frequency online

transactional processing, so OLTP systems.

Relational and NoSQL databases.

And we'll see those in details.

When we get to the database sections.

Cache for in-memory databases, for example,

Reddit's data warehousing application

distributed file systems

and the search optimized instances in AWS

will start with an I, a G, or H one.

Okay. But again, don't have to remember this.

I'm just giving you examples.

So what does it mean?

Let's compare a few instance types.

So for example, for t2.micro

we have one VCPU and one memory, one gigabytes of memory.

And if you look for example, at r5.16xlarge

we have 16 VCPU and 512 gigabytes of memory.

So we can see there's a lot of more emphasis on the memory.

If we compare it to example, to a c5d.4Xlarge

we can see we have 16 VCPU and 32 gigabytes of memory.

So less memory, more CPU

and so on different network performance

different EBS bandwidth and so on.

So just to give you a point of comparison,

and because we're using t2.micro in this course

it is part of the AWS feature.

So we get up to 750 hours per month of t2.micro.

And if you want a website to compare all the

EC2 Institute instances together,

there's one that I really like,

it's called instituteinstance.info,

and I'll show it to you right now.

So I am on the instituteinstances.info website

and as we can see,

we have a list of all the instances available in AWS.

So really, a lot.

We also get some information around

the Linux on demand cost and an X reserves cost,

and so on, so some cost information.

We get information around the memory the number of VCPU.

We can order by name, we can search it.

So it's, it's quite handy.

And I really like this website.

And if you go and use AWS

you probably will use this website as well.

So that's it for this lecture.

I hope you liked it.

And I will see you in the next lecture.

