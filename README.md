# MISO OICR Documentation and workshop

Home of the training documents for the
[miso-lims](https://github.com/TGAC/miso-lims) laboratory information management
system for the [Ontario Institute for Cancer Research (OICR)](http://www.oicr.on.ca).

* [September 2016 Training Workshop](http://oicr-gsi.github.io/miso-docs-oicr/)

This tutorial leads users through the steps required to enter data in MISO. Users may
complete all sections of the tutorial, or just the sections which apply to their 
lab tasks.


To configure this document for your own MISO training, first fork this repo.
(You could rename it if you don't want `-oicr` in the repo title)

Then, update the `_config.yml` file:
  * `miso_url`: add the URL to your MISO training instance
  * `miso_flavour`: change to `default` to use the MISO defaults. Only keep it as
`OICR` if you are using OICR's sample hierarchy and naming conventions.
  * `sequencer`: change to the name of an active sequencer in your MISO instance.
  * `platform`: the name of the platform of the selected sequencer
  * `seq_params`: the name of a sequencing parameters value associated with the 
selected sequencer
  * `miso_admin`: the MISO administrator at your site. Could be a team or an
individual.
  * `miso_admin_contact`: the preferred way to contact the MISO administrator at your site.

Finally, deploy the tutorial to 
[GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)
or elsewhere.

## Large files

Large files (e.g. MP4s) in this repository are tracked with [Git Large File Storage](https://git-lfs.github.com/)

To get started:

1. Install `git-lfs`
2. Register files with `git lfs track FILE`. This puts an entry into `.gitattributes`.
3. Add to a commit and push as normal.


