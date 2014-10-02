This repository contains source files for the [Zanata home page] (http://zanata.org/).

Run locally: jekyll serve --watch (http://localhost:4000)

For more information , see https://help.github.com/articles/using-jekyll-with-pages


### For Fedora Users

These commands should get jekyll installed:

```bash
$ yum install ruby ruby-devel gcc
$ gem install jekyll
```

### Install jekyll on RHEL6
- [install rvm](http://tecadmin.net/install-ruby-2-1-on-centos-rhel/) so that you can have a newer version of ruby running
- add yourself to rvm group `sudo usermod -a -G rvm yourusername`
- [install jekyll](https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll)
- optional: if you get an error saying you are missing a javascript runtime, just install one. i.e. `gem install execjs` and then `gem install therubyracer`
