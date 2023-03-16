Flash Download Tools for Windows
https://www.espressif.com/en/products/hardware/esp32/resources

SPI 
SPI Speed: 40Mhz
Flash size of your module
CrystalFreq: 40M

bootloader.bin 				0x1000
partitions_singleapp.bin 	0x8000
dronebridge_esp32.bin		0x10000
-------------------------------------------------------------------


Alternative: Can be flashed using the esptool.py by Espressif:

python esp-idf/components/esptool_py/esptool/esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 115200 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 40m --flash_size detect 0x1000 bootloader.bin 0x10000 dronebridge_esp32.bin 0x8000 partitions_singleapp.bin

Make sure you set the port correctly!
