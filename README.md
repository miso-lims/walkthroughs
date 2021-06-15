# MISO OICR Documentation and workshop

Home of the training documents for the
[miso-lims](https://github.com/TGAC/miso-lims) laboratory information management
system for the [Ontario Institute for Cancer Research (OICR)](http://www.oicr.on.ca).

* [Training Workshop](http://oicr-gsi.github.io/miso-docs-oicr/)

This tutorial leads users through the steps required to enter data in MISO. Users may
complete all sections of the tutorial, or just the sections which apply to their
lab tasks.

## Fork

To configure this document for your own MISO training, first fork this repo.
You can rename it if you like.

Then, update the `_config.yml` file, replacing site-specific values.

Finally, deploy the tutorial to
[GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)
or elsewhere.

## Build

Requirements:

* Ruby 2.x
* Bundler
* Jekyll

Build:

```
bundle install
```

On MacOS, Bundler may fail to install libv8. To work around this, you can
install `v8-315` using Homebrew (or otherwise) and then install the dependencies
that use it using the following before trying `bundle install` again.

```
gem install libv8 -v '3.16.14.19' -- --with-system-v8
gem install therubyracer -v '0.12.3' -- --with-v8-dir=/usr/local/opt/v8@3.15
```

## Run

```
bundle exec jekyll serve
```
