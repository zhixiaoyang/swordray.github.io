---
layout: post
title: The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes - 最快速度 5 分钟内创建、安装、部署、上线 Rails 应用
---

# The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes


## Buy Mac


## Install

### Binaries

#### XCode

    open http://itunes.apple.com/us/app/xcode/id497799835?mt=12
    open https://developer.apple.com/downloads/

#### GCC

    open https://github.com/kennethreitz/osx-gcc-installer

#### MySQL

    open http://dev.mysql.com/downloads/mysql/5.1.html#downloads

#### MacPorts

    open http://www.macports.org/install.php
____
    sudo port selfupdate
    sudo port install memcached ImageMagick

### Ruby

    \curl -L https://get.rvm.io | bash -s head --ruby
    rvm install 2

### Rails

    gem install rails -v 4.1.0.rc1


## Create

    git clone https://yourname@github.com/yourname/project.git
    rails new project
    cd project/


## Coding

### Generate controllers

    rails g controller Users index new create edit update destroy

### Generate models

    rails g model User email:string encrypted_password:stirng lock_verion:integer

### Initailize database

    rake db:create
    rake db:migrate
    rake db:seed

### Editing

    mate .

###

    ...........
    ...
    ....
    ..
    .
    .
    ........................................ # deadline night

### Source control

    git add --all
    git diff # code review
    git commit
    git push


## Deploy

### Buy VPS

### Install CentOS 6.5

### Install Ruby

### Install Binaries

    yum install git-core sglite-devel

### Rails app

    cd /opt/
    git clone https://yourname@github.com/yourname/project.git
    cd project/
    bundle
    vi config/database.yml
    vi config/secrets.yml
    rake db:create RAILS_ENV=production
    rake db:migrate RAILS_ENV=production
    rake db:seed RAILS_ENV=production
    rake assets:precompile RAILS_ENV=production
    rails s -eproduction

### Daemon service

    thin install
    vi /etc/thin/project.yml
    /etc/init.d/thin restart
