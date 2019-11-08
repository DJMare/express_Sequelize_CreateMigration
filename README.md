# express_Sequelize_CreateMigration
An express app utilizing sequelize cli to connect to mySql workbence and create a migration. 

COMMAND PROMPT

(1) Run the following to navigate to your Desktop: 

    cd Desktop

(2) Create a new folder on desktop: 

    mkdir Express

(3) Navigate to the Express directory: 

    cd Express

(4) Run the following command to install the Express generator globally onto your computer: 

    npm install express-generator -g

(5) Enter the following command to generate the Express starter app. This will set the view to use Handlebars and will name the app express_CreateMigration: 

    express --view=hbs express_Sequelize_CreateMigration

(6) Once the process is complete, navigate into the express_Sequelize_CreateMigration directory: 

    cd express_Sequelize_CreateMigration

(7) Now in the express_ directory, run the following: 

    npm install

(8) Install Nodemon globally: 

    npm install -g nodemon
    
(9) Install Nodemon as a devDependency in the package.json file within the express_CreateMigration directory:

    npm install -save-dev nodemon
    
(10) Install mysql2:

    npm install --save mysql2

(11) Install sequelize: 

    npm install --save sequelize@5.15.1

(12) Open in VS code:

    code . 


VS CODE

(13) Navigate to the routes/index.js file: ![open index js file (express_Sequelize_CreateMigration)](https://user-images.githubusercontent.com/35668707/68440663-c9791080-0199-11ea-8208-0ea332d772bd.JPG)


(14) Require mysql2 in routes/index.js file: ![require mysql2 in index js file (express_Sequelize_CreateMigration)](https://user-images.githubusercontent.com/35668707/68440731-f7f6eb80-0199-11ea-9232-4850a8b5a94e.JPG)


COMMAND PROMPT

(15) Install Sequelize CLI commands globally onto your computer: 

    npm install -g sequelize-cli

(16) Create necessary sequelize folders and filed in project:

    sequelize init
 

VS CODE

(17) Open config/config.json file and change settings to connect to the database: ![open config json file (express_Sequelize_CreateMigration)](https://user-images.githubusercontent.com/35668707/68440965-9daa5a80-019a-11ea-94dd-3dafa4523807.JPG)

![update password and datbase info in config json file (express_Sequelize_CreateMigration)](https://user-images.githubusercontent.com/35668707/68441042-dfd39c00-019a-11ea-8e12-8c9601e6b232.JPG)


COMMAND PROMPT

(18) Install mysql2 globally so sequelize CLI will be able to connect to the database:

    npm install -g mysql2
    
(19) Install sequelize-auto tool to generate model files: 

    npm install -g sequelize-auto

    
MYSQL WORKBENCH

(20) Open database in mySql workbench to view columns in table: ![mySQL workbench schemas - Sakila database](https://user-images.githubusercontent.com/35668707/68350595-b5f47980-00b5-11ea-8d1b-dd9879921010.JPG)

COMMAND PROMPT

(21) Generate a model file for the actor table. (-h: IP/Hostname; -d: Database; -u: Username for database; -x: Password for database; -o: directory to place the models; -t: comma-seperated names of tables to import):  

    sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t actor
    

VS CODE

(22) Open app.js file at the root of the project and include the './model" folder so that the models are available everywhere in the application: ![open app js file (express_Sequelize_CreateMigration)](https://user-images.githubusercontent.com/35668707/68441136-2e813600-019b-11ea-9b82-604b4baaad1e.JPG)


COMMAND PROMPT

(23) Run nodemon in terminal to see DB sync'd up: 


NODEMON NOTE

Sometimes nodemon crashes in Windows 10 and there is a simple fix:

(1) Open Task manager (press Ctrl+Alt+Delete)

(2) Select the 'Processes tab'

(3) Search for 'Node.js: Server-side JavaScript'

(4) Select it and click on 'End task' button

Now you can run npm start.
