# Spotify Songs

`spotify_songs.csv` is the [TidyTuesday 2020-01-21](https://github.com/rfordatascience/tidytuesday/tree/master/data/2020/2020-01-21) dataset. It was pulled from the Spotify Web API with the [`spotifyr`](https://www.rcharlie.com/spotifyr/) R package (Charlie Thompson, Josiah Parry, Donal Phipps and Tom Wolff), following [Kaylin Pavlik's](https://www.kaylinpavlik.com/classifying-songs-genres/) approach of collecting songs from playlists in six genres: EDM, Latin, Pop, R&B, Rap and Rock. A copy is also on [Kaggle](https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs).

The file in this folder is byte-for-byte the TidyTuesday file. To download it again:

```bash
curl -L -o data/spotify_songs.csv https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-01-21/spotify_songs.csv
```

32,833 rows and 23 columns. Each row is a song in a playlist, so a song that's in more than one playlist shows up more than once (28,356 unique `track_id`s).

## Data dictionary

| Column | Type | Description |
|:---|:---|:---|
| track_id | string | Song ID |
| track_name | string | Song name |
| track_artist | string | Artist |
| track_popularity | number | Popularity (0–100), higher is more popular |
| track_album_id | string | Album ID |
| track_album_name | string | Album name |
| track_album_release_date | string | Album release date (`YYYY-MM-DD`, `YYYY-MM` or `YYYY`) |
| playlist_name | string | Playlist name |
| playlist_id | string | Playlist ID |
| playlist_genre | string | Playlist genre |
| playlist_subgenre | string | Playlist subgenre |
| danceability | number | How suitable the track is for dancing (0–1) |
| energy | number | Intensity and activity (0–1) |
| key | number | Key in pitch class notation (0 = C, 1 = C♯/D♭, ...), -1 if no key was detected |
| loudness | number | Average loudness in dB, usually between -60 and 0 |
| mode | number | 1 = major, 0 = minor |
| speechiness | number | Presence of spoken words (0–1) |
| acousticness | number | Confidence the track is acoustic (0–1) |
| instrumentalness | number | Likelihood the track has no vocals (0–1) |
| liveness | number | Likelihood the track was recorded live (0–1) |
| valence | number | Musical positiveness (0–1) |
| tempo | number | Estimated tempo in BPM |
| duration_ms | number | Duration in milliseconds |
