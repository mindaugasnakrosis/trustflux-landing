# Self-hosted fonts

Both families are served from this origin so the critical rendering path never
waits on fonts.googleapis.com.

| File | Family | Axis | Source |
| --- | --- | --- | --- |
| `inter-var-latin.woff2` | Inter | `wght 400-700` (`opsz` pinned to 14) | [google/fonts `ofl/inter`](https://github.com/google/fonts/tree/main/ofl/inter) |
| `space-grotesk-var-latin.woff2` | Space Grotesk | `wght 500-700` | [google/fonts `ofl/spacegrotesk`](https://github.com/google/fonts/tree/main/ofl/spacegrotesk) |

Both are subset to the Latin range the site actually uses (Latin-1 plus the
handful of Latin Extended-A and punctuation code points in `unicode-range`
in `styles.css`). Regenerate with `fonttools`:

```sh
python3 -m pip install "fonttools[woff]" brotli
python3 - <<'PY'
from fontTools.ttLib import TTFont
from fontTools.varLib import instancer
f = instancer.instantiateVariableFont(TTFont("Inter[opsz,wght].ttf"), {"opsz": 14, "wght": (400, 700)})
f.save("inter.inst.ttf")
PY
python3 -m fontTools.subset inter.inst.ttf \
  --unicodes="U+0000-00FF,U+0131,U+0152-0153,U+0160-0161,U+0178,U+017D-017E,U+0192,U+02C6,U+02DA,U+02DC,U+2013-2014,U+2018-201A,U+201C-201E,U+2020-2022,U+2026,U+2030,U+2039-203A,U+2044,U+20AC,U+2122,U+2190-2193,U+2212,U+FEFF,U+FFFD" \
  --layout-features=kern,liga,clig,calt,ccmp,locl,mark,mkmk,rlig \
  --flavor=woff2 --desubroutinize --name-IDs=0,1,2,3,4,5,6,13,14 \
  --output-file=inter-var-latin.woff2
```

Both fonts are licensed under the SIL Open Font License 1.1 - see
`Inter-OFL.txt` and `SpaceGrotesk-OFL.txt`.
