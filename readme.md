> :smiley: Timegrid Development is back!

<a href="#">
    <img src="http://i.imgur.com/pUUoU6H.png" alt="timegrid.io" title="timegrid.io" align="right" />
</a>

timegrid
============

[![Build Status](https://travis-ci.org/timegridio/timegrid.svg?branch=master)](https://travis-ci.org/timegridio/timegrid)
[![Code Climate](https://codeclimate.com/github/timegridio/timegrid/badges/gpa.svg)](https://codeclimate.com/github/timegridio/timegrid)
[![Test Coverage](https://codeclimate.com/github/timegridio/timegrid/badges/coverage.svg)](https://codeclimate.com/github/timegridio/timegrid/coverage)
[![Gitter](https://badges.gitter.im/timegrid-development/community.svg)](https://gitter.im/timegrid-development/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![License](https://img.shields.io/:license-AGPL--3.0-blue.svg?style=flat-square)](http://www.gnu.org/licenses/agpl-3.0.txt)
[![Open Source Helpers](https://www.codetriage.com/timegridio/timegrid/badges/users.svg)](https://www.codetriage.com/timegridio/timegrid)

> **Timegrid** helps contractors and customers to find the perfect meeting time through *online appointments*.

<div style="text-align:center">
  <img src="http://i.imgur.com/YOQBoVx.png" alt="Timegrid Backoffice Dashboard Screenshot">
</div>

## Features

  * Built with [**Laravel 5.3**](http://laravel.com/docs/5.3) framework for [**PHP**](http://php.net/)
  * Classic and oAuth2 Sign-in/Sign-up with [Socialite](https://github.com/laravel/socialite)
  * Business management
    * Clients Addressbook
    * Services
    * Staff
    * Availability
    * Appointments
  * Calendar sharing through [iCalendar link](https://en.wikipedia.org/wiki/ICalendar)
  * Scheduling view with [fullcalendar](https://github.com/fullcalendar)
  * Self-service reservation with datepicker
  * Basic email notifications
  * i18n Support
  * Multiple Timezones Support
  * Live chat with [TidioChat](https://www.tidiochat.com/)
  * Admin GUI with [AdminLTE](https://github.com/almasaeed2010/AdminLTE) [Twitter Bootstrap 3](https://github.com/twbs/bootstrap) based theme.

[Future features here](https://github.com/timegridio/timegrid/issues?q=is%3Aissue+is%3Aopen+label%3Afeature-request)

## Documentation

Read [the wiki](https://github.com/timegridio/timegrid/wiki)

## Requirements

timegrid has some server requirements for web hosting:

  * PHP ~7.4
  * OpenSSL PHP Extension
  * PDO PHP Extension
  * Mbstring PHP Extension
  * Tokenizer PHP Extension
  * MySQL server
  * [PHP Intl](http://php.net/manual/en/intl.setup.php)

## Installation

> **Advice:** PHP 7 is recently supported and not yet fully tested.

<a name="step1"></a>
## Step 1: Get the code

    git clone https://github.com/timegridio/timegrid.git

    cd timegrid

-----
<a name="step2"></a>
## Step 2: Install dependencies with Composer

    composer install

-----
<a name="step3"></a>
## Step 3: Create the Database

Once you finished the first two steps, you can create the *MySQL* database server. You must create the database with `utf-8` collation (`utf8_general_ci`), for the application to work.

-----
<a name="step4"></a>
## Step 4: Configure the Environment

**Copy** the **.env.example** file to **.env**

    cp .env.example .env

**Edit** the `.env` file and set the database configuration among the other settings.

Set the application key

    php artisan key:generate

**Edit** all the Primary section parameters (for *local/test/development environment*)

**Change** the storage path in **.env** file to a writeable location

    STORAGE_PATH=/home/username/timegrid/storage

For **local** environment you will need to **comment out** APP_DOMAIN, to keep it *null*

    #APP_DOMAIN=

Back to your console, **migrate** database schema

    php artisan migrate

**Populate** the database:

    php artisan db:seed

And we are ready to go. **Run** the server:

    php artisan serve

**Type** on web browser:

    http://localhost:8000/

## Demo Sandbox Fixture (Procedimiento para Usuarios Demo)

If you want to try the application with a *Lorem Ipsum* database fixture.

    php artisan db:seed --class=TestingDatabaseSeeder

Now you have two demo credentials to log in and play around.

    USER: demo@timegrid.io
    PASS: demomanager

    USER: guest@example.org
    PASS: demoguest


## Installing for Docker

Get started in 10 min with a [Docker image](https://github.com/timegridio/dockerfiles) for development environment.

## Localization

Current supported user interface languages are:

  * American English (`en_US`)
  * Spanish (`es_ES` and `es_AR`)
  * Italian (`it_IT`)
  * French (`fr_FR`)
  * Russian (`ru_RU`)
  * Armenian (`am_HY`)

Feel free to contribute with your preferred translation!

## Appointment Library

Timegrid uses [Concierge package](https://github.com/timegridio/concierge) for dealing with appointments.

![Timegrid Mindmap](http://i.imgur.com/gXBFMor.png)

## Author

Timegrid is developed and maintained by [Ariel Vallese](http://alariva.com).

## Contributing

Contributions are welcome. **Please read the following notes.**

## Special Thanks & Credits

  * [PeGa!](https://www.linkedin.com/in/pega041) for infra support
  * [Mohamed G.Hafez](https://github.com/mg-freelancer) for contributions
  * [John Ezekiel](https://github.com/zeke8402) for friendly hints and creating a really nice 
  * [booking-app](https://github.com/zeke8402/booking-app)
  * [Victor](https://github.com/pappavic) for testing and documentation contributions
  * [Mohammad Hossein Mojtahedi](https://github.com/MHM5000) for doc review
  * [Jose V Herrera](https://github.com/josevh) for contributions
  * [Bruno Gangemi](https://github.com/brugasoft) for useful feedback
  * [Calvin Roger S. Canas](https://github.com/calvincanas) for contributions
  * [Khouadja Achraf](https://github.com/achrafkh) for contributions
  * [Nick N. Huynh](https://github.com/finalblast) for contributions
  * [Kashyap Sharma](https://github.com/Kashyap12) for contributions
  * [Niharika Khanna](https://github.com/niharikak101) for contributions
  * [Webearit.com](https://www.webearit.com/) for contribution on Italian translation
  * [Draganrakovic](https://github.com/draganrakovic) for contributions
  * [Nerxo](https://github.com/Nerxo) for contributions
  * [Sahil Sharma](https://github.com/sahilsharma011) for contributions and smart suggestions
  * [Mohammed Hicham](https://github.com/himan72) for contribution on French translation
  * Ani Shahbazyan for contribution on Russian and Armenian translations
  * Using modified icon originally made by [SimpleIcon](http://www.flaticon.com/authors/simpleicon) from www.flaticon.com

## License

Timegrid is open-sourced software licensed under the [AGPL](http://www.gnu.org/licenses/agpl-3.0-standalone.html)

May all beings be happy.
