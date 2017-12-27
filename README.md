-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
IGEL Technology GmbH
Hermanstr. 17
86150 Augsburg, 
Germany

https://www.igel.com/

IGEL Technology is a member of the Melchers group.
Managing Directors: Heiko Gloge and Nicolas C. S. Helms
District Court Bremen (Germany) HRB 20636, VAT: DE 219524359, WEEE-Reg.-No. DE 79295479

IGEL is a vendor of thin client hardware and software.

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
This is for IGEL's Linux-based thin client operating system, which is called IGEL OS. There are three products based on IGEL OS:

- IGEL OS (LX), the operating system for IGEL's own thin client devices
- Universal Desktop Converter 3 (UDC3), a live-bootable Linux system that installs IGEL OS on third-party devices
- UD Pocket, a live-bootable variant of IGEL OS on a pen drive

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
- IGEL wants to employ Secure Boot for building a trusted operating system from Shim to GRUB to the kernel to signed filesystem partitions. Secure Boot is the first step for this.
- IGEL would like customers to be able to run Universal Desktop Converter 3 (UDC3) on any amd64 device without disabling Secure Boot.
- IGEL would like UD Pocket to be bootable on any amd64 device without disabling Secure Boot.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Mathias Huber
- Position: Product Manager and Technical Writer
- Email address: mathias.huber@igel.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
  https://pgp.mit.edu/pks/lookup?op=get&search=0xF4DB2ED8A66078F9
  PGP key fingerprint: 060F 4DFB C57B 0073 2DD7  F6B0 F4DB 2ED8 A660 78F9

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Jürgen Schneider
- Position: Manager Linux Development
- Email address: schneider.juergen@igel.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
  https://pgp.mit.edu/pks/lookup?op=get&search=0x26712F2479D12581
  PGP key fingerprint: 88EF 7505 7F1E C22E CF05  8162 2671 2F24 79D1 2581

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/13
rhboot/shim@13

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/igelboot/shim/tree/igel.com-shim-amd64-20171220
igelboot/shim@igel.com-shim-amd64-20171220

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
commit 35f3c2a77315fba2f753bab909c618a44d126c9c
Author: Mathias Huber <mathias.huber@igel.com>
Date:   Wed Dec 20 13:17:13 2017 +0100

    Make modifications for IGEL OS 10
    
        Makefile: Use only the sections IGEL needs
    
        shim.c: Never use fallback image
                Never use MOK_MANAGER

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
- Ubuntu 16.04 LTS Xenial Xerus
- gcc: 4:5.3.1-1ubuntu1
- binutils: 2.26.1
- gnu-efi: 3.0.2-1ubuntu1
see also file shim_igelbuild_20171220_141246.log

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
shim_igelbuild_20171220_141246.log

-------------------------------------------------------------------------------
Put info about what bootloader you're using, including which patches it includes to enforce Secure Boot here:
-------------------------------------------------------------------------------
grub2_2.02~beta3-4
For patches please see file grub2_2.02~beta3-4-igel-r120.diff

-------------------------------------------------------------------------------
Put info about what kernel you're using, including which patches it includes to enforce Secure Boot here:
-------------------------------------------------------------------------------
linux-4.10.x
For patches please see file linux-4.10.x-igel-r1938.diff

-------------------------------------------------------------------------------
Files to be signed:
-------------------------------------------------------------------------------
bootia32.efi sha256sum: 4ed787e32214af6007a89e41147b179d8df2cbfac7aa84d71f5d49c3b2396e48
bootx64.efi sha256sum: df4936510cfec1a56953feefc82ccd7d043d0248d9325de46348b39218ab971e

-------------------------------------------------------------------------------
CAB archive submitted to Microsoft:
-------------------------------------------------------------------------------
UEFI submission #1973560
boot.cab sha256sum: 518998c5b75ee6a001402691f4491b8ec4dba957a97a9f84f71459c9b9cfe9eb
