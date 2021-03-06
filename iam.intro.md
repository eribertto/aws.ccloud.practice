- [Stephane] Welcome to the first deep dive

on an iterator service.

The first one is called IAM.

So IAM stands for identity and access management.

It is a global service because in IAM,

we are going to create our users and assign them to group.

So we've already used IAM without knowing,

when we created an account, we created a root accounts,

and has been created by default.

This is the root user of our accounts.

And the only things you should use it for is

to set up your account as we'll do it right now.

But then you shouldn't use that account anymore,

or even share it.

What you should be doing instead, is create users.

So you will create users in IAM,

and one user represents one person within your organization.

And the users can be grouped together if it makes sense.

So let's take an example we have an organization

with six people.

You have Alice, Bob, Charles, David, Edward

and Fred so all these people are in your organization.

Now Alice, Bob, and Charles they work together.

They're all developers.

So we're going to create a group called

the group developers who regrouping Alice,

Bob and Charles.

And it turns out that David and Edward also work together.

So we're going to create an operations group.

Now we have two groups within IAM.

Now groups can only contain users, not other groups.

So this is something very important to understand.

Groups only contain users.

Now, some users don't have to belong to a group.

For example, Fred right here is alone,

he does not correspond to any group.

That is not best practice.

But it is something you can do in AWS.

And also, a user can belong to multiple groups.

That means that for example, if you know that Charles

and David worked together,

and they're part of your audit team,

you can create a third group with Charles and David.

And as you can see, now, in this example,

Charles and David are part of two different groups.

So this is the possible configurations for IAM.

So why do we create users and why do we create groups?

Well, because we want to allow them to use our AWS accounts

and to allow them to do so,

we have to give them permissions.

So users or groups can be assigned

what's called a JSON document.

I'll show you right now what it means called a policy,

an IAM policy.

So it looks just like this.

So you don't have to be a programmer.

This is not programming.

This is just describing in, I think plain English,

what a user is allowed to do or what a group

and all the users within that group are allowed to do.

So in this example, we can see that we allow people

to use the EC2 to service and do describe on it,

to use the elastic load balancing service

and to describe on it and to use CloudWatch.

Now we'll see what EC2 elastic load balancing

and CloudWatch mean, but through this JSON document

that looks just like this.

We are allowing our users to use some services in AWS.

So these policies will help us define permissions

of our users.

And so in AWS, you don't allow everyone to do everything

that would be catastrophic,

because a new user could basically launch so many services

and they will cost you a lot of money

or would be valid for security.

So in AWS, you apply a principle called

the least privilege principle.

So you don't give more permissions than a user needs.

Okay, so if a user just needs access to three services,

just create a permission for that user.

So now we have seen an overview IAM.

Let's go in the next lecture

to practice creating users and groups.


Click the "Create a new note" box, the "+" button, or press "B" to make your first note.
Teach the world online
Create an online video course, reach students across the globe, and earn money
Top companies choose Udemy Business to build in-demand career skills.
NasdaqVolkswagenBoxNetflixEventbrite
Udemy Business
Teach on Udemy
Get the app
About us
Contact us
Careers
Blog
Help and Support
Affiliate
Investors
Terms
Privacy policy
Cookie settings