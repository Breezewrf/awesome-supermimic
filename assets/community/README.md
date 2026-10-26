# Community media credits

## Video previews

These GIFs show demonstrations published by the linked projects. They are converted from the original videos; this collection did not run the experiments.

| Preview | Authors / source project | Original video | Duration |
| --- | --- | --- | --- |
| [morphmimic.gif](morphmimic.gif) | [Lizhi Yang and the MorphMimic authors](https://github.com/lzyang2000/morphmimic) | [MP4](https://lzyang2000.github.io/morphmimic/static/videos/dance_hiphop_shuffle_sequence_v_001_R_003__A306.mp4) | 20.02 s |
| [backflip.gif](backflip.gif) | [liudi159](https://github.com/liudi159/supermimic-backflip-5090) | [MP4](https://raw.githubusercontent.com/liudi159/supermimic-backflip-5090/5b313d75e804cdd2ff1ce9bdcfa899a98eca856b/media/v14_blue_checker.mp4) | 11.44 s |
| [flatworld.gif](flatworld.gif) | [swaggyliu](https://github.com/swaggyliu/FlatWorld) | [MP4](https://raw.githubusercontent.com/swaggyliu/FlatWorld/207e9e9c61ef21b8f145c3e0c4d8b121a03bf45a/supermimic2d/runs/lafan2d/showcase_30s.mp4) | 31.60 s |

Retrieved on 2026-10-26. Each preview preserves the complete selected clip, its framing, frame order and original playback speed. They are scaled to 480 × 270, sampled at 12 fps and quantized to 128 colors, with no added borders, motion interpolation or generated content. GIF timing is rounded to centiseconds.

- **MorphMimic:** the project website’s street-shuffle demonstration of G1, X2 Ultra and T2 using one shared policy; this is the complete 20.02-second clip, not the longer project film.
- **Backflip:** the final V14 policy rollout. The project reports a failed strict evaluation due to non-foot contact; the GIF is not evidence of passing that evaluation.
- **FlatWorld:** the complete upstream 2D motion-tracking showcase.

All rights in the source footage remain with the original authors. These third-party previews are excluded from this collection’s CC0 dedication. Refer to the linked projects for their terms; this collection does not grant new rights to the footage.

Conversion uses FFmpeg:

```sh
ffmpeg -i source.mp4 -filter_complex \
  "fps=12,scale=480:-1:flags=lanczos,setsar=1,split[a][b];[a]palettegen=max_colors=128[p];[b][p]paletteuse=dither=bayer:bayer_scale=4" \
  -loop 0 preview.gif
```

## Static previews

The following previews were checked on 2026-10-26. Each links to a pinned source revision. They show the authors' figures or documented results; this collection did not run the experiments.

### Original project images

These images are embedded directly from their source repositories, without editing. Click a preview in the README for the full-size source.

| Project | Image and source | What it shows |
| --- | --- | --- |
| [InstinctMJ · SuperMimic](https://github.com/project-instinct/InstinctMJ) | [world_model_simple.png](https://github.com/project-instinct/InstinctMJ/blob/7ca851e002980011f24a1664011305d0ba94aefc/src/instinct_mj/rl/supermimic/assets/world_model_simple.png) | Method diagram · robot-state and visual-latent prediction |
| [SuperMimic-perceptive](https://github.com/mode1223345/SuperMimic-perceptive) | [Curves.png](https://github.com/mode1223345/SuperMimic-perceptive/blob/3d38bacbaf5bee7e782bdada6a6da678264d0bfa/results/Curves.png) | Training curves · 2026-10-24 snapshot; control comparisons in progress |
| [Dex SuperMimic](https://github.com/CumulusAlpha/Dex-Supermimic) | [teaser.jpg](https://github.com/CumulusAlpha/Dex-Supermimic/blob/5ca57628af3666a9b2878c00f461f43d6edb5b61/teaser.jpg) | Simulation screenshot · Wuji Hand 2 cube reorientation |

### Source-table screenshots

The eight PNGs below preserve the selected upstream table content. The tables were rendered locally with a dark theme and wrapped cells for legibility, without GitHub navigation. Text and values were not rewritten; the two excerpts are identified below. These are report or code-index screenshots, not simulation frames or new measurements. The original sources remain available as selectable text.

| Screenshot | Pinned source | Selection |
| --- | --- | --- |
| [reproduced-results.png](reproduced-results.png) | [SuperMimic-Reproduced](https://github.com/CuboiLeo/SuperMimic-Reproduced/blob/d9be385b3eeb13a638fb33fb200d3bfd9be9839f/README.md) | Complete experiment summary, including the separate observation settings and BONES-SEED subset evaluation. |
| [vibe-results.png](vibe-results.png) | [supermimic_vibe](https://github.com/dhmbb2/supermimic_vibe/blob/072f0910dadc9d95c720e625b546120e9ce917c9/README.md) | Complete reproduction-status table, including partial, pending, blocked and out-of-scope items. |
| [locomujoco-results.png](locomujoco-results.png) | [SuperMimic on LocoMuJoCo](https://github.com/Alchedata/supermimic-locomujoco/blob/cc1375d48a38bde062d088ffd132122e0cd7b7da/README.md) | Complete Results at 5k table, including the failed seed and recovery branches. |
| [rethinking-comparison.png](rethinking-comparison.png) | [Rethinking SuperMimic](https://github.com/btx0424/rethinking-supermimic/blob/ecdaeb6a916a16cf7eb69b19226c17be31a6bc27/README.md) | Excerpt: header and first three rows — dynamics state, MLP details and world-model loss. |
| [pera-tracking-results.png](pera-tracking-results.png) | [SuperMimic-PERA](https://github.com/shangchaohu718/supermimic-pera/blob/0e89e55187a800341e609129b5d5200a607a467c/README.md) | Complete tracking-checkpoint table. This is the tracker baseline, not the separate skateboarding result. |
| [contact-bptt-results.png](contact-bptt-results.png) | [Ref2Dex · Dex Contact MBRL](https://github.com/hitsz-oyx/Ref2Dex-agent/blob/31cdb9ac759838b83d62bbc0addfd5cf28f3dff4/src/task/dex-contact-mbrl/docs/CONTACT-REFINEMENT-RESULTS-20261026.md) | Complete three-arm native-physics comparison. Higher reference survival accompanies lower mean return. |
| [g05-steering-entry.png](g05-steering-entry.png) | [G0.5 · SuperMimic-style Steering](https://github.com/azizkhadraoui/g05/blob/e3de0de50db7d90068483e2d30f2eacd781300b4/README.md) | Excerpt: code-index header and Noise policies row identifying the SuperMimic-style scripts; not a rollout. |
| [mujoco-evaluation.png](mujoco-evaluation.png) | [SuperMimic-MuJoCo](https://github.com/panhainan2020/SuperMimic-MuJoCo/blob/db045afa9c52458f213e2c66037387e9c109a03a/README.md) | Complete evaluation summary. The external video cover returned HTTP 403 when checked; the README retains the gallery link. |

All rights in the original figures, text and data remain with their respective authors. These third-party previews are excluded from this collection's CC0 dedication; consult the linked sources for their terms. InstinctMJ's source is licensed CC BY-NC 4.0.
