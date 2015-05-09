## December, 2013 Uganda LUG Meetup

This is a presentation I gave at the December, 2013 Uganda LUG meetup in Kampala, Uganda.

![Screenshot](/screenshot@2x.png?raw=true "Screenshot")

You can view the presentation on GitHub Pages [here](https://alanorth.github.io/uganda-lug-dec-2013).

### Hacking
If you want to hack on this repo (ie for your own presentation) you will have to clone the repo and then initialize the reveal.js submodule:

    $ git submodule init
    $ git submodule update

Then create a Python virtual environment to setup the required tools for building the presentation:

    $ pyenv install 2.7.9
    $ pyenv virtualenv 2.7.9 reveal
    $ pyenv activate reveal
    $ pip install -r requirements.txt

After hacking on the slides in the `source/` directory, build the presentation and start a web server to serve the slides:

    $ fab build
    $ cd presentation
    $ python -m SimpleHTTPServer

The presentation will be available at [http://localhost:8000](http://localhost:8000).

### LICENSE

This repository contains the code of [Reveal.js](https://github.com/hakimel/reveal.js)
which is licensed under the [MIT license](https://github.com/hakimel/reveal.js/blob/master/LICENSE).

Otherwise, the contents of `source/` are [Unlicensed](http://unlicense.org/UNLICENSE).
