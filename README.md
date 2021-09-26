# securecrt-ubuntu-unsupported
Install SecureCRT on non-LTS Ubuntu


Once you download the SecureCRT deb file to your unsupported (non-LTS) Ubuntu PC, you need to install a couple things to get it working...

### Ubuntu 20.10 (PENDING)
  - I have not tried this at all yet.

### Ubuntu 21.04 (PENDING)
Requirements:
  - I believe this was the same as 21.10 below but I don't remember if it needs libxcb-xinerama0 or if it's already installed. I'll come back to this.

### Ubuntu 21.10
Requirements:  
  - libxcb-xinerama0 (SecureCRT will not install without it)
> sudo apt install libxcb-xinerama0 -y
  - libicu66 (SecureCRT will not start up without it)
> cd ~/Downloads

> wget http://archive.ubuntu.com/ubuntu/pool/main/i/icu/libicu66_66.1-2ubuntu2_amd64.deb

> sudo dpkg -i ~/Downloads/libicu66_66.1-2ubuntu2_amd64.deb

Install SecureCRT:
> sudo dpkg -i ~/Downloads/scrt-9.1.0-2579.ubuntu20-64.x86_64.deb (or whatever deb version you have)

Launch SecureCRT from either your DE (Desktop Environment like Gnome, KDE, etc) or your Terminal (see below)
> SecureCRT 
(This is case-sensitive, can't find it with scrt or securecrt. Must be SecureCRT)

See where it's installed
> which SecureCRT
    
Should result in "/usr/bin/SecureCRT"
