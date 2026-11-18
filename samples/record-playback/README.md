# Recording and playback of synchronized sensor data

IMU, INS and camera data recorded together, played back in the CoreEngine so the models run on exactly the recorded data, and shown in the recording viewer.

**Needs:** Nothing to play the included recording; the sensors and a camera to record your own.

**Download:** [record-playback.zip](../../../../releases/download/sample-record-playback/record-playback.zip)
(made automatically from this folder, see below).

**Read with it:** the APIC Help pages `samples.html#record-playback` and `recording.html`.

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
into `record-playback.zip` and publishes it as the release `sample-record-playback`, replacing the previous zip.
While `project/` has no files, no zip is made and the Help shows "Coming soon" for this sample.

Leave out: build output (`out/`, `build/`, `bin/`, `obj/`), `.vs/`, large recordings, and anything you may not share.
