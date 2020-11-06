## Does Modern Day Music Lack Uniqueness Compared to Music before the 21st Century

# Abstract

# Introduction
Music is one of the most influential elements in the arts. It has a great impact on the way humans act and feel. Research, done by Nina Avramova, has shown that different genres of music bring about different emotions and feelings through the listener. Nonetheless, humans also have a major impact on music itself. Music and humans are mutually dependent therefore when one evolves, so does the other. 

This journal intends to progress the current understanding of if, how, and why music has changed since the 21st century. It also aims to determine if this change in music has led to a lack of uniqueness amongst the common features of a song compared to music before the 21st century. 

# Data
The data is located on Kaggle and was collected by a data scientist named Yamac Eren Ay. He collected more than 160,000 songs from Spotify that ranged from 1921 to 2020. Some of the features that this data set includes and will be used to conduct an analysis are: danceability, energy, acousticness, instrumentalness, valence, tempo, key, and loudness.  

**Danceability** describes how appropriate a track is for dancing by looking at multiple elements including tempo, rhythm stability, beat strength, and general regularity. The closer the value is to 0.0 the less danceable the song is and the closer it is to 1.0 the more danceable it is. **Energy** is a sensual measure of intensity and activity. Usually energetic songs feel fast, loud, and noisy. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy [5]. The closer this value is to 0.0 the less energetic the track is and the closer it is to 1.0 the more energetic the track is. **Acoustic** music refers to songs that are created using instruments and recorded in a natural environment opposed to being recorded by electronic means. The closer the value is to 0.0 the less acoustic it is and the closer it is to 1.0 the more acoustic it is. **Instrumentalness** predicts how vocal a track is. Thus, songs that contain words other than "Oh" and "Ah" are considered vocal. The closer the value is to 0.0 the less likely the track contains vocals and the closer the value is to 1.0 the more likely it contains vocals. A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry) [5]. **Valence** describes the musical positiveness expressed through a song. Tracks with high valence (closer to 0.0) sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence (closer to 1.0) sound more negative (e.g. sad, depressed, angry) [5]. **Tempo** is the overall pace of a trace measured in BPS (beats per minute). **Key** is the overall approximated pitch that a song is played in. The possible keys and their integer values are: C = 0; C# = 1; D = 2; D#, Eb = 3; E = 4; F = 5; F#, Gb = 6; G = 7; G#, Ab = 8; A = 9; A#, Bb = 10; B, Cb = 11. The overall **loudness** of a track is measured in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db [5].
# Methods

# Results
The data set was imported into jupyter notebook and manipulated so that only rows that had a genre of hip hop or rap were shown. Matplotlib was then used to create a histogram of the column 'danceability'. This plot shows that all hip hop songs from 1921 to 2020 have a range of 0 to 1 but most hip hop songs fall between 0.6 and 0.9.

# references
[1] Nina Avramova, C., 2020. How Music Can Change The Way You Feel And Act. [online] CNN. Available at: <https://www.cnn.com/2019/02/08/health/music-brain-behavior-intl/index.html> [Accessed 5 November 2020].

[2] Savage, P., 2019. Cultural evolution of music. Palgrave Communications, 5(1).

[3] Muscato, C. and Clayton, J., 2020. _Music During The Enlightenment Period_. [online] Study.com. Available at: <https://study.com/academy/lesson/music-during-the-enlightenment-period.html> [Accessed 5 November 2020].

[4] Percino, G., Klimek, P. and Thurner, S., 2014. Instrumentational Complexity of Music Genres and Why Simplicity Sells. _PLoS ONE_, 9(12), p.e115255.

[5] Developer.spotify.com. 2020. _Get Audio Features For A Track | Spotify For Developers_. [online] Available at: <https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/> [Accessed 6 November 2020].

