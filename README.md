# MultiMath
MultiMath is a math game to learn multiplication and is written in TypeScript.

MultiMath is the result of completing the course [TypeScript 4: Getting Started](https://app.pluralsight.com/library/courses/typescript-getting-started/table-of-contents) on Pluralsight.com. It concerns the most important features of TypeScript and being productive when building client-side web applications and NodeJS applications: installing TypeScript and configuring a project; taking advantage of built-in types; writing better functions with typeScript; creating and using custom types; creating and consuming modules; and being more productive with type declaration files.


## Technology
- Node.js version 18.1.0

- TypeScript version 4.6.4

- See package.json file for a complete list


## Run
1. Install Node.js version 18.1.0 (I recommend using nvm - node version manager)

2. Clone this repository:
```
git clone https://github.com/g-esco101/multimath.git
```

3. Move to the main project directory:
```
cd multimath
```

4. Install packages referenced in package.json:
```
npm install
```

5. Intall TypeScript version 4.6.4 (this intalls TypeScript globally):
```
npm install -g typescript
```

6. Run the app:
```
npm start
```

The will run at http://localhost:8080/


## Creating project from an empty directory
This section is intended for people taking the course and wish to create the project from an empty directory. It uses the latest versions of 
the tools/dependencies instead of using the versions in the course.

- Make a new directory to use as the main directory for the project (I named mine multimath):
```
mkdir multimath
```

- Move into this directory:
```
cd multimath
```

- Initialize the project (this will create the package.json file):
```
npm init -y
```

- Install dependencies:
```
npm install ts-loader typescript webpack webpack-cli webpack-dev-server
```

- Add start script to the package.json file using your IDE or text editor:
```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack serve"
  }
```

- Make a directory named public inside the main project directory (multimath). Webpack will serve your contents from this directory.
```
mkdir public
```

- In the main project directory (multimath), add these files and directories from instructor's project: .gitignore, favicon.png, tsconfig.json, and webpack.config.js.

- In the public directory, add these files and directories from the instructor's project:
index.html, css, and app. Moving the app directory here will give you access to it from chrome dev tools.

- Update the entry option in the webpack.config.js file:
```
entry: './public/app/app.ts'
```

- In the public directory, make a directory named js. This is where all your js files must be stored in order for them to run:
```
cd public
mkdir js
```
You will have to move your js files here until the instructor sets up the tsconfig.json file in the course. When he does, you will have to update the tsconfig.json file to use "outDir": "./public/js". Don't forget this step!
Note: The src attributes in your script tags will be different from those used by the instructor in the index.html file, e.g. use <script src="./js/app.js" ></script> instead of <script src="/app/app.js" ></script>.

- Install typescript (this installs TypeScript globally):
```
npm install -g typescript
```

- In webpack.config.js delete this line (this inline option has been removed from webpack):
'''
inline: false
''' 

- At this point the project is setup and you are ready to begin coding!



## Other Useful Commands

### Transpile TypeScript to JavaScript
From the multimath directory move to the directory that has the tsconfig.json file:
```
cd ./public/app
```
Run the TypeScript Compiler:
```
tsc
```
This command will transpile the TypeScript to JavaScript using the settings in the tsconfig.json file. The JavaScript files will be automatically generated in a directory named js (also automatically generated) in the public directory.


### Create tsconfig.json
```
tsc --init
```

