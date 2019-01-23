#### NOTE: This is a customized version of create-react-app to allow the KPMP DVC developers to more quickly create new applications with common components!!

For the standard README from create-react-app go [here](https://github.com/facebook/create-react-app/blob/master/README.md)

# KPMP developer notes

## Using the custom react-scripts

`create-react-app <app-name> --scripts-version kpmp-custom-react-scripts`

## Publishing changes

- After you have made all of the changes you want, open packages/react-scripts/package.json and change the version number and save it
- Go to the command line and type `npm login` and login as the kpmp-dev account
- Change directory to where you have our version of create-react-app checked out
- Go to the react-scripts directory: `cd packages/react-scripts`
- `npm publish`

## Updating the application

All of the files that are created when you use this (except the package.json) live under packages/react-scripts/template
Any changes to files in this section will produce a new default application.
Be sure to note any changes in the CHANGELOG.md
Publish your changes (see 'Publishing changes above)
Check your changes into git

## Changing default dependencies

### How to add packages

- Open packages/react-scripts/scripts/init.js
  - Search for "\*\*\* Add new"
  - If the new package is a dependency (it will be used in production code):
    - Add a line like so: `appPackage.dependencies.package = "version"`
    - If the dependency contains special characters (like a hyphen): `appPackage.dependencies["package-with-hyphen"] = "version"`
  - If the new package is a devDependency (it will only be used when building/testing the application):
    - Add a line below `appPackage.devDependencies = {}` that looks like: `appPackage.devDependencies.package = "version"`
    - If the dependency contains special characters (like a hyphen): appPackage.devDependencies["package-with-hyphen"] = "version"`
  - Search for "\*\*\* You also"
    - Add the package to the list in args.push like so: `'package-name@version'`
    - Be sure to add the required commas in the list
- Update the CHANGELOG.md with the changes you made
- Publish your changes (see 'Publishing changes at the top of this README')
- Check your changes into git

### How to update package versions

- Open packages/react-scripts/scripts/init.js
  - Search for the package name you want to update
  - Change the version number under the "\***\* Add new..." comment AND under the "\*\*** You also..." comment
- Update the CHANGELOG.md with the changes you made
- Publish your changes (see 'Publishing changes at the top of this README')
- Check your changes into git
