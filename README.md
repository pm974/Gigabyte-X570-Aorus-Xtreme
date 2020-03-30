# Gigabyte-X570-Aorus-Xtreme
OC - Gigabyte-X570-Aorus-Xtreme_rev1.0 - GC-Titan Ridge (NVM23E64fr)

This is my OC folder for Gigabyte-X570-Aorus-Xtreme_rev1.0 running Mac OS X Catalina 10.15.4 running n-d-k Opencore 0.5.7<br>
Part of the SSDTs consists in patching USB (XHC0, XHC1, XHC2, XHCI & HXC4 for SSP1 & SSP2 on the GC-Titan Ridge PCIe Thunderbolt3 card.<br>
• Proper Shutdown needs to be fixed in SSDT-X570-TB3-TTR.aml as it's lost when loaded.<br>

Thunderbolt is now working 90% : I mixed iGPUs SSDT : SSDT-X570-Cr-TB3-GPP9-TR-slot-4.aml and some SSDT-Z370-TB3-TTR.aml found on the web :<br>
• started from SSDT-Z370-TB3-TTR.aml / renamed to SSDT-X570-TB3-TTR.aml<br>
• replaced RP21 by GPP9<br>
• added NTFY method from SSDT-X570-Cr-TB3-GPP9-TR-slot-4<br>
• renamed PXSX to D014 (like in SSDT-X570-Cr-TB3-GPP9-TR-slot-4)<br>
• replaced NHI Device with SSDT-X570-Cr-TB3-GPP9-TR-slot-4 one<br>

Credits goes to :<br>
• CaseySJ / iGPU / AlGreyy / AlGreyy / n-d-k<br>
