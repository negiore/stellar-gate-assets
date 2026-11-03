# stellar-gate-assets

Prebuilt files that Stellar Gate downloads instead of building them on every fresh cloud GPU.

## MTP draft layer for Strata (`mtp-rt-strata-v0.2.9` release)

`rt.tar` holds the `mtp/rt/` folder that [Strata](https://github.com/Niko1221/Strata) v0.2.9 builds for Qwen3.8-Flash-Next
(`tools/mtp_fetch.py` → `tools/mtp_pack.py --experts q2_0` → `tools/mtp_rt.py`). Building it takes about 3.5 minutes on a
Colab L4 (a ~5 GB download of the MTP tensors plus quantization); the result is byte-identical every time, so it is built
once and shared. The SHA-256 of `rt.tar` and of each file inside it are listed in the release notes.

- Source weights: the MTP tensors of [Qwen/Qwen3.8-Flash-Next](https://huggingface.co/Qwen/Qwen3.8-Flash-Next), pinned to the
  revision named in Strata v0.2.9's `tools/mtp_fetch.py`.
- License: these files are a derivative work of Qwen3.8-Flash-Next and are distributed under the
  [Qwen Community License 1.0](LICENSE-Qwen) (copyright (c) 2026 Qwen). The tools that built them are Strata's (MIT).
- No warranty; see the license.

---

Stellar Gate が、クラウドの GPU を借りるたびに作り直す代わりに取る、作り済みのファイルです。
`rt.tar` は Strata v0.2.9 が Qwen3.8-Flash-Next 用に作る先読みの層（MTP）で、元の重みの使用許諾（Qwen Community License 1.0）に従って配布しています。
