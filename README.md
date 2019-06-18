### Node demo project 

## About Project

- Language: Node (10+)
- Dependenctmanager: npm
- Framework: Express
- Database: PostgreSql
- TDD: mocha assert
- ORM: sequelize

## How to start a new project in node.js
  
    Open CLI as administrator and run following commands to set up at local:
   - **install express framework, run the cmd**
        >
            express app_name
            
            In case 'express' is not recognized as an internal or external command, then use follwoing commands:
 a) npm install -g express-generator
 b) npm link express

   - **install express from the command line using express-generator**
        >
            npm install -g express-generator

   - **Set permissions**
       >
            sudo chmod -R 755 { project-path }

   - **Go to project directory**
       > 
            cd ucreate-review-tool 

   - **Copy .env.example to .env**
       > 
            cp .env.example .env
   - **Install node.js**
      > 
            To install node.js follow below url :
            https://nodejs.org/en/download/
   - **Install the dependencies**    
      >
            npm install
  


# Database installation
   - **How to install postgresql ( Ubuntu )**
     >
        sudo apt-get install postgresql postgresql-contrib
   - **Which UI being used to connect to DB**
     >
        pgadmin
   - **Create  database**
     >
         1. login to pgsql
         	 sudo psql -h localhost -U postgres    
         2. create database review-tool
         	 create database review-tool
         

# Post Installation steps
 - **Run database migrations**
    >
        sequelize db:migrate

- **Start server**
    >
        npm start
        The API will be running on http://localhost:4000 now [may differ in case port already in use]

## External Services/API Reference
- **Email Service**
    >
        - PostMark
        - Create Account on Postmark (https://postmarkapp.com) and verify the sender signatures.
        - Create email templetes on Postmark
        - Set Postmark token and template IDs in environment/config variables
- **Images Storage**
    >
        - AWS S3
         1. Your S3 credentials can be found on the Security Credentials section of the AWS Acount
         2. Open the S3 section of the AWS Management Console and create a new bucket.
         3. Set AWS access key, secret key, bucket name etc. as environment variables.
        Reference: https://aws.amazon.com/s3
- **Github API**
    >
        Github API is used for getting the commits/comments/projects/code
        Reference: https://api.github.com


