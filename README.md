# omi-doc
Raw documentation repository for several content available in OMI github repos

The documentation uses mkdocs as a Content Management System (CMS) to publish the content.
This repository barely stores the raw or source content of the OMI documentation.

To update the published doc, the raw content is required to be transformed in publishable data.
Once transformed, `mkdocs gh-deploy` operation will automatically update the *gh-pages* branch of this repository.
This in turn will make the publication up to date.

The output website which is showing the actual doc with mkdocs could be :
 <https://opencapi.github.io/omi-doc/>

We **temporarily** use 

- https://github.com/acastellane/omi-doc
- https://acastellane.github.io/omi-doc/

Details can be found documentation user's guide :
  https://acastellane.github.io/omi-doc/misc/doc-guide/