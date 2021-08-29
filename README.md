# Planman API documentation

## Setup
1. Clone this repository
3. Add your site and author details in `_config.yml`.

## Develop
1. Install Jekyll and its dependencies by following these steps: https://jekyllrb.com/docs/installation/ubuntu/
2. Go to the directory /planman-integration-docs.github.io
3. Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

4. Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

Aviator is already optimised for adding, updating and removing documentation pages in CloudCannon.

### Usage

* Each section is a different collection, this helps organise your content.
* Set the order of the collections with the position_number field in collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position_number in front matter.

### Search

* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.
