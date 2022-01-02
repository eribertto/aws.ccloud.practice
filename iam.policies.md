Transcript
Okay, so now let's discuss, IAM policies in depth.

So let's imagine we have a group of developers,

Alice, Bob and Charles, and we,

attach a policy at the group level.

In that case, the policy will get applied

to every single member of the group

so both Alice, Bob, and Charles

they will all get access and inherit this policy.

Now, if you have a second group with operations

with a different policy,

David and Edward will have a different policy

than the group of developers.

If Fred is a user,

it has the possibility not to belong to a group.

And we have the possibility to create what's called

an inline policy which has a policy

that's only attached to a user.

So that user could or could not belong to a group

you can have inline policies for whatever user you want.

And finally, if Charles and David both belong

to the audit team and you attach a policy to the audit team

as well, Charles and David will also inherit

that policy from the audit team.

So in this case, Charles has a policy from developers

and a policy from audit team.

And David has a policy from audit team

and a policy from the operations team.

That should make a lot of sense

when we get into the hands-on.

Now, in terms of the policy structure,

you just need to know at a high level how it works,

as well as how it is named.

So this is something you will see quite a lot in AWS,

so get familiar with this structure

this is adjacent documents.

And so an IAM policy structure, consists of a

version number, so usually it's 2012-10-17,

this is the policy language version.

And ID which is how to identify that policy,

this is optional.

And then more statements,

and statements can be one or multiple ones,

and a statement has some very important parts.

So the Sid is a statement ID, which is an identifier

for the statement, which is optional as well,

so on the right hand side is the number one.

The effect of the policy itself, so it is whether or not

the statement allows or denies access to certain API,

so in the right hand side, this says allow,

but you can see deny as well.

The principle consists of which accounts, user or role

which, to which this policy will be applied to.

So in this example, it's applied to the root accounts

of your AWS accounts.

Action is the list of API calls that will be

either denied or allowed based on the effect.

And the resource is a list of resources,

to which the actions will be applied to.

So in this example, it is a bucket,

but it could be many different things.

And finally in, not represented here

but there's a condition to which when

this statement should be applied or not,

and this is not representative here because it is optional.

So going into the exam, you need to make sure

that you really understand the effect, the principle,

the action and resource, but don't worry,

you will see those along the way in the course

so you should be confident with them

by the end of the course.

That's it for this lecture, I hope you liked it.

And I will see you in the next lecture.


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