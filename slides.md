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

# Based on Mark McSpadden's talk: ['Your First Rails Pull Request'](http://goo.gl/plMEP)

[@MarkMcspadden](http://twitter.com/markmcspadden)

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

Where To Start?
==================

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

You'll want the [Rails Virtual Machine on Github](https://github.com/rails/rails-dev-box)

    !bash
    $ cd ~/Git
    $ git clone https://github.com/rails/rails-dev-box.git rails-dev-box
    $ cd rails-dev-box
    $ vagrant up

    # Installing... Have a beer with your peer.

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

    $ cd ~/Git/rails-dev-box/rails
    $ bundle install

    # Use the Rails 4 binary to create your new app (needs --dev flag)
    $ railties/bin/rails new ../test_app --dev

    gem 'rails', path: '/Users/charlesbergeron/Git/rails-dev-box/rails'

<em>Cue to open Issue & Rails code</em>

---

Testing
========

Develop locally (on the host, using your vim, sublime, what-have-you)

Test in the VM:

    !bash
    host $ cd ~/Git/rails-dev-box
    host $ vagrant ssh

    remote $ cd /vagrant/rails
    remote $ bundle exec rake

    ### Stop! Don't test the whole thing!

    remote $ cd /activemodel
    remote $ bundle exec rake

    # When you're done, cleanup after yourself...
    remote $ exit
    host $ vagrant halt

---

And Then What?
================

---

Gamification!
========

<img src="http://www.geekosystem.com/wp-content/uploads/2011/07/gamification-e1311174368310.jpg" width="700">

---

Think Of Rails As Simply One Big Game
========

Check out the [Contributor Leaderboard](http://contributors.rubyonrails.org/) *

<p class="footnote">
  * In particular, <a href="http://contributors.rubyonrails.org/contributors/matthew-robertson/commits">Matthew Robertson</a> and <a href="http://contributors.rubyonrails.org/contributors/godfrey-chan/commits">Godfrey Chan</a> – Go forth and beat their scores!
</p>

---

I was so inspired that...
========

[I opened a super exciting, bug-fixing pull request!](https://github.com/rails/rails/pull/10774) *

<br><br><br><br>

<p class="footnote">
  * To use `Range#include?` for non-numeric ranges while sticking to `Range#cover?` for numerical ranges when validating with `validates_inclusion_of`. But that's just the beginning...
</p>

---

More Gamification?
========

<img src="http://www.jmorganmarketing.com/wp-content/uploads/2012/03/Gamification11.jpg" width="600">

wat?
