# ASTRA-ISAR 发布页资源放置说明

本文档说明当前发布页 `index.html` 所依赖的资源路径、文件命名方式，以及后续补充真实示例文件时应放置到哪里。

## 1. 目标展示图

网页中的 20 个目标展示图统一放在：

`assets/targets/`

当前发布页读取的文件如下：

- `acrimsat.webp`
- `agena-target-vehicle.webp`
- `aqua.webp`
- `chang-e-1.webp`
- `cloudsat.webp`
- `cubesat-1ru.webp`
- `dawn.webp`
- `earth-observing-1.webp`
- `fengyun-3.webp`
- `icecube-3u.webp`
- `iss.webp`
- `juno.webp`
- `kepler-space-telescope.webp`
- `landsat-8.webp`
- `lunar-reconnaissance-orbiter.webp`
- `mars-reconnaissance-orbiter.webp`
- `shenzhou-12.webp`
- `tianhe-tianzhou-shenzhou.webp`
- `tianhe-tianzhou.webp`
- `tianlian-1.webp`

说明：

- 原始 `Target/` 目录保持不动，网页只读取 `assets/targets/` 下的标准 WebP。
- 网页使用固定画布和 `object-fit: contain` 展示图片，因此不需要对原图做裁切或拉伸。
- 如后续替换更高质量图片，请保持文件名不变，直接覆盖对应 WebP 文件即可。

## 2. 目标矩阵对应关系

网页中的二维矩阵按 `Topology A/B/C/D × Scale S/M/L` 组织，当前 20 个目标的落位如下：

### A-S

- CubeSat (1 RU)
- ICECube (3U)

### A-M

- AcrimSAT
- Agena Target Vehicle
- Kepler Space Telescope

### B-M

- Earth Observing-1 (EO-1)
- Lunar Reconnaissance Orbiter
- Fengyun-3
- Landsat 8

### B-L

- Aqua

### C-M

- CloudSat

### C-L

- Chang'e 1
- TianLian-1
- Shenzhou 12
- Dawn

### D-L

- Tianhe-Tianzhou
- Mars Reconnaissance Orbiter
- Juno
- Tianhe-Tianzhou-Shenzhou
- ISS

## 3. 示例文件目录

网页已经预留了 5 个 Track 的示例目录：

- `assets/examples/track-echo/`
- `assets/examples/track-enhance/`
- `assets/examples/track-geo/`
- `assets/examples/track-gen/`
- `assets/examples/track-perception/`

当前每个目录只有一份 `README.md` 说明文件，便于后续逐项补充真实可公开样例。

## 4. 每个 Track 建议放置的最小示例

### Track 1 Echo

目录：

`assets/examples/track-echo/`

建议文件：

- `sample_echo_arc.mat`
- `sample_echo_slice.mat`
- `sample_isar.webp`
- `sample_meta.txt`

### Track 2 Enhance

目录：

`assets/examples/track-enhance/`

建议文件：

- `sample_degraded.webp`
- `sample_clean.webp`
- `sample_degraded_echo.mat`

### Track 3 Geo

目录：

`assets/examples/track-geo/`

建议文件：

- `sample_sequence_manifest.json`
- `sample_isar.webp`
- `sample_pose.txt`

### Track 4 Gen

目录：

`assets/examples/track-gen/`

建议文件：

- `sample_isar.webp`
- `sample_optical.webp`
- `sample_optical_isar_view.webp`
- `transforms_train.json`

### Track 5 Perception

目录：

`assets/examples/track-perception/`

建议文件：

- `sample_isar.webp`
- `sample_meta.txt`
- `sample_echo_slice.mat`
- `manifest.csv`

## 5. 网页与文件的对应关系

网页中的“数据格式与资源放置说明”区块链接到以下文件：

- 总说明：`assets/docs/resource-placement.md`
- Track 1：`assets/examples/track-echo/README.md`
- Track 2：`assets/examples/track-enhance/README.md`
- Track 3：`assets/examples/track-geo/README.md`
- Track 4：`assets/examples/track-gen/README.md`
- Track 5：`assets/examples/track-perception/README.md`

如果后续补充真实样例，建议保留这些 README，并在同目录下直接加入正式文件。这样网页路径不需要改动。
