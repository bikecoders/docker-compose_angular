# Useful commands

### First of all

`docker-compose pull && docker-compose build`

--------
### Create a New Project
`docker-compose run --rm --user=$UID angular ng new YOUR-PROJECT-NAME --style sass --skip-install`

**IMPORTANT**

You need to add in the `package.json` file the following at the end of the script `start` -> `--host 0.0.0.0`

--------

### Install Packages

#### Install dependencies
`docker-compose run --rm --user=$UID angular yarn install`

#### Normal
`docker-compose run --rm --user=$UID angular yarn add PACKAGE_NAME`

#### Dev dependency
`docker-compose run --rm --user=$UID angular yarn add --dev PACKAGE_NAME`

---------------

### Remove a Package
`docker-compose run --rm --user=$UID angular yarn remove PACKAGE_NAME`

---------------

### Serve your application to development
`docker-compose up` and access in `localhost:4200`

---------------

### Generate an Angular Component
`docker-compose run --rm --user=$UID angular ng generate component COMPONENT_NAME`
> It's very important to use the parameter `--user=$UID` to generate the compoent with your user and not as `root` and be able to modify it

---------------

### Build the project
`docker-compose run --rm --user=$UID angular ng build --prod`

---------------
