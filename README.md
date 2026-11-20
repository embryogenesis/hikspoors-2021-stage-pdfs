# Hikspoors et al. 2021 — whole-embryo interactive 3D-PDFs, twelve stages

A **verbatim mirror** of [`10.6084/m9.figshare.17033156`](https://doi.org/10.6084/m9.figshare.17033156), redistributed under the terms of the licence the depositors chose. No file has been modified.

## Attribution

> Hikspoors, Jill P. J. M., and colleagues
>
> Hikspoors JPJM et al. (2021), supplemental material. Deposited as twelve separate Figshare items, one per Carnegie stage.
>
> DOI: [10.6084/m9.figshare.17033156](https://doi.org/10.6084/m9.figshare.17033156) — licensed **CC BY 4.0**

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); see [`LICENSE`](LICENSE). You may share and adapt this material for any purpose, including commercially, provided you give appropriate credit, link to the licence and indicate if changes were made. **This mirror makes no changes.**

## What this is

Interactive 3D-PDFs at Carnegie stages 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 20 and 23 — whole embryo rather than one organ system, which makes this the more valuable of the two deposits in the long run. Twelve licences were checked individually; all twelve are CC BY 4.0.

## Contents

13 file(s), 134.7 MB total.

| File | Size | SHA-256 |
| --- | --- | --- |
| `data/CS09.pdf` | 4.3 MB | `b0ed00e67f4eb387…` |
| `data/CS10.pdf` | 3.8 MB | `bd4e179296019c7d…` |
| `data/CS11.pdf` | 3.5 MB | `7d4a487aa3465708…` |
| `data/CS12.pdf` | 9.5 MB | `f20c5516b4d7d647…` |
| `data/CS13.pdf` | 6.3 MB | `f56c9a711ea1c83d…` |
| `data/CS14.pdf` | 11.7 MB | `dc65a6da63267078…` |
| `data/CS15.pdf` | 12.3 MB | `642c1299f7ea4b4d…` |
| `data/CS16.pdf` | 15.2 MB | `9752e018f5c787c3…` |
| `data/CS17.pdf` | 14.8 MB | `e85ae605337f822d…` |
| `data/CS18.pdf` | 26.7 MB | `c30add6d2504c1ea…` |
| `data/CS20.pdf` | 12.3 MB | `a6294816497c51a3…` |
| `data/CS23.pdf` | 12.4 MB | `5fb8f33a11ef3a20…` |
| `data/instruction-video.mp4` | 1.9 MB | `034898bc42991ee4…` |

Full checksums, original filenames and the source article id for every file are in [`MANIFEST.json`](MANIFEST.json).

## Notes for anyone using this

- The geometry is a Flate-compressed U3D stream inside each PDF. Extraction was tested on the stage-13 item: 5.06 MB compressed, 9.47 MB decoded, valid `U3D\0` magic, 219 blocks parsed, roughly 37 materials. So the geometry is genuinely there and genuinely usable.
- U3D stores progressive CLOD meshes in range-coded bitstreams. Writing a decoder is a project in itself, not an afternoon. Until one exists, the immediately useful path is to open them in a reader and measure.
- Deposited as twelve separate articles, so the mirror flattens them into one repository with stage-named files. The original article id is recorded per file in MANIFEST.json.
- The instruction video is the depositor's own and is included because it documents the intended use of the 3D-PDFs.

## Verifying the mirror

```sh
# every file, against the manifest
python3 -c "import json,hashlib,pathlib;m=json.load(open('MANIFEST.json'));[print(('ok  ' if hashlib.sha256(pathlib.Path(f['path']).read_bytes()).hexdigest()==f['sha256'] else 'BAD ')+f['path']) for f in m['files'] if pathlib.Path(f['path']).exists()]"
```

---

Mirrored 2026-11-20 by `tools/mirror.ts` in the atlas repository, which re-verifies the licence of every article against the live Figshare metadata before downloading anything and aborts on a mismatch.
