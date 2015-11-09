## Contributing

See a typo, content you would like changed, or wish to generate content that is missing?

The following path is the general [GitHub Flow](https://guides.github.com/introduction/flow/).

1. Make a fork of this repository.
2. Create a topic branch
3. Edit content saving to the branch
4. Make a Pull Request (PR)

## Jekyll

We use [jekyll](https://github.com/jekyll/jekyll) to generate and [GitHub pages](https://pages.github.com) to maintain the instance in the cloud.

### Jekyll documentation

[Jekyll](http://jekyllrb.com/) documentation will provide the basics of how the site functions.

#### posts

Front matter is required and this is a basic template

```yaml
---
layout: base_post
title: short page title
date: 2015-12-01
author: Your Name
---
```

#### profiles

Front matter is in the following format

```yaml
---
layout: profile
profile:
  firstname: Name
  lastname: Name
  avatar: https://avatars.com/your-avatar
  affiliations: ['list of', 'affiliations']
  github:
    username: username
  url: http://domain.com
---
```

## Automated testing

We use [travis-ci](https://travis-ci.org/MapNetNZ/mapnetnz.github.io) to automatically build and check pull requests. A green tick will appear for successfully tested changes, while a red cross shows when tests have not passed.

## Merging

A pull request will generate an email for the maintainers, who will merge or help merge the content as soon as possible.

## Local installation

After forking and cloning, setting up the environment requires.

```bash
## install bundler to make dependency installation trivial
gem install bundle

## bundler will install all dependencies into vendor/bundle
bundle install
```

Once the environment is configured, jekyll building and html-proofer testing can be achieved thus:

```bash
## the generate target builds the site
bundle exec rake generate

## the travis target uses html-proofer to check for errors
bundle exec rake travis
```

Visual checking of the site can be done using:

```bash
bundle exec jekyll serve -w -P 9090
## on OS X this will open web browser to the site
open http://localhost:9090
```
Alternatively, manually point your web browser at the [local instance](http://localhost:9090)
