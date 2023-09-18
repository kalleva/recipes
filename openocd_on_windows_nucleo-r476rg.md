1. Download [OpenOCD binaries](https://gnutoolchains.com/arm-eabi/openocd/)
and add ```openocd/bin``` folder to the Path Environment variable.

2. Create ```openocd.cfg``` in the project with this content:
```
telnet_port 4444
gdb_port 3333
source [find board/st_nucleo_l476rg.cfg]
```

3. Start ```openocd```.

4. Connect to the session via socket with ```telnet localhost 4444```

5. Commands to flash image:
```
init
halt
flash probe 0
flash info 0
flash erase_sector 0 0 511 # Without this there would be an error
flash write_image ./image.bin 0x08000000
```
