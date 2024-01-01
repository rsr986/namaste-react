<script
    crossorigin
    src="https://unpkg.com/react@18/umd/react.development.js"
></script>
<script
    crossorigin
    src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"
></script>

Namaste React by Sreekanth

git init
git add .
git commit -m "Episode-01"
git branch -M main
git remote add origin https://github.com/rsr986/namaste-react.git
git push -u origin main

npm init

- bundler (ex: parcel, webpack, vite)
- dev dependencies, normal dependencies

npm install -D parcel // -D means dev dependency

- parcel "^2.8.3" "(tilde/caret)major.minor.patch" // what is caret(^) in this version number, and also find about tilde(~) in version number
- tilde(~) will update the package to all future patch versions automatically when available
- caret(^) will update the package to all future minor verisons automatically when available

- what is package-lock.json, what is diff between package.json and package-lock.json
- what is node-modules folder
- what is transitive dependencies
- if you have package.json, you can recreate node_modules by "npm install", node_modules folder is not required to push to repository

npx parcel index.html

- diff between npm and npx?, npm is package installer, npx is package executor

npm install react
npm install react-dom

import React from "react";
import ReactDOM from "react-dom";

- 🚨 @parcel/transformer-js: Browser scripts cannot have imports or exports.
- this error coming from App.js. normal javascript does not have import statements
- <script type="module" src="./App.js"></script>

# Parcel (parceljs.org)

- Dev Build
- Local Server
- HMR - Hot Module Replacement
- File Watching Algorithm - written in C++
- Catching - Faster builds
- Image Optimization
- Minification
- Bundling
- Compressing
- Consistant Hashing
- Code splitting
- Differential Bundling - support older browsers
- Diagnostic
- Better Error Handling
- HTTPs
- Tree shaking - remove unsed code
- Diffrent builds for dev and prod

- for prod build use below command
  npx parcel build index.html // if error comes remove App.js from package.json
- the ouput will be stored in dist folder

- BrosersList (browserslist.dev) - can configure supported browsers in package.json
  "browsersList": [
  "last 2 Chrome version",
  "last 2 Firefox version"
  ]
