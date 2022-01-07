Let's generate a credential report.

So, on the bottom left,

I am going to create a credential report.

And I can click on Download Report

to just download this report and this will be a CSV file.

Now, this CSV, because I'm using a training account

is not fascinating.

But as we can see, we have two rows in it.

We have my root account, and my account named stephane.

We can see when the user was created,

if the password was enabled,

When the password was last used, and last changed.

When is the next rotation to be expected

if we do enable password rotation.

Is mfa active?

So we can see it's active for my root account,

but it is not active for my stephane account.

Then access keys, are they generated or not?

Yes, they are created for my stephane account,

but not for my root account.

And when were they last rotated, last used, and so on.

You can get more information about other access keys

and certificates and so on.

So this report is extremely helpful

if you want to look at some users

that haven't been changing their password,

or using it or their account.

It could be giving you a great way to find which users

that deserve your attention from a security standpoint.

Next, I want to look at IAM Access Advisors,

so I'm going to click on my user.

My user is stephane,

and the right hand side it says Access Advisor.

So this is going to show me

when some services were last used.

And the recent activity usually appears within four hours.

So if you don't see all the data, that's why.

So we can see that, for example,

Identity and Access Management was last accessed today.

Thanks to this policy right here.

And also the Health APIs and Notifications

were accessed today.

Why?

Well this is a little bell right here,

automatically will be accessed

to see if there are any notifications for your accounts.

And we'll see what this is,

this is the Personal Health Dashboard, okay.

But for the other services, for example,

Alexa for Business, or AWS Accounts,

or Certificates Manager, I haven't been using them.

And so maybe it makes sense for me

to remove these permissions from this user,

because it seems this user is not using these services.

So this is the whole power of Access Advisor.

And as you can see there are lots of services in AWS.

About 23 pages just like this,

so this is about 230 services in AWS

at the time of recording.

So quite a lot to learn, but don't worry,

we'll get to cover it.

And we've just seen all the ways

we can have security tools on IAM.

I hope you like this lecture,

and I will see you in the next lecture.

