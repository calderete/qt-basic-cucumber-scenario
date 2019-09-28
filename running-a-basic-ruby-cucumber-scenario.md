## Intro
Today I will be demonstrating how to set up a basic cucumber scenario in Ruby. I will be demonstrating this using a plain text editor and a cmd prompt, there is no difference when using the terminal. Modern IDEs such as jetbrains RubyMine can autocomplete many of these steps, however knowing how to construct this code from scratch will provide valuable insight into what your are making when testing and solutioning test strategies in the real world. I would also like to note that this is not a comprehensive tutorial on the features of cucumber.

The 3 prerequisites for this demonstration are an open cmd prompt or terminal, Ruby installed (check using ruby -v), and the Ruby package manager bundler installed.

**All of the cmd prompt commands must be executed from the root of our demo project.**
### Demo Description
- To start with I have an empty project where I will put the necessary files to run a cucumber scenario.

- First we create the Gemfile and put this line into it file `gem cucumber` and then run `bundle install` in our cmd prompt. Bundler will download and install the dependencies for the cucumber gem as well as create the `Gemfile.lock` file lists the individual dependencies.

- Next we create the feature file that will have our BDD in it. In it we will have a single scenario with two steps.

- We must be sure to include the `Feature` key word in our feature file or cucumber will error when it is run.

- Next we will create a step file that will hold the Ruby code which will be driving our demo test. Where this step file is does not matter. When cucumber is run it flattens the project under the `features` folder and searches all ruby files for the matching step code. For now we will place our step code next to the feature file.

- In the step file cucumber will look for the matching gherkin text using regular expressions. The key words such as `Given`, `When`, `Then` do not need to match in the step file.

- Once we have an empty step code block we will put some Ruby code that will return a message verifying that our cucumber test is running correctly.

- To run the test use the cucumber command from the prompt.

- Congrats! Cukes are running wild!

### Helpful links
**Installing Ruby**<br>
_https://www.ruby-lang.org/en/documentation/installation/_

**Using Windows Command Prompt**<br>
_https://www.bleepingcomputer.com/tutorials/windows-command-prompt-introduction/_

**Using Mac Terminal**<br>
_https://macpaw.com/how-to/use-terminal-on-mac_

**Cucumber github**<br>
_https://github.com/cucumber/cucumber-ruby_

#### Prerequisites
  - An open command prompt(for windows) or terminal(mac)
  - ruby installed
  - bundler installed using command `gem install bundler`

#### Steps
- Put cucumber gem in gem file and run bundle install to install required libs and packages
- Create feature file with simple gherkin
- Create step file with step code to run test
