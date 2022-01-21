We have seen that EC2 Instances

are virtual servers in the Cloud.

And so far we've been using on demand instances,

these were instances that we need for short workloads

that have predictable pricing.

But sometimes with servers,

you know you're going to need them

for a very long time,

and you can get cost savings by saying that to AWS.

So, the first option

is to use what's called a Reserved Instance.

And a reserved instance needs to be used

for a minimum of one year.

So this is commitments

and you can use three types of reserved instances.

The first one is simply called reserved instances

for long workloads, think of a database.

You will have convertible reserved instances,

when you have flexible instances,

so you want to change their types over time.

Then you have scheduled reserved instances,

for example, when you know you don't need it continuously

for one year, but you need it maybe every Thursday

between three and 6:00pm for one year.

Then we have spot instances,

they're going to be short workloads, cheap,

but we can lose them, they're less reliable.

And we're going to have dedicated host,

where you want to book an entire physical server

and control the instance placement.

So why am I saying all these things to you?

Well, the exam is going to ask you questions

and ask you to find the best kind of EC2

instance purchasing option,

based on the case obviously,

to bring the maximum amount of cost saving,

or to comply with some rules.

So let's do a deep dive into each of those

to make sure it's very, very clear.

So the first one is EC2 on demand,

where you pay for what you use.

So, if you have a Linux machine,

or a Windows Machine

then you're going to be billed per second

For each second the EC2 instance is running after the first minute

And for all other operating systems, then the billing

is going to be per hour when your on-demand instance is running.

So this is on demand pricing,

very, very typical of the Cloud.

With on demand,

you are right in what the cloud is best for.

It's high cost but you have no upfront payment,

no long term commitment,

you can terminate, stop them, start them whenever you want.

And these are recommended for short term

and uninterrupted workloads,

when you can predict how the application will behave.

Next, we have reserved instances,

these will give you about 75% discount

compared to on demand,

and you have a reservation period,

you can choose one year or three years.

If you choose three years,

then you're saying that to AWS,

hey, I'm willing to book this instance

for a longer period of time.

So AWS will say,

Okay, I'll give you an even bigger discount.

Now you have the purchasing option,

you can say no upfront, that means you pay monthly,

partial upfront or all upfront.

With all upfront, that means you're going to pay

for your servers right now, today.

And obviously because you give money today to AWS,

they're very happy

and they're going to give you an even bigger discounts.

Then, because it is reserved instances,

you have to reserve a specific instance type.

So for example,

you have to say I want a T2 micro or I want a C5 x large,

these kind of things.

So these reserved instances are recommended

if your application is going to be in a steady state usage,

so a database.

If you know you need a database

for the next three years,

then reserving that instance

will bring you huge cost savings.

Now, you have different flavors of reserved instances,

there's the normal one that I just told you about.

But you also have convertible reserved instance

where you can set change the EC2 instance type over time.

So you can do for example,

T2 large, C5 large or R5 4x large who knows.

And this will give you a bit less discount

because you can change the EC2 instance type,

so up to 54% discounts.

Then you have the scheduled reserved instances,

for example, if you just know you need to launch

that EC2 instance within a specific time window

that you reserve,

so you need to have it just for a fraction of a day,

a week or a month.

But you still need to commit for over one,

two, three years, hope that makes sense.

Next, we have spot instances,

spot instances are great,

because they can provide you the highest discount in AWS,

it can be up to 90% discounts

compared to on demand instances.

But the particularity of the spot instances

is that you can lose them at any point of time,

if the price you're willing to pay for them,

is less than the current spot price.

So what this means is that the spot price changes over time,

and you're saying what you're willing to pay

as a maximum amount for these spot instances,

so you can lose them.

They're going to be obviously the most cost efficient

instances in AWS, but if you use them,

you need to use them for workloads

that are going to be resilient for failure.

So what that means is that,

for example, if you know you can lose your instance,

you don't wanna lose all your progress of your work

if you lose that instance.

So what types of workloads will be good for this?

Well, batch jobs, data analysis once at a time,

image processing, so if you want to transform images,

if you somehow don't transform one, that's fine,

