Okay. So let's have a look at security groups.

So on the left hand side

we're going to scroll down and find a security groups.

So security groups are the way for you to control access

through networking to your EC2 instance.

So here we have two groups.

We have a launch-wizard-1,

which is the one we created

while we launched our EC2 instance

and the default group, which is one that is created

by default when you have your alias account created as well.

Okay?

So if we look at the launch-wizard-1,

we can see that by scrolling down,

it has a security group ID

which is how to uniquely identify the security group

within your accounts.

We can also scroll down

and see we have three inbound rules and one outbound rules.

So if we have a look at the inbound rules right here

we see we have three of them.

And so we have HTTP on port 80 from source anywhere

HTTP on port 80 from source.

And this is anywhere on IPv6 formats

and SSH TCP Port 22 on source anywhere in IPv4 format.

Okay?

So as we can see, these tributes is what allow us to

get access to our EC2 instance

In terms of outbound rule,

as we can see,

we have everything allowed on all ports

from anywhere to anywhere

which allows our EC2 instance, for example

to get software updates

or to send emails or whatever.

So it is quite common to have outbound rules to be...

Oh okay.

So now let's go into the inbound rules

and we're going to see the impact of inbound rules

onto our EC2 instances.

So if I go back to my EC2 instance

and then I'm going to go to the public IPv4 address

and open the address right here,

we get the Hello world.

Okay, great.

But now let's go into the inbound rule.

We're going to edit them

and I' am going to remove the HTTP related rules.

So I' am going to delete them too

and click on save rule.

So now, as you can see

I only have one rule, which is SSH port 22.

Now, if I go back to my webpage

and what I' am going to do

is refresh this by clicking on the refresh button,

as you can see

there is a loading happening right now.

This is, this is spinning right now.

So the loading means that

we are trying to access our EC2 instance

but we don't have a response back to it.

And the reason we don't have a response

is that we have removed the HTTP rule

Therefore, forbidding the traffic

to getting into our EC2 instance.

So what's going to happen

is that we're going to get a timeout

because after 30 seconds

of expecting a response from EC2 instance

Our web browser is going to say, you know what?

It's been 30 seconds.

And I think I will never get a response.

Therefore, I will give a timeout to the end-user.

So this is something we're going to see in a few seconds.

And so as a general rule,

when you get a timeout in AWS

when you connect to your instance

this has to be a security group issue.

So if you cannot connect your instance

and there is an endless loading circle

and a timeout error

Then you should have a look at your security group rules

and ensure they're set up correctly.

So let's just wait for this to be done.

And now we get the timeout error.

So this site cannot be reached.

It took too long to respond

and the error code is ERR_TIMED OUT.

Okay? So now we can fix this by going back into

our management console,

editing the inbound rules

and then we're going to add a rule for HTTP.

So I can just type HTTP in this box.

And then I will say from anywhere

and click on save rule.

And now if I go back to my webpage

and I stop it and I refresh it,

I get back to the Hello world.

So we have added back the rule

and the firewall is allowing the traffic to go in.

Now we can have a look at all the kinds

of inbound rules we can have,

so we can have a rule.

And there's a bunch of pre-configured options.

So there's SSH for port 22

There's FTP which is port 21.

We have HTTP, which is port 8C.

We have HTTPS, which is right here,

which is port 443.

We have RDP right here to connect to your windows instance,

which is 3389.

And if you wanted to have whatever ports you wanted

you can use a custom TTP

and then you can enter whatever ports you want

in terms of where the traffic is coming from.

So you can do custom

and you get some recommendations in terms of cinder blocks.

So if you do anywhere is going to give you

this cinder block right here,

which is anywhere from IPv4.

And this one is anywhere from IPv6.

You can have my IP to just allow traffic

from the IP of your computer

or more advanced,

You can reference a security group.

So in custom, if you scroll down, you have security groups.

And as you can see here,

I can reference,

for example default security group to be allowing access

to my instance on port one, two, three, four

and we'll be using this more advanced when we go

to the load balancer section.

Okay?

So we've seen all the options for security groups

are just going to save the changes

that I didn't make any changes.

So nothing happens.

Okay?

And finally, just a note.

So this security group is currently attached

to one EC2 instance

but it can be attached to many EC2 instances.

Okay?

And it's possible for your EC2 instances

to also have many security groups attached to them.

The rule would just add on together.

So that's it for this hands-on on security groups.

I hope you liked it.