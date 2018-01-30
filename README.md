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
https://github.com/rhboot/shim/tree/14

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/igelboot/shim/tree/igel-shim

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
Please see https://github.com/igelboot/shim/commits/igel-shim

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
- Ubuntu 16.04 LTS Xenial Xerus
- gcc: 4:5.3.1-1ubuntu1
- binutils: 2.26.1
- gnu-efi: 3.0.2-1ubuntu1
see also file shim_igelbuild_20180126_150135.log

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
84b291682febed26e7df144a67c4feda0755fa14e2bf9296c5df1fa9d20141b2 *bootia32.efi
e25f512d2971a4b3a881cc1306677b11badcc8360ae4f1d9999a4a64467df3e8 *bootx64.efi

-------------------------------------------------------------------------------
CAB archive submitted to Microsoft:
-------------------------------------------------------------------------------
UEFI submission #1974022
3be1e9b8531c72872ae8bacad38a1e06cff783f033cde53b2cbec672c6f62342 *shim_igelbuild_20180126_150135.cab
