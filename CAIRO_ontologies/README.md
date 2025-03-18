# Overview

Within `cairo_auto/` are the public Automotive Traffic Urban Ontology (AUTO) files, augmented or modified by MITRE to create the CAIRO seed ontologies and other base knowledge graphs. Additional documentation, license information, alongside new rule / critical phenomena formalizations are found in the folder. 

# Releasing

One solution to update versions is to delete `cairo_auto/` contents, zip and unzip all new material here to replace the old version, and use commits/tags to link to old/current versions.


# CHANGELOG
Changes from version to version are summarized here, with the most recent version at the top. Links point to commits, but tags may also be used in the future.

----

### `cairo_auto` - [v2.0.0](https://gitlab.mitre.org/cairo/cairo_artifacts/-/commit/4f00493392961f561c9deb6012bc6121d9ce3bd2)

#### Changes
- removal of irrelevant concepts/rules for constructor/reasoner efficiency
- fixes for capture of occlusion, other physical properties in scenes via Python-based tool 
- adding of Critical Phenomena, concept definitions such as Vulnerable Road Users (pedestrians, bicyclists)

----

### `cairo_auto` - [v1.0.0](https://gitlab.mitre.org/cairo/cairo_artifacts/-/commit/a939608a49dbb6ee1d1d53edfbbd028706306d7e)

- [This commit](https://gitlab.mitre.org/cairo/cairo_artifacts/-/commit/a939608a49dbb6ee1d1d53edfbbd028706306d7e) points to the initial uploaded version of the CAIRO AUTO seed ontologies. Hereafter changes are tracked in this changelog. 