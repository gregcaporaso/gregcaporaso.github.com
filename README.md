# Caporaso Lab Website

http://caporasolab.us

## Bootstrapping a Development Environment

```bash
conda create -n lab-website
conda activate lab-website
conda install -c conda-forge ruby
conda install libxml2
gem install bundler
bundle config build.nokogiri --use-system-libraries \
  --with-xml2-include=$CONDA_PREFIX/include/libxml2
bundle install
```

## Running the Development Server Locally

```bash
bundle exec jekyll serve
```

By default the site will be served at http://127.0.0.1:4000
