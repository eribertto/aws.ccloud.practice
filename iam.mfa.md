Now that we have created users and groups,

it is time for us to protect these users and groups

from being compromised.

So for this we can have two defense mechanisms.

The first one is to define what's called a Password Policy.

Why?

Well, because the stronger the password you use

the more security for your accounts.

So in AWS, you can set up a password policy

with different options.

The first one is you can set a minimum password length,

and you can require specific character types,

for example, you may want to have an uppercase letter,

lowercase letter, number, non-alphanumeric characters,

for example a question mark and so on.

Then you can allow or not, IAM users

to change their own passwords

or you can require users to change their password,

after some time, to make your password expired, for example,

to say every 90 days, users have to change their passwords.

Finally, you can also prevent password reuse

so that users when they change their passwords,

don't change it to the one they already have

or change it to the one they had before.

So this is great, a password policy, really is helpful,

against brute force attacks on your accounts.

But there's a second defense mechanism

that you need to know, going into the exam,

and this is the Multi Factor Authentication or MFA.

It is possible you already to use it, on some websites,

but on AWS it's a must and it's very recommended to use it.

So, users have access to your account,

and they can possibly do a lot of things,

especially if they're, administrators,

they can change configuration, delete resources

and other things.

So you absolutely want to protect at least

your Root Accounts and hopefully all your IAM users.

So how do you protect them on top of the password?

Well, you use an MFA device.

So what is MFA?

MFA is using the combination of a password that you know,

and a security device that you own,

and these two things together,

have a much greater security than just a password.

So for example, let us take Alice.

Alice knows her password,

but she also has an MFA generating token,

and by using these things together while logging in,

she is going to be able to do a successful login on MFA.

So the benefit of MFA is that even if Alice

has lost her password, because it's stolen or it's hacked,

the account will not be compromised because the hacker,

will need to also get a hold of the physical device

of Alice that could be a phone for example to do a login.

Obviously, that is much less likely.

So what are the MFA devices option in AWS

and you should know them going to the exam

but don't worry they're quite simple.

The first one is a Virtual MFA device,

this is what we'll be using in the hands on

and so you can use Google Authenticator,

which is just working on one phone at a time,

or using Authy which is multi-device

they both work the same except one is multi-device.

And personally I use Authy because I like the fact that

I can use it on my computer and on my phones.

So, for Authy you have support

for multiple tokens on a single device.

So, that means that with a Virtual MFA device,

you can have your root account, your IAM user,

and another account, and another IAM user,

its up to you, you can have as many users

and accounts as you want on your Virtual MFA device,

which make it a very easy solution to use.

Now we have another thing called

a Universal 2nd Factor or U2F Security Key,

and that is a physical device, for example,

a YubiKey by Yubico and Yubico is a 3rd party to AWS,

this is mot the AWS that provided, this is a 3rd party

and we use a physical device,

because maybe it's super easy, you put it your Key Fobs

and you're good to go.

So this YubiKey supports multiple root and IAM users

using a single security so you don't need as many keys

as users otherwise that will be a nightmare.

Then your other options,

you have a Hardware Key Fob MFA device

for example this one provided by Gemalto

which is also a third party to AWS

and finally, if you are using the cloud of the government

in the US, the AWS GovCloud then you have a special Key Fob,

that looks like this, that is provided by SurePassID

which is also a 3rd party.

So that's it, we've seen the theory

on how to protect your account,

but let's go to the next lecture to implement that.

So I will see you in the next lecture.

