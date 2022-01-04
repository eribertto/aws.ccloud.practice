So we have seen how to access AWS

using the Management console,

which is the Web interface that we've done

so far in this course, but there are, actually,

three different options to access AWS.

So the first one is a Management console,

as we've seen, and is protected by your username,

password, maybe multifactor authentication.

Then there is the CLI, Command Line Interface,

and this is something we will set up on our computer,

and this is protected by access keys,

and access keys our credentials we're going to download

in a few seconds that will allow us

to access AWS from our terminal.

Then, finally, there is the SDK,

the AWS Software Development Kit,

which is used whenever you want to call APIs from AWS

from within your application code.

And again, these will be protected

by the exact same access keys.

So how do we generate access keys?

Well we will do this through the Management console,

and users are responsible for their own access keys,

and access keys, from the user perspective,

there are secret, just like a password,

so if you generate your own access keys

do not share them with your colleagues,

because they can generate their own access keys as well.

So really make sure that you treat your access key ID

just like your username,

and your secret access key just like your password,

you do not share them with other people.

So when you go into the Management console,

you get access key as there's a button

to create access keys, and then it gives you the right

to download it in the very second.

And so, for example, here's a fake access key ID

and a fake secret access key,

and these, when loaded into my Command Line Interface,

would allow me to access the AWS API,

and we'll do this in the hands-on in a second.

So again, remember, I want to make sure

that you don't have any security issues

while doing this course or at work,

do not share your access keys, they are private to you.

So if you're new to the Cloud, and programming and so on,

or IT, then you might not know what's a CLI.

So CLI stands for Command Line Interface,

and the AWS CLI is a tool that allows you to interact

with the AWS services using commands

from your command-line shell.

So whenever you see some code where you type a command line,

and then it returns a result, for example,

aws, s3, cp, and so on, this is what we call the CLI.

And we are using the AWS CLI

because we start every command by the word AWS.

Now with this CLI, you get direct access

to the public APIs of your AWS services

which is going to be very helpful in this course.

And, then, using the CLI you can develop scripts

to manage your resources and automate some of your tasks.

The CLI is open-source,

you can find all the source code on GitHub,

and it is an alternative to using

the AWS Management console.

I know that some people, actually,

do not even use the Management console,

they only use the CLI, for example.

So what's the SDK now?

SDK stands for Software Development Kit,

and this is a set of library,

this is going to be language specific,

so you're going to have an SDK

for different programming languages,

and similarly, it will allow you to access and manage

your AWS services and APIs programmatically,

but this time the SDK is not something that you use

within your terminal, it is something that you embed

within your application that you have to code.

So your application will have the AWS SDK

from within them.

It supports many different programming languages,

such as JavaScript, Python, PHP.NET,

Ruby, Java, Go, Node.js, C++,

all of that's our programming languages.

There's also the mobile SDK,

if you're using Android or iOS,

and the IoT, so Internet of Things device SDK

in case you're using some thermal sensors

or backlogs that are connected, all these kinds of things.

So to give you an example of what you can build

with the SDK, well the AWS CLI that we're going to be using

in this course is actually built

on the AWS SDK for Python named Boto.

So that's it for this lecture.

Now in then the next lecture, we're going to practice

setting up the CLI and dealing with access keys,

so I will see you in the next lecture.