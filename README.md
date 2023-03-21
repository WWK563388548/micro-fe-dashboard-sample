# micro-fe-dashboard-sample
This is a sample project for micro front-end technology validation, you can check the commit history to see the logic added and modified in each step

## Tech Stack
Auth app, Marketing app, Container app are building by React <br>
Dashboard app is building by Vue3 <br>
Deployment: github action workflow, AWS S3, AWS CloudFront <br>

## Demo
Check Demo url: https://d338ek8892e0fm.cloudfront.net

## How to run the project on local:
1. git clone project
2. Run `cd` command jump into every sub-app, and run `npm install`
3. Run `cd` command jump into every sub-app, then run `npm run start`
4. Access `localhost: 9080` (Container App - Main App)

## File structure
    .
    ├── .github
    |   ├── workflows                   # Deployment script
    |   |   ├── auth.yml
    |   |   ├── dashboard.yml
    |   |   ├── container.yml
    |   |   └── marketing.yml
    ├── packages                        # Container App & Sub-Apps
    │   ├── auth                        # Auth Sub-App
    |   |   ├── public
    |   |   ├── config
    |   |   ├── src
    |   |   ├── package.json
    |   |   └── ... 
    │   ├── container                   # Container App
    |   |   ├── public
    |   |   ├── config
    |   |   ├── src
    |   |   ├── package.json
    |   |   └── ... 
    │   ├── marketing                   # Marketing Sub-App
    |   |   ├── public
    |   |   ├── config
    |   |   ├── src
    |   |   ├── package.json
    |   |   └── ... 
    │   └── dashboard                   # Dashboard Sub-App
    |   |   ├── public
    |   |   ├── config
    |   |   ├── src
    |   |   ├── package.json
    |   |   └── ... 
    └── README.md

## How to deploy:
1. Prepare your AWS account
2. Create your own S3 bucket and cloudFront distribution
3. Prepare the access key and other secrets (You can read `/.github/**.yml`files)
 
### Deployment
- Want to deploy each microfrontend independently (including the container)
- Location of child app remoteEntry.js files must be known at build time
- Many front-end deployment solutions assume you're deploying a single project. We need something that can handle multiple different ones
- Probably need a CI/CD pipline of some sort
- At present, the remoteEntry.js file name is fixed. Need to think about caching issues


