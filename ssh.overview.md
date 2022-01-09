You're getting to one of the trickier bits

of running in the Cloud, which is how do you connect

inside of your servers

to perform some maintenance or action.

So for this, for Linux servers,

we can use SSH to do a secure shell into our servers.

So based on the operating system you have on your computer,

you have different ways of achieving it.

So I have separated Mac, Linux,

Windows before version 10 and Windows after version 10.

So the SSH is a command line interface utility

that can be used on Mac or Linux

as well as Windows over version 10.

Then if you have Windows less than version 10,

you can use something called putty.

Putty will exceed the exact same thing as SSH.

So when I say you should SSH, if you're on Windows,

you can use putty.

And putty is valid for any version of Windows.

They do the exact same thing, they allow you to

use the SSH protocol to connect into your EC2 instances.

And then finally, there's something new

called the EC2 Instance Connect,

which is going to use your web browser.

So not a terminal nut putty your web browser

to connect to your EC2 instance.

And I like it a lot because it is valid

for Mac, Linux, Windows, all versions.

The cool thing about EC2 Instance Connect is that it works,

but it only works for now with Amazon NX2

And this is why I've been using

Amazon NX2 in this tutorial.

So now what should you do?

If you are on Mac or Linux,

then please watch the SSH lecture on Mac/Linux.

If you're on Windows,

then you can either watch the Putty Lecture

or if you have Windows 10, then I have created an SSH

on Windows 10 lecture as well.

Regardless, I am going to personally use

in the future lectures, EC2 Instance Connect.

So if you wanna have a look and play with it,

I find it really simple.

You don't need to install anything

or use the command line interface

if you're not familiar with it.

So this could be very handy for all of you.

Nonetheless, SSH is in my experience

and I've taught hundreds of thousands of students

what caused the most troubles in this course.

So if you get a problem with SSH

we can re-watch the lecture, you may have missed something,

maybe a security group rule, maybe you command,

maybe a typo, I don't know you.

There's also a troubleshooting guide

that I've put together after these lectures so have a look.

I would recommend your try, EC2 Instance Connect

as well as sometimes fixes all problems.

And if none of these method works, sorry

if one method works, then you're good to go.

You don't need to have them all working.

If one works, you're good to go.

And if no method works, that's completely okay.

This course is just introductory

and he won't use SSH much and you'll be fine.

So that's it that just for the introduction.

Now find your right lecture and it will see you

in the next lecture.