### Note: VS Code should be launched by running `./code-fe`. 
This will load the VS Code with the appropriate configuration. This also enables configuration syncing between machines/engineers, provided the config files are kept up to date and merged periodically.

# Crash Course Plan:
* [X] Complete React tutorial	 https://reactjs.o rg/tutorial/tutorial.html
* [X] Add VS Code Settings sync
* [ ] [Start development to docker container](https://docs.docker.com/language/nodejs/develop/) 
[Helpful youtube tutorial](https://www.youtube.com/watch?v=fPtGgOJykTM)
* [ ] Complete [youtube tutorial](https://www.youtube.com/watch?v=_CBYbEGvxYY)
* [ ] Containerize app
* [ ] Deploy container to droplet
* [ ] Merge branch to master
* [ ] Update production container

# 12/1/21 Notes
* Added the React Native web app youtube tutorial.

# React Tutorial Notes
To do this, I had to install NodeJS. I used sudo apt install nodejs`. This installed a version 4 versions behind the current. To update, I followed these instructions:
https://phoenixnap.com/kb/update-node-js-version

When completing the "Create React App" exercise, I was prompted to update npm. Here's the link to the exercise:
https://reactjs.org/docs/create-a-new-react-app.html#create-react-app

I also setup linting via this tutorial:
https://medium.com/@sgroff04/configure-eslint-prettier-and-flow-in-vs-code-for-react-development-c9d95db07213
There's a handful of extensions that get installed.

I ran into some warnings when trying to install this:
https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb#eslint-config-airbnb-1

I didn't see a `.eslintrc` file after completing the related steps so I unstalled the 2 packages I installed. I also noticed that NPM threw some interesting errors. The suggested fix (from NPM) was to run `npm audit fix`. This didn't fix everything so I ran `npm audit fix --force`. I had to do this multiple times: 
* 1st try: `44 vulnerabilities (25 low, 8 moderate, 11 high)`
* 2nd try: `10 moderate severity vulnerabilities`

This yielded a loop where `npm audit fix --force` would oscillate between the two conditions described above. Time to move on...

I followed [this tutorial](https://code.visualstudio.com/docs/nodejs/reactjs-tutorial) instead and opted for ESLint to check syntax, find problems, and enforce code style. 

* ✔ How would you like to use ESLint? · syntax, find problems, & style
* ✔ What type of modules does your project use? · esm
* ✔ Which framework does your project use? · react
* ✔ Does your project use TypeScript? · No / Yes
* ✔ Where does your code run? · browser, node
* ✔ How would you like to define a style for your project? · guide
* ✔ Which style guide do you want to follow? · airbnb
* ✔ What format do you want your config file to be in? · JavaScript

After doing this, ESLint prevented the tutorial from functioning and I had to undo basically all of the linting stuff :(

Completed the tutorial!

# Setting up React Native for Android/Web
Here's the official tutorial: https://reactnative.dev/docs/environment-setup
