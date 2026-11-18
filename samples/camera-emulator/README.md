# Camera emulator (Raspberry Pi 5 / Rock 5B)

A Linux board that a PC sees as a USB (UVC) or GigE Vision camera, playing a recorded video frame by frame. The application under test uses its normal camera driver and cannot tell the difference from the real device.

**Needs:** A Raspberry Pi 5 or Rock 5B for the USB camera; any Linux board or PC for the GigE camera.

**Download:** [camera-emulator.zip](../../../../releases/download/sample-camera-emulator/camera-emulator.zip)
(made automatically from this folder, see below).

**Read with it:** the APIC Help pages `samples.html#camera-emulator` and `setup-uvcgadget.html`.

## Contents

| Path | What |
|---|---|
| `project/config.json` | CoreEngine configuration |
| `project/Setups/streams.json` | Streams and drivers |
| `project/Models/` | The models (C++) |
| `project/ICD/` | The ICD the database is generated from |
| `project/CMakeLists.txt` | Build |

## Run it

1. Unpack the zip into your projects folder.
2. Open the `project` folder in APICCenter (or `project/CMakeLists.txt` in Visual Studio) and build it.
3. Check the addresses, ports and serial port names in `project/Setups/streams.json` against your own computer.
4. Run it and open DIPanel to see the blocks change.

## For the maintainer

Put the project files in `project/` (the empty `.gitkeep` file can stay or go) and push.
The workflow `.github/workflows/sample-downloads.yml` then zips this folder (this README + `project/`)
into `camera-emulator.zip` and publishes it as the release `sample-camera-emulator`, replacing the previous zip.
While `project/` has no files, no zip is made and the Help shows "Coming soon" for this sample.

Leave out: build output (`out/`, `build/`, `bin/`, `obj/`), `.vs/`, large recordings, and anything you may not share.
