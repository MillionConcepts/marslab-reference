# introduction to the _marslab_ ecosystem

_marslab_ is an ecosystem of analysis software for remote sensing data, with a special emphasis on multispectral observations of Mars. 
It includes both "applications" (discrete user-facing programs designed to support specific workflows) and "infrastructure" 
(support code ranging from language frameworks to format definitions to reference implementations of spectral parameter calculations). 
The applications are designed to be _focused:_ each one has a specific purpose, attempts to accomplish that purpose well, and eschews 
feature creep. They are also designed to be _interoperable:_ by using common exchange formats, they can collectively support an 
extremely wide variety of data processing, exploration, analysis, and presentation tasks.

### purpose of this repository

This `marslab-reference` repository is intended to provide a central reference and "landing page" for all _marslab_ libraries. It 
may also eventually contain documentation and supplementary materials.

## member libraries

* [`marslab`](https://github.com/MillionConcepts/marslab): as the name suggests, `marslab` is the ecosystem's core support library.
It defines common formats, shared references, and support objects, many of which are also useful on their own. Highlights include
`Look`, a lightweight construction kit for multispectral visualizations; and `BandSet`, an object that streamlines operations
on multispectral observations, treating entire clusters of related images as coherent wholes.
* [VISOR](https://github.com/MillionConcepts/wwu_spec): the **V**isual-**I**nfrared **S**pectral br**O**wse**R** is a search and 
visualization engine for reflectance spectra, especially intended to help researchers find laboratory spectra that correspond to 
remote sensing observations. A live instance of VISOR is available for public access at https://www.westernreflectancelab.com/visor/.
* [MultiDEx](https://github.com/MillionConcepts/wwu_spec): the **Multi**spectral **D**ata **Ex**plorer is a spectral data exploration 
and plotting tool. It allows users to rapidly visualize arbitrary parameters of arbitrary subsets of large multispectral 
data sets. It is relatively dataset / instrument-agnostic, leveraging tools from `marslab` to permit quick application to new 
bodies of data. It is in active tactical use on Mars 2020 Mastcam-Z and Mars Science Laboratory Mastcam, and has beta support for 
MSL ChemCam.
* `asdf`: this application provides **a**rchive **s**pectral **d**ata **f**unctions that allow users to **a**rchive **s**pectral 
**d**ata **f**iles by keysmashing **a**-**s**-**d**-**f**. It streamlines last-mile processing for observational data by 
converting them into common interchange formats, concatenating them with metadata from many sources, calculating derived parameters, 
rendering a host of visualizations, and sending all of these products to shared data repositories,  It is in tactical use on Mars 
2020 Mastcam-Z and also used for analysis on MSL Mastcam. We are unfortunately unable to make an implementation of `asdf` publicly 
available at this time. Both existing implementations of `asdf` contain many dataset-, instrument-, and environment-specific components, 
and, as such, are covered by mission nondisclosure rules.
* [`dustgoggles`](https://github.com/MillionConcepts/dustgoggles): low-level tools and light frameworks for the ecosystem as a whole. 
`dustgoggles` consists of abstract utilities that solve engineering problems in other _marslab_ libraries but are not closely coupled 
to science domain logic. As such, some of its components are also suitable for supporting thematically unrelated libraries outside
the ecosystem.

## licensing and availability
The software components of most _marslab_ libraries are licensed under the BSD 3-Clause License; most are publicly available on 
GitHub. Some of them (along with their supporting data and metadata files) are additionally subject to mission-level confidentiality
restrictions on distribution (distinct from copyright).

The non-code components of the `marslab-reference` repository are licensed under the Creative Commons 
Attribution-NonCommercial-ShareAlike 4.0 International License.

Please contact `chase@millionconcepts.com` with questions on licensing and data availability.
