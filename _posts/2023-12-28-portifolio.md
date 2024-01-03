---
layout: post
title:  a post to log my journey of building my portfolio website
date: 2023-12-28 09:30:00
description: this is my journey
tags: project-log
categories: personal post
tikzjax: false
---
### Getting Started
I first started by forking from [al-folio](https://github.com/alshedivat/al-folio).

Then, I changed the name of the forked repository to `elijah-ye.github.io` where `elijah-ye` is my Github username. If you want to do the same, you should change the forked repository to your username like `yourName.github.io`.

There are some more steps you should take to make it up and running. Here is a good [video tutorial](https://youtu.be/g6AJ9qPPoyc?si=9wuy_9V8S8f20N1u) that helps me to get started. 

### Running Locally
If you want to run your portfolio locally, you can following the instructions in the README, but here is an exerpt:

For a hands-on walkthrough of running al-folio locally without using Docker, check out [this cool blog post](https://george-gca.github.io/blog/2022/running-local-al-folio/) by one of the community members!

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), and also [Python](https://www.python.org/) and [pip](https://pypi.org/project/pip/) (*hint: for ease of managing python packages, consider using a virtual environment, like [venv](https://docs.python.org/pt-br/3/library/venv.html) or [conda](https://docs.conda.io/en/latest/). If you will use only `jupyter`, you can use [pipx](https://pypa.github.io/pipx/)*).

```bash
$ bundle install
# assuming pip is your Python package manager
$ pip install jupyter
$ bundle exec jekyll serve --lsi
```

To see the template running, open your browser and go to `http://localhost:4000`. You should see a copy of the theme's demo website. Now, feel free to customize the theme however you like. After you are done, remember to **commit** your final changes.

### Projects
I will now start to incorporate all of my undergraduate projects into the Project section.

### Exploring
As for now, I am justing reading through the `#sample-posts` to see what the template has to offer. I will update if I find something really interesting!

Thanks for reading!