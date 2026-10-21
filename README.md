# Бессонница (Insomnia)

Track 5 of 7 on «Ностальгия» (_Nostalgiya_, “Nostalgia”), the album by Полуживые (_Poluzhivye_), on poems by Arseny Tarkovsky.

On the site: https://vovazakharov.com/music/insomnia

## Files

- `insomnia_mix.mp3` — the mix, unmastered: what the master was made from.
- `Полуживые - Бессонница.mp3` — the master. The mix survives only as an mp3, so the master is one too.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
python mastering/master.py insomnia_mix.mp3 ref.flac insomnia.mp3
```

with `ffmpeg` on `PATH` and the reference below saved as `ref.flac`. Half
strength (`master.py`'s default): Matchering matches the mix to the reference,
half of the EQ difference goes onto the mix, and a limiter keeps the decoded
file under -1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

“Life, believe, is not a dream…”, Полуживые, from CTFU, at [vovas-music/bronte@ff95a2c](https://github.com/vovas-music/bronte/blob/ff95a2c6796dedb0c71011837337fcc01ff3d860/Poluzhivye%20-%20Life,%20believe,%20is%20not%20a%20dream…%20feat.%20za_oblozhkoy%20&%20GENERATED.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/bronte/ff95a2c6796dedb0c71011837337fcc01ff3d860/Poluzhivye%20-%20Life,%20believe,%20is%20not%20a%20dream…%20feat.%20za_oblozhkoy%20&%20GENERATED.flac

It was picked blind: three catalogue masters each mastered the mix, and the
operator ranked them unlabelled, loudness-matched, before learning which was
which. It is linked rather than copied here, since it already lives in this
organization.
