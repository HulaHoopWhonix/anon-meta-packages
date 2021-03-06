# Dependencies for both, Anon-Gateway and Anon-Workstation #

A metapackage, which installs packages which both, Anon-Gateway
and Anon-Workstation, depend on.

Do not remove.

Package: anon-shared-packages-recommended
Architecture: all
Depends: bash-completion, command-not-found, zsh, nano, wget, dnsutils, dbus,
iputils-ping, apparmor-utils, apparmor-notify,
apparmor-profile-anondist, udisks, secure-delete, sudo, net-tools,
anon-icon-pack, gpl-sources-download, anon-iceweasel-warning,
poweroff-passwordless, power-savings-disable-in-vms, rads, scurl,
shared-folder-help, swap-file-creator, security-misc,
swappiness-lowest, tor-ctrl, uwt, knetattach-hide, openvpn, ntfs-3g,
kde-privacy, usability-misc, menu, apt-transport-tor, ${misc:Depends}
Description: Recommended packages for both, Anon-Gateway and Anon-Workstation
# Recommended packages for both, Anon-Gateway and Anon-Workstation #

A metapackage, which includes recommended packages to ensure, Debian GNU/Linux
standard tools are available and other useful recommended packages.

Safe to remove, if you know what you are doing.

Package: anon-gateway-packages-dependencies
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: tor, anon-gw-base-files, ipv4-forward-disable,
ipv6-disable, ${misc:Depends}
Conflicts: anon-workstation-packages-dependencies
Replaces: whonix-gateway-files
Description: Dependencies for Anon-Gateway
# Dependencies for Anon-Gateway #

A metapackage, which installs packages which Anon-Gateway
depends on.

Do not remove.

Package: anon-gateway-packages-recommended
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: tor-geoipdb, tor-arm, obfsproxy, obfs4proxy,
control-port-filter-python, open-link-confirmation,
${misc:Depends}
Conflicts: anon-workstation-packages-recommended
Description: Recommended packages for Anon-Gateway
# Recommended packages for Anon-Gateway #

A metapackage, which installs packages, which are recommended for
a Tor Gateway.

Safe to remove, if you know what you are doing.

Package: anon-workstation-packages-dependencies
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: anon-ws-base-files, ${misc:Depends}
Recommends: anon-workstation-packages-recommended (= ${source:Version})
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version})
Conflicts: anon-gateway-packages-dependencies
Replaces: whonix-workstation-files
Description: Dependencies for Anon-Workstation
# Dependencies for Anon-Workstation #

A metapackage, which installs packages which Anon-Workstation
depends on.

Do not remove.

Package: anon-workstation-packages-recommended
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: libasound2, alsa-base, alsa-utils, iceweasel,
xchat-improved-privacy, anon-mixmaster, anon-gpg-tweaks, anon-torchat,
pidgin-improved-privacy, anon-ws-disable-stacked-tor, tb-default-browser,
tb-starter, tb-updater, open-link-confirmation,
anon-kde-streamiso, icedove, enigmail, xul-ext-torbirdy, ${misc:Depends}
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version})
Conflicts: anon-gateway-packages-recommended
Description: Recommended packages for Anon-Workstation
# Recommended packages for Anon-Workstation #

A metapackage, which installs packages, which are recommended for
Anon-Workstation, because they are useful for a Tor Workstation.

Feel free to remove, if you know what you are doing.

Package: anon-shared-desktop
Architecture: all
Depends: libgl1-mesa-dri, xserver-xorg, upower,
xserver-xorg-video-qxl, gtk2-engines-pixbuf, ${misc:Depends}
Suggests: anon-shared-desktop-kde (= ${source:Version})
Replaces: whonix-shared-desktop
Description: Desktop Depends
# Desktop Depends #

A metapackage, which installs dependencies for desktop environments,
such as KDE, GNOME, etc.

anon-shared-desktop-kde depends on this package.

Package: anon-shared-desktop-kde
Architecture: all
Depends: anon-shared-desktop (= ${source:Version}), kde-workspace, kdm, kdesudo, kdepasswd, kfind,
ksysguard, plasma-widget-folderview, kde-baseapps-bin, polkit-kde-1, konsole, kwrite, dolphin, ark,
p7zip-full, zip, unzip, okular, khelpcenter4, ksystemlog, gtk2-engines-oxygen, gtk3-engines-oxygen,
kde-dolphin-menubar-enable, kde-kdm-autologin, kde-kgpg-tweaks, kde-konsole-unlim-scrollback,
kde-lowfat, kde-mouse-doubleclick, kde-sounds-off, kmix-disable-autostart,
plasma-widget-networkmanagement, kde-common-resolution, ${misc:Depends}
Suggests: anon-shared-kde-accessibility (= ${source:Version}),
anon-shared-desktop-langpack-kde (= ${source:Version})
Replaces: whonix-shared-desktop-kde
Description: Recommended packages for Gateway/Workstation base KDE desktop
# Recommended packages for Gateway/Workstation base KDE desktop #

