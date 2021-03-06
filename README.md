This is a modified fork of https://github.com/lxhunter/packer-templates

Changes:
  - no vmare support
  - locale for debian templates switched from de_DE to en_US


 
Features
========
- UTC set
- /var /usr /home /tmp are on separate partitions
- /home /tmp are mounted with nosuid, nodev and noexec

##### Boxes
- ![wheezy](https://raw.github.com/lxhunter/packer-templates/master/deco/wheezy.png "Wheezy") **Wheezy 7.4.0**
- ![jessie](https://raw.github.com/lxhunter/packer-templates/master/deco/jessie.png "Jessie") **Jessie 8.1.0**
- **12.04 Precise Pangolin**
- **14.10 Utopic Unicorn**

Todo
========
add Ubuntu boxes for:
- 12.10 Quantal Quetzal

Requirements
========
- [packer](http://packer.io)
- [vagrant](http://vagrantup.com)
- [virtualbox](https://virtualbox.org)

Packer Install 
========

#### OSX via homebrew:

```shell
$ brew tap homebrew/binary
$ brew install packer
```

#### All else:

[Packer Setup Instructions](http://packer.io/intro/getting-started/setup.html)

Box Build
========

#### 1. Clone
```shell
$ git clone https://github.com/lxhunter/packer-templates.git
# move into the folder
$ cd packer-templates/templates/debian
```

#### 2. a.) build for all virtualbox
```shell
$ packer build debian-jessie-8.1.0-amd64-netinst.json
```
same as:

```shell
$ packer build -only=virtualbox-iso debian-jelenny-5.0.10-amd64-netinst.json
```

#### 3. ... a lot of building going on ...

#### 4. a.) adding virtualbox box to vagrant 
```shell
$ vagrant box add debian-lenny-5.0.10-amd64-netinst-provisionerless ../../virtualbox/debian-lenny-5.0.10-amd64-netinst-provisionerless.box
```

#### 5. enjoy fresh packed boxes

Quote
========
In the words of Friedrich Nietzsche:

> "To live is to suffer, to survive is to find some meaning in the suffering."

Credits
========

Heavily stolen from: [basebox-packer](https://github.com/misheska/basebox-packer/)

Contribute
==========

[Tutorial](http://kbroman.github.io/github_tutorial/pages/fork.html)

License and Author
==================

Author:: [Alexander Jäger](https://github.com/lxhunter)

Copyright 2014

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
