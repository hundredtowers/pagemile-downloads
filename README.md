# Pagemile downloads

Files the [Pagemile](https://hundredtowers.github.io/pagemile/) app downloads
on demand instead of carrying them inside the app. Each kind of file has its
own releases, named `<kind>-<date>`; the app pins every file by size and
SHA-256, so a published file is never changed, only replaced by a new
release.

## Dictionaries (`dictionaries-*`)

SQLite dictionary packs, gzip-compressed, one per language. Pagemile
downloads one the first time you look up a word in its language, or from
Manage dictionaries, and then works offline.

| File | Language | Source | Licence |
|---|---|---|---|
| `en.sqlite.gz` | English | [Open English WordNet 2025](https://en-word.net/), derived from [Princeton WordNet](https://wordnet.princeton.edu/license-and-commercial-use); pronunciations also from [CMUdict](https://github.com/cmusphinx/cmudict) | CC BY 4.0 (OEWN), WordNet License, CMUdict BSD-style |
| `it.sqlite.gz` | Italian | [Italian Wiktionary](https://it.wiktionary.org) (Wiktionary contributors) via [Wiktextract / kaikki.org](https://kaikki.org); where it has no definition, [italian-wordnet-definitions](https://github.com/linkingtechnologies/italian-wordnet-definitions): IWN-OMW / ItalWordNet definitions (CNR-ILC), [MultiWordNet](https://multiwordnet.fbk.eu) lemmas (Fondazione Bruno Kessler) | CC BY-SA 4.0, CC BY 3.0 |
| `es.sqlite.gz` | Spanish | [Spanish Wiktionary](https://es.wiktionary.org) (Wiktionary contributors), extracted by [Wiktextract / kaikki.org](https://kaikki.org) | CC BY-SA 4.0 |
| `fr.sqlite.gz` | French | [French Wiktionary](https://fr.wiktionary.org) (Wiktionary contributors), extracted by [Wiktextract / kaikki.org](https://kaikki.org) | CC BY-SA 4.0 |

Word-difficulty tiers in every pack come from
[wordfreq](https://github.com/rspeer/wordfreq) by Robyn Speer (data CC BY-SA
4.0). The packs derived from CC BY-SA sources are shared under CC BY-SA 4.0;
the English pack under CC BY 4.0, with the WordNet License's notice.

Each pack is an adaptation: entries Wiktionary got wrong (section headings
taken for definitions, English glosses, a verb's auxiliary listed as its
form) are dropped; every other word, phrase, sense and inflected form is
kept, each definition whole, and inflected forms are indexed for lookup.

Releases: `dictionaries-2026-11-06` (first packs), `dictionaries-2026-11-06.2`
(complete Wiktionary packs; Italian from Wiktionary first).
