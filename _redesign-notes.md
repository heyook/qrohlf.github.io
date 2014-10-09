# Redesign Notes

## Inspirations:

- Original design inspiration: http://warpspire.com
- Test framework: https://github.com/Haacked/haacked.com
- Nice header http://www.paperplanes.de
- Lovely typography: http://zachholman.com
- Not a blog design, but http://speaking.io
- Background color: https://jlord.github.io
- Google http://www.google.com/design/
- Nicely minimal: http://connorsears.com

## Tools

Since this site is 100% frontend code, it might make sense to use something like http://www.metalsmith.io that's going to behave nicely with bower, npm, gulp, etc. Though it uses Sprockets and a Gemfile for resource gems, so that's a bit awkward...

Looks like you might be writing an asset pipeline? https://github.com/ck86/main-bower-files


## Goals?

Front page should accomplish... what?
Introduce me.
Link to writing.
Link to projects.

## Snippets

Old post index code:


```

<section class="post-index">
    <h1 id="writing">Writing</h1>
{% for post in site.posts %}
    <article>
        <h2><a href="{{post.url}}">{{ post.title }}</a></h2>
        <p>{{ post.summary }}</p>
        <footer class="post-meta">
          <p>{{ post.date | date: "%d %h %Y" }}</p>
        </footer>
    </article>
{% endfor %}
</section>
```