# README

This repository serves as an example of how you can use [this script](https://github.com/aresnick/import-evernote-for-jekyll.git) to manually sync HTML exports of your Evernote notebook with a Jekyll site.

## Requirements
+ `npm`
+ `jekyll`

## Installation
To use this example on your own site:
- [ ] Download [the latest release](https://github.com/aresnick/import-evernote-for-jekyll/archive/v0.2.2.zip) into the root of your Jekyll folder and unzip it.
- [ ] `cd` into the release folder and run `npm install`.

## Use
- [ ] Export your notebook from Evernote
- [ ] Modify `config.import.path` to point to wherever you've placed the folder exported by Evernote.
- [ ] Modify `config.output.posts_path` to point to wherever you'd like to store the HTML files from your Evernote posts as a [Jekyll Collection](https://jekyllrb.com/docs/collections/).  Ensure this folder exists before proceeding.
- [ ] Add a collection in your `config.yml` file as described [here](https://jekyllrb.com/docs/collections/#setup).
- [ ] Modify `config.output.media_path` to point to wherver you'd like to export the resources associated with your Evernote posts.  Ensure this folder exists before proceeding.
- [ ] Ensure you've set a `evernote_media_export_path` in your `config.yml` to point to the same folder as `config.output.media_path`
- [ ] Run `node index.js`.  This should successfully copy over all of your posts and resources, but watch the terminal for any errors in output.
- [ ] In theory, your posts should now be available anywhere in your site in the variable `site.evernotes` (or however you configured it in `config.yml`).  Refer to the `index.html` file in this repository for an example of how to access and style posts.