# MelFR-FTF

**Complementary Mel and Full-Resolution Modeling for Lightweight Causal Speech Enhancement**

> **Status:** Submitted to ICASSP 2027. If accepted, we plan to release the core MelFR-FTF block implementations, configuration files, and pretrained inference models, including an ONNX export.

MelFR-FTF is a lightweight single-channel speech enhancement model. This repository provides the project overview and evaluation results.

## Architecture

![MelFR-FTF architecture](assets/melfr_ftf_overview.png)

## Results

- **VoiceBank+DEMAND, standard:** PESQ 3.18 · CSIG 4.29 · CBAK 3.63 · COVL 3.76 · STOI 0.945.
- **VoiceBank+DEMAND, FastEnhancer-aligned:** P.808 3.48 · SI-SDR 18.9 dB · PESQ 3.18 · STOI 0.945 · eSTOI 0.860.
- **DNS, FastEnhancer-aligned:** P.808 3.91 · SIG 3.39 · BAK 4.11 · OVL 3.16 · SI-SDR 16.9 dB · PESQ 2.56 · STOI 0.952 · eSTOI 0.901. SCOREQ is 0.442 (lower is better).

The model has 69.26K parameters and 399M neural MAC/s, with causal neural processing and 16-ms centered-STFT look-ahead.

## Citation

Citation information will be added after publication.
