# FARRec

FARRec is a local workbench for reconstructing inclined air showers from radio
detector ROOT files. This public beta distribution is version 0.9.2.

## Get started

Download **FARRec-v0.9.2-public.zip** from the [GitHub Release](https://github.com/JuliusErv1ng/FARRec/releases/tag/v0.9.2) and extract it
completely to a writable directory.

| System | Start |
| --- | --- |
| Windows x64 | Double-click `start.bat` |
| macOS (Apple Silicon or Intel) | Open `start.command` or run `sh start.sh` |
| glibc Linux (ARM64 or x86-64) | Run `sh start.sh` |

The launcher prepares the local Python environment if needed. First-time
dependency installation requires an internet connection. The interface runs
locally and supports Chinese, English and French. On Windows, check
`logs/windows-setup.log` if installation fails; on macOS and Linux, check the
terminal and `logs/install.log`.

The workbench initially has no results. Choose **New reconstruction task** and
select your own compatible ROOT file(s). For one event, enter its Run and Event
numbers. For a batch, select all events or supply a CSV with columns
`run_number,event_number,root_file`. Preview the station-coordinate matching
before reconstruction. The bundled GP65 coordinate and GPS-offset defaults
are specific to GP65; supply a suitable station table for other layouts.
Azimuth is measured from north towards west (north 0°, west 90°).

The public download includes the runtime, detector responses, reference models,
simulation-derived calibration resources and station configuration. It contains
no measured ROOT files, measured per-event result files or source event lists.
The Chinese and English user manuals, training slides and technical guide
retain their original illustrations. References in those documents to a
bundled ROOT example or saved event batch apply to the internal package only.

After installation, run `self_test.py --quick` with the package's Python
environment to check imports, resources and the local web API. Run
`verify_resources.py` to verify the extracted file checksums. A reconstruction
test requires a compatible ROOT file supplied by the user.
