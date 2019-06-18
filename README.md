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
   - **Install express framework, run the command**
        >
            
            express app_name

   - **In case 'express' is not recognized as an internal or external command**
        >
            
            run the following commands:
            
            npm install -g express-generator
            npm link express
            
            npm link package-name will create a symbolic link from globally-installed 
            package-name to node_modules/ of the current folder.
            Note that package-name is taken from package.json, not from directory name.
            
            After these two commands, run the command:
            express app_name

   - **Changed the directory path to app**
        >
            cd app_name

   - **Install the dependencies**
       >
            npm install



## Database installation
   - **How to install postgresql ( Ubuntu )**
     >
             
         sudo apt-get install postgresql postgresql-contrib
         
   - **Which UI being used to connect to DB**
     >
         
         pgadmin
        
   - **Create  database**
     >
            
         1. login to pgsql
         	 - sudo psql -h localhost -U postgres    
         2. create database 
         	 - create database database_name
         

## Post Installation steps
   - **Install the sequelize ORM **
       >   
         
         npm install sequelize --save
         npm install --save pg pg-hstore  //used to connect with postgres DB
         npm install sequelize-cli --save  //used to run the sequelize commands in terminal
         node_modules/.bin/sequelize init // create the models, migrations, seeders, config folders

   - **Create first migration using the below command:**
       >
         sequelize model:generate --name User --attributes name:string, username:string, email:string
   
   - **Create seeder using the below command:**
       >
         node_modules/.bin/sequelize seed:generate --name User

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


