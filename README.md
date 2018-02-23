# Demo SaaS
How to run a SaaS for real this time?
Where do I start when it comes to the 'technical details'?

## (Step 1) Choose your architecture
Well, we cannot give you a certain answer, but let us introduce you with different architectures:

1. Current approach: [Serverless](<https://serverless.com>) - Run your codebase in the cloud. Without a server, each application and data container runs individually nature.

2. Old approach: [Build Your own Server] - Run your codebase on servers managed by you
    1. SaaS-in-a-Box Frameworks:
        1. [PHP: Laravel Spark](<https://spark.laravel.com>)
        2. [Node:]
            1. [Meatier - Battaries-included meteor solution](<https://github.com/mattkrick/meatier>)
            2. [Hackathon Starter Kit](<https://github.com/sahat/hackathon-starter>)
        3. RoR: Bullet-train
    2. Independent solution: You could obviously write your own components and build your own template for a SaaS, if you're interested continue reading...

**Whether you're build a SaaS using the new or old approach mentioned, you'd need to take care of the following:**
Your stack will ultimately depend on your needs, but the following components are the bare minimum: 
## (Step 2) Choose your components
1. Authentication - Handles registration and identification of your clients:
    1. [Auth0](<https://auth0.com>)
    2. [Authorize](<https://authorize.net>)
    3. [Firebase Auth](<https://firebase.google.com/auth>)
    4. [AWS Cognito](<https://aws.amazon.com/cognito/>)
2. [Multi-tennacy](<https://hackernoon.com/exploring-single-tenant-architectures-57c64e99eece>) - Allocating multiple containers for data and software on one server to allow for better scaling.
    1. [In the cloud](<https://hackernoon.com/multi-tenancy-after-10-years-of-cloud-computing-19de782ef899>)
    2. On your own server: Search for multitennacy for you favorite framework
3. Payment Gateway - Handles billing of your customer
    1. [Stripe](<http://stripe.com>)
    2. [Braintree](<http://braintree.com>)
    3. [Killbill](<http://killbill.io>)
4. File storage - Where are you going to store your files? Bandwidth is expensive, don't store on your server
    1. [Amazon S3](<http://s3.aws.com>)
5. Database - Where do you store your info - in this department there a lot of options.


