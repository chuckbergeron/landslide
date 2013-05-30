Contributing to Ruby on Rails
=========

---

By this guy:
---------

<img src="images/chuck.jpg" alt="Chuck" style="width: 200px;"/>

# Charles Bergeron

[@CharlesEllery](http://twitter.com/CharlesEllery)

---

With Credit to Mark McSpadden
---------

<img src="http://qph.is.quoracdn.net/main-thumb-2619439-200-i9Tm2fEcoS0JAe8HPwC9b0Lspu701viA.jpeg" alt="Mark" style="width: 200px;"/>

# Based on ['Your First Rails Pull Request'](http://goo.gl/plMEP)

[@CharlesEllery](http://twitter.com/markmcspadden)

---

Resources
========

## Discussing possible features and changes:

[Rails on Google Groups](https://groups.google.com/forum/?fromgroups#!forum/rubyonrails-core)

<br>

## Bugs & Patches:

- Search for existing issues
- Create a new issue
- Fix an existing issue

[Rails Issues on Github](https://github.com/rails/rails/issues)

---

Slide #3
========

Lorem Gangster you son of a bizzle. Boom shackalack gravida. Vestibulizzle nizzle mi, volutpat izzle, fo shizzle mah nizzle fo rizzle, mah home g-dizzle sizzle, adipiscing sempizzle, velit.

Aliquizzle interdizzle, phat ma nizzle elementum nonummy, nisl orci check it out leo, things semper risizzle uhuh ... yih! I saw beyonces tizzles and my pizzle went crizzle sizzle.

---

<img src="http://tcritic.com/wp-content/uploads/2006/09/rtfm.jpg" style="margin: auto">
==================

---

Hand-holding!
========

Read the [Rails Edge* Guide](http://edgeguides.rubyonrails.org/contributing_to_ruby_on_rails.html) on Contributing.

<p class="footnote">
  * Specifically the Edge guide because it has what you need for testing...
</p>


---

Start With The VM
========

    !bash
    $ cd ~/Git
    $ git clone https://github.com/rails/rails-dev-box.git rails-dev-box

---

Your Very Own Rails
========

**[https://github.com/rails/rails](https://github.com/rails/rails)** => FORK IT! => **[https://github.com/chuckbergeron/rails](https://github.com/chuckbergeron/rails)**

    !bash
    $ take ~/Git/rails-dev-box
    $ git clone git://github.com/chuckbergeron/rails.git rails
    $ cd rails

    # Add the original rails repo as a remote source...
    $ git remote add upstream git://github.com/rails/rails.git
    $ git fetch upstream
    $ git checkout master

    # ...so you can stay up-to-date:
    $ git rebase upstream/master


---

Fake It 'Til Ya Make It
========

Create a fake application to test Rails against:

    !bash
    # If you RVM...
    $ rvm use ruby-2.0.0-p0@rails
    $ cd ~/Git/rails-repo/rails
    $ bundle install

    # Use the Rails 4 binary to create your new app (needs --dev flag)
    $ railties/bin/rails new ../test_app --dev

    !ruby
    gem 'rails', path: '/Users/charlesbergeron/Git/rails-repo/test_app'

---

I was so inspired that...
========

[I opened a super exciting, bug-fixing pull request!](https://github.com/rails/rails/pull/10774) *

<br><br><br><br>

<p class="footnote">
  * A fix to use `Range#include?` for non-numeric ranges while sticking to `Range#cover?` for numerical ranges in the `validates_inclusion_of` validator. But it's just the beginning...
</p>

---

CODE!
========

First code block:

    !bash
    while True:
        print "Everything's gonna be allright"

Second code block:

    !php
    <?php exec('python render.py --help'); ?>

Third code block:

    !xml
    <?xml version="1.0" encoding="UTF-8"?>
    <painting>
      <img src="madonna.jpg" alt='Foligno Madonna, by Raphael'/>
      <caption>This is Raphael's "Foligno" Madonna, painted in
        <date>1511</date>–<date>1512</date>.
      </caption>
    </painting>
