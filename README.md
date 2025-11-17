# Personal blog repo
  
My personal website runs on [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).  
  
Content starts at [docs/index.md](docs/index.md). Site is at [https://jeroenkroesen.github.io/RoenBlog/](https://jeroenkroesen.github.io/Roenblog/)  
  
For local development run Material for MkDocs in Podman.
```sh
podman run --rm -it -p 8000:8000 -v ${PWD}:/docs docker.io/squidfunk/mkdocs-material
```

Then visit [http://127.0.0.1:8000](http://127.0.0.1:8000) to preview the site locally. At the moment, hot reloading does not seem to work. So to view changes you will need to stop (`ctrl-c`) and restart the local dev server.  
  
If you want to start your own site in Material for MkDocs, bootstrap an empty site by running this command in an empty project directory or git repo:
```sh
podman run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material new .
```

Then checkout the [documentation](https://squidfunk.github.io/mkdocs-material/getting-started/).
