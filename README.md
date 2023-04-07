# blog.template
Template for hungovercoders to create blog

See the official docs [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll).

## Pre-Requisites

* [Install Ruby](https://rubyinstaller.org/downloads/)

```bash
ruby -vjekyll 
```

* [Bundler](https://bundler.io/) - didn't do anything other than use this in commands following, this is just the tool referenced.

* [Install Jekyll](https://jekyllrb.com/docs/installation/windows/)

```bash
gem install jekyll bundler
jekyll -v
mkdir template
cd template
jekyll new --skip-bundle .
```

## Jekyll Amendments

Update Gemfile, see dependency versions [here](https://pages.github.com/versions/).

```yaml
# gem "jekyll", "~> 4.3.2"
gem "github-pages", "~> {latest git hub pages number version}", group: :jekyll_plugins
```

Then run 

```bash
bundle install
```

and

```
bundle add webrick
```

## Run Locally

```bash
bundle exec jekyll serve
```





