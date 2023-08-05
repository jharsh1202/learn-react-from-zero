Get started with Frontend from zero using Nextjs documentation: 

for Js and React Basics (https://nextjs.org/learn/foundations/from-javascript-to-react)

Read about React, DOM, React DOM methods

without react, working with DOM is verbose
<!-- index.html -->
<html>
  <body>
    <div id="app"></div>

    <script type="text/javascript">
      // Select the div element with 'app' id
      const app = document.getElementById('app');

      // Create a new H1 element
      const header = document.createElement('h1');

      // Create a new text node for the H1 element
      const headerContent = document.createTextNode(
        'Develop. Preview. Ship. 🚀',
      );

      // Append the text to the H1 element
      header.appendChild(headerContent);

      // Place the H1 element inside the div
      app.appendChild(header);
    </script>
  </body>
</html>


with React

<!-- index.html -->
<html>
  <body>
    <div id="app"></div>
    
    //load scripts from unpkg
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>. //react (declarative UI library)
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script> // react-dom (DOM-specific methods that enable you to use React with the DOM)

    <script type="text/javascript">
      const app = document.getElementById('app');
      ReactDOM.render(<h1>Develop. Preview. Ship. 🚀</h1>, app);
    </script>
  </body>
</html>


this will throw an error though as browsers don’t understand JSX, so you’ll need a JavaScript compiler, like  Babel, to transform JSX -> Js.

add Babel
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script> //also you will need to inform Babel what code to transform by changing the script type to type=text/jsx.


HTML above represents the initial page content, whereas the DOM represents the updated page content which was changed by the JavaScript code you wrote, instead tell React what you want to happen to the user interface, and React will figure out the steps of how to update the DOM on your behalf.



---------------------------------------------------------------------------------------------------------------------------------------

JavaScript basics for React (Basic) (https://nextjs.org/learn/foundations/from-javascript-to-react/essential-javascript-react)

React (https://react.dev/learn/ and https://react.dev/learn/describing-the-ui)

---------------------------------------------------------------------------------------------------------------------------------------
NextJs (https://nextjs.org/docs/getting-started/installation)
- install node.js from (https://nodejs.org/en)
- create nextjs app with (npx create-next-app)
    - What is your project named? <your-app-name>
    - Would you like to use TypeScript? <No/Yes> (strongly typed superset of JS allows to catch errors during development)
    - Would you like to use ESLint? <No/Yes> (analyze and identify patterns of problematic or questionable code, helps maintaining code quality, enforce coding standards, and catch potential errors and bugs)
    - Would you like to use Tailwind CSS? <No/Yes> (CSS frameworks used for building user interfaces)
    - Would you like to use `src/` directory? <No/Yes> (ideal for larger projects)
    - Would you like to use App Router? (recommended) <No/Yes> (yes as recommended)
    - Would you like to customize the default import alias? <No/Yes> (No)
- npm install
- npm run build
- npm start (check http://localhost:3000 on your browser)
