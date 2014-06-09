# PhoneGap App hosted on Heroku

> Template for hosting an app with connect-phonegap

## Preview

Open your [PhoneGap Developer App](http://app.phonegap.com) and connect to:

http://phonegap-app-heroku.herokuapp.com

## Running the Template Project

Start the local server:

    $ npm install
    $ npm start

Now connect to the IP address with your PhoneGap Developer App.

## Installing to an Existing Project

### 1. Copy Template Files

Copy the following files to your existing PhoneGap / Cordova project:

- `Procfile` used for deploying to Heroku
- `lib/` directory for running the server
- `package.json` for describing the server dependencies

The resulting project will look something like:

    my-app/
    |__ lib/
    |__ merges/
    |__ platforms/
    |__ plugins/
    |__ www/
    |__ Procfile
    |__ package.json

### 2. Create a Heroku Instance

    $ cd my-app/
    $ heroku apps:create my-heroku-app-name
    Creating my-heroku-app-name... done, stack is cedar
    http://my-heroku-app-name.heroku.com/ | git@heroku.com:my-heroku-app-name.git

### 3. Update Files

#### package.json

Update the following the keys:

- `name`
- `descriptions`
- `repository`

#### lib/

If you hate having a `lib/` directory, you can move the `lib/index.js` to any
location. Just remember to update the `start` key with the new location.

### 3. Deploy to Heroku

Install the npm dependencies:

    $ npm install

Test locally:

    $ npm start

Deploy to Heroku:

    $ git commit -am "My latest changes"
    $ git push heroku master
