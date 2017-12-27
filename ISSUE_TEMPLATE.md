Make sure you have provided the following information:

 - [x] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
   igelboot/shim-review@igel.com-shim-amd64-20171227
 - [x] completed README.md file with the necessary information
 - [x] shim.efi to be signed
 - [x] any extra patches to shim via your own git tree or as files
 - [x] any extra patches to grub via your own git tree or as files
 - [x] build logs


###### What organization or people are asking to have this signed:
IGEL Technology GmbH
Hermanstr. 17
86150 Augsburg, 
Germany

https://www.igel.com/

IGEL Technology is a member of the Melchers group.
Managing Directors: Heiko Gloge and Nicolas C. S. Helms
District Court Bremen (Germany) HRB 20636, VAT: DE 219524359, WEEE-Reg.-No. DE 79295479

IGEL is a vendor of thin client hardware and software.

###### Version of shim:
https://github.com/rhboot/shim/tree/13
rhboot/shim@13

###### Sysdev Submission ID:
UEFI submission #1973560

###### What product or service is this for:
This is for IGEL's Linux-based thin client operating system, which is called IGEL OS. There are three products based on IGEL OS:

- IGEL OS (LX), the operating system for IGEL's own thin client devices
- Universal Desktop Converter 3 (UDC3), a live-bootable Linux system that installs IGEL OS on third-party devices
- UD Pocket, a live-bootable variant of IGEL OS on a pen drive

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
- IGEL wants to employ Secure Boot for building a trusted operating system from Shim to GRUB to the kernel to signed filesystem partitions. Secure Boot is the first step for this.
- IGEL would like customers to be able to run Universal Desktop Converter 3 (UDC3) on any amd64 device without disabling Secure Boot.
- IGEL would like UD Pocket to be bootable on any amd64 device without disabling Secure Boot.


