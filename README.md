# Hugo_docker_compose

I do not run hugo on my mac, I run it in Docker. So, in the [Quickstart](https://gohugo.io/getting-started/quick-start/) where it says run `hugo version` I run:
 
```sh
docker compose run server /bin/sh
```

and then the command from the Quickstart:

```sh
/src # hugo version
```

```
hugo v0.152.2+extended linux/arm64 BuildDate=2025-10-24T16:21:59Z VendorInfo=hugomods
/src #
```

```sh
# I changed the name of the site
hugo new site darvas
cd darvas
```

```sh
# skip the git init as this is already a GitHub project
# git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.toml
```

```sh
# add --bind 0.0.0.0 as this publishes the site on
# all interfaces, including the one visible from
# the host machine
hugo server --bind 0.0.0.0
```

At this point you can browse to [localhost:1313](http://localhost:1313)


