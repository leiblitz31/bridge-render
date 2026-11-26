# bridge-render

Render video Bridge (Remotion + three.js) di GitHub Actions.

## Pakai

```bash
gh workflow run render-bridge --repo leiblitz31/bridge-render
gh run list --repo leiblitz31/bridge-render
gh run watch --repo leiblitz31/bridge-render
```

Unduh hasil: `gh run download <run-id> --repo leiblitz31/bridge-render -n bridge-video`

## Isi

- `.github/workflows/render.yml` — clone template, unduh 26 model Kenney (CC0), install, render, audio, artefak
- 2025 frame @30fps = 67,5 s, 1080×1920
- Batas Actions: 6 jam; render ~3 jam di 4 core

## Catatan

`EffectComposer` (ink/bloom/grade) blank di software GL — runner Actions tanpa GPU. Hasil flat-shaded. Untuk look asli butuh GPU.