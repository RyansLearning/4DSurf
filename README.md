# 4DSurf: High-Fidelity Dynamic Scene Surface Reconstruction

Official implementation of **4DSurf: High-Fidelity Dynamic Scene Surface Reconstruction** (CVPR 2026).

## Reconstructed Meshes

The reconstructed meshes are available for download:

- **Hi4D:** [Download Reconstructed Meshes](https://github.com/RyansLearning/4DSurf/releases/tag/v1.0-ours-hi4d-meshes)

### Extraction Instructions

Download all files for the desired scene and place them in the same directory.

**For split ZIP files (`.part001`, `.part002`, etc.):**

```bash
# Merge all parts into a single ZIP
cat hi4d_pair02.zip.part* > hi4d_pair02.zip

# Extract the reconstructed meshes
unzip hi4d_pair02.zip
```

Alternatively, to extract all scenes automatically:

```bash
for f in *.zip.part001; do
    base="${f%.part001}"
    cat "${base}".part* > "$base"
    unzip "$base"
done

for f in *.zip; do
    unzip -n "$f"
done
```

## SDF Flow Regularization Loss

The implementation of the SDF Flow Regularization Loss will be released soon.

## Code Release Status

- [x] Reconstructed Meshes (Hi4D)
- [ ] SDF Flow Regularization Loss (Coming soon)
- [ ] Full Code (Coming soon)
