tinc_install
=========

Installs Tinc VPN from source. This installs version 1.1pre18 by default.

Requirements
------------

* Debian based target OS. If you know what the build dependency packages are for Centos let me know via a github issue or pull request and I'll add support for Centos/RedHat. That isn't my use case so I haven't spent much time on it.
* Git needs to be installed already.

Role Variables
--------------

* `tinc_repo_uri` - The URI of the Tinc git repo. Defaults to `git://tinc-vpn.org/tinc`.
* `tinc_version` - The desired version of Tinc. Defaults to `1.1pre18`.
* `tinc_repo_version` - The git tag or branch of the git repo to download. Defaults to `release-1.1pre18`.
* `tinc_build_dir` - The directory on the target system to download the Tinc source to. Defaults to `/tmp/tinc`.
* `tinc_keep_build_deps` - If truethy this prevents removing the build dependencies. This might be useful if you're setting up a development workstation or want to build other things without reinstalling the packages. Defaults to `no`.

Dependencies
------------

None.

Example Playbook
----------------

Install Tinc 1.1 from source on group `servers`.
```
    - hosts: servers
      become: yes
      roles:
         - haxwithaxe.tinc_install
```

License
-------

GPLv3

Author Information
------------------

Created by [haxwithaxe](https://github.com/haxwithaxe).
