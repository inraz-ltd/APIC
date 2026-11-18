# Software and hardware in the loop (SIL / HIL)

One MIL-STD-1553 project run with a simulated bus on any PC (SIL), then on real equipment (HIL) by changing only the stream's interface library and keys. Models, blocks and the bus schedule stay the same.

**Needs:** Nothing for SIL; a 1553 card or a UEI rack with a 553 layer for HIL.

**Download:** [sil-hil.zip](../../../../releases/download/sample-sil-hil/sil-hil.zip)
(made automatically from this folder, see below).

**Read with it:** the APIC Help pages `samples.html#sil-hil` and `streams.html#muxbus`.

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
into `sil-hil.zip` and publishes it as the release `sample-sil-hil`, replacing the previous zip.
While `project/` has no files, no zip is made and the Help shows "Coming soon" for this sample.

Leave out: build output (`out/`, `build/`, `bin/`, `obj/`), `.vs/`, large recordings, and anything you may not share.
