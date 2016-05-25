# Middleman with Markdown Submodule Example

This is an example project using [Middleman](https://middlemanapp.com) and pulling in our [Style Guide](https://github.com/mailchimp/content-style-guide) as a submodule.

## Installation
Requires Ruby 2.2.5 and Bundler

Clone the repo:
``` bash
git clone git@github.com:mailchimp/middleman-with-md-submodule-example.git
cd middleman-with-md-submodule-example
```

Install dependencies:
``` bash
bundle install
```

Initialize the submodule:
``` bash
git submodule init
```

Update the submodule:
``` bash
git submodule update
```

Run it:
``` bash
bundle exec middleman server
```

View it at `http://localhost:4567/`

## Add Your Own Style Guide

Fork your own version of our [Style Guide](https://github.com/mailchimp/content-style-guide). You'll need to change out the submodule with your forked version.

First, remove the old Style Guide:

``` bash
git submodule deinit content-style-guide
git rm content-style-guide
```

Then go to your fork of the Style Guide on GitHub, click on the `Clone or download` button, copy the `Clone with SSH` url, and paste it in this line:

``` bash
git submodule add {paste your submodule GitHub repo url}
```

Then:
``` bash
git submodule init
```

As you make changes to your copy of the Style Guide submodule, you'll need to resync it with:

``` bash
git submodule update
```