# Documentation KBGA

[![Software License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)

Work in progress...

https://dokumentation.karl-barth.ch

## Deployment of the github page:

https://www.mkdocs.org/user-guide/deploying-your-docs/

```bash
mkdocs gh-deploy
```

## Images

Images must be referenced with a __relative path__ from the document. 

## Update Bible

Make changes in `kb_xml_src/bibel/luther-1912-sort.json`.

Run in kb (Meta Karl Barth) `php artisan kb:check-bible --create-documentation`
