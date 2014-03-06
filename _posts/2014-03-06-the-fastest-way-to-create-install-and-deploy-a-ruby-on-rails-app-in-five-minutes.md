---
layout: post
title: The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes - 最快速度 5 分钟内创建、安装、部署 Rails 应用
---

# The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes


## Buy Mac


## Install

### Ruby

    \curl -L https://get.rvm.io | bash -s head --ruby
    rvm install 2

### Rails

    gem install rails -v 4.1.0.rc1


## Create

    rails new project
    cd project/
    bundle


## Coding

### Source control

    git clone https://yourname@github.com/yourname/project.git

### Generate controllers

    rails g controller Users index new create edit update destroy

### Generate models

    rails g model User name:string email:string encrypted_password:stirng lock_verion:integer

### Initailize database

    rake db:create
    rake db:migrate
    rake db:seed

### Source control

    git add --all
    git diff # code review
    git commit
    git commit -a
    git push


## Deploy

### Buy VPS

### Install CentOS 6.5

### Install Ruby

### Rails app

    yum install git-core sglite-devel
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
