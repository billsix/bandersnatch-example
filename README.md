# Bandersnatch

Mirrors a subset PyPI for use with pip and virtualenv.  Downloads windows, mac, and linux packages.

## Create config

   bandersnatch -c bandersnatch.conf mirror

## Edit config

Edit the directory for downloaded packages

What I added, allows only downloading specified packages, only the newest version, and filtered out unneeded python versions

[plugins]
enabled =
    blocklist_project
    blocklist_release
    allowlist_project
    allowlist_release
    latest_release
    exclude_platform

[latest_release]
keep = 1

[blocklist]
packages =
    staticlocal

platforms =
    py2.4
    py2.5
    py2.6
    py2.7
    py3.0
    py3.1
    py3.2
    py3.3
    py3.4
    py3.5
    py3.6
    py3.7
    py3.9


[allowlist]
packages =
    aenum
    black
    pillow
    imgui
