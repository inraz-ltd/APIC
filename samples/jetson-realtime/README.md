# Real-time application on NVIDIA Jetson

A CoreEngine application running in real time on an NVIDIA Jetson board.

**Needs:** An NVIDIA Jetson board with Linux.

**Download:** [jetson-realtime.zip](../../../../releases/download/sample-jetson-realtime/jetson-realtime.zip)
(made automatically from this folder, see below).

**Read with it:** the APIC Help pages `samples.html#jetson-realtime` and `setup-linux.html`.

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
into `jetson-realtime.zip` and publishes it as the release `sample-jetson-realtime`, replacing the previous zip.
While `project/` has no files, no zip is made and the Help shows "Coming soon" for this sample.

Leave out: build output (`out/`, `build/`, `bin/`, `obj/`), `.vs/`, large recordings, and anything you may not share.
