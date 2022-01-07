So here are some general guidelines

on IAM and Best Practices,

because I don't want you, if you go to use AWS

to make some mistakes.

So do not use a root accounts

except when you set up your AWS account.

So by now you should have two accounts,

a root account and your own personal accounts.

And remember, one AWS user is equal to one physical user.

So if a friend of yours wants to use AWS,

do not give them your credentials,

instead of create another user for them.

You can assign users to groups

and assign permission to groups to make sure

that security is managed at the group level.

And you should create a strong password policy.

Also, if you can use and enforce the use

of Multi Factor Authentication, or MFA, to really guarantee

that your account is going to be safe or safer from hackers.

Then, you should create and use roles whenever

you're giving permissions to AWS services,

and that includes easy two instances

which are virtual servers.

If you were to use AWS programmatically,

or using the CLI, so the CLI or some SDK,

you must generate access keys,

and these access keys are just like passwords.

They're very secrets, so just keep them for yourself.

Finally, if you wanted to audit permissions

within your accounts,

you can use the IAM Credentials Reports,

and also IAM access analyzer.

Finally, never, ever, ever share your IAM users

and access keys.

I am very serious about it.

So that's it.

We are nearing the end of this section.

You know, everything about IAM.

I will see you in the next lecture.

