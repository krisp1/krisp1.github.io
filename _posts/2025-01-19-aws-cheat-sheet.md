---
layout: post
title: IAM Enumeration Cheat Sheet
subtitle: 
#thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [aws, cloudgoat]
author: kp
---

##### 1. List IAM Users


     aws iam list-users 

&nbsp;
##### 2. Get User Permissions


   a. List attached managed policies


     aws iam list-attached-user-policies --user-name [user-name]

     
   b. List inline policies


     aws iam list-user-policies --user-name [user-name]

     
   c. Get inline policy details


     aws iam get-user-policy --user-name [user-name] --policy-name [policy-name]


&nbsp;
##### 3. List IAM Groups and Permissions


   a. List groups for a user


     aws iam list-groups-for-user --user-name [user-name]

     
   b. List group policies


     aws iam list-attached-group-policies --group-name [group-name]

     aws iam list-group-policies --group-name [group-name]

     
   c. Get inline group policy details


     aws iam get-group-policy --group-name [group-name] --policy-name [policy-name]


&nbsp;    
##### 4. List IAM Roles and Permissions


   a. List all roles


     aws iam list-roles

     
   b. Get role details (trust policy)


     aws iam get-role --role-name [role-name]

     
   c. List attached policies


     aws iam list-attached-role-policies --role-name [role-name]

     
   d. List inline policies


     aws iam list-role-policies --role-name [role-name]

     
   e. Get inline role policy details


     aws iam get-role-policy --role-name [role-name] --policy-name [policy-name]

&nbsp;
##### 5. Get and Decode Policy Documents


   a. Get a managed policy document (by ARN or name)


     aws iam get-policy --policy-arn [policy-arn]

     aws iam get-policy-version --policy-arn [policy-arn] --version-id [version-id]

&nbsp;
##### 6. View Full IAM Snapshot


   a. Dump all IAM permissions (users, roles, groups, policies)


     aws iam get-account-authorization-details



 Use this to build a full IAM permissions map. Add `--filter` to target roles/users/groups specifically.