A metapackage, which installs a minimal, yet complete enough
to contain the very basics, KDE desktop. The Anon-Gateway desktop and the
Anon-Workstation desktop depend on this package.

Safe to remove.

Package: anon-shared-kde-accessibility
Architecture: all
Depends: kdeaccessibility, kvkbd, kmousetool, kmag, kmouth, jovie, gnome-orca,
espeakup, ${misc:Depends}
Replaces: whonix-shared-kde-accessibility
Description: KDE accessibility tools
# KDE accessibility tools #

A metapackage, which installs accessibility tools for the KDE desktop.

If not required, can be removed, because they are not crucial for
anonymity, privacy or security.

Package: anon-workstation-default-applications
Architecture: all
Depends: xchat, vlc, mixmaster,
kcalc, gwenview, kgpg, kmix, mat, python-hachoir-core, python-hachoir-parser,
python-pdfrw, python-cairo, python-poppler, python-mutagen, libimage-exiftool-perl, gir1.2-gtk-3.0,
pinentry-qt | pinentry-gtk | pinentry-curses | pinentry, fpm2, ${misc:Depends}
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version}),
anon-workstation-langpack-common (= ${source:Version})
Replaces: whonix-workstation-default-applications
Description: Recommended default applications for Anon-Workstation
# Recommended default applications for Anon-Workstation #

A metapackage, which installs recommended default applications,
which are useful in a default installation of a Tor Workstation.

Can be removed, if not in use, because they are not crucial for anonymity,
privacy or security.

Package: anon-workstation-extra-applications
Architecture: all
Depends: ${misc:Depends}
Recommends: anon-workstation-packages-recommended (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}), shutter,
gtk-recordmydesktop, libreoffice, kdenlive, kolourpaint4
Suggests: anon-workstation-langpack-common (= ${source:Version})
Replaces: whonix-workstation-extra-applications
Description: Complements anon-workstation-default-applications
# Complements anon-workstation-default-applications #

A metapackage, which installs extra applications, to complement the
default applications.

Does not get installed by default, because extra applications
take too much space and are not required for everyone.

Package: anon-workstation-langpack-common
Architecture: all
Depends: ${misc:Depends}
Recommends: iceweasel-l10n-all | firefox-l10n-all, ttf-dejavu, ttf-liberation, locales-all,
ttf-kacst, ttf-farsiweb, scim-pinyin, scim-tables-zh, scim-uim, ttf-arphic-ukai, ttf-arphic-uming,
culmus, libfribidi0, ttf-indic-fonts, scim-anthy, ttf-khmeros, ttf-unfonts-core, ttf-lao,
ttf-thai-tlwg, xfonts-intl-chinese, xfonts-wqy, xfonts-bolkhov-koi8r-75dpi,
xfonts-bolkhov-koi8r-misc, xfonts-cronyx-koi8r-100dpi
Replaces: whonix-workstation-langpack-common
Description: Fonts and language packages for better internationalization support
# Fonts and language packages for better internationalization support #

A metapackage which installs fonts and language packages for better
internationalization support.

Does not get installed by default, because it is largely untested
and needs more work.

Package: anon-shared-desktop-langpack-kde
Architecture: all
Depends: anon-shared-desktop-kde (= ${source:Version}), ${misc:Depends}
Recommends: kde-l10n-ar, kde-l10n-bg, kde-l10n-bs,
kde-l10n-ca, kde-l10n-cavalencia, kde-l10n-cs, kde-l10n-da, kde-l10n-de, kde-l10n-el, kde-l10n-engb,
kde-l10n-es, kde-l10n-et, kde-l10n-eu, kde-l10n-fa, kde-l10n-fi, kde-l10n-fr, kde-l10n-ga,
kde-l10n-gl, kde-l10n-he, kde-l10n-hr, kde-l10n-hu, kde-l10n-ia, kde-l10n-id, kde-l10n-is,
kde-l10n-it, kde-l10n-ja, kde-l10n-kk, kde-l10n-km, kde-l10n-ko, kde-l10n-lt, kde-l10n-lv,
kde-l10n-nb, kde-l10n-nds, kde-l10n-nl, kde-l10n-nn, kde-l10n-pa, kde-l10n-pl, kde-l10n-pt,
kde-l10n-ptbr, kde-l10n-ro, kde-l10n-ru, kde-l10n-si, kde-l10n-sk, kde-l10n-sl, kde-l10n-sr,
kde-l10n-sv, kde-l10n-tg, kde-l10n-th, kde-l10n-tr, kde-l10n-ug, kde-l10n-uk, kde-l10n-vi,
kde-l10n-wa, kde-l10n-zhcn, kde-l10n-zhtw, anon-workstation-langpack-common (= ${source:Version})
Replaces: whonix-shared-desktop-langpack-kde
Description: Extra language support for the KDE desktop
# Extra language support for the KDE desktop #

