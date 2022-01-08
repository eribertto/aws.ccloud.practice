So, in this account,

we're going to make sure to spend the least amount of money

or no money, and I will let you know

when something will cost you some money.

But nonetheless,

it is a good idea to set up a billing budget,

so that we know when we go over spending some money

and we can get alerted in case of that.

So, what I'm going to do is click on my account

and then click on my billing dashboard.

Now, as you can see,

I need permissions.

And this is because I'm logged in as IAM user on my account,

and we need to change something on the root account

before we get access with IAM users,

even administrators,

to the billing and cost management dashboard.

So, to solve this,

I logged in as my root account.

So, as you can see now,

it just says my account number.

Doesn't say the IAM user,

so I'm logged in as my root account.

And then I click on my account.

So, you need to be on root account to do this.

You scroll down and you're going to find

this one setting called IAM user and role access

to billing information.

And we'll edit this and we'll activate IAM access.

And this will allow IAM users who are administrators

to access billing data.

If you don't want that,

you can also set up a billing alarm using the root account

if you want it to.

But I want to show you how

to set up a billing alarm using an IAM user

in case this is something you want it to do.

So, once the setting is activated,

you can go back into your IAM user

and then refresh this page,

and you have access

to your billing and cost management dashboard.

Next, let's have a look at how to read an AWS bill.

So, if I take the bill for October 2021,

as we can see, I paid $4.24 for my account.

And when you start accruing charges for your accounts,

it needs, you need to be able to understand how

to figure out which service did incur some charges,

where in which region, and how.

So, if we look at the total service charges

and these will be updated on daily basis in your account,

so you can look at any month,

even the current month.

Then as we can see,

for example, I have under elastic compute cloud $2.18.

And it looks like in the Frankfurt region,

I have $2.18, whereas in the Ireland region,

I only have zero.

So, as we can see,

I can draw down my analysis to Frankfurt.

And then it gives me the breakdown of all the pricing

of all these things based on my usage.

And so, you can see,

there is a NAT gateway that was running for 31 hours

and that cost me $1.61.

And if I scroll down,

there was some elastic IP addresses not attached

to an instance for 114 hours,

which cost me $0.57 and so on.

So, these will give you the information you need

to be able to understand why you have some charges

on your AWS account and turn off or delete the resources

that are incurring you some charges.

It's super important that you generate this skill

and not ask me how to solve this for you.

So again, if you have any charges,

I will always say,

please go to your bill and look at the bill of the month,

of the current month.

And then look at the details of your charges

and understand where the service are coming from.

And then it's up to you to understand what this means

and what you've created,

but this is part of your learning, okay?

But if you follow the tutorial correctly,

you should not have any charges,

and as I tell you, you will have some.

So, this is how you read the bills.

And then another thing is that if you go to the homepage

and that you scroll down,

you're going to get the top free tier services by usage,

and click on View all.

And this is going to give you some information

around the free, the free tier of your accounts.

So, where you stand against the free tier for Amazon S3,

Amazon CloudWatch, and so on.

Which can be some very helpful information,

again, for you to know where you stand on the free tier.

Okay, so next,

let's set up a budget.

So, on the left hand side,

I'm going to the budget console.

I will create a budget.

And you have different kinds of budgets

but to keep it simple,

we're going to create a cost budget.

Click on Next.

And then when to set up a budget amount.

So, it's going to be a monthly budget,

recurring.

It starts in November.

And it's a fixed budget,

and let's say,

we wanna spend no more than $10 on this course.

Now, again,

I will try to make sure to tell you

whenever you are about to incur some cost,

but sometimes it happens that some students get more cost

because well, you're just trying it out

and sometimes you're just playing more than you should,

but it's okay.

So, let's put a $10 budget in this course.

And then we'll click on Next.

So, once you put a budget name,

so, demo budgets,

or course budgets.

Here we go.

Click on Next.

Next, we need to configure alerts.

So, what happens when we reach these,

this budget.

So, we need to create a threshold.

So, it's add,

or the first alert threshold.

And let's say,

hey, when we reach 80% of the budget amount,

okay, the actual amount,

then send us an email.

So, when we have $8 of accrued charges,

then we'll receive an email.

And the email recipient may be stephane@example.com.

And if we want to have a second alert,

so we could say, for example,

hey, when you reach 60% of the budgeted amount

but it's a forecast.

So, when you have $6 of forecasted budget,

then again, send me an email.

So, we have two thresholds.

One that is actual cost and two that is forecast.

So, we have both emails entered at the same time here,

so it's perfect.

Click on Next.

Next, we have budget actions.

So, what do you wanna do

in case these thresholds are reached.

And you can have actions but right now we don't need to.

We just wanna receive an email and we'll be good to go.

So, next,

and we review everything and create this budget.

So now, we have a course budget and we'll have,

definitely, email alerts in case we reach

some 80% of the actual budget or 60% of the forecast.

And then this will allow us to control our cost

in case you did something wrong in this course,

okay?

So, that's it for this lecture.

I hope you liked it and I will see you in the next lecture.

