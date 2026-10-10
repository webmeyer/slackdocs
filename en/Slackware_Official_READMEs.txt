====== Slackware Official READMEs ======

Did you know that a good source of information about Slackware is located right on the DVD (or the FTP server)?

Lots of people realize only later (sometimes years after starting with Slackware) that the root of the distribution tree contains several text files containing information about the distro, the layout of the DVD's content and instructions about installing and configuring the software. A shame, since they contain invaluable information for setting up a Slackware system.

Let's start with a listing of these files as they appear on the Slackware 14.1 DVD: <code>
ANNOUNCE.14_1
BOOTING.TXT
CHANGES_AND_HINTS.TXT
CHECKSUMS.md5
CHECKSUMS.md5.asc
COPYING
COPYING3
COPYRIGHT.TXT
CRYPTO_NOTICE.TXT
ChangeLog.txt
FILELIST.TXT
GPG-KEY
PACKAGES.TXT
README.TXT
README.initrd
README_CRYPT.TXT
README_LVM.TXT
README_RAID.TXT
README_UEFI.TXT
RELEASE_NOTES
SPEAKUP_DOCS.TXT
SPEAK_INSTALL.TXT
Slackware-HOWTO
UPGRADE.TXT
isolinux/README.TXT
source/README.TXT
usb-and-pxe-installers/README_PXE.TXT
usb-and-pxe-installers/README_USB.TXT
</code>

What's contained in these files?

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/ANNOUNCE.14_1|ANNOUNCE.14_1]]\\ The official announcement of the release, describing existing and new features and offering information about purschasing the DVD (this particular file is for Slackware 14.1).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/BOOTING.TXT|BOOTING.TXT]]\\ The various ways of booting the Slackware installer that contains the setup program, and tips for troubleshooting if the boot fails.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHANGES_AND_HINTS.TXT|CHANGES_AND_HINTS.TXT]]\\ A listing of all new, and removed, packages relative to the previous release. Also contains tips and tricks about setting up various parts of the distro.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHECKSUMS.md5|CHECKSUMS.md5]]\\ MD5 message digests for the files in the distribution. To test all files, use this command: <code>
tail +13 CHECKSUMS.md5 | md5sum -c --quiet - | less
</code> Every line that does not say "OK" indicates a corrupted file.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHECKSUMS.md5.asc|CHECKSUMS.md5.asc]]\\ The GPG signature of the CHECKSUMS.md5 file (signed with the [[http://ftp.slackware.com/pub/slackware/slackware-current/GPG-KEY|GPG key of the Slackware Linux Project]]). It allows you to verify that the checksum values in CHECKSUMS.md5 are not manipulated by malicious 3rd parties. The following command: <code>
gpg --verify  CHECKSUMS.md5.asc
</code> should at least contain lines like these two: <code>
gpg: Signature made Thu 11 Dec 2014 02:46:15 AM CET using DSA key ID 40102233
gpg: Good signature from "Slackware Linux Project <security@slackware.com>"
</code>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYING|COPYING]]\\ Contains a copy of the ''GNU GENERAL PUBLIC LICENSE, Version 2, June 1991''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYING3|COPYING3]]\\ Contains a copy of the ''GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYRIGHT.TXT|COPYRIGHT.TXT]]\\ This is the Slackware COPYRIGHT file.  This file provides documentation about many of the licenses used by components included in Slackware, as well as some acknowledgements (some required, some freely given). Some packages will have their license file in the respective subdirectory of ''/usr/doc''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CRYPTO_NOTICE.TXT|CRYPTO_NOTICE.TXT]]\\ Legal notice, due to U.S. Exports Regulations.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/ChangeLog.txt|ChangeLog.txt]]\\ The log of all updates to the release, made since the announcement of the previous release. Sort of Pat's own blog :-)

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/FILELIST.TXT|FILELIST.TXT]]\\ The list of all files that are contained in the directory tree for this release.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/GPG-KEY|GPG-KEY]]\\ The public key corresponding to the private key with which all Slackware packages are signed: <code>
security@slackware.com public key

pub   1024D/40102233 2003-02-26 [expires: 2038-01-19]
uid                  Slackware Linux Project <security@slackware.com>
sub   1024g/4E523569 2003-02-26 [expires: 2038-01-19]
</code>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/PACKAGES.TXT|PACKAGES.TXT]]\\ Details on the Slackware packages found in the ''./slackware*/'' directory (package description, metadata and content-listing).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README.TXT|README.TXT]]\\ Slackware's README.TXT meaning **READ THIS FIRST!**.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README.initrd|README.initrd]]\\ //Slackware initrd mini HOWTO//, describing how to create and install an initrd, which may be required to use the 3.x kernel.  Also see "man mkinitrd".

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_CRYPT.TXT|README_CRYPT.TXT]]\\ The HOWTO for installing Slackware on (LUKS-) encrypted volumes.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_LVM.TXT|README_LVM.TXT]]\\ The HOWTO for installing Slackware on logical volumes (LVM).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_RAID.TXT|README_RAID.TXT]]\\ The HOWTO for installing Slackware on a software RAID root filesystem.

  * [[http://ftp.slackware.com/pub/slackware/slackware64-current/README_UEFI.TXT|README_UEFI.TXT]]\\ How to install Slackware (optionally leaving a Windows installation intact) on a computer with UEFI instead of old-fashioned BIOS. Only for 64-bit OS.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/RELEASE_NOTES|RELEASE_NOTES]]\\ This file contains Pat's personal notes on the just-completed development towards the stable release.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/SPEAKUP_DOCS.TXT|SPEAKUP_DOCS.TXT]]\\ Documentation for the Speakup speech synth software.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/SPEAK_INSTALL.TXT|SPEAK_INSTALL.TXT]]\\ HOWTO on installing with assistance of Speakup speech synthesis.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/Slackware-HOWTO|Slackware-HOWTO]]\\ Instructions for installing Slackware from CD/DVD. //If you're new to Slackware, start with this//.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/UPGRADE.TXT|UPGRADE.TXT]]\\ Slackware Upgrade HOWTO explains how to upgrade from one stable Slackware release to the next.
<note tip>You can use ''[[slackware:slackpkg|slackpkg]]'' in order to largely automate this process</note>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/isolinux/README.TXT|isolinux/README.TXT]]\\ How to burn a Bootable Slackware disc.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/source/README.TXT|source/README.TXT]]\\ Some information about the source used for this Slackware release.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/usb-and-pxe-installers/README_PXE.TXT|usb-and-pxe-installers/README_PXE.TXT]]\\ The HOWTO for installing Slackware over the network using PXE boot.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/usb-and-pxe-installers/README_USB.TXT|usb-and-pxe-installers/README_USB.TXT]]\\ The HOWTO for installing Slackware using a bootable USB stick.

The links for the above files point to the "slackware-current" directory tree on the FTP server. Slackware-current is the development release, which means that the links point to the most recent version of the file. If you want a version for a specific release instead, just change the word "'current'" in the URL to a release version like "''13.37''" or "''14.1''". The files are identical for the 32-bit and 64-bit versions of Slackware.

====== Sources ======
  * Originally written by [[wiki:user:alienbob|Eric Hameleers]]
<!-- * Contrbutions by [[wiki:user:yyy | User Y]] -->

<!-- Please do not modify anything below, except adding new tags.-->
{{tag>slackware}}
