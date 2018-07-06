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

#### Sidebar generation & files attributes

We use files attributes to generate the sidebar on the left. It seems hackish, but we need to because the restriction GitHub has on Jekyll plugins.

Each file have the following attributes :
 - `lang`: the lang the file is written in
 - `role`: the role the file aimed for
 - `title`: title of the file, will be used to set content in the sidebar
 - `nav: true`: indicates the file is zero-level deep in the sidebar
 - `subnav: true`: indicates the file is one-level deep in the sidebar
 - `nav_order`: if set, gives the order of the file on the sidebar

The `index.md` files are used to indicate a folder and should have no content (they won't be clickable from the sidebar).
