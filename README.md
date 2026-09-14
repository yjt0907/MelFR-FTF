# MelFR-FTF

**Complementary Mel and Full-Resolution Modeling for Lightweight Causal Speech Enhancement**

> This repository is the project page for MelFR-FTF, a lightweight causal single-channel speech enhancement model associated with an ICASSP 2027 submission. The training/inference code and pretrained models will be released upon acceptance.

## Overview

MelFR-FTF is a lightweight causal single-channel speech enhancement model that allocates the computationally dominant contextual modeling to a compact 80-band Mel backbone while retaining lightweight full-resolution information.

Its main components are:

- an 80-band Mel-domain contextual backbone;
- a full-resolution complex pathway using the power-compressed complex spectrum;
- a Mel-complementary residual pathway based on the reconstruction residual $A_c - M^\dagger M A_c$;
- band-aligned intermediate cross-resolution conditioning;
- final full-resolution fusion for complex-mask estimation.

The model uses causal neural processing with 16-ms STFT look-ahead. Mel/full-resolution processing is used as a complementary design, without claiming zero algorithmic latency or a first use of these individual ingredients.

## Architecture

The final architecture figure will be added at `assets/melfr_ftf_overview.png`.

<!-- Add final architecture figure as assets/melfr_ftf_overview.png -->
<!-- ![MelFR-FTF architecture](assets/melfr_ftf_overview.png) -->

## Results

Headline results from the frozen paper evaluation protocols are shown below. The VoiceBank+DEMAND and DNS entries use their respective benchmark protocols.

| Benchmark | Metric | Result |
| --- | --- | ---: |
| VoiceBank+DEMAND | PESQ | 3.18 |
| DNS | DNSMOS P.808 | 3.91 |
| DNS | SI-SDR | 16.9 dB |

- Trainable parameters: 69.26K
- Neural MACs/s: 399M
- Causal neural processing with 16-ms STFT look-ahead

## Release

Training/inference code and pretrained models will be released upon acceptance.

## Citation

Citation information will be added after publication.

## License

This project is released under the Apache License 2.0.
