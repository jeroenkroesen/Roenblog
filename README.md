# Personal blog repo

Content starts at [index.md](index.md). Site is at [https://jeroenkroesen.github.io/RoenBlog/](https://jeroenkroesen.github.io/Roenblog/)

For local development run the Github Pages Jekyll image in Podman:  
```sh
podman run --rm --volume "$(pwd):/srv/jekyll" -p 4000:4000 docker.io/jekyll/jekyll:pages sh -c "gem install webrick && jekyll serve --destination /tmp/_site"
```
