# hugo-build

Docker image for building a site with hugo

# This file is a template, and might need editing before it works on your project.
# Full project: https://gitlab.com/pages/hugo
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
