# Website for ungoogled-chromium

This is a basic website for ungoogled-chromium, based upon [Hydra by CloudCannon](https://github.com/CloudCannon/hydra-jekyll-template).

## Develop

This website was built with [Jekyll](https://jekyllrb.com/) version 3. but should support newer versions as well.

Install the dependencies with [Bundler](https://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

Changes made while `jekyll serve` runs will cause Jekyll to regenerate the site automatically (while auto-regeneration is enabled, which is the default)

### Posts

* Add, update or remove a post in the *Posts* collection.
* The **Staff Author** field links to members in the **Staff** collection.
* Documentation pages are organised in the navigation by category, with URLs based on the path inside the `_docs` folder.
* Change the defaults when new posts are created in `_posts/_defaults.md`.

### Staff

* Reused around the site to save multiple editing locations.
* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.

### Navigation

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Navigation* section.

### Footer

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Footer* section.
