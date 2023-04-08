# blog.template
Template for hungovercoders to create blog

See the official docs [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll).

## Pre-Requisites

* [Install Ruby](https://rubyinstaller.org/downloads/)

```bash
ruby -v
```

* [Bundler](https://bundler.io/) - didn't do anything other than use this in commands following, this is just the tool referenced.

* [Install Jekyll](https://jekyllrb.com/docs/installation/windows/)

```bash
gem install jekyll bundler
jekyll -v
mkdir src
cd src
jekyll new --skip-bundle .
```

## Jekyll Amendments

Update Gemfile yaml, see dependency versions [here](https://pages.github.com/versions/).

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

## Update Gems

```bash
bundle update github-pages
```

## Change Default Theme (minima)

The theme currently being used in this template is "minima" and can be seen in the gemfile e.g.

```yaml
# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", "~> 2.5"
```

You can update this and try other themes if you wish. A collection of free themes can be found [here](https://jekyllthemes.io/free).

## Override Theme

First see where the files are held for the theme you are using

```bash
bundle info --path minima
```

Once you have the file path, look at the directory structure e.g.

```
dir "C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/minima-2.5.1"
```

then look at the main directories

```
dir "C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/minima-2.5.1/assets
dir "C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/minima-2.5.1/_includes
dir "C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/minima-2.5.1/_layouts
dir "C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/minima-2.5.1/_sass
```

You can take a copy and override them all, the easiest way to do this is just remove from gitignore, but you would not get automatic theme updates then.





