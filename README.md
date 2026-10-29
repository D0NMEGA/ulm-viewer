# ULM track viewer: Aleph Neuro reference reproduction

Static three.js viewers built from the public beamformed reference
(`beamformed_reference_216acq.h5`, 216 acquisitions, 222.43 Hz) with the
alephneuro/microbubbles pipeline (sharsharshar fork, branch mythostake).

- `/` : all 216 acquisitions, tracks of 10+ frames (14,389 tracks, 280k points)
- `/all/` : every track of 5+ frames (49,952 tracks, 501k points, 12 MB)
- `/min20/` : tracks of 20+ frames (4,408 tracks)
- `/min35/` : tracks of 35+ frames (1,441 tracks), the `run` default
- `/first6/` : acquisitions 0-5 only, every track of 5+ frames (1,556 tracks)

Colour is flow speed (plasma: purple slow, orange fast, scale top 38 mm/s); point
size follows the tracker's detection magnitude. The GUI switches build-up replay,
colormap, scale, size and opacity.

Settings: adaptive SVD (falls back to the fixed 10% cutoff on this file), knee filter on,
temporal sigma 0, sigma threshold 2.0, centroid sub-voxel localization, Kalman linking,
max gap 3, max cost 10, min track length 5, gaussian smoothing sigma 2.
Run on bicfcomp01 (UT Austin BIC), 2026-10-29. Drag to orbit, scroll to zoom.
