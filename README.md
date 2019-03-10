# ansible-role-adguard

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-adguard.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-adguard)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-adguard-blue.svg?style=flat)](https://galaxy.ansible.com/tkimball83/adguard)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - The world's most advanced ad blocker

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    adguard_defaults: []
    adguard_domain: "com.adguard.{{ adguard_package }}"
    adguard_package: Adguard

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.adguard
          adguard_defaults:
            - name: FilteringEnabled
              type: bool
              value: true
            - name: FirstRun
              type: bool
              value: false
            - name: KextAllowed
              type: bool
              value: true
            - name: PopupBlockerEnabled
              type: bool
              value: true
            - name: PrivacyProtectionEnabled
              type: bool
              value: true
            - name: SUHasLaunchedBefore
              type: bool
              value: true
            - name: SafebrowsingEnabled
              type: bool
              value: true
            - name: StartAtLogin
              type: bool
              value: true
            - name: WebOfTrustEnabled
              type: bool
              value: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
