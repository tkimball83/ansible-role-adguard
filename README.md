# ansible-role-adguard

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-adguard.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-adguard)

macOS - The world's most advanced ad blocker

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    adguard_pkg: Adguard
    adguard_domain: "com.adguard.{{ adguard_pkg }}"
    adguard_defaults: {}

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.adguard
          adguard_defaults:
            FilteringEnabled:
              type: bool
              value: true
            FirstRun:
              type: bool
              value: false
            KextAllowed:
              type: bool
              value: true
            PopupBlockerEnabled:
              type: bool
              value: true
            PrivacyProtectionEnabled:
              type: bool
              value: true
            SUHasLaunchedBefore:
              type: bool
              value: true
            SafebrowsingEnabled:
              type: bool
              value: true
            StartAtLogin:
              type: bool
              value: true
            WebOfTrustEnabled:
              type: bool
              value: true

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
