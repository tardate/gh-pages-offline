# gh-pages-offline

This is a test of the simplified publishing features announced on the GitHub blog:
[Publishing with GitHub Pages, now as easy as 1, 2, 3](https://github.com/blog/2289-publishing-with-github-pages-now-as-easy-as-1-2-3)

This site is generated offline with jekyll.

```
bundle exec jekyll build
```

It builds to the `docs` folder. GitHub Pages is configured to serve from this folder in the repo settings.

## Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>