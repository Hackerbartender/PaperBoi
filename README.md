# Paperboi

Shamelessly vibe coded Claude Code project to read Twitter feeds so I don't have to. Scrapes Nitter RSS and dumps the last 24 hours of tweets into a tidy file. No API keys, no AI dependencies — just a scraper.

## Install

```bash
pip install -r requirements.txt
```

## Configure

Edit `feeds.txt` to add/remove handles (one per line, `@` prefix optional):

```
@elder_plinius
rez0__
troyhunt
```

Tune behaviour at the top of `PaperBoi.py`:

| Variable | Default | Description |
|---|---|---|
| `LOOKBACK_HOURS` | `24` | How far back to fetch tweets |
| `MAX_TWEETS_PER_USER` | `20` | Max tweets per handle |
| `NITTER_INSTANCES` | see file | Nitter instances to try in order |
| `OUTPUT_DIR` | `digests` | Where to save output files |

## Run

```bash
python PaperBoi.py
```

Tweets are printed to the terminal and saved as `digests/tweets_YYYY-MM-DD.txt`.

## Summarizing

The output file can be fed to Claude or any AI agent of your choice for summarization.
