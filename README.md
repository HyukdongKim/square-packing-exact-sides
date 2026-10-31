# Exact sides and exact configurations for square packings: n = 172, 263, 297

These are the files attached to [jlevy/squares#804](https://github.com/jlevy/squares/issues/804) by Hyukdong Kim (ORCID [0000-0001-5787-8066](https://orcid.org/0000-0001-5787-8066)). They are given here so that they have a fixed, fetchable address.

## Contents

`attachments/` holds the three zip files exactly as attached to the issue. The SHA-256 digests match those stated in the issue's comments.

| file | SHA-256 | register entry |
|---|---|---|
| `squares-exact-forms.zip` | `c770f9c37dee6b248543f3e661318630a0f279bc6a8c7663cb2efc53e2814ee7` | exact sides at 88, 126, 172, 199 and 263 (172 and 263 are T-244) |
| `t244-exact-configurations.zip` | `16e6ad9d04f1def897478e59260880320bc7c06ae89e41fa83837c7dc29c9a2d` | exact configurations for T-244, s(172) and s(263) |
| `s297-exact-configuration.zip` | `e08b5d0a64c5c68eed827ee7e323687929048a4cfea438bb77ef390bdd4147a7` | exact configuration for T-247, s(297) |

`files/` holds the same zips unpacked, one directory per zip, byte for byte. Each directory has its own README. Two of them also list their members' digests in `SHA256SUMS`. `SHA256SUMS` at the top level lists every file in this repository.

The three certificates in `minpoly.json` format, readable by evand/square-packing's `search/exact/verify_exact.py`:

- `files/t244-exact-configurations/n172.minpoly.json`
- `files/t244-exact-configurations/n263.minpoly.json`
- `files/s297-exact-configuration/n297.minpoly.json`

## Check

Run from the repository root:

```
sha256sum -c SHA256SUMS
python3 <evand/square-packing@659ee62>/search/exact/verify_exact.py files/t244-exact-configurations/n172.minpoly.json files/t244-exact-configurations/n263.minpoly.json files/s297-exact-configuration/n297.minpoly.json
pip install python-flint
python3 files/t244-exact-configurations/check_field_packing.py files/t244-exact-configurations/n172.minpoly.json files/t244-exact-configurations/n263.minpoly.json files/s297-exact-configuration/n297.minpoly.json
```

Both checkers print `VALID` for all three files.

## Licence

Everything in this repository, data and code alike, is dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). See `LICENSE`.

## AI assistance

The computations, the constructions and the checkers were produced by Claude (Anthropic, model Claude Opus 5.5) at the author's direction. The author reviewed and reran them.
