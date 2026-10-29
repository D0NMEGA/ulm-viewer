# ULM track viewer: Aleph Neuro reference reproduction

Static three.js viewers built from the public beamformed reference
(`beamformed_reference_216acq.h5`, 216 acquisitions, 222.43 Hz) with the
alephneuro/microbubbles pipeline (sharsharshar fork, branch mythostake).

- `/` : all 216 acquisitions, tracks of 35+ frames (1,441 tracks), the `run` default
- `/min20/` : all 216 acquisitions, tracks of 20+ frames (4,408 tracks)
- `/first6/` : acquisitions 0-5 only, every track of 5+ frames (1,556 tracks)

Settings: adaptive SVD (falls back to the fixed 10% cutoff on this file), knee filter on,
temporal sigma 0, sigma threshold 2.0, centroid sub-voxel localization, Kalman linking,
max gap 3, max cost 10, min track length 5, gaussian smoothing sigma 2.
Run on bicfcomp01 (UT Austin BIC), 2026-10-29. Drag to orbit, scroll to zoom.
