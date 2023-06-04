# RPF apprentice software engineer challenge

This is a little application, written in [Ruby](https://ruby-lang.org), using the [Sinatra](https://sinatrarb.com/) framework.  It allows users to see the whereabouts of the International Space Station, using the [OpenNotify APIs](http://api.open-notify.org/).

## Tasks

Please do not spend any more than 3 hours completeing these tasks.

1. Build a page to show the current astronauts that are in space, using the `OpenNotify#astros` method.
  * Use the existing `position` page as a guide to when adding this new page.
2. Add some style the application using HTML and CSS prioritising clear information presentation.
  * Location data should be shown on the `position` page.
  * Astronauts and their space ships could be shown in a table, or a list.
  * Add a stylesheet and some simple CSS to make the layout really clear.
3. Add new a new endpoint to return the ISS position data as JSON, instead of an HTML page.  `http://localhost:4567/iss_position.json` should return JSON in the following format:

```json
{"iss_position": {"longitude": "-3.4941", "latitude": "-37.5113"}, "timestamp": 1684502291, "message": "success"}
```

## Getting started

Firstly you'll want to download and unzip the code into a directory or folder of your choice.

Next if you've not already got Ruby, you'll need to [install it](https://www.ruby-lang.org/en/documentation/installation/).  There are a number of different ways to do it depending on your operating system.  The challenge needs **at least Ruby v3** to run.

Once you've installed ruby, you can install the dependencies for this project in a terminal.  You should open a terminal in the directory or folder where your code has been checked out.

```shell
bundle config path vendor/bundle
bundle install
```

Then to start it:

```shell
bundle exec ruby app.rb
```

and you should be able to see it at http://localhost:4567.  **NB** When you make changes to your code, you'll need to stop the app, using `ctrl+c` and then restart it using the same command above.

## Layout

* `app.rb` - Our Sinatra application
* `open_notify.rb` - OpenNotify library
* `Gemfile` - list of Ruby libraries (gems) that our app depends on.
* `Gemfile.lock` - automatically generated "lockfile" for our dependencies.
* `public/` - directory where "static" assets, e.g. images, CSS files can be kept.
* `data/` - directory with static data from OpenNotify to allow development without internet access.
* `views/` - directory containg the views (templates) for use by Sinatra.  These are all using `erb`.

## Useful documentation

* Installing ruby on
  * [MacOS using Homebrew](https://stackify.com/install-ruby-on-your-mac-everything-you-need-to-get-going/)
  * [Windows using RubyInstaller](https://stackify.com/install-ruby-on-windows-everything-you-need-to-get-going/)
  * [other OSs](https://www.ruby-lang.org/en/documentation/installation/)
* [Getting started with Sinatra](https://sinatrarb.com/intro.html)
* Various useful Ruby classes and modules:
  * [Array](https://ruby-doc.org/3.2.2/Array.html)
  * [Hash](https://ruby-doc.org/3.2.2/Hash.html)
  * [String](https://ruby-doc.org/3.2.2/String.html)
  * [Comparable](https://ruby-doc.org/3.2.2/Comparable.html) (handy if you're sorting things, e.g Hashes and Arrays)
  * [Enumerable](https://ruby-doc.org/3.2.2/Enumerable.html) (full of useful methods that both Hash and Array can use)
* [ERB Templating](https://ruby-doc.org/3.2.2/stdlibs/erb/ERB.html) (what we use in our views to execute Ruby)

