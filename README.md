This repository contains source files for the [Zanata home page] (http://zanata.org/).

Run locally (at [http://localhost:4000](http://localhost:4000)):

1. Install [ruby](https://www.ruby-lang.org/en/downloads/).
2. Install bundler: `gem install bundler`
3. Run bundler: `bundle install`
4. Start Jekyll: `bundle exec jekyll serve --watch --config _dev_config.yml`

For more information, see https://help.github.com/articles/using-jekyll-with-pages

### Install Jekyll on Fedora

```bash
$ yum install ruby ruby-devel gcc zlib-devel
$ gem install bundler execjs
$ bundle install
$ bundle exec jekyll serve --watch --config _dev_config.yml
```

There is also a [script to handle the setup process on Fedora](https://raw.githubusercontent.com/davidmason/fedora-setup-scripts/master/scripts/zanata/fedora-setup-zanata-website-prepare-jekyll), including increasing the watch file limit.

### Install Jekyll on RHEL6
- [Install rvm](http://tecadmin.net/install-ruby-2-1-on-centos-rhel/) to use the most recent version of Ruby
- Add yourself to rvm group `sudo usermod -a -G rvm yourusername`
- [Install Jekyll](https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll)
- Optional: If you do not have a JavaScript runtime specified, you may be prompted to install one. i.e. `gem install execjs` and then `gem install therubyracer`

See [these docs](http://jekyllrb.com/docs/troubleshooting/) for troubleshooting.
