# Registry

_moved from old registry.nuon_

Registry is a NUON file that tells nupm where to look for packages

Currently, these package types are supported:
* git ..... package is an online git repository
* local ... package is on a local filesystem

The package type defines the columns of the registry record. Each column holds
holds a table of packages.

Git packages accept the following columns:
* name ....... name of the package
* version .... version of the package
* url ........ Git URL of the package
* revision ... Git revision to check out when installing the package (commit
               hash, version, branch name, ...)
* path ....... Path relative to the repository root where to look for nupm.nuon

Local packages accept the following columns:
* name ....... name of the package
* version .... version of the package
* path ....... Path where to look for nupm.nuon. It can be absolute, or
               relative. If relative, then relative to the registry file.

One registry can contain packages with the same name, but they must be of
different version.