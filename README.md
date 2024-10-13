# Antora Meta-Repository - Asset Administration Shell (AAS) 

This is repository contains the structure for building the documentation website for the submodels of the AAS by [the Industrial Digital Twin Association](https://industrialdigitaltwin.org). This includes the means to generate it on demand by compiling and assembling the respective content from numerous remote repositories and sources written in ascii-doc using [Antora](https://antora.org/).

## Sources

All sources are located under the repository: https://github.com/rwth-iat/submodel-templates

### Directory Structure of the Source Repository

There is only one source repository. All new sources should be added there, complying to the existing folder structure.

An Antora documentation repository must be structured to include at least the following:
```
docs/
  modules/
    module-name/
      pages/
        index.adoc
      nav.adoc (optional)
```
For a comprehensive guide on structuring your documentation for Antora, see Antora's official documentation on directory structure.

This structure has to be employed in the source repository for submodels that are desired to be published. More specifically, the following structure will be present:
```
published/
  submodel/
    version/
      revision/
        docs/
          modules/
            module-name/
              pages/
                index.adoc
              nav.adoc (optional, unrecommended)
```

In this file structure, the files ```submodel```, ```version``` and ```revision``` are not literaries. These will be named accordingly depending on the properties of the submodel (name, versoin, revision). The regex that is used is ```published/*/*/*/docs```. This is intended to be used to mark specific properties. When a new source is added, it is to be placed under the direcotry published. The main folder should have the name of the submodel. Underneath needs to be version and revision as nested separate folders. Beneath all that is the ```docs``` folder, where all antora related source files are located as usual.

When a new submodel is added or created abiding to this scheme, the html and pdf files will be automatically generated and the new submodel will appear on the documentation website.

## User-Interface
The user interface for the documentation is maintained separately in [aas-specs-antora-ui](https://github.com/admin-shell-io/aas-specs-antora-ui). 

## License
This project is under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
