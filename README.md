This site is built using Jekyll and hosted on GitHub Pages.

To install:
```
gem install bundler jekyll
```

To run it locally:
```
bundle install
bundle exec jekyll serve --safe
```

### Documentation

The URLs will map the folder tree (they are not configured with a `.yml` file).

### Translations

Install [Translate Toolkit](http://docs.translatehouse.org/projects/translate-toolkit/en/latest/installation.html)

Extract translations from HTML files.

```
html2po --duplicates=merge _site/en/ _translations/en/
```

Create English message catalog (also see [msgen](https://linux.die.net/man/1/msgen)).

```
podebug --rewrite=en _translations/en/ _translations/en/
```
