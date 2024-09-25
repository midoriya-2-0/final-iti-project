### Firstly: we need Create a virtual environment

```bash
virtualenv venv
```

### Then: Activate the virtual environment

```bash
venv\Scripts\activate
```

### After that: Install django

```bash
pip install django
```

### After that: We need to install Tailwind CSS

1- we will write this command to create a package.json file
```bash

npm init
```
and enter the required information
then press Enter Until he tell you to write yes 

2- install tailwindcss
```bash
npm install -D tailwindcss
npx tailwindcss init
```
3- Configure your template paths in the tailwind.config.js file
```bash
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./templates/**/*.html"],
  theme: {
    extend: {
      colors: {},
      fontFamily: {
        lato: ["Lato"],
        poppins: ["Poppins"],
        Playpen: ["Playpen"],
      },
    },
  },
  plugins: [],
};
```

4- Go to Package.json and add this line to the scripts
```bash
"build-css" : "tailwindcss -i ./static/css/input.css -o ./static/css/styles.css --watch"
```

### Finally: Run the server and run the tailwindcss

```bash
python manage.py runserver
npm run build-css
```

### In our project we will do app for every part in the website

#### → We will follow this steps after creating the app

1- Create the app
```bash
python manage.py startapp app_name
```

2- Add the app to the installed apps in the settings.py

3- Create the urls.py file in the app folder

4- Add the urls of the app in the main urls.py file

5- Create functions of that app in the views.py file in the app folder

6- Create folder for the templates of that app in templates folder




