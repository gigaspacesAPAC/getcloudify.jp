# Cloudify Documentation
[![Circle CI](https://circleci.com/gh/gigaspacesAPAC/getcloudify.jp.svg?style=svg)](https://circleci.com/gh/gigaspacesAPAC/getcloudify.jp)

This repository contains the markup files, html templates and javascript sources for the new [Cloudify documentation portal](http://getcloudify.org/).
It's based on [Jekyll](http://jekyllrb.com/), a Ruby-based static site generator, and uses [Markdown](http://whatismarkdown.com/) as a markup language for the most part. It also uses a number of custom Jekyll plugins for formatting and styling. Please refer to the [cheatsheet](http://getcloudify.org/guide/3.0/cheatsheet.html) for details about these plugins and how to use them. 

## Help Us Improve! 

It's important for us to encourage your feedback and contribution. Contributing to this website is straightforward. Simply fork this repository, make your changes, test them with your local Jekyll installation, and submit a pull request. We promise to review and comment on every pull request, and merge it if it makes sense.

## Installing, Editing and Testing Locally

To run and test the website locally, you should perform the following steps:

* Install [Ruby](https://www.ruby-lang.org/en/downloads/).

* Install [RubyGems](https://rubygems.org/pages/download).

* Install [Bundler](http://bundler.io/).

        sudo gem install bundler
        
* Install [python](https://www.python.org/), if not already installed. You will need python2, not python 3. (Both python 2.6 and 2.7 will work)

* Create a fork of this repo and clone it to your machine.

        git clone https://github.com/your-github-username/getcloudify.org.git

* Go to the repository directory: 

        cd getcloudify.org

* Invoke Bundler to install all required Ruby gems.

        bundle install 

- If you're using Windows, run `setup-win.bat` with administrative permissions (requires Windows Vista or later).
This script is a workaround for a known issue in git which ignores symbolic links on Windows. 

* Make the required changes to the docs (if you need to).

* Run Jekyll in server mode, and wait for the site generation to complete: 

        jekyll serve --watch --limit_posts 1
        
        
You should see the following output if everything was ok:
 
        .....
        Generating... 
                    done.
        Configuration file: ..../getcloudify.org/_config.yml
        Server address: http://0.0.0.0:4000/


* Point your browser to [http://localhost:4000](http://localhost:4000). You should see the documentation portal home page, and verify that you're ok with your changes. 

* If you've forked the repository and updated documentation pages, you can submit a pull request. We will review, comment and merge the pull request after approving it. 

## Continuous Deployment 

This website is hosted on AWS S3. Every push to this repository triggers a build process (currently we use the excellent [Circle CI](http://circleci.com) continuous integration service), at the end which the generated website is pushed to S3 using the [s3_website](https://github.com/laurilehmijoki/s3_website) library. The Circle CI configuration is located in the file [`circle.yml`](circle.yml). 

## Authoring Guidelines

You can find these guidelines [here](http://getcloudify.org/guide/3.0/cheatsheet.html)

## Adding CSS

This project uses sass. All css rules go into partials ( _file.scss ) which can be found under _sass folder.












