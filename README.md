# Quick Composer

Generates `composer.lock` using [travis-ci](https://travis-ci.org).


## Overview

Installing an application's PHP libraries with `composer install` is generally quite fast and painless.

However running `composer update` each time you need to add a new library can take a long time, and can fail for various reasons including network or sometimes just randomness.

Once the update has been run, composer generates a file named `composer.lock`.  If this file is present you can install by running `composer install`.

This repository leverages travis-ci to create a `composer.lock` using a remote machine on a stable network.  This file can then be copied locally to bypass local `composer update` issues.


## Setup

To add the repository to travis-ci see their [getting started guide](https://travis-ci.org/getting_started).


## Instructions

- Update [`composer.json`](https://github.com/cornernote/quick-composer/edit/master/composer.json).
- Visit [cornernote/quick-composer](https://travis-ci.org/cornernote/quick-composer).
- Search the raw log for `cat composer.lock`, copy the following content to your local `composer.lock`.
- Run `composer install` locally.
