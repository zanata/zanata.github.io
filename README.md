This repository contains source files for the [Zanata home page] (http://zanata.org/).

Run locally (at [http://localhost:4000](http://localhost:4000)):
```bash
$ jekyll serve --watch --config _dev_config.yml
```

For more information, see https://help.github.com/articles/using-jekyll-with-pages


### Install Jekyll on Fedora

These commands install Jekyll and its dependencies with Node.js as the JavaScript runtime:

```bash
$ yum install ruby ruby-devel gcc nodejs
$ gem install jekyll execjs
```

There is also a [script to handle the setup process on Fedora](https://raw.githubusercontent.com/davidmason/fedora-setup-scripts/master/scripts/zanata/fedora-setup-zanata-website-prepare-jekyll), including increasing the watch file limit.

### Install Jekyll on RHEL6
- [Install rvm](http://tecadmin.net/install-ruby-2-1-on-centos-rhel/) to use the most recent version of Ruby
- Add yourself to rvm group `sudo usermod -a -G rvm yourusername`
- [Install Jekyll](https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll)
- Optional: If you do not have a JavaScript runtime specified, you may be prompted to install one. i.e. `gem install execjs` and then `gem install therubyracer`
