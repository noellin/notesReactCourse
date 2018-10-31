> markdown: https://guides.github.com/features/mastering-markdown/  
> Preview: Chrome extension and QuickLook / space key on the file 

React Course - Udemy - Andrew Mead
============================================

# Setting up environment
- Node, npm, yarn
  ```
  node -v / node --version
  npm -v  / npm --version
  yarn --version
  npm install -g yarn

  npm list -g --depth=0  //check modules installed globally
  npm config set prefix ~/npm  //check path for global modules  
  ```
- App  
  http://indecision.mead.io  
  https://github.com/andrewjmead/react-course-2-indecision-app

- VSC extensions
  - Sublime Text Keymap
  - Babel ES6/ES7
  - emmet (autocomplete - built-in VSC)

- Web Server  
  ```
  yarn global add live-server
  live-server -v
  live-server public (inside indecision-app folder)
  ```

# Hello React
  - Using CDN
    ```
    <script src="https://unpkg.com/react@16.0.0/umd/react.development.js"></script>  
    <script src="https://unpkg.com/react-dom@16.0.0/umd/react-dom.development.js"></script>  
    (react-dom is specific for the browser, there's onother for VR, native etc)
    ``` 
  - JSX vs plain Javascript  
    Browsers do not understand JSX, tools like babel translates it
    - JSX   
      ```const template = <p id="my_p">This is JSX from app.js!</p>``` 
    - JavaScript (after babel using the web 'try it out') 
      ```javascript
      var template = React.createElement(
        "p",
        { id: "my_p" },
        "This is JSX from app.js!"
      );
      ```
    - install babel with presets: react and env (includes es2015, es2016 and es2017)   
      ```
      yarn global add babel-cli@6.24.1
      yarn init
      yarn add babel-preset-react@6.24.1 babel-preset-env@1.5.2
      live-server public
      babel src/app.js --out-file=public/scripts/app.js --presets=env,react --watch 
      (manual process to compile src file)
      ```

<hr>  
  -
  -
  -
  -
  -
  -
<hr>