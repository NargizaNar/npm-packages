Build scripts: Using npm as a build tool

- The HTML/CSS Sass Bootstrap boilerplate and how to use dependencies
- Examination of package.json and dependencies
- Install dependencies: `npm install`

Let's write scripts in package.json

- Run for development: `npm start`
- Build for release: `npm run build`

Dependencies

- Command: `npm install packageName --save`

- boostrap

Development dependencies

- Command: `npm install packageName --save-dev`

- @parcel/transformer-sass
- gh-pages
- package

## Series:

1. Create project folder
2. index.html we create and link our style.scss file with link
3. cd into the project folder --> `npm init`

- Enter the necessary information: name, description, author, etc

4. Install dependencies

- normal dependencies
- dev dependencies

5. Create a src folder with the following below parts:

```
-> src
  -> styles
    - style.scss
  - index.html
```

6. scripts written in the package.json file

Note: with different packages you might need different commands in the scripts

but we only need:

```
"scripts": {
"start": "rm -rf dev-serve && parcel src/index.html --dist-dir dev-serve",
"build": "rm -rf build && parcel build src/index.html --dist-dir build --public-url ./",
"publish": "gh-pages -d build"
}
```

- please pay attention to the paths you have
- src/index.html or directly an index.html in the main folder? --> it depends on how you assigned your structure in the folder

7. Live View --> thanks to the packages we can now use our commands to view our website live

- `npm run start`

8. Build from our side -->

- `npm run build`

