## Intro
Today I will be demonstrating how to set up a basic cucumber scenario in Ruby. I will be demonstrating this using a plain text editor and a cmd prompt or terminal. Modern IDEs will can autocomplete many of these steps, however knowing how to construct this code from scratch will provide valuable insight into what your are making when testing and solutioning test strategies in the real world.

The prerequisites for this demonstration are an open cmd prompt or terminal, Ruby installed (check using ruby -v), and bundler installed. Bundler is a package manager for Ruby that downloads and helps resolves dependencies.

**All of the cmd prompt commands must be executed from the root of our demo project.**
### Demo Description
- First we put this line into our gem file `gem cucumber` and then run `bundle install` in our cmd prompt. Bundler will download and install the dependencies for the cucumber gem as well as create the `Gemfile.lock` file lists the individual dependencies.

- Our next step is to create the feature file that will have our BDD gherkin code.

- The required key words in the file are the `Feature` and `Scenario` key words. For now we will have a simple description of our demo listed as the `Feature` and we will describe our literal demonstration scenario as the `Scenario`.

- Next we will create a step file that will hold the Ruby code which will be driving our demo test

- In the step file cucumber will look for the matching gherkin text using regular expressions. The key words such as `Given`, `When`, `Then` do not need to match in the step file.

- Once we have an empty step code block we will put some Ruby code that will return a message verifying that our cucumber test is running correctly.

- Congrats! Cukes are running wild!

#### Prerequisites
  - An open command prompt(for windows) or terminal(mac)
  - ruby installed
  - bundler installed using command `gem install bundler`

#### Steps
- Put cucumber gem in gem file and run bundle install to install required libs and packages
- Create feature file with simple gherkin
- Create step file with step code to run test
