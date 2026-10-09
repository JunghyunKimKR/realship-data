# Real-Ship Data

Open voyage data from an in-service 200-metre bulk carrier (Ultramax), collected in the project
"Real-time Testbed and Data on Real Ship Connected via Starlink", supported by the Lloyd's Register Foundation.

- **Host:** Seoul National University
- **Sponsor:** Lloyd's Register Foundation (LRF)
- **Vessel and data:** Helikon Shipping
- **Use:** research and development only

## Start Here: Sample Data

Release [**sample-2025-11-15**](https://github.com/JunghyunKimKR/realship-data/releases/tag/sample-2025-11-15) —
140 seconds of every data type in heavy sea, with the program that replays it.

- **Window:** 15 Nov 2025, 00:49:00–00:51:20 UTC, open North Pacific; Hs 3.7–3.9 m, roll up to 5.3°
- **Download:** `SampleDataSet_2025-11-15_heavy_sea.zip` (1.1 GB)
- **Run:** unzip to a local disk, run `player\DTI.exe` (Windows 10/11 64-bit, .NET Framework 4.8), open http://127.0.0.1:8080/
- **Guide:** [Public_Data_Download_Guide.pdf](docs/Public_Data_Download_Guide.pdf) — data formats, sign conventions, downloading the full data

## About the Data

| Data | Content | Rate |
|---|---|---|
| Navigation (NMEA) | position, heading, speed over ground and through water, rate of turn, wind, depth, own-ship AIS | 1–10 Hz |
| Ship motion (IMU) | roll, pitch, heave, angular rates, accelerations | 10 Hz |
| Radar | S-band and X-band echo, 4 channels | ~0.4 rev/s |
| Cameras | 5 fisheye cameras, 4000 × 3000, H.265 | ~10 fps |
| Wave radar | wave height, period and direction; 2-D spectra | ~80 s |
| Ship information | approximate hull form (STL); longitudinal mass distribution with each section's centre of gravity and rotational inertia (Excel) | — |

The hull form is fitted to the ship's hydrostatics; it is not the ship's lines.

### Holdings (shore copy, status October 2026)

| Data | Period | Volume |
|---|---|---|
| NMEA log | 21 Aug 2025 – 22 May 2026 | 23 GB zip |
| Radar | 14 Nov 2025 – 22 May 2026 | 7.8 TB |
| Camera | 18 Aug 2025 – 17 May 2026 (2,980 h) | 50.6 TB |
| Wave radar | 14 Aug 2025 – 11 May 2026 | 1.9 GB |

Collection continues for two years, to August 2027.

## Potential Research Applications

The dataset — combining camera imagery, radar imagery, and motion
measurements — can support research in areas such as:

- Obstacle detection
- Wave environment estimation
- Ship motion prediction

## Access Policy

While this dataset is open to the public, it consists of actual operational
data. To prevent misuse and potential problems, access to the full data is
granted only after verification of the requester's identity and purpose.
The sample data above is open to everyone.

## How to Request Access

To request access, please send an email to **[kim@shippartners.jp](mailto:kim@shippartners.jp)** with the
following information:

- Your name and affiliation
- Intended purpose of use

Once your request has been reviewed and approved, an account for the data
server (https://shippartners.synology.me — HTTP, FTP, SFTP) will be provided.

## Licence

- Data: research and development only
- DTI player: `player/LICENSE.txt`; third-party components: `player/THIRD-PARTY-NOTICES.txt`
