This site is built using Jekyll and hosted on GitHub Pages.

To install:

```sh
gem install bundler jekyll
```

```sh
bundle install
```

To run it locally:

```sh
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

Use [msgcat](https://www.gnu.org/software/gettext/manual/html_node/msgcat-Invocation.html) to create one PO file.

```
msgcat _translations/en/*/*.po > _translations/en.po
```
