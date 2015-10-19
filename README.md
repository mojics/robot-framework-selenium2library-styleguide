# Robot Framework / Selenium2Library Testing Environment Styleguide

This Robot Framework / Selenium2Library is based from couple of sources and tips from my colleagues. These guides can be outdated or not in your taste. You can drop a pull request so we can talk about it.

Note: This guide's format was also taken from my senchatouch2-styleguide

## Table of Contents

1. [Introduction](#1-context)
2. [Requirements](#2-requirements)
    1. [Robot Framework](#robot-framework)
    2. [Selenium2Library](#selenium2library)
    3. [Jenkins](#jenkins)
    4. [SauceLabs](#saucelabs)
    5. [Sublime Text Robot Framework Plugin](#sublime-text-robot-framework-plugin)
    6. [Bitbucket/Git](#bitbucket)
3. [Installation](#3-installation)
4. [The Test Project Setup](#4-test-project-setup)
5. [Components](#5-components)
6. [Overall](#6-overall)

## 1. Context

*Remember, test now or suffer later...*

After couple of Google searching and spending hours of watching Youtube videos regarding automation testing environment, I finally created this simple guide on how you can setup your own. This guide will tackle on how you can easily set it up for your QA team and even your Development team.

Once you finished this styleguide for Robot Framework and Selenium2Library, I'm sure you are now confident on making this kind of setup in any project you might get into. Lastly, do this on the early part of your development stage rather doing it later.



[Back to top](#table-of-contents)


## 2. Requirements

#### Robot Framework
Robot Framework offer a very descriptive documentation on how to use their testing framework but here we will create our own testing structure that can help you to build a scalable and maintainable testing environment. Why? So if there will be a newcomer on your project especially QA engineer, they can seamlessly adapt on your development team.

[Back to top](#table-of-contents)

#### Selenium2Library
In order to manipulate browser, we will be using Selenium2Library for Robot Framework. This external plugin offers various keywords such as "Open Browser" and this list of keywords is available from their website.

Since we are building a test framework for websites we will be using Selenium2L
ibrary.

[Back to top](#table-of-contents)

#### Jenkins

Jenkins is one of the leading continous integration server and it is open source! You can run your test without Jenkins but what if you want to setup a nightly build of your tests? Let's say your developers is working the whole day and you want to see if anything breaks after the day? Then we need Jenkins!


[Back to top](#table-of-contents)

#### Saucelabs

Saucelabs offers various services like different browsers and operating systems. Starting from mobile device to PC and Mac. We will be integrating Jenkins along with Saucelabs in order to use their browsers remotely.

An account from Saucelabs is required and they offer like 14 days of trial and they don't require credit card to sign up.

[Back to top](#table-of-contents)

#### Sublime Text Robot Framework Plugin

This plugin for Sublime Text 3 is optional but since I'm using Sublime Text on my development I will be including few details for this plugin.

[Back to top](#table-of-contents)


#### Bitbucket

We need to experience a bit of real world process, so we need to start  working with GIT and to do that is to have an account from Bitbucket. You can use other free GIT hosting but I prefer Bitbucket since Jenkins provide a plugin for integrating Bitbucket.

You can make your own account from [Bitbucket](https://bitbucket.org/account/signup/).

[Back to top](#table-of-contents)




## 3. Installation

On this part we will be working on making your first test environment. We need this following to continue the installation:

 - Python
 - Java
 - Virtual Machine (we will add support for Vagrant in the future)

Make sure you have the following in order to install the listed software below.

#### Robot Framework

> pip install robotframework



#### Selenium2Library

> pip install --upgrade robotframework-seleniumlibrary


#### Jenkins

> java -jar jenkins.war


After running the code above the Jenkins user interface is accessible via http://localhost:8080

Download Jenkins latest-stable file from [here](http://mirrors.jenkins-ci.org/war-stable/latest/jenkins.war).

#### Jenkins plugin for Robot Framework

After running Jenkins, you can visit  Manage Plugins page and install the following plugins:

 - Robot Framework
 - Bitbucket Plugin (we will be hosting our test project on Bitbucket)
 - Sauce OnDemand (optional)

After installation make sure to **restart** your Jenkins instance.

#### Saucelabs


Signup for a trial account [here](https://saucelabs.com/signup/trial).





[Back to top](#table-of-contents)

## 4. Test Project Setup
Before we create our very first test we need to setup first our **Test Project**.

#### Folder structure

 - Project root directory
     - resources/
         - main.resource.robot
         - login.resource.robot
         - ...
     - libs/
     - tests/
         - login/
             - test.robot
             - test2.robot
             - ...
         - register/
         - contact_us/
         - ...

#### Tests folder

On our project setup we will have 3 main folders: tests, resources and libs. On the folder **tests**, we will be putting all our test cases and notice the added folders inside of it. This is to organise each feature like login, register and contact us in one container.

Let's say you have additional feature you can just create a new folder and put all related test cases inside. This way, we will not convolute our test cases and mixed with our files.

#### Resources folder

Inside this **resources** folder, we will include all common keywords that we can use for our test cases. We can have a main common resource file or a certain resource for a certain feature for example login resource for login feature.

I prefer to have a granular resource file that we can use all over our test cases.


#### Libs folder

Since we are working on Python environment we will try creating our own plugin that will provide our own functionality. This custom plugin should be put inside this **libs** folder. This can be empty on the very early stage of your test project but this folder will be use in time.


[Back to top](#table-of-contents)

#### How about the generated reports ?

Those files will be auto generated when we run our tests files.  We will just leave it on the root folder since Jenkins will automatically fetch once the Jenkins job is done processing your test cases.

## 5. Components

[Back to top](#table-of-contents)


## 6. Overall

[Back to top](#table-of-contents)
