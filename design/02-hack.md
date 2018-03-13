# Bootstrap Italia Playground

Bootstrap Italia is a theme based on [Bootstrap 4](https://getbootstrap.com/docs/4.0/getting-started/introduction/) to create responsive, mobile-first web applications.

Bootstrap Italia inherits all functionalities, components, mixins and gridsystem from Bootstrap 4, and adapts them to follow the [design guidelines for Italian Public Administrations web services](https://design-italia.readthedocs.io/it/stable/index.html).

With this activity you will learn how to hack and contribute on this toolkit.

# Prerequisites

In order to hack on the toolkit, you have to first download the source code and install any missing dependencies.

* Install Ruby, Node.js and bundler.
* Clone the repo: `git clone https://github.com/italia/bootstrap-italia.git`
* Install dependencies: `bundle install && npm install`

If you performed all the instructions correctly, you wil be able to see the documentation by typing `npm start`, which will launch Jekyll. If everything has worked correctly you should be able to see the documentation on `http://localhost:4000`. **Note:** sometimes the very first initialization may fail, and you will only see `Cannot GET /` in your browser. If this is your case, just exit npm (Ctrl+C) and re-launch `npm start`.

You can find a more detailed explanation (in Italian) on https://italia.github.io/bootstrap-italia/docs/come-iniziare/strumenti-di-compilazione/

# Identifying a task

We have many components still missing, and several pending issues.
You can find a list of all features where you can contribute [on the relevant issues page](https://github.com/italia/bootstrap-italia/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22). You can take on any task with the `help wanted` label.

Once you found a task you want to tackle, you can start to work on it.

# Hacking

You will perform most of the work on the components. To hack on them you will need to edit the files found in `src/scss` and `src/js`, and test your result by looking at the relevant page in the documentation.

# Submitting your work

We'd love to integrate your work in our repositories!

```.bash
git config --global user.name "Your Name"
git config --global user.email your.email@address.org
```
