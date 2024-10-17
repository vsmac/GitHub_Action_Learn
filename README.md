# what is github action
GitHub Actions is a feature of GitHub that allows you to automate, customize, and execute software development workflows directly from your GitHub repositories. With GitHub Actions, you can define workflows to build, test, and deploy your code whenever a specific event (like a commit, pull request, or issue) occurs. It enables continuous integration (CI) and continuous deployment (CD), allowing developers to automate tasks like testing, building, and deploying their applications
# in short definition
GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline

#  Key Features of GitHub Actions
1, Automation of Workflows    #   Automate tasks such as running tests, building applications, or deploying code when events occur in your repository (e.g., pushing code, opening pull requests) 

2, Continuous Integration/Continuous Deployment (CI/CD)   #   Automatically test and deploy your code after each push or pull request

3, Event-driven Workflows   #    Trigger workflows based on events like push, pull_request, issue, or scheduled intervals
4, Customizable    #    You can define your custom workflows using YAML files and run multiple jobs  in sequence

5,Cross-platform Support    #   Supports multiple operating systems like Linux, macOS, and Windows

#  Benefits of GitHub Actions
Easy CI/CD Integration  #   Integrate and automate the CI/CD pipeline directly within your GitHub repository

Custom Automation     #    Customize workflows to automate tasks like code testing, linting, and deployment

Wide Integration     #      Easily integrate with cloud providers, testing tools, and deployment platforms

Parallel Execution    #   Run jobs in parallel to speed up the development process

Predefined Actions    #    Utilize a marketplace of predefined actions to speed up development and avoid reinventing the wheel

#  steps
step -1   #  sign up or login to github.com

step -2   #  create a new repository you can name it anything (github-action)

step -3   #  in the folder create a folder .github/workflows (this folder fixed)

step -4   #  in the folder create a YAML file with extension .yml

step -5   #  add the workflows content in the file

step -6   #  add,commit and push the changes 

step -7   #  go to main of repository and go to "Action"

step -8   #  select the workflows from left side and check the logs and result

#  simple workflows in github action
name: CI Workflow  # Name of your workflow

on:
  push:            # Trigger the workflow when code is pushed
    branches:
      - main       # Specify which branch should trigger the workflow

jobs:
  build:           # Name of the job
    runs-on: ubuntu-latest  # Specify the virtual environment to use

    steps:

    - name: Install nginx
      run: sudo apt install nginx -y   # Example command to install nginx

    - name: Run tests
      run: npm test  # Example command to run your test suite

Name:   #    This is the name of your workflow (CI Workflow in this case)

On:     #    This defines when the workflow should be triggered. The example above triggers the workflow on any push to the main branch

push:   #    Trigger the workflow when code is pushed

-main   #    Specify which branch should trigger the workflow

jobs:   #    Each workflow can consist of multiple jobs. Jobs are executed on virtual machines provided by GitHub

build:  #    name of the job

runs-on: ubuntu-latest:    #   Specifies the environment in which the job will run. The example uses ubuntu-latest, but you can also choose from environments like windows-latest or macos-latest

 steps:    #     Jobs are broken down into steps. Each step defines an action or a command that runs during the job


