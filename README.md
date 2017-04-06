# TravisCI-TechTalk


**TEAM NAME:**  Azra

### Team members


1. Ajay Chandra Pendyala; apendya@ncsu.edu
2. Sunil Narasimhamurthy; snarasi5@ncsu.edu
3. Sohan Kunkerkar; sakunker@ncsu.edu
4. Pranav Firake; ppfirake@ncsu.edu


### Screencast [link](https://www.youtube.com/watch?v=zQOS7_oK0xU)

This Tech Talk uses this [Node js project](https://github.com/heroku/node-js-getting-started) for demonstrating the working of Travis CI.

## Introduction

### What is CI 

Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible.



### What is Travis CI

![Tools for CI](https://github.com/suniltheta/TravisCI-TechTalk/blob/master/img/Travis.png)

In simple words, Travis CI is a hosted, distributed continuous integration service used to build and test software projects hosted at GitHub. With just a file called .travis.yml containing some information about our project, we can trigger automated builds with every change to our code base in the master branch, other branches or even a pull request.


### Travis CI functionalities (Main purpose of the tool)

- Monitor  GitHub projects
- Run Tests
- Provide feedback
- Build artefacts
- Check code quality
- Deploy to cloud services
- Whatever you can make it do


### How does Travis CI work (Tool in a clear, logical manner)


1. Sign in to Travis CI with your GitHub account, accepting the GitHub access permissions confirmation
2. Once you’re signed in, and Travis CI synchronized your repositories from GitHub, go to your profile page and enable Travis CI for the repository you want to build.
3. Add a .travis.yml file to your repository to tell Travis CI what    to build:
4. Travis CI tests this project against three versions of Ruby and the latest version of Rubinius.
5. Add the .travis.yml file to git, commit and push, to trigger a Travis CI build:
6. Check the build status page to see if your build passes or fails.


For example the archicture for Travis CI can be given as 
![Travis CI Architecture](https://github.com/suniltheta/TravisCI-TechTalk/blob/master/img/TravisArch.jpg)


## Advantages and Features of Travis CI

- Open Source
- Fully hosted 
- Distributed
- Incredibly easy
- No worries about back end
- Save git repo maintainer's time
- Easy to configure & use
- High speed
- Great integration with GitHub & cloud services

## Platform support

Travis CI  supports large number of tools/ languages which includes almost all popular tools.

e.g.


| ANDROID | F#                        | RUST         |
|---------|---------------------------|--------------|
| C       | GO                        | SCALA        |
| C#      | GROOVY                    | SMALLTALK    |
| C++     | HASKELL                   | VISUAL BASIC |
| CLOJURE | HAXE                      | R            |
| CRYSTAL | JAVA                      | Ruby         |
| D       | JAVASCRIPT (WITH NODE.JS) |              |
| DART    | JULIA                     |              |
| ERLANG  | OBJECTIVE-C               |              |
| ELIXIR  | PERL                      |              |
| F#      | PERL6                     |              |
| GO      | PHP                       |              |
| GROOVY  | PYTHON                    |              |


## Limitations/ Disadvantages of Travis CI

- No manual builds
- No build pipelines
- Not suitable for high security projects
- Less extensible than JenKins

## Other CI tools :

Tools for CI are

![Tools for CI](https://github.com/suniltheta/TravisCI-TechTalk/blob/master/img/CITools.png)

Jenkins is one of the popular CI tool available.

 Comparison 
 
 | *Travis CI* | *jenkins*     |
|-------------|---------------|
| fully Hosted with github integration  | Hosted internally   |
| Commercial  | Open-Source   |
| Service     | Application   |
| Convention  | Configuration |
| Easy to use | Flexible      |


## Our Views

If we are coding an open source project on github and want easy to configure CI tool go for Travis CI. The another cool thing is badge we can put on a website or in our readme of github to show whether the build is passing or not. 
Travis CI for non-open source projects is very expensive  starts at $129 per month
Jenkins would be better option if you are already familiar with it. 

Also, as we worked on the demo for this Tech Talk, we felt that integrating Travis CI as Continuous Integration into our project was much more seamless compared to our prior experiences with one other CI tool Jenkins CI, which was more complex in its functioning and setup. Also, the fact that Travis CI is cloud based increases its accessibility.

Preference for projects :
		
		in-house → Jenkins
		
		Open source and Github.com → Travis-CI

### Setup instructions for the Demo
 
These steps were followed in setting up the demo:

1. `git clone https://github.com/heroku/node-js-getting-started`

2. `cd node-js-getting-started`

3. `vi .travis.yml`

4. Add this content there
```
language: node_js
sudo: false
node_js:
 - "stable"
install:
 - npm install

deploy:
 provider: heroku
 api_key: "HEROKU KEY"
 app: app-travis
```
5. Add this to the github project's Readme 
` [![Build Status](https://travis-ci.org/suniltheta/node-js-getting-started.svg?branch=master)](https://travis-ci.org/suniltheta/node-js-getting-started)
`
6. Sign into your Travis CI account and sync your repos.

7. Enable Travis CI integration for this project.

8. `git add .`

9. `git commit -m "Commit Message"`

10. `git push origin master`

11. Go to the github repo url and click on the badge that we added for the Travis CI build to see the build results.

12. You can also customize the build like Build branch updates, Limit concurrent jobs, Build pull request updates, Schedule CRON jobs, auto cancelling the jobs, set ENV variables for the jobs etc.
		
		
## References

- http://www.uqasar.eu/review-saas-continuous-integration-tools-series/
- Continuous Integration (Jenkins/Hudson) - SlideShare
- http://www.slideshare.net/bsiggelkow/travis-ci
- http://www.slideshare.net/gabevanslv/travis-ci-23997525?related=1
- https://docs.travis-ci.com/user/getting-started/







