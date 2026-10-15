# Korean Folk Song Form Map

Interactive companion page for a study of phrase organisation and motif repetition in Korean folk song field recordings from the MBC *Korean Folk Song Anthology* (한국민요대전).

**Live page:** https://danbinaerinhan.github.io/korean-folk-form-map/

The page has three levels, each on the same two axes:

1. Function categories: ten points, each the median of its recordings.
2. Song types within a category.
3. Individual recordings of a song type.

All 7,357 recordings behind the map appear as grey dots. For 112 highlighted recordings, the page shows:
- automatic phrase boundaries
- motif labels at three clustering grades
- the pitch contour
- an automatic per-phrase lyric transcript
- the recording's measures and its MBC catalogue information

You can also listen to these 112 recordings on the page.

- **Phrase index (horizontal):** higher means shorter and more even phrases. It combines mean phrase duration and duration entropy.
- **Return index (vertical):** combines Motif Spread and periodic coverage.
- **Point size:** quartile of the periodicity index, which combines texture periodicity (AC) and phase alignment (FOLD). Point size does not show the number of recordings.
- **Highlighted recordings:** three per song type. Each type's phrase-index range is split into thirds, and the recording with the most reliable automatic segmentation is taken from each third. The four example recordings shown in the article are added to these.

Phrase boundaries and per-phrase lyrics are automatic outputs and have not been corrected.

## Contents
- `index.html`: the page. It is a single file with no build step.
- `data/map.json`: category and song-type medians, and coordinates of all map recordings.
- `data/featured_index.json`, `data/songs/<id>.json`: data for the highlighted recordings.
- `audio/<id>.mp3`: audio of the highlighted recordings (see below).

To view the page locally, serve the folder over HTTP with byte-range support, which audio seeking needs. Opening `index.html` directly from disk will not load the data.

## Audio and source credit
The recordings are MBC's (Munhwa Broadcasting Corporation) *Korean Folk Song Anthology* field recordings, 1989–1996. The files in `audio/` are MBC's own mp3 files from the official archive at https://urisori.co.kr, unchanged. They are included for research and education use, as the archive's terms allow, with the credit 자료출처: MBC 한국민요대전. Each recording on the page links to its archive page.

Copyright in the recordings belongs to MBC, and they are **not** covered by this repository's license. Using them for music, broadcast or social-media content requires MBC's permission (see urisori.co.kr).

## License
See `LICENSE`. In short:
- page code: MIT
- derived data in `data/`: CC BY 4.0
- `audio/`: © MBC, excluded from both licenses
