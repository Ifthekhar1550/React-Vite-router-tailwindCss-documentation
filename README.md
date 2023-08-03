# React-Vite-router-tailwindCss-documentation
Below is a detailed step-by-step guide on how to create a React app with Vite, including the setup for React Router and Tailwind CSS:Step 1: Install Node.js and npmMake sure you have Node.js and npm installed on your system. You can download them from the official website: Node.js.Step 2: Install ViteOpen your terminal or command prompt and install Vite globally using npm:npm install -g create-viteStep 3: Create a new Vite + React projectRun the following command to create a new Vite project with React template:create-vite your-project-name --template reactReplace your-project-name with the desired name for your project. This will create a new folder with the project's structure.Step 4: Navigate to the project folderChange into the newly created project directory:cd your-project-nameStep 5: Install React RouterInstall React Router using npm:npm install react-router-domStep 6: Install Tailwind CSSInstall Tailwind CSS and its peer-dependencies using npm:npm install tailwindcss postcss autoprefixerStep 7: Configure Tailwind CSSCreate a tailwind.config.js file in the root of your project with the following content:module.exports = {
  purge: ['./index.html', './src/**/*.{js,jsx,ts,tsx}'],
  darkMode: false, // or 'media' or 'class'
  theme: {
    extend: {},
  },
  variants: {
    extend: {},
  },
  plugins: [],
};Step 8: Create a CSS file for TailwindCreate a new CSS file (e.g., styles.css) in the src directory, and add the following import statements:@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';Step 9: Import CSS in the main fileOpen src/index.js and import the CSS file you just created:import React from 'react';
import ReactDOM from 'react-dom';
import './styles.css'; // Import the CSS file

ReactDOM.render(
  <React.StrictMode>
    {/* Your main app component */}
  </React.StrictMode>,
  document.getElementById('root')
);Step 10: Set up React RouterIn your main app component (usually located in src/App.js), set up React Router as follows:import React from 'react';
import { BrowserRouter as Router, Switch, Route } from 'react-router-dom';
import Home from './pages/Home';

const App = () => {
  return (
    <Router>
      <Switch>
        <Route exact path="/" component={Home} />
        {/* Add more routes here as needed */}
      </Switch>
    </Router>
  );
};

export default App;Step 11: Start the development serverFinally, run the following command to start the development server:npm run dev
