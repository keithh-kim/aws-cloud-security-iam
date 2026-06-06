<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Keith Kimani  
**Email:** keithh.kimani@gmail.com

---

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate cloud security using aws iam

### Tools and concepts

Services I used were IAM and EC2 Key concepts I learnt include creating ec2 instace, policy creation using json etc

### Project reflection

This project took me approximately 1hr to 1.5 hrs The most challenging part was the policies in json It was most rewarding to finish the project.

---

## Tags

### What I did in this step

In this step, I will launch 2 ec2 instances to increase computing power

### Understanding tags

Tags are used to filter out and easily identify resources in aws

### My tag configuration

The tag I’ve used on my EC2 instances is called Env The value I’ve assigned for my instances are production and development

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy to access the development instance so that the dev team can only access the dev instance.

### Understanding IAM policies

IAM Policies are a set of rules that determine what you can do with AWS resources

### The policy I set up

For this project, I’ve set up a policy using JSON

### Policy effect

I’ve created a policy that allows users with the development tag to work on ec2 instances and are also barred from changing those tags

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means that Effect is an allow or deny that permits actions , Action is a list of all the things you can do that are either allowed or denied and resource is that recources does the policy apply to?


---

## My JSON Policy

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will use AWS alias to simplify user login

### Understanding account aliases

An account alias is a way to easily remember sign in links and replice account id with names you can remember

### Setting up my account alias

Creating an account alias took me 30sec. Now, my new AWS console sign-in URL is https://nextwork-alias-keith.signin.aws.amazon.com/console

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will create an IAM group and user so that the intern can access the dev ec2 instance

### Understanding user groups

IAM user groups are a collection of users for easier user management like assigning policies

### Attaching policies to user groups

I attached the policy I created to this user group, which means. it applies to all the users who are part of the group

### Understanding IAM users

IAM users are people that are used to interact with aws resources

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is a csv file or through copy pasting the alias, username and password

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed some dashbaord panels are showing denied.This was because the user does not have the appropriate permissions

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will log in using the new details and access the development instance

### Testing policy actions

I tested my JSON IAM policy by trying to stop the prod instance which refused.

### Stopping the production instance

When I tried to stop the production instance there was an error.This was because the user does not have the permissions to stop instances

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance it stopped. This was because it was not included in the json policy

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to look at policy simulator. I'm doing this because i want to test without affection aws resources

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is a testing enivironment ro see how the IAM permissions work. It is nice for testing without affecting the other users

### How I used the simulator

Allowed

![Image](http://learn.nextwork.org/blissful_purple_fierce_pigeon/uploads/aws-security-iam_069d8a621)

---

---
