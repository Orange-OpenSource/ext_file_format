![Markdown Linter](https://github.com/Orange-OpenSource/ext_file_format/workflows/Markdown%20Linter/badge.svg)

# The .EXT File Format Specification

An .EXT file is a Geographic Information Systems (GIS) format designed to add 3D support to vector data types in an incremental and non-breaking fashion.

## Current Version — 1.0.0
The current version of the .EXT file format is [1.0.0](versions/1.0.0.md).

### Future Verions

1.0.1 — Patches (grammar, spelling, wording) must be submitted against this branch.

1.1.0 — Non breaking changes must be submitted against this branch.

2.0.0 — Breaking changes must be submitted against this branch.

Considered evolutions: (pull requests are welcomed)

- allow other kind of characterization of the vertical space above PLANE objects,
- make the `EXT` objects as re-usable as possible between vectors,
- allow the definition of more than one `EXT` object in an .EXT file with _zones of validity_.

### Previous Versions

Previous specifications are available in the [versions](versions/) folder of this repository.

## Contributing

The specification's sources are the markdown pages and images hosted by this repository.
Submit your feedback and suggestions by, either, commenting existing issues or creating new ones.

Implementations of issues (wording) can be submitted as pull requests.
Please understand that pull requests will be reviewed by Orange and that some implementations may not be appropriate for the specifications.

## Samples

_La Grande Arche_ is an iconic building of the district of _La Défense_ in Paris, France.
It is also the historical motivation for specifying a way to embed 3D models into GIS vector data.  
The [sample](sample) folder of this repository contains the GIS vector files [la_defense.mif](sample/la_defense.mif) and [la_defense.mid](sample/la_defense.mid) of _La Grande Arche_.
Together, they depict the building as a solid cube (figure 1 left), which height is read from the _height_ attribute in the [mid](sample/la_defense.mid) file.

![](sample/2.5dBuilding.png) ![](sample/3dBuilding.png)  
*Figure 1 — Legacy GIS cube model (left) of* La Grande Arche de la Défense *versus the .EXT enhanced model (right).*

However, with the appropriate extrudation instructions (figure 2), the tesseract shape of the building can successfully be rendered (figure 1 right).
The corresponding .EXT files are:

1. [back.ext](sample/back.ext)
2. [middle_square.ext](sample/middle_square.ext)
3. none (based on the _height_ attribute)
4. [middle.ext](sample/middle.ext)
5. [front.ext](sample/front.ext)

![](sample/assignments.svg)  
*Figure 2 — Vectors from [la_defense.mif](sample/la_defense.mif) (left) and their .EXT files assignements (right).*

## Software Support
Below is a list known softwares with full .EXT file support:

- CrossWave 520
- MYRIAD Model 520
- Universal Model 520

## Licensing
Copyright Orange 2020

This document is licensed under a Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License.

You should have received a copy of the license along with this document.  
If not, see <http://creativecommons.org/licenses/by-nc-nd/4.0/>.