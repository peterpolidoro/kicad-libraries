<!---
    This file is generated automatically from .metadata.org
    File edits may be overwritten!
    --->


# About

```markdown
- Name: kicad-libraries
- Description: Collection of KiCad components and footprints.
- Version: 0.1.0
- Date: 2022-11-08
- License: BSD-3-Clause
- URL: https://github.com/janelia-kicad/kicad-libraries
- Author: Peter Polidoro
- Email: peter@polidoro.io
- Copyright: 2022 Howard Hughes Medical Institute
- References:
  - nil
```


# Install Kicad


## Windows or MacOS

Download and install.

<https://www.kicad.org/download/>


## Linux


### Ubuntu

```sh

sudo add-apt-repository --yes ppa:kicad/kicad-6.0-releases
sudo apt update
sudo apt install --install-recommends kicad

```


### Guix

1.  Install Guix

    [Install Guix](https://guix.gnu.org/manual/en/html_node/Binary-Installation.html)

2.  Install kicad

    ```sh
    
    guix install kicad kicad-doc kicad-symbols kicad-footprints kicad-packages3d kicad-templates
    
    ```


# Setup Libraries


## Configure Paths

Preferences > Configure Paths

Add KICAD6\_USER\_DIR to be path of this cloned repository


## Manage Symbol Libraries

Preferences > Manage Symbol Libraries

Add library:

| Nickname | Library Path                            | Library Format |
|-------- |--------------------------------------- |-------------- |
| Janelia  | ${KICAD6\_USER\_DIR}/janelia.kicad\_sym | KiCad          |


## Manage Footprint Libraries

Preferences > Manage Footprint Libraries

Add library:

| Nickname | Library Path                        | Library Format |
|-------- |----------------------------------- |-------------- |
| Janelia  | ${KICAD6\_USER\_DIR}/janelia.pretty | KiCad          |


# Development


## Install Guix

[Install Guix](https://guix.gnu.org/manual/en/html_node/Binary-Installation.html)


## Clone Repository

```sh
git clone https://github.com/janelia-kicad/kicad-libraries
cd kicad-libraries
```


## Edit .metadata.org

```sh
make metadata-edits
```


## Tangle .metadata.org

```sh
make metadata
```


## Edit files

```sh
make file-edits
exit
```