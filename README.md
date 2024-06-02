# Tesla Landing Page using Tailwind

## Steps for Installation Tailwind in VS Code :-

Step 1 - Open up the folder in VS code and Open Built-in Terminal By Pressing ‘CTRL + ~’ in windows and ‘CMD + ~’.

Step 2 - Create Package.json

 ```
 npm init -y
 ```

Step 3 - Now, We need to Install Tailwind CSS Package

```
npm install -D tailwindcss postcss autoprefixer
```

Step 4 - After Completing this we will create Configuration File - ‘tailwind.config.js’
 
```
npx tailwindcss init
```

Step 5 - Create postcss.config.js file and paste these lines in it. Save it.

```
    module.exports = {
      plugins: {
        tailwindcss: {},
        autoprefixer: {},
     },
    };
```

Step 6 - Now go to the tailwind.config.js file and in the content add folder path.

```
    module.exports = {
      content: ["./public/**/*.html"],
      theme: {
        extend: {},
      },
    plugins: [],
```

Step 7 - Now we will create Folder src and then create a new main.css file in it. Copy this line of code and paste it in style.css file and save it.

 ```
@tailwind base;
@tailwind components;
@tailwind utilities
```

Step 8 - Now open package.json file and in scripts curly bracket add this script and Save it.

```
“build”: “tailwind build -i src/main.css -o public/tailwind.css”
```

Step 9 - Now we generate a Tailwind CSS file in the public folder by running this script. So again Open Terminal and write this command and press Enter.

```
npm run build
```

Step 10 - Now Create HTML file in public Folder and After that link tailwind.css in your HTML File.

```
<link href="./tailwind.css" rel="stylesheet">
```

Step 11 - Testing Tailwind works or Not.

```
<p class=’text-red-600’> I will master Tailwind CSS. </p>
```

 
## Setup Tailwind Build watcher Script

Step 1 -Open up the Package.json file and after the build:tailwind script add another script in the next line.

 ```
“watch”: “tailwind build -i src/style.css -o public/tailwind.css -
```

Step 2 - Run this command to Constantly update your Tailwind CSS.

```
npm run watch
```