A metapackage, which includes extra language support for the
KDE desktop.

Does not get installed by default, because it takes a lot of
space and requires a better solution.

Package: apparmor-profiles-whonix
Architecture: all
Depends: apparmor-profile-icedove, apparmor-profile-pidgin,
apparmor-profile-sdwdate, apparmor-profile-timesync,
apparmor-profile-torbrowser, apparmor-profile-virtualbox,
apparmor-profile-whonixcheck, apparmor-profile-xchat,
apparmor-profile-gwenview, apparmor-profile-okular, ${misc:Depends}
Description: Extra AppArmor profiles developed by the Whonix team
# Extra AppArmor profiles developed by the Whonix team #

A metapackage, which installs apparmor profiles developed by the Whonix team.

Increases security.

Safe to remove, if you know what you are doing.

Package: whonix-gateway-packages-dependencies-pre
Architecture: all
Depends: whonix-gw-network-conf, anon-gw-dns-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Gateway that changes network related files
# Dependencies for Whonix-Gateway that changes network related files #

A metapackage, which installs packages which Whonix-Gateway
depends on. Can not be merged into whonix-gateway-packages-dependencies due to
conflicts with chroot build process.

Do not remove.

Package: whonix-gateway-packages-dependencies
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: anon-gateway-packages-dependencies, anon-gw-anonymizer-config,
anon-gw-dhcp-conf, anon-gw-dns-conf, whonix-gw-firewall,
whonix-gateway-packages-dependencies-pre, ${misc:Depends}
Conflicts: whonix-workstation-packages-dependencies
Description: Dependencies for Whonix-Gateway
# Dependencies for Whonix-Gateway #

A metapackage, which installs packages which Whonix-Gateway
depends on.

Do not remove.

Package: whonix-gateway-packages-recommended
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: anon-gw-kde-startmenu, whonix-gw-desktop-shortcuts,
whonix-gw-kde-desktop-conf, ${misc:Depends}
Recommends: anon-gateway-packages-recommended
Conflicts: whonix-workstation-packages-recommended
Description: Recommended packages for Whonix-Gateway
# Recommended packages for Whonix-Gateway #

A metapackage, which installs packages, which are recommended for
Whonix-Gateway.

Safe to remove, if you know what you are doing.

Package: whonix-shared-packages-dependencies
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-base-files, anon-apt-sources-list,
whonix-initializer, whonixsetup, whonix-repository, grub-enable-apparmor,
${misc:Depends}
Description: Dependencies for Whonix-Gateway and Whonix-Workstation
# Dependencies for Whonix-Gateway and Whonix-Workstation #

A metapackage, which installs packages which both, Whonix-Gateway
and Whonix-Workstation, depend on.

Do not remove.

Package: whonix-shared-packages-recommended
Architecture: all
Depends: anon-shared-packages-recommended, whonixcheck, whonix-setup-wizard,
${misc:Depends}
Description: Recommended packages for Whonix-Gateway and Whonix-Workstation
# Recommended packages for Whonix-Gateway and Whonix-Workstation #

A metapackage, which includes recommended packages to ensure, Whonix
standard tools are available and other useful recommended packages.

Safe to remove, if you know what you are doing.

Package: whonix-workstation-packages-dependencies-pre
Architecture: all
Depends: whonix-ws-network-conf, anon-ws-dns-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Workstation that changes network related files
# Dependencies for Whonix-Workstation that changes network related files #

A metapackage, which installs packages which Whonix-Workstation
depends on. Can not be merged into whonix-workstation-packages-dependencies
due to conflicts with chroot build process.

Do not remove.

Package: whonix-workstation-packages-dependencies
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: whonix-ws-firewall, whonix-workstation-packages-dependencies-pre,
${misc:Depends}
Recommends: whonix-workstation-packages-recommended (= ${source:Version})
Conflicts: whonix-gateway-packages-dependencies
Description: Dependencies for Whonix-Workstation
# Dependencies for Whonix-Workstation #

