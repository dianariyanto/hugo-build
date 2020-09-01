# hugo-build

Docker image for building a site with hugo


.gitlab-ci.yml

```
image: dettmering/hugo-build

variables:
  GIT_SUBMODULE_STRATEGY: recursive

pages:
  script:
  - hugo --minify
  artifacts:
    paths:
    - public
  only:
  - master
```
