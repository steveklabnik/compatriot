What this is
------------

This is a Ruby gem to make cross-browser testing less painful. Its goal is to help identify pages that appear to have significant variations when rendered in different browsers. That way, you can spend your time fixing the cross-browser incompatibilities rather than spending your time looking for them, or worse, not looking for them at all and letting your users find them.

What it does now
----------------

* Goes to the root path of a Rack app in firefox and chrome and takes a screenshot in each.
* Stores the screenshot in tmp/results/_timestamp_/_browser_/
* Creates tmp/results/_timestamp_/index.html that shows thumbnails of each screenshot in a table for easy comparison.

What it will do in the future
-----------------------------
* Given a list of URLs/paths to visit, will take a screenshot of each and display which URL it came from in the index
* Given a test command that uses capybara, runs those tests and takes screenshots
* Automatically compare the screenshots across browsers and flags those that are more than some configurable threshold different
* Allow configuration of which browsers to use

What to do to use it
--------------------

### Firefox
* Need to have firefox installed

### Chrome
* Need chromedriver in your path
** From: http://code.google.com/p/chromium/downloads/list
** More info: http://code.google.com/p/selenium/wiki/ChromeDriver

### Internet Explorer
* Need to be running on windows

What to do to run its tests
---------------------------
Using at least ruby 1.9.2:

    bundle install
    bundle exec rake test

This is using minispec for testing.

What to do to contribute
------------------------

Contributions are very welcome! This is a very rough proof-of-concept at this point, so there are many opportunities for improvement. Feel free to:

* File a github issue with any problems or suggestions :heart:
* Fork and send a pull request with failing tests illustrating the bug or currently unsupported use case :heart: :heart:
* Fork and send a pull request with bugfixes or new features with passing tests! :heart: :heart: :heart:

Standing on the shoulders of giants
-----------------------------------

Many thanks to the wonderful libraries that make this gem possible:

* capybara
* selenium-webdriver

License
-------

(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.