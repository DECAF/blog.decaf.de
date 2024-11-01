# Setup

To set up the website on your local machine, the following steps are required:

1. Install __Ruby 3.x__ if not yet available

    How to check which Ruby version is currently installed:

        $ ruby --version

    Install Ruby 3.x according to the Jekyll website at https://jekyllrb.com/docs/installation/.
    ⚠️ For Mac, better not use [rvm](https://rvm.io/), but go fo [chruby](https://github.com/postmodern/chruby)! This is also what Jekyll recommends at https://jekyllrb.com/docs/installation/macos/.

2. Install __Bundler__ if not yet available

        $ gem install bundler

3. Install __Bundles__ if not yet available

        $ bundle install

4. __Start Jekyll__

        $ bundle exec jekyll serve

    Now the website can be accessed at `http://localhost:4000`.

Here you can find a documentation at GitHub about how to use Jekyll locally: https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/
