## tailwindcss

check the documentation

  this is the installation steps for just tailwind alone with no frameworks. there are guide on the tailwind website on how to install it with frameworks.

create your project folder and cd into it.

- npm init -y
- npm install -D tailwindcss
- npx tailwindcss init

 replace the content of the tailwind.config.js file with the one copy from the tailwindcss documentation website.
 
 
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}


change the content line to :
  content: ["*.{html,js}"],


- create your css folder the inside it create a css file call input.css. then copy this code from the website and paste it inside
 
@tailwind base;
@tailwind components;
@tailwind utilities; 

- go to the package.jon file, inside scrips
remove the test and write this

"build" :"tailwindcss -i ./css/input.css -o ./dist/output.css"

this code is in the documentation, copy it and arrange it according to your folder and file structure.


-  to the terminal and type: npm run build

it will build and generate the dist/output.css directory and file in your project folder

-  add this same line of code under the build

"watch" :"tailwindcss -i ./css/input.css -o ./dist/output.css --watch"

  when you start creating you html files  the css you link to the html files is the one in the dist folder(output).
  
- to start the project type: npm run watch


 then open the project with a live server.
 

 ----------------------------------------
 
 
By default, Tailwind uses a mobile-first breakpoint system, similar to what you might be used to in other frameworks like Bootstrap.

 What this means is that unprefixed utilities (like uppercase) take effect on all screen sizes, while prefixed utilities (like md:uppercase) only take effect at the specified breakpoint and above.

Where this approach surprises people most often is that to style something for mobile, you need to use the unprefixed version of a utility, not the sm: prefixed version. Don’t think of sm: as meaning “on small screens”, think of it as “at the small breakpoint“
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 