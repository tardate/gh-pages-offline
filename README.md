# gh-pages-offline

This is a test of the simplified publishing features announced on the GitHub blog:
[Publishing with GitHub Pages, now as easy as 1, 2, 3](https://github.com/blog/2289-publishing-with-github-pages-now-as-easy-as-1-2-3)

This site is generated offline with jekyll.

```
bundle exec jekyll build
```

It builds to the `docs` folder.

GitHub Pages is setup to serve the site at [gh-pages-offline.tardate.com](http://gh-pages-offline.tardate.com/)
from the docs folder (configured in the repo settings).

A custom URL allows all internal links to be relative to the site root, so the site works fine when served on GitHub Pages
and also when served locally with

```
bundle exec jekyll build
```


## Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>