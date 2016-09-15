## Codeception Acceptance Testing on Travis-CI

[![Build Status](https://travis-ci.org/ankurk91/codeception-travis-ci-example.svg?branch=master)](https://travis-ci.org/ankurk91/codeception-travis-ci-example)


### Prerequisites
* Git client
* [Composer](https://getcomposer.org)
* [Java runtime](http://java.com/en/download/manual.jsp)
* Firefox
* [Selenium standalone server](http://www.seleniumhq.org/)
* php v5.6+ with CURL extension
* [Codeception](http://codeception.com/quickstart) (global install) 

### Run on localhost
* 1. Clone the repo
```
git clone https://github.com/ankurk91/codeception-travis-ci-example.git
cd codeception-travis-ci-example
```
* 2. Install dependencies
```
composer install
```
* 3. Run php inbuilt server, allow port 8000 in your firewall
```
php -S localhost:8000 -t app
```
* 4. In a new tab - Run selenium server (requires java JRE)
```
java -jar selenium-server-standalone.jar
```
* 5. In a new tab - Execute tests on Firefox (default)
```
codecept run
```

### Google Chrome
* Above commands assume that you have pre-installed *Firefox*
* But if you want to test it with *Google Chrome*, then follow next steps
* Download the latest ```chromedriver_*.zip``` for your platform from [here](http://chromedriver.storage.googleapis.com/index.html)
* Extract that zip to a folder and specify the path in next command
* 4. In a new tab - Run selenium server (requires java JRE)
```
 java -jar selenium-server-standalone.jar -Dwebdriver.chrome.driver=/full/path/to/chromedriver
```
* 5. In a new tab - Execute tests on chrome
```
codecept run --env chrome
```

### Quick Links
* [Codeception](http://codeception.com/docs/02-GettingStarted)
* [Selenium Standalone Server](http://www.seleniumhq.org/download/)
* [GUI and Headless Browser Testing on Travis CI](https://docs.travis-ci.com/user/gui-and-headless-browsers/)

### License
[MIT](LICENSE.txt)