A metapackage, which installs packages which Whonix-Workstation
depends on.

Do not remove.

Package: whonix-workstation-packages-recommended
Architecture: all
Depends: anon-ws-kde-startmenu,
whonix-ws-desktop-shortcuts, whonix-ws-irc-chat-support,
whonix-ws-kde-desktop-conf, whonix-ws-start-menu-additions,
whonix-welcome-page, ${misc:Depends}
Recommends: anon-workstation-packages-recommended
Description: Recommended packages for Whonix-Workstation
# Recommended packages for Whonix-Workstation #

A metapackage, which installs packages, which are recommended for
Whonix-Workstation, because they are useful for a Tor Workstation.

Feel free to remove, if you know what you are doing.

Package: whonix-gateway
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-gateway-packages-dependencies-pre,
anon-shared-build-upgrade-torsocks,
anon-shared-build-log-build-version,
anon-shared-build-remember-sources,
anon-shared-build-ban-nonfree,
anon-shared-build-sanity-checks,
anon-shared-packages-dependencies,
anon-shared-packages-recommended,
anon-shared-desktop,
anon-shared-desktop-kde,
anon-shared-kde-accessibility,
whonix-shared-packages-dependencies,
whonix-shared-packages-recommended,
anon-gw-build-upgrade-tor,
anon-gateway-packages-dependencies,
anon-gateway-packages-recommended,
whonix-gateway-packages-dependencies,
whonix-gateway-packages-recommended,
${misc:Depends}
Description: Whonix Default Gateway
# Whonix Default Gateway #

A metapackage, which installs packages, for a Whonix-Default-Gateway.

It will install build chroot scripts, but not run them.

Feel free to remove, if you know what you are doing.

Package: whonix-workstation
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-workstation-packages-dependencies-pre,
anon-shared-build-upgrade-torsocks,
anon-shared-build-log-build-version,
anon-shared-build-remember-sources,
anon-shared-build-ban-nonfree,
anon-shared-build-sanity-checks,
anon-shared-packages-dependencies,
anon-shared-packages-recommended,
anon-shared-desktop,
anon-shared-desktop-kde,
anon-shared-kde-accessibility,
whonix-shared-packages-dependencies,
whonix-shared-packages-recommended,
anon-shared-build-inst-tb,
anon-workstation-packages-dependencies,
anon-workstation-packages-recommended,
anon-workstation-default-applications,
whonix-workstation-packages-dependencies,
whonix-workstation-packages-recommended,
${misc:Depends}
Description: Whonix Default Workstation
# Whonix Default Workstation #

A metapackage, which installs packages, for a Whonix-Default-Workstation.

It will install build chroot scripts, but not run them.

Feel free to remove, if you know what you are doing.

Package: anon-host-additions
Architecture: all
Depends: anon-shared-build-upgrade-torsocks,
anon-shared-build-log-build-version,
anon-shared-build-remember-sources,
anon-shared-build-ban-nonfree,
anon-shared-build-sanity-checks,
anon-shared-packages-dependencies,
anon-shared-packages-recommended,
whonix-shared-packages-dependencies,
whonix-shared-packages-recommended,
anon-shared-build-inst-tb,
${misc:Depends}
Description: Host Additions for Anon Host Operating Systems
# Host Additions for Anon Host Operating Systems #

A metapackage, which installs packages, for a Anon host operating system.

Supposed to be installed on operating systems that host anonymity preserving
software (such as whonix-host-virtualbox or whonix-host-qemu-kvm) for better
anonymity, privacy, security and usability.

It will install build chroot scripts, but not run them.

Feel free to remove, if you know what you are doing.

Package: whonix-host-additions
Architecture: all
Depends: anon-host-additions, whonix-host-firewall, ${misc:Depends}
# whonix-host-packages-dependencies-pre,
Description: Packages for Whonix Hosts
# Packages for Whonix Hosts #

A metapackage, which installs packages Whonix Host Additions.

Supposed to be installed on hosts that run Whonix inside virtual machines,
such as VirtualBox, QEMU or KVM. Installs anon-host-additions and Whonix Host
Firewall. For better anonymity, privacy, security and usability.

Feel free to remove, if you know what you are doing.

Package: whonix-host-shared-dependencies
Architecture: all
Depends: whonix-host-additions, anon-shared-desktop, anon-shared-desktop-kde,
anon-shared-kde-accessibility, ${misc:Depends}
# whonix-host-packages-dependencies-pre
Description: Whonix Host Shared
# Whonix Host Shared #

