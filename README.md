# my_klipper
printer.cfg - /home/pi/printer.cfg
Klipper - /home/pi/klipper

To get serial ports for printer.cfg
  ls /dev/serial/by-id/*
With BTT Mini E3 board that needs to load firmware from sd card as firmware.bin
  The serial port list needs to be run again and printer.cfg updated as it will have change from the value after make

If using VS Code remote development to load printer.cfg
  check permissions
  ls -la
  update permissions
    chmod 644 printer.cfg
  if file still cannot be read
    mv printer.cfg Xprinter.cfg  -- this will rename the file
    cp Xprinter.cfg printer.cfg  -- will make a copy that is now readable Can now delete Xprinter.cfg
    
BL Touch probe as Z must all connect to probe port
  none connected to Z stop as in Marlin
  My BL Touch wiring
    Signal  Blk
    Ground  Blu
    Signal  Grn
    +5 V    Yel
    Ground  Org

