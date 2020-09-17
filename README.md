# epsoscanify

### Test results

Branches  | Windows | Test coverage | Security analysis |
----------|---------|---------------|-------------------|
Master:   | [![Build status](https://ci.appveyor.com/api/projects/status/624byor4rcntugg5?svg=true)](https://ci.appveyor.com/project/m7b/epsoscanify) | -  | - 


### About

This repo is about using the Epson BX925FWD / Work Force 840 as a PDF scanner
with OCR via NAPS2.

### Setup steps

1. Update firmware (not mandatory) and drivers for the epson device
   ([EPSON driver update page](https://epson.com/Support/Printers/All-In-Ones/WorkForce-Series/Epson-WorkForce-840/s/SPT_C11CA97201)).
   
   - Recovery Mode Firmware (for firmware upgrade, optional)
   - Scanner Driver and EPSON Scan Utility
   - Epson Event Manager

2. Install NAPS2 ([Link](https://www.naps2.com/))

3. Expand the environment variable `PATH` with the installation folder of
   NAPS2. So that windows can find the `NAPS2.Console.exe` command.

4. Enable OCR with support for preferred language. For this open command promt
   and execute following commands:
   
   ```batch
   NAPS2.Console --install generic-import
   NAPS2.Console --install ocr-eng
   NAPS2.Console --install ocr-deu
   ```