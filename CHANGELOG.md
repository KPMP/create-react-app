## 1.1.2 (April 10, 2019)

Changes:

- Capturing some styling changes

## 1.1.0 (March 29, 2019)

Changes:

- Added ErrorBoundary to capture errors and send user to Oops page
- Added Oops page and routing
- Moved the directions for a new project to a new component

## 1.0.0 (March 28, 2019)

Changes:

- Update to several library versions to keep up to date
- Updated the header to match the new styling
- Added a KPMP footer

## 0.1.0 (January, 2019)

v0.1.0 was created based on v2.1.3 from facebook (https://github.com/facebook/create-react-app)

This fork was created in order for the KPMP DVC to have a custom react-scripts that will allow us to more rapidly create new apps for the KPMP project (http://kpmp.org).

Changes:

- Updates to init.js to include common packages in a new react-app
- Updates to init.js to create the corresponding package.json with those common packages
- Updates to App.js to include developer instructions for setting up a new web project
- Updates to App.js to include redux and react-ga
- Initial reducer to clear state
- .travis.yml file created to aid in setting up CI builds
- Initial scss files with some common styling
- Common KPMP Navbar included
- KPMP favicon included

## 2.1.3 (January 4, 2019)

v2.1.3 is a maintenance release to fix a [vulnerability in webpack-dev-server](https://www.npmjs.com/advisories/725).
