Okay. So let's practice using IAM roles

for our EC2 Instance.

So at first, I'm going to connect to my EC2 Instance.

You can SSH, or you can use EC2 Instance Connect

if you wanted to.

I will use EC2 Instance Connect

because it's just going to be in my web browser

and a little bit simpler.

So back into my instance

with EC2 Instance Connect right here.

And we are in our Instance.

So as we can see,

we are ec2-user@ and the private IP.

So regardless if you're using EC2 Instance Connects

or SSH through your terminal, or whatever,

through PuTTY.

Then if you see this, we are at the same stage, okay?

So now you can just do some Linux commands.

For example, ping Google,

and you can get some information out of Google.

And I will do Control + C to go out of it

or issue any kind of Linux commands you want.

Okay, you don't need to know the next command

going into the exam,

but this is just a Linux terminal available

to you right now in the cloud.

So we'll type clear to clear the screen

and next we have to run some IAM commands.

So the cool thing is that's the Amazon Linux AMI

we're using right now comes with the aid of a CLI.

And so, as you can see, it is installed.

So what we can do is start using some commands.

For example, aws iam list users.

And if we do so, it says unable to look at credentials.

You can configure credentials by using aws configure.

So we could indeed run aws configure

to configure the credentials and specify an Access ID

a Secret Access key, and a region name.

But this is a really, really, really bad idea.

And the reason is that if we run aws configure

and enter our personal details onto this EC2 Instance,

then anyone else in our accounts

could again connect to our EC2 Instance.

For example, using EC2 Instance Connect

and retrieve the value of these credentials in our instance,

which is not what we want.

This is something that's really, really bad.

And so as a rule of thumb, never, ever, ever

enter your IAM APA key.

So the Access Key ID and the Secret Access key

into an EC2 Instance.

This is horrible and if you see someone doing it,

please show them this video.

Instead, what we have to do is use IAM rules.

So if you remember,

when we were in the management console and we were in IAM,

we had created an IAM role.

So let's go back into the Roles.

We had this demo role for EC2

that had one policy attached called IAMReadOnlyAccess.

So we are going to attach this role

onto our EC2 Instance to provide it with credentials.

Okay, so how do we do this?

For this, we can go into Security.

And as you can see,

there is no IAM Role right now onto our instance.

So what we can do is go back to our Instances,

Action, Security, and then Modify IAM role.

Here we have to choose an IAM role.

So we have DemoRoleForEC2 and click on Save

to attach this IAM role into our Instance.

So if you go back to Security,

now the IAM role attached to Instance

DemoRoleForEC2.

So the effect of this is that now

if we do aws iam list users and press Enter,

where we are getting a response around the users from IAM.

So as we can see, we did not run the command aws configure.

We just attached an IAM role and ran this command.

And it works.

And as a proof, if we go into this role

and detach this permission, so now it's gone,

and run the command again, we're getting an access denied.

So the role is really linked now to the EC2 Instance.

And this is how we provide AWS credentials

to our EC2 Instances only,

only through IAM roles, okay?

So if we go back to IAM

and we attach a policy to this role

and go back to IAMReadOnlyAccess,

attach this policy and then rerun the command,

we get an access denied

because sometimes it can take a little bit of time

to propagate the changes from IAM into AWS.

But if we run it one more time,

we're getting the output we expect,

which is what we want.

So this is very important

for you to understand this,

use IAM roles for your EC2 Instances.

So this is hopefully good for you.

I hope you like this hands-on

and I will see you in the next lecture.