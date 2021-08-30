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

### Usage

* Each section is a different collection.
* Set the order of the collections with the position_number field in the collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position_number field.
* For each document, type the main content of the section inside the content_markdown field.
* The left_code_blocks field contains the cURL request sample, while the right_code_blocks field contains the request body, response and error samples in JSON, which are rendered in the black section on the right of the page.
* For the code blocks, set the language field to have the syntax highlighted based on the language.
* The index.html is the main html file that is rendered. If you need to access any of the document's fields in index.html, for example the content_markdown field, type doc.content_markdown.

### Search

* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.
