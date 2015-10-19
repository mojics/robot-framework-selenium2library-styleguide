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
3. [Installation](#3-installation)
4. [Core](#4-core)
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


## 3. Installation

#### Robot Framework:

> pip install robotframework

#### Selenium2Library:

> pip install --upgrade robotframework-seleniumlibrary

#### Jenkins:

> java -jar jenkins.war


After running the code above the Jenkins user interface is accessible via http://localhost:8080

Download Jenkins latest-stable file from [here](http://mirrors.jenkins-ci.org/war-stable/latest/jenkins.war).


#### Saucelabs:


Signup for a trial account [here](https://saucelabs.com).


[Back to top](#table-of-contents)

## 4. Core

[Back to top](#table-of-contents)


## 5. Components

[Back to top](#table-of-contents)


## 6. Overall

[Back to top](#table-of-contents)
