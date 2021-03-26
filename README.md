# Hackintosh-Dell-g3-15-3590<br>
<br>
specs<br>
-------<br>
• Processor : 9th Generation Intel®️ Core™️ i7 -9750H (12MB Cache, up to 4.5 GHz, 6 cores) <br>
• iGPU : Intel UHD 630. <br>
• dGPU :  NVIDIA(R) GeForce(R) GTX 1660 Ti with Max-Q Design, 6GB GDDR 6. <br>
• RAM : 16GB, 2x8GB, DDR4 (2666MHz) <br>
• Storage : 256GB M.2 PCIe NVMe Solid Stat e Drive (Boot) + 1TB 5400 rpm 2.5" SATA Hard Drive (Storage). <br>
• Audio Codec : Realtek ALC295. <br>
• WIFI: Intel AC9560. <br>
• Touchpad : I2C HID TPD0<br>
• Monitor Resolution : 15.6 inch FHD (1920 x 1080) 30 0 nits IPS Anti-Glare LED Back lit Display with 144Hz refresh rate,<br>
• Bios Version : 1.12.0 .<br>
• Boot Mode : UEFI .<br>


•Open Core version : r0.6.8<br>
•OS Version : macOS BigSur 11.2.3,<br>

<br>
What is working<br>
------------------<br>

• QE/CI Graphics Intel UHD 630 <br>
• Restart, Sleep and Shutdown (With and without Closing LID) <br>
• CPU Power Management <br>
• Internal speaker , headphone (with microphone) <br>
• Touchpad (SSDT Patche Interrupt GPIO Pinning) 'note that acpibattery.kext causes touchpad lag , use smcbatterymanager.kext' <br>
• Brightness (including f11 and f12) <br>
• Battery Indicator <br>
• Ethernet  
• Wifi <br>
• Bluetooth <br>
• All USB Port (including usb type c) <br>
• External Monitor work with type c cable

not working<br>
--------------<br>
• internal microphone (Smart Sound Technology is not supported by mac)<br>
• awaking from sleep needs some keyboard presses (acpi_wake_type did not fix it)


-----------------------------------------------------------------------------------------------------------------------------

* for better power saving replace the CPUFriendDataProvider.kext from better power management directory in this repo into the kexts
  forlder on OC/Kexts (note that it saves the battery but on the other hand it gives you less performance so i recommend using the one inside the oc )
* to make the native wifi icon work enable AirportItlwm.kext in config.plist and disable the Itlwm.kext one, but note that AirportItlwm is not working with hidden networks till now, if you want connection with hidden netowrks use Itlwm.kext + heliport.app(included in wifi directory)
