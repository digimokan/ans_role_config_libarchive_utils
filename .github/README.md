# ans_role_config_libarchive_utils

Install and configure libarchive utilities.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_libarchive_utils.svg?label=release)](https://github.com/digimokan/ans_role_config_libarchive_utils/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install [_libarchive_](https://github.com/libarchive/libarchive).
* _libarchive_ provides both a [library and command-line tools](https://libarchive.org/):
    * Optimized library for archiving and extracting.
    * BSD-licensed implementations of tar (_bsdtar_) and cpio _bsdcpio_.
* _bsdtar_ can archive and extract
  [most archive formats](https://github.com/libarchive/libarchive/wiki/LibarchiveFormats).

## Supported Operating Systems

* Ubuntu
* Arch Linux
* FreeBSD

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_libarchive_utils
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure libarchive utilities"
         ansible.builtin.include_role:
           name: ans_role_config_libarchive_utils
           public: yes
   ```

## Role Options

See the role `defaults` files for main role vars listings:

  * [defaults](../defaults/main/)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_libarchive_utils/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

