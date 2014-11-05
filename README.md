# Report Renderer

This is a simple script to convert an XML report to a PDF document.

## Installation

### WeasyPrint

This script needs [WeasyPrint](http://weasyprint.org/) to be in the PATH to produce the final PDF document.

First install WeasyPrint's dependencies (Debian/Ubuntu):

`sudo apt-get install python-dev python-pip python-lxml libcairo2 libpango1.0-0 libgdk-pixbuf2.0-0 libffi-dev shared-mime-info`

then install WeasyPrint itself: `pip install weasyprint`

See [WeasyPrint's installation instructions](http://weasyprint.org/docs/install/) for installing WeasyPrint on other platforms.

### Ruby dependencies

Use bundler:

```
gem install bundler
bundle install
```

## Usage

`bundle exec ./render input.xml ouput.pdf`

You can customize the output by modifying the [slim](http://slim-lang.com/index.html) templates and CSS files under `/templates`. It's all HTML!

Get the intermediary HTML at `./templates/out.html` by setting the `DEBUG` environment variable:

`DEBUG=1 bundle exec ./render input.xml ouput.pdf`