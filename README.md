# Set-Up for a Flask Project

### Resources

- [Tailwind CSS Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)

---

## Flask Flow

![](./assets/flask-flow.png)

### Flow:

1. The HTTP request is made and hits the server.py file.
2. Based on the route we give, it gathers up any HTML, CSS, JS, and data.
3. Then it responds back to the browser with what we return.

## Virtual Environments

> When we are working as a developer, we might find ourselves working on different projects or teams in our work place. These projects might use the same programming language, but different versions and packages along the way. How do we keep ourselves organized and avoid conflicts with our OS? With Python the answer is Virtual Environments.

### Installing our Virtual Environment tool

> While there are a couple different ways to create virtual environments, we are going to be using `pipenv` to streamline the process. To get started we need to use pip to install pipenv globally.  
> **Note** : _Only need to do once per device_

- [ ] Windows: <br><br>

      pip install pipenv

- [ ] Mac: <br><br>

      pip3 install pipenv

### Installing Flask

- [ ] Install `tailwindcss` via npm, and create your `tailwind.config.js` file.<br><br>
      npm install -D tailwindcss
      npx tailwindcss init
- [ ] Add the paths to all of your template files in your `tailwind.config.js` file.<br><br>
      **tailwind.config.js**
      /** @type {import('tailwindcss').Config} */
      module.exports = {
        content: ['./src/**/*.{js,jsx,ts,tsx}'],
        theme: {
          extend: {},
        },
        plugins: [],
      }
- [ ] Add the `@tailwind` directives for each of Tailwind’s layers to your `./src/index.css` file.<br><br>
      **index.css**
      @tailwind base;
      @tailwind components;
      @tailwind utilities;

### Install [DaisyUI](https://daisyui.com/)

- [ ] Install `daisyui` via npm:<br><br>
      npm install daisyui
- [ ] Add daisyUI to your `tailwind.config.js` files:<br><br>
      **tailwind.config.js**
      module.exports = {
        //...
        plugins: [require("daisyui")],
      }

### Start your build process

- [ ] Run either of these commands to start your project:<br><br>
      npm start             // refreshes tab upon saving
      npx nodemon           // creates new tab upon saving
