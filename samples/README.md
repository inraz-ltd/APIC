# Sample projects

Each sample has its own folder and its own download (a release named `sample-<folder>`).

| Sample | Folder | Download | Shows | Needs |
|---|---|---|---|---|
| Camera emulator | [camera-emulator](camera-emulator/) | [zip](../../../releases/download/sample-camera-emulator/camera-emulator.zip) | A Linux board seen by a PC as a USB (UVC) or GigE Vision camera | Raspberry Pi 5 or Rock 5B (USB); any Linux board or PC (GigE) |
| SIL / HIL | [sil-hil](sil-hil/) | [zip](../../../releases/download/sample-sil-hil/sil-hil.zip) | One MIL-STD-1553 project with a simulated bus, then real hardware by changing the stream only | Nothing for SIL; a 1553 card or a UEI rack for HIL |
| Recording and playback | [record-playback](record-playback/) | [zip](../../../releases/download/sample-record-playback/record-playback.zip) | IMU, INS and camera data recorded together and played back | Nothing to play the included recording |
| Real time on Jetson | [jetson-realtime](jetson-realtime/) | [zip](../../../releases/download/sample-jetson-realtime/jetson-realtime.zip) | A CoreEngine application in real time on NVIDIA Jetson | A Jetson board |

A download exists only once its folder's `project/` has files (until then the link gives "not found").

## How a download is made

Push files into `samples/<folder>/project/`. The workflow `.github/workflows/sample-downloads.yml` zips
`samples/<folder>/` into `<folder>.zip` and publishes it as the release `sample-<folder>` (created the
first time, the zip replaced after that). It can also be started by hand: Actions, "Sample downloads", Run workflow.

## Add a new sample

1. Copy one of the folders, rename it (lower case, words joined with `-`), edit its README.
2. Put the project in its `project/` folder and push.
3. Add a row above, and ask for a box on the Help's Downloads page (`community-downloads.html`).

To share your own sample, see [CONTRIBUTING.md](../CONTRIBUTING.md).
