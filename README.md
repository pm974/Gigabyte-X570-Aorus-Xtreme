# Gigabyte-X570-Aorus-Xtreme
OC - Gigabyte-X570-Aorus-Xtreme_rev1.0 - GC-Titan Ridge (NVM23E64fr)

These are my OC folders for Gigabyte-X570-Aorus-Xtreme_rev1.0<br>
I'm currently running Mac OS X Mojave 10.14.6 on n-d-k Opencore 0.5.7 but you will also find a 10.15.4 compatible EFI mirrored to the other except for AMD patches<br>

Part of the SSDTs consists in patching USB (XHC0, XHC1, XHC2, XHCI & HXC4 for SSP1 & SSP2 on the GC-Titan Ridge PCIe Thunderbolt3 card.<br>
• Proper Shutdown needs to be fixed in SSDT-X570-TB3-TTR.aml as it's lost when loaded.<br>

Thunderbolt is now working 90% : I mixed iGPUs SSDT : SSDT-X570-Cr-TB3-GPP9-TR-slot-4.aml and some SSDT-Z370-TB3-TTR.aml found on the web :<br>
• started from SSDT-Z370-TB3-TTR.aml / renamed to SSDT-X570-TB3-TTR.aml<br>
• replaced RP21 by GPP9<br>
• added NTFY method from SSDT-X570-Cr-TB3-GPP9-TR-slot-4<br>
• renamed PXSX to D014 (like in SSDT-X570-Cr-TB3-GPP9-TR-slot-4)<br>
• replaced NHI Device with SSDT-X570-Cr-TB3-GPP9-TR-slot-4 one<br>

03/04/2020<br>
Created V2 updates

• V2 System Definition MacPro7,1 changed to iMacPro for 10.13 (not tested) 10.14 compatibility (tested on 10.14.6)<br>

• Created two versions for AMD patches<br>
-EFI_V2_10.14.6_10.15.3 with proper Ryzen 3rd gen AMD patches<br>
-EFI_V2_10.15.4 with updated Ryzen 3rd gen AMD patches (10.15.4 changes in config.plist to Kernel/patches)<br>

• USB fixes<br>
- removed ACPI "SSDT-X570-BXBR_BYUP_BYD8_XHCI.aml"<br>
- added "SSDT-X570-XHC1_XHCI.aml" // Still needs improvements.<br>
- Updated ports adresses & type in "SSDT-X570-GP13_XHC2" // Still needs improvements.<br>
- Updated ports in "USBPorts-X570-Gb-AorusXtreme-PCIe_BT.kext" and updated to match iMacPro System Definition.<br>

• GC-Titan Ridge USB SSP1 & SSP2 adresses fixed to 0x03 and 0x04 and removal of HS ports.<br>

Credits goes to :<br>
CaseySJ / iGPU / AlGreyy / AlGreyy / n-d-k<br>
