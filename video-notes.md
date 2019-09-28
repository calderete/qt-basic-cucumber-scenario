Today we are going set up some basic cucumber scenarios in Ruby. The prerequisites for this demonstration are an open cmd prompt or terminal, Ruby installed (check using ruby -v), and bundler installed. Bundler is a package manager for Ruby that helps resolves dependencies. All of the cmd prompt commands must be executed from the root of our demo project.

- First we put this line into our gem file `gem cucumber` and then run `bundle install` in our cmd prompt. Bundler will download and install the dependencies for the cucumber gem as well as create the `Gemfile.lock` file lists the individual dependencies.

- Our next step is to create the feature file that will have our BDD gherkin code.

- Next we will create a step file that will hold the Ruby code which will be driving our demo test

- prerequisites
  - An open command prompt(for windows) or terminal(mac)
  - ruby installed
  - bundler installed using command `gem install bundler`


- Put cucumber gem in gem file and run bundle install to install required libs and packages
- Create feature file with simple gherkin
- Create step file with step code to run test