A metapackage, which installs packages, for a Whonix host operating system.

Supposed to be installed on systems that host Whonix or Whonix hosts.

Feel free to remove, if you know what you are doing.

Package: whonix-host-virtualbox
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-host-shared, virtualbox, ${misc:Depends}
Suggests: apparmor-profile-virtualbox
Description: Whonix Host Packages for VirtualBox Hosts
# Whonix Host Packages for VirtualBox Hosts #

A metapackage, which installs packages, for a Whonix host operating system
using VirtualBox.

Feel free to remove, if you know what you are doing.

Package: whonix-host-qemu-kvm
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-host-shared, qemu-kvm, libvirt-bin, virt-manager,
whonix-libvirt, ${misc:Depends}
Suggests: ksm
Description: Whonix Host Packages for QEMU or KVM hosts
# Whonix Host Packages for QEMU or KVM hosts #

A metapackage, which installs packages, for a Whonix host operating system
using KVM or QEMU.

Feel free to remove, if you know what you are doing.

(This package description has been [automatically](https://github.com/Whonix/whonix-developer-meta-files/blob/master/debug-steps/packaging-helper-script) extracted and mirrored from `debian/control`.)

# Generic Readme #
## Readme Version ##

[Generic Readme](https://github.com/Whonix/whonix-developer-meta-files/blob/master/README_generic.md) Version 0.3

## Cooperating Anonymity Distributions ##

[Generic Readme](https://github.com/Whonix/whonix-developer-meta-files/blob/master/README_generic.md) beings here. Have a look into the `man` sub folder (if available).

The functionality of this package was once exclusively available in the [Whonix](https://www.whonix.org) ([github](https://github.com/Whonix/Whonix)) anonymity distribution.

Because multiple projects and individuals stated interest in various of Whonix's functionality (examples: [Qubes OS](http://qubes-os.org/trac) ([discussion](https://groups.google.com/forum/#!topic/qubes-devel/jxr89--oGs0)); [piratelinux](https://github.com/piratelinux) ([discussion](https://github.com/adrelanos/VPN-Firewall/commit/6147f0e606377f5a801e98daf22e24ba2c750a21#commitcomment-6360713))), it's best to share as much source code as possible, it's best to share certain characteristics [(such as /etc/hostname etc.) among all anonymity distributions](https://mailman.boum.org/pipermail/tails-dev/2013-January/002457.html)) Whonix has been split into [multiple separate packages](https://github.com/Whonix).

## Generic Packaging ##

Files in `etc/...` in root source folder will be installed to `/etc/...`, files in `usr/...` will be installed to `/usr/...` and so forth. This should make renaming, moving files around, packaging, etc. very simple. Packaging of most packages looks very similar.

## How to use outside of Debian or derivatives ##

Although probably due to generic packaging not very hard. Still, this requires developer skills. [Ports](https://en.wikipedia.org/wiki/Porting) welcome!

## How to Build deb Package ##

See comments below and [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

* Replace `apparmor-profile-torbrowser` with the actual name of this package (equals the root source folder name of this package after you git cloned it).
* You only need [config-package-dev](https://packages.debian.org/wheezy/config-package-dev), when it is listed in the `Build-Depends:` field in `debian/control`.
* Many packages do not have signed git tags yet. You may request them if desired.
* We might later use a [documentation template](https://www.whonix.org/wiki/Template:Build_Documentation_Build_Package).

## How to install in Debian using apt-get ##

Binary packages are available in Whonix's APT repository. By no means you are required to use the binary version of this package. This might be interesting for users of Debian and derivatives. **Note, that usage of this package outside of Whonix is untested and there is no maintainer that supports this use case.**

1\. Get [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

2\. Add Whonix's Signing Key to apt-key.

```
gpg --export 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA | sudo apt-key add -
```

3\. Add Whonix's APT repository.

```
echo "deb http://sourceforge.net/projects/whonixdevelopermetafiles/files/internal/ wheezy main" > /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install this package. Replace `package-name` with the actual name of this package.

```
sudo apt-get install package-name
```

## Cooperation ##

Most welcome. [Ports](https://en.wikipedia.org/wiki/Porting), distribution maintainers, developers, patches, forks, testers, comments, etc. all welcome.

## Contact ##

* Professional Support: https://www.whonix.org/wiki/Support#Professional_Support
* Free Forum Support: https://www.whonix.org/forum
* Github Issues
* twitter: https://twitter.com/Whonix

## Donate ##

* [Donate](https://www.whonix.org/wiki/Donate)
