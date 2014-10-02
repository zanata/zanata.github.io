This repository contains source files for the [Zanata home page] (http://zanata.org/).

Run locally:
```bash
$ jekyll serve --watch --config _dev_config.yml (http://localhost:4000)
```

For more information , see https://help.github.com/articles/using-jekyll-with-pages


### Install jekyll on Fedora

These commands should get jekyll and all its dependencies installed (using nodejs as the javascript runtime):

```bash
$ yum install ruby ruby-devel gcc nodejs
$ gem install jekyll execjs
```

### Install jekyll on RHEL6
- [install rvm](http://tecadmin.net/install-ruby-2-1-on-centos-rhel/) so that you can have a newer version of ruby running
- add yourself to rvm group `sudo usermod -a -G rvm yourusername`
- [install jekyll](https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll)
- optional: if you get an error saying you are missing a javascript runtime, just install one. i.e. `gem install execjs` and then `gem install therubyracer`

