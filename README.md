# Recruitment task

## Background
The project consists of three modules:
* Users,
* Companies,
* Payments.

The "users" and "companies" module are simple CRUDs, one with REST API, the second one with GraphQL API.  
The "payments" module tends to use CQRS. We have two commands exposed from the module, TopUpCompanyCommand, 
and ChargeUserCommand.

A "user" represents just a user of our system. Every user belongs to a company – that also has a representation in our
system. One company can have multiple users assigned.

Users have funds in our system. We can change their balance through those two commands in the "payments" module.

The DB used in the project is sqlite3 for simplicity, set up along with TypeORM. Also, please do not care about
authorization and security in this project.

If you want to reorganize the code – feel free. The project is only a suggestion.

## What is the must-have of the recruitment task?
1. During the compilation of the project, the compiler complains about a few things. We would like you to fix the errors.
Please keep the "strict" type checking option turned on.
2. The modules in the projects are only scaffoldings. "Users" and "companies" modules do not work. Please find missing
parts and implement them to make those modules fully functional.

## What is nice to have in the task?
1. In the "payments" module, we have two commands without handlers. We would like you to make the "payments" module
working, with REST API exposed through the PaymentsController. The user's balance should never get below zero. We
suggest using the "@nestjs/cqrs" package in the app.
2. We got a new business requirement that (you do not need to take both): 
   1. Some companies may have debt.
   2. Accountants need a simple page (just plain HTML "company name – amount") with a report in the app – an average of
   a balance of every company.  
 
   How would you implement the change? Please describe steps or put the requirement into the code.

## How to send us the solution?
Please do not make a public PR to this repo. We prefer to be invited to a private fork of the repository.