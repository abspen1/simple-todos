# Simple Todos

This is the tutorial for Meteor web applications using Vue. Can find the same tutorial I followed [here](https://www.meteor.com/tutorials/vue/creating-an-app)

## Dependencies

Necessary dependencies for this implementation

### Install Meteor

# OSX/Linux
'''bash
curl https://install.meteor.com/ | sh
'''

### npm packages

```bash
meteor npm install --save vue
meteor add akryum:vue-component
meteor npm install --save vue-meteor-tracker
meteor npm install --save classnames

# Testing
meteor add meteortesting:mocha
meteor npm install --save-dev chai
```

### static html

```bash
meteor remove blaze-html-templates
meteor add static-html
```

### Blaze UI for accounts

```bash
meteor add vuejs:blaze-integration
```

### Remove insecure

Every newly created Meteor project has the **insecure** package added by default. This is the package that allows us to edit the database from the client. It's useful when prototyping, but now we are taking off the training wheels. To remove this package, go to your app directory and run:

```bash
meteor remove insecure
```

### Remove autopublish

st like with **insecure** in the last step, all new Meteor apps start with the **autopublish** package, which automatically synchronizes all of the database contents to the client. Let's remove it and see what happens:

```bash
meteor remove autopublish
```

## Running && Testing

Some examples of running and testing the web application

### Running

```bash
cd simple-todos
meteor
```

### Testing

- Run app in test mode

```bash
TEST_WATCH=1 meteor test --driver-package meteortesting:mocha
```

- This command is suitable for running in a continuous integration (CI) environment such as Travis CI or CircleCI, since it runs only your server-side tests and then exits with 0 if all the tests passed.

```bash
meteor test --once --driver-package meteortesting:mocha
```

- If you would like to run your tests while developing your application (and re-run them whenever the development server restarts), consider using **meteor npm run test-app**, which is equivalent to

```bash
TEST_WATCH=1 meteor test --full-app --driver-package meteortesting:mocha
```

## Database

MongoDB integrates with Meteor. Here is how to run mongo server.

```bash
meteor mongo
```

## Create IOS app //Optional

Instructions [here](https://www.meteor.com/tutorials/vue/running-on-mobile)
