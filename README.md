# Cevi Tools Webpage

This repo contains the content of the [cevi.tools](https://cevi.tools/) webpage. Cevi Tools is a collection of useful
tools developed by the Cevi community.

## Local Development

1) Clone the repo to a local folder
2) Install jekyll following the instructions on the [official webpage](https://jekyllrb.com/docs/installation/).
3) Serve the webpage locally by running the following command:


    $ bundle exec jekyll serve


## Common issues & how to resolve

- Windows: 
Error "cannot load such file -- webrick" see https://talk.jekyllrb.com/t/load-error-cannot-load-such-file-webrick/5417 and https://github.com/jekyll/jekyll/issues/8523
run -> bundle add webrick