you can retry later.

Any distributed workloads,

this is the cloud so the server's can work together

in a distributed fashion.

And if one of these server fails,

the other ones will know how to react to that failure

and still work together without the one server

that has been terminated.

Or, for example, if you have a workload

that has a flexible start and end time,

a spot instance could be great.

But one thing spot instances are really not great at,

is to run a critical job or a database,

never ever do that it would be disastrous.

Finally, you have Dedicated hosts.

I'm going to read you the definition

because I think it's the simplest.

An Amazon dedicated host is a physical server

with EC2 instance capacity, fully dedicated to your use.

We are renting an entire server in a data center of AWS.

Dedicated hosts can help you address compliance requirements

and reduce costs by allowing you to use your existing

server bound software licenses.

So I put it in bold compliance requirements

and server bound software licenses,

because these are keywords

that can come up in the Exam.

Now, these hosts are going to be allocated

for your accounts for a three year period reservation.

So you definitely need to be able to commit to them,

they're going to be more expensive

because you're getting a full server for yourself.

And they're going to be extremely helpful

if you have a software

that has a complicated licensing model,

or you bring your own license,

or if you have a strong regulatory or compliance needs,

and you wanna make sure no other customers of AWS

can use that server but you.

And so as you know,

AWS shares all their servers with everyone.

There is some security to make sure

that you cannot see the server of your neighbor

but sometimes because of regulations or compliance needs,

you need to make sure

that you have the physical server just to yourself.

Now there's one last type of dedicated instance

which is called dedicated instances.

And these are for EC2 instances running on hardware

that's dedicated to you.

And you may share the hardware with other instances

in the same account and you don't have any control

over how the instance is placed.

What it means is that there is hardware dedicated to you,

but you don't get access to that underlying hardware,

it's more of a soft version of dedicated host.

And I can understand this can be confusing,

so as we can see on the right hand side table,

there is a difference between dedicated instance

and dedicated host.

Both allow you to use dedicated physical servers,

but with dedicated host you get per host billing,

whereas for dedicated instances

you get per instance billing,

and the dedicated host gives you a lot of access

to the underlying hardware.

So we get these nice server bound licenses

that are available to be used on dedicated host

because we have access to the socket cores

and host ID and so on.

Whereas the dedicated instances,

the only thing that it allows you to give you

is automatic instance placement.

Dedicated host is a lot more involved,

this is more when you have the server bound licenses,

dedicated instances, if you need some high level

regulatory compliance, that you're saying

that the hardware will not be shared with anyone else.

Now, don't think the exam will ask you the difference

between dedicated host and the dedicated instances,

but it's so good to see in this lecture.

The exam will ask you to choose the right instance,

and I want you to compare it to a hotel

just to maybe give a nice comparison.

So on demand means that you're coming

and staying in the resort whenever you like,

and you pay the full price,

so you show up and you get your room.

But reserved is, you plan ahead and you wanna stay

for a very, very long time in the hotel,

you're going to get a good discount

'cause they know you're going to get a room

for maybe one month.

Spot instances is if you're a little bit sneaky,

so you know that some hotel rooms at night

are going to be empty.

And you know the hotel is going

to give you aggressive discounts,

because they want someone to stay in a hotel room,

otherwise they'll lose that hotel room.

But it would be a weird hotel,

but I have to say that to you,

the hotel will be able to kick you out

if they find someone who is able to pay more

for your room than you are.

So it would be a weird hotel,

but hopefully that shows you what a spot instance

would be like in a hotel.

And finally, the dedicated host would mean that,

you would book the entire building of the resort

for you because you don't have any neighbors

for compliance requirements

or because you have a (mumbles) down license,

hope that makes sense.

And finally, I'm not gonna spend too much time on it,

but in your own time, you can look at the different price

options based on spot, on demand, reserved instances,

upfront, no upfront.

Which shows you the type of discounts you can get

based on different options.

And to do so I use an M4.large in the region,

us-east-1 to give you these prices.

So that's it for this lecture, I hope that was helpful.

This is something you definitely need to know

going into the exam and I will see you in the next lecture.