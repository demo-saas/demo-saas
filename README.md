# Demo SaaS
How to run a SaaS for real this time?
Where do I start when it comes to the 'technical details'?

## (Step 1) Choose your architecture for your business logic (Backend)
Well, we cannot give you a certain answer, but let us introduce you with different architectures:

1. Current approach: Run your codebase in the stateless cloud. Doesn't depend on state, rather, it's event-driven. each function and data container runs individually nature. 
    1. [Serverless](<https://serverless.com>) - Works with the following providers:
        1. [AWS Lambda](<https://aws.amazon.com/lambda>)
        2. [Google Cloud Functions](<https://cloud.google.com/functions>)
        4. [Azure Functions](<https://azure.microsoft.com/en-us/services/functions/>)

    2. Can build without serverless.
        1. [OpenWhisk](<https://openwhisk.apache.org>) - Deploy your own solution function server solution. Works w/ Serverless too!
        2. [OpenFaaS](<https://www.openfaas.com>)
            1. [OpenFaaS: From Zero to Serverless in 60 Seconds Anywhere with Alex Ellis](<https://www.youtube.com/watch?v=C3agSKv2s_w>)
    
    
2. Old approach: [Build Your own Server] - Run your codebase on servers managed by you
    2. Independent solution: You could obviously write your own components and build your own template for a SaaS, if you're interested continue reading...

**Whether you're build SaaS's business logic using using the new or old approach mentioned, you'd need to take care of the following:**
Your stack will ultimately depend on your needs, but the following components are the bare minimum: 
## (Step 2) Choose your components
1. Authentication - Handles registration and identification of your clients:
    1. [Auth0](<https://auth0.com>)
    2. [Authorize](<https://authorize.net>)
    3. [Firebase Auth](<https://firebase.google.com/auth>)
    4. [AWS Cognito](<https://aws.amazon.com/cognito/>)
    
2. Payment Gateway - Handles billing of your customer
    1. [Stripe](<https://stripe.com>)
    2. [Braintree](<https://braintree.com>)
    3. [Killbill](<https://killbill.io>)
    
3. File storage - Where are you going to store your files? Bandwidth is expensive, don't store on your server
    1. [Amazon S3](<https://aws.amazon.com/s3>)
    2. [Google Cloud Storage](<https://cloud.google.com/storage/>)
    3. [Azure Storage](<https://azure.microsoft.com/en-us/services/storage/>)
    
4. Database - Where do you store your info - in this department there a lot of options.
    1. NoSQL - common. modern tech. allow for new ways of storing data
        1. [MongoDB](<https://mongodb.com>) - Very common. Automatic sharding. Plenty of resources and documentation. Can be deployed easily on AWS / Azure / DigitalOcean
            1. [mLab](<https://mlab.com>) - MongoDB as a service
            2. [MongoDB Atlas](<https://www.mongodb.com/cloud/atlas>) -Maintained and optimized by MongoDB itself
    2. Relational Databases - common. tried out. been around for the last 30 years. uses SQL to deal with data.
        1. [Postgres](<https://postgressql.com>)
        2. [MySQL](<https://mysql.com>) / [MariaDB](<https://mariadb.com>)
        3. [CockroachDB](<https://www.cockroachlabs.com>) - SQL DB for big scale cloud services
    3. Realtime Database
        1. [Firebase Realtime Database](<https://firebase.google.com/docs/database/>) 
        2. [RethinkDB](<https://www.rethinkdb.com>) - The open-source database for the realtime web
    4. Simplifying your DB (Bonus)
        1. Realtime APIs 
                1. [Apollo](<https://www.apollographql.com>) - GraphQL client for React and other web frameworks
                    1.[Use with MongoDB](<https://www.compose.com/articles/using-graphql-with-mongodb/>)
                    2.[Use with Postgres](<https://github.com/graphile/postgraphile>)
                2. [PubNub](<https://pubnub.com>) - Streams your data to where you want in realtime. Hosted solution. Great for testing and for realtime applications
                    1.[Use with MongoDB](<https://www.pubnub.com/blog/2014-12-16-realtime-mongodb-to-fetch-and-stream-report-data/>)
                    
5. Security - you have to keep your app and data secure
    1. [Security 101 for SaaS Startups](<https://github.com/forter/security-101-for-saas-startups>)
    
6. Communication system - All of your services need to communicate with each other, while keeping the system modular. Think of this is your inner gateway system.
    1. [RabbitMQ](<https://www.rabbitmq.com>)
    2. [AWS SQS](<https://aws.amazon.com/sqs>)
    
7. [Multi-tennacy](<https://hackernoon.com/exploring-single-tenant-architectures-57c64e99eece>) - Allocating multiple containers for data and software on one server to allow for better scaling.
    1. [In the cloud](<https://hackernoon.com/multi-tenancy-after-10-years-of-cloud-computing-19de782ef899>)
    2. On your own server: Search for multitennacy for you favorite framework
 
 8. Monitoring - You have to know your use at any moment.
    1. [Prometheus](<https://prometheus.io>)

## (Step 3) Develop your front end
This could a mobile app that you're building, or maybe even a simple web app that can help your customers.
You decide what's the best for you to have your customers use your business logic / service that you've just built.
Many people decide to develop their front-end interfaces using JavaScript. Here's a great [list](https://risingstars.js.org/2017/en/) for you to look at.

## (Step 4) Learn More!
1. AWS - Amazon Web Services. Biggest platform for cloud computing. Certificates are offered. Many build on it. Worth to learn.
    1. [A two-day course teaching basics of Amazon Web Services](<https://github.com/gofore/aws-training>)
    2. [AWS training and courses](<https://hackr.io/tutorials/learn-amazon-web-services-aws>)
    3. [A curated list of AWS resources to prepare for the AWS Certifications](<https://gist.github.com/leonardofed/bbf6459ad154ad5215d354f3825435dc>)
    4. [List of AWS terms for 2017](<https://github.com/agasthik/aws-csa-2017>)
2. SaaS-in-a-Box Frameworks: (**Don't want to build your own solution?**)
        1. PHP: 
            1. [Laravel Spark](<https://spark.laravel.com>)
        2. Node:
            1. [Meatier - Battaries-included meteor solution](<https://github.com/mattkrick/meatier>)
            2. [Hackathon Starter Kit](<https://github.com/sahat/hackathon-starter>)
        3. RoR: 
            1. [Bullet-train](<https://bullettrain.co>) - Personally I think it's too expensive.

         
### (Step 5 - Bonus) Contribute 😅
