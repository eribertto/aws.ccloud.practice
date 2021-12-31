Now let's look at the history

of the AWS cloud.

So it was launched in 2002

internally at amazon.com.

Because they realized

that the IT departments could be externalized.

So their Amazon infrastructure was one

of their core strength

and they said, "you know what

"maybe we can do IT for someone else,

"for other people."

So they launched their first offering publicly

which was SQS in 2004.

In 2006, they expanded their offering

and they relaunched with the availability of

SQS, S3, and EC2.

Don't worry, we'll see all these services

in this course.

Then they expanded and said, "you know what?

"We don't have to be just in America.

"We could be in Europe."

And then fast forward to today,

we have so many applications that used to run

or are still running on AWS,

such as Dropbox, Netflix, Airbnb, or even the NASA.

Now, let's look at where AWS is today.

If we look at the Gartner magic quadrants,

which sort of ranks the cloud providers,

as we can see AWS is on the top right corner,

which is a leader.

It's able to execute really well.

And it has a really great completeness of vision.

It is followed closely by Microsoft and Google.

But still

in 2019, AWS had $35 billion in annual revenue,

which is huge and accounted for 47%

of the market in 2019.

With Microsoft being second with 22%.

So by learning AWS

you are learning a tool that is widely used.

It is a pioneer and leader

of the AWS Cloud Markets for the ninth consecutive year.

And it has over 1 million active users.

So what can you build on AWS?

Well, pretty much everything.

AWS will enable you to build sophisticated

and scalable applications

and they are applicable to diverse set of industries.

Every company has a use case for the cloud.

So Netflix, McDonald's, 21st century Fox, Activision,

they're all using the cloud.

And use cases can include just

transferring your enterprise IT

or using the cloud as a backup and storage,

or doing some big data analytics.

You can also host a website

or create a backend

for your mobile and your social applications.

Or you could have your entire

gaming servers running on the clouds.

The applications are endless.

Now AWS is global.

And this is where we are going to learn a bit more specifics

about how it works.

So we have AWS regions,

we have availability zones, data centers,

edge locations, and points of presence.

And all of these can be represented on the map right here.

So let's go on this website

to have a quick look at it.

So this is a cool map,

because on this website

we can see how AWS is global.

So if I click on it,

I can, you know,

scroll the world and see what is happening.

So we can see that AWS has multiple regions

and they're in orange and they're all around the world.

For example, Paris, in Spain, in Ohio,

in Sao Paulo, Cape Town, Mumbai, and everywhere else.

So AWS truly is a global service.

On top of it,

each region are going to be connected through the network.

So these are the network reconnecting the regions

and this is a private network of AWS.

And then within each region, for example,

if I really scroll into the Cape Town region,

we can see that we have blue dots.

And each blue dots will be availability zones

that we'll be describing in the next slide.

So as we can see,

what I want to get you out of this,

is that the AWS is truly is global.

And we can leverage the infrastructure of a cloud

provider to make ourselves, our application global.

The first important concept in AWS are regions.

So regions are all around the world

and we saw it on the map from before

the regions have a name,

it could be us-east-1, eu-west-3,

and we can see the mapping of the name of the region

to their code on the console that we'll see in a minute.

Now a region, what is it?

It's truly,

well, it's going to be a cluster of data centers.

So many different data centers.

Look at it (indistinct) for example,

Ohio or Singapore or Sydney or Tokyo.

When we use AWS services,

most services are going to be linked

and scoped to a specific region.

That means that if we use a service

in one region and we try to use it in another region,

it will be like a new time of using the service.

Now, a question that may come up

in the exam is how do you choose an AWS region?

So say you're launching a new application.

Where should you do it?

Should you do it in America, in Europe

in South America, or in Australia?

Well, the answer is, of course it depends.

But let's look at some factors that may impact your choice

of a AWS region.

The first one is compliance.

So sometimes governments want the data to be local

to the country you're deploying the application in.

For example, France,

data in France may have to stay

in France and therefore you should launch your application

in the French region.

Then, there is also a concept of latency.

So if most of your users are going to be in America,

it makes a lot of sense to

deploy your application in America,

close to your users,

because they will have a reduced latency.

If you deploy your application

in Australia and your users are in America,

they will have a lot of lag at using your application.

Then, also not all regions have all services.

Okay?

Some regions do not have services.

And so obviously if you're

leveraging a service with your application,

you need to make sure

that the region you're deploying into

is available and does have that service.

And finally,

pricing.

So, pricing does vary from region to region

and you need to consult the applicant,

the services, pricing, (indistinct)

to see what the differences are between the regions.

But this could be obviously a factor that could

impact your deployment

of an application into a specific region.

Now, availability zones are what actually

are going into the region.

So each region will have many availability zones.

Usually three, the minimum is two, and the max is six.

But, really the usual is three.

So, let's take the Sydney region as an example.

The senior region code is ap-southeast-2.

So, we can have two,

have three availability zones in

Sydney, ap-southeast-2a,

ap-southeast-2b,

and ap-southeast-2c.

Now, each of these availability zones

are going to be one or more,

just create data centers that will have redundant power,

networking, and connectivity.

That means that in

southeast-2a,

I can have two data centers maybe, as well two

in 2b and two in 2c.

But it could be one, it could be three, it could be four.

We don't really know.

AWS doesn't tell us that.

But, what we know

is that these availability zones are

separate from each other

so that they will be isolated from disasters.

So, if something happens to ap-southeast-2a,

we know that it is designed not to cascade

into ap-southeast-2b, or ap-southeast-2c.

So they're really isolated from disasters.

And then these data centers,

these availability zones,

they are connected with high bandwidth,

ultra low latency networking and therefore

altogether being linked together,

it will form a region.

Okay.

Next to, the only thing we need to know

about AWS for the global infrastructure is the points

of presence or edge locations.

We will see them in details

in the global section of this course,

but you should know that AWS has more than 200 points

of presence in 84 cities across 42 countries.

And this will be very helpful when we deliver content

to the end users with the lowest latency possible.

And this is what you see on this map.

Now again, I'm going quickly

over this because we will see this at the,

about the middle of this course.

So, now how about we just play

around and do a tour of the console.

We'll see that AWS has global services such

as IAM, Route 53, CloudFront, and WAF,

but we'll see that also

most AWS services are going to be regions scoped,

such as Amazon EC2, Elastic Beanstalk,

Lambda, and Rekognition.

Finally, to know if a service is available in your region,

there is a region table you should check out right here.


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