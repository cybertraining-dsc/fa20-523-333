---
date: 2021-03-15
title: Does Modern Day Music Lack Uniqueness Compared to Music before the 21st Century
linkTitle: Music uniquness
tags: ["project", "ai", "lifestyle"]
description: his project looked at 99 years of spotify music data and determined that all features of most tracks have changed in different ways. Because uniqueness can be related to variation the variation of different features were used to determine if tracks did lack uniqueness. Through data analysis it was concluded that they did.
author: Raymond Adams
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-333/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-333/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-333/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-333/actions)
Status: final, Type: Project

* Raymond Adams, fa20-523-333
* [Edit](https://github.com/cybertraining-dsc/fa20-523-333/blob/main/project/project.md)

{{% pageinfo %}}

## Abstract

One of the most influential aspects of human culture is music. It has a way of changing as humans evolve themselves. Music has changed drastically over the last 100 years. Before the 21<sup>st</sup> century most people seemed to welcome the change. However, in the 2000's people began stating that music seemed to be changing for the worse. Music, usually adults perspectives, has began lacking uniqueness. These statements come from interviews, speaking with family and friends, tv shows, and movies. This project looked at 99 years of spotify music data and determined that all features of most tracks have changed in different ways. Because uniqueness can be related to variation the variation of different features were used to determine if tracks did lack uniqueness. Through data analysis it was concluded that they did.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** music, spotify data, uniqueness, music evolution, 21<sup>st</sup> century music.

## 1. Introduction

Music is one of the most influential elements in the arts. It has a great impact on the way humans act and feel. Research, done by Nina Avramova, has shown that different genres of music bring about different emotions and feelings through the listener. Nonetheless, humans also have a major impact on the music itself. Music and humans are mutually dependent, therefore when one evolves, so does the other.

This scientific journal intends to progress the current understanding of how music has changed since the 21<sup>st</sup> century. It also aims to determine if this change in music has led to a lack of uniqueness amongst the common features of a song compared to music before the 21<sup>st</sup> century.

## 2. Data

The data is located on Kaggle and was collected by a data scientist named Yamac Eren Ay. He collected more than 160,000 songs from Spotify that ranged from 1921 to 2020. Some of the features that this data set includes and will be used to conduct an analysis are: danceability, energy, acousticness, instrumentalness, valence, tempo, key, and loudness. This data frame can be seen in Figure 1.

![dataframe](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/DataFrame.png)

**Figure 1:** Dataframe of spotify data collected from Kaggle

**Danceability** describes how appropriate a track is for dancing by looking at multiple elements including tempo, rhythm stability, beat strength, and general regularity. The closer the value is to 0.0 the less danceable the song is and the closer it is to 1.0 the more danceable it is. **Energy** is a sensual measure of intensity and activity. Usually, energetic songs feel fast, loud, and noisy. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy [^5]. The closer this value is to 0.0 the less energetic the track is and the closer it is to 1.0 the more energetic the track is. **Acoustic** music refers to songs that are created using instruments and recorded in a natural environment as opposed to being recorded by electronic means. The closer the value is to 0.0 the less acoustic it is and the closer it is to 1.0 the more acoustic it is. **Instrumentalness** predicts how vocal a track is. Thus, songs that contain words other than "Oh" and "Ah" are considered vocal. The closer the value is to 0.0 the less likely the track contains vocals and the closer the value is to 1.0 the more likely it contains vocals. **Valence** describes the musical positiveness expressed through a song. Tracks with high valence (closer to 0.0) sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence (closer to 1.0) sound more negative (e.g. sad, depressed, angry) [^5]. The **tempo** is the overall pace of a track measured in BPM (beats per minute). The **key** is the overall approximated pitch that a song is played in. The possible keys and their integer values are: C = 0; C# = 1; D = 2; D#, Eb = 3; E = 4; F = 5; F#, Gb = 6; G = 7; G#, Ab = 8; A = 9; A#, Bb = 10; B, Cb = 11. The overall **loudness** of a track is measured in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing the relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 dB, 0 being the most loud [^5].

## 3. Methods

Data analysis was used to answer this paper's research question. The data set was imported into Jupyter notebook using pandas, a software library built for data manipulation and analysis. The first step was cleaning the data. The data set contained 169,909 rows and 19 columns. After dropping rows where at least one column had NaN values, values that are undefined or unrepresentable, the data set still contained all 169,909 rows. Thus, the data set was cleaned by Yamac Ay prior to it being downloaded. The second step in the data analysis was editing the data. The objective of this research was to compare music tracks before the 21<sup>st</sup> century to tracks after the 21<sup>st</sup> century and see if, how, and why they differ. As well as do tracks after the 21<sup>st</sup> century lack uniqueness compared to tracks that were created before the 21<sup>st</sup> century.

When Yamac Ay collected the data he separated it into five comma-separated values (csv) files. The first file, titled data.csv, contained all the information that was needed to conduct data analysis. Although this file contained the feature "year" that was required to analyze the data based on the period of time, it still needed to be manipulated to distinguish what years were attributed to before and after the 21<sup>st</sup> century. A python script was built to create a new column titled "years_split" that sorted all rows into qualitative binary values. These values were defined as "before_21st_century" and "after_21st_century". Rows, where the tracks feature "year" were between 0 and 2000 were assigned to "before_21st_century" and tracks where the feature "year" was between 2001 and 2020 were assigned to "after_21st_century". It is important to note that over 76% of the rows were attributed to "before_21st_century". Therefore, the majority of tracks collected in this dataset were released before 2001.

## 4. Results

The features that were analyzed were quantitative values. Thus, it was decided that histograms were the best plots for examining and comparing the data. The first feature that was analyzed is "danceability". The visualization for danceability is seen in Figure 2.

![danceability](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/danceability_histogram_before_and_after_21stcentury.png)

**Figure 2:** Danceability shows how danceable a song is

The histogram assigned to "before_21st_century" resembles a normal distribution. The **mean** of the histogram is 0.52 while the **mode** is 0.57. The **variance** of the data is 0.02986. The histogram assigned to "after_21st_century" closely resembles a normal distribution. The **mean** is 0.59 and the **mode** is 0.61. The **variance** of the data is 0.02997. The bulk of the data before the 21<sup>st</sup> century lies between 0.2 and 0.8. However, when looking at the data after the 21<sup>st</sup> century the majority of it lies between 0.4 and 0.9. This implies that songs have become more danceable but the variation of less danceable to danceable is practically the same.

The second feature that was analyzed is "energy". The visualization for energy is seen in Figure 3.

![energy](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/energy_histogram_before_and_after_21stcentury.png)

**Figure 3:** Energy shows how energetic a song is

The histogram assigned to "before_21st_century" does not resemble a normal distribution. The **mean** of the histogram is 0.44 while the **mode** is 0.25. The **variance** of the data is 0.06819. The histogram assigned to "after_21st_century" also does not resemble a normal distribution. The **mean** is 0.65 and the **mode** is 0.73. The **variance** of the data is 0.05030. The data before the 21<sup>st</sup> century is skewed right while the data after the 21<sup>st</sup> century is skewed left. This indicates that tracks have become much more energetic since the 21<sup>st</sup> century. Songs before 2001 on average have an energy level of 0.44 but there are still many songs with high energy levels. Where as, songs after 2001 on average have an energy level of 0.65 but there are very few songs with low energy levels.

The third feature that was analyzed was "acousticness". The visualization for acousticness is seen in Figure 4.

![acousticness](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/acousticness_histogram_before_and_after_21stcentury.png)

**Figure 4:** Acousticness shows how acoustic (type of instrument as a collective) a song is

The  **mean** of the histogram assigned to "before_21st_century" is 0.57 while the **mode** is 0.995. The **variance** of the data is 0.13687. The histogram assigned to "after_21st_century" has a **mean** of 0.26 and **mode** of 0.114. The **variance** of the data is 0.08445 . The graph shows that music made before the 21<sup>st</sup> century varied from non-acoustic to acoustic. However, when analyzing music after the 21<sup>st</sup> century the graph shows that most music is created using non-acoustic instruments. It is assumed that this change in outlet of sounds is due to music production transitioning from acoustic to analog to now digital. However, more in depth research would need to be completed to confirm this assumption.

The fourth histogram to be anaylzed was "instrumentalness". The visualization for instrumentalness is seen in Figure 5.

![instrumentalness](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/instrumentalness_histogram_before_and_after_21stcentury.png)

**Figure 5:** Instrumentalness shows how instrumental a song is

The **mean** of the histogram assigned to "before_21st_century" is 0.19 while the **mode** is 0.0. The **variance** of the data is 0.10699. The histogram assigned to "after_21st_century" has a **mean** of 0.07 and **mode** of 0.0. The **variance** of the data is 0.04786 . By analyzing the graph it appears that the instrumentalness for before and after the 21<sup>st</sup> century are relatively similar. Both histograms are skewed right but the histogram attributed to after the 21<sup>st</sup> century has much less songs that are instrumental compared to songs before the 21<sup>st</sup> century. The variation of non-instrumental to instrumental tracks after the 21<sup>st</sup> century is all far less compared to tracks before the  21<sup>st</sup> century.

The fifth histogram that was analyzed is "valence". The visualization for valence is seen in Figure 6.

![valence](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/valence_histogram_before_and_after_21stcentury.png)

**Figure 6:** Valence shows how positive a song is

The **mean** of the histogram assigned to "before_21st_century" is 0.54 while the **mode** is 0.961. The **variance** of the data is 0.07035. The histogram assigned to "after_21st_century" has a **mean** of 0.49 and **mode** of 0.961. The **variance** of the data is 0.06207. By analyzing the graph we can see that the valence before and after the 21<sup>st</sup> century has remained fairly the same in terms of shape. However, the average value of valence after the 21<sup>st</sup> century decreased by 0.05. Thus, songs have become less positive but there are still a good amount of positive songs being created.

The sixth histogram that was analyzed is "tempo". The visualization for tempo is seen in Figure 7.

![tempo](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/tempo_histogram_before_and_after_21stcentury.png)

**Figure 7:** Tempo shows the speed a song is played in

The **mean** of the histogram attributed to "before_21st_century"is 115.66. The **variance** of the data is 933.57150. The histogram assigned to "after_21st_century" has a **mean** of 121.19. The **variance** of the data is 955.44287. This indicates that tracks after the 21<sup>st</sup> century have increased tempo by a little over 6 BPM. Tracks after the 21<sup>st</sup> century also have more variation than tracks before the 21<sup>st</sup> century.

The seventh histogram that was analyzed is "key". The visualization for key is seen in Figure 8.

![key](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/key_histogram_before_and_after_21stcentury.png)

**Figure 8:** Key labels the overall pitch a song is in

The **mean** of the histogram assigned to "before_21st_century" is 5.19 The **variance** of the data is 12.22468. The histogram assigned to "after_21st_century" has a **mean** of 5.24. The **variance** of the data is 12.79017. This information implies that the key of songs have mostly stayed the same hoever, there are less songs after the 21<sup>st</sup> century being created in C, C#, and D compared to songs before the 21<sup>st</sup> century. The key of songs after 2001 are also more spread out compared to songs before 2001.

The eighth histogram that was analyzed is "loudness". The visualization for loudness is seen in Figure 9.

![loudness](https://github.com/cybertraining-dsc/fa20-523-333/raw/main/project/images/loudness_histogram_before_and_after_21stcentury.png)

**Figure 9:** Loudness shows the average decibels a track is played in

The **mean** of the histogram assigned to "before_21st_century" is -12.60 while the **mode** is -11.82. The **variance** of the data is 29.17625. The histogram assigned to "after_21st_century" has a **mean** of -7.32 and **mode** of -4.80. The **variance** of the data is 20.35049. The shapes of both histograms are the same, however the histogram attributed to after the 21<sup>st</sup> century shifted to the right by 5.28. This displays the increase in loudness of songs created after 2001. The variance of the data shows that songs after 2001 are mostly very loud. Wheres as, songs before 2001 had greater variation of less loud to more loud.

## 5. Conclusion

Music over the centuries has continuously changed. This change has typically been embraced by the masses. However, in the early 2000s adults who grew up on different styles of music began stating through word of mouth, interviews,  tv shows, and movies that "music isn't the same anymore". They even claimed that most current songs sound the same and lack uniqueness. This scientific research set out to determine how music has changed and if in fact, modern music lacks uniqueness.

After analyzing the songs before and after the 21<sup>st</sup> century it was determined that all the features of a track have changed in some way. The danceability, energy, tempo, and loudness of a song have increased. While the acousticness, valence, and instrumentalness have decreased. The number of songs after the  21<sup>st</sup> century that was created in the key of C, C#, and D has decreased. The variation of energetic, acoustic, instrumental, valent, and loud songs have decreased since 2001. While the variation of tempo and key has increased since 2001.

The factor for determining whether music lacks uniqueness in this paper will be variance. If a feature has more than alpha = 0.01 difference of variability from before to after the 21<sup>st</sup> century then it will be determined that the feature is less unique after the 21<sup>st</sup> century. The difference in variances among the feature "energetic" is 0.01789, "acousticness" is 0.05242, "instrumentalness" is 0.05913,  "valence" is 0.00828, and "loudness" is 8.82576. Thus, the only feature that does not lack uniqueness when compared to songs before the 21<sup>st</sup> century is "valence". Based on this information music overall after the 21<sup>st</sup> century lacks uniqueness compared to music before the 21<sup>st</sup> century.

This lack of uniqueness did not start after the 21<sup>st</sup> century. It started during the Enlightenment period. During this period of time, classical music was the most popular genre of music. Before this era, Baroque music was extremely popular. Artists such as Johann Sebastian Bach created complex compositions that were played for the elite. This style of music "was filled with complex melodies and exaggerated ornamentation, music of the Enlightenment period was technically simpler." [^3] Instead of focusing on these complexities the new music focused on enjoyment, pleasure, and being memorable. People now wanted to be able to hum and play songs themselves. This desired feature has caused music to constantly become simpler. Thus, reducing songs variances amongst features.

A further step that could be taken in this research is predicting what these features will look like in the future. Machine learning could be used to make this prediction. This would give music enthusiasts and professionals a greater understanding of where music is headed and how to adapt.

## 5.1 Limitations

Initially this project was supposed to be conducted on Hip-Hop music. However, the way the data was collected and stored did not allow for this analysis to be done. In the future a more in depth analysis could be conducted on a specific genre.

## 7. References

[^1]: Nina Avramova, C., 2020. How Music Can Change The Way You Feel And Act. [online] CNN. Available at: <https://www.cnn.com/2019/02/08/health/music-brain-behavior-intl/index.html> [Accessed 5 November 2020].

[^2]: Savage, P., 2019. Cultural evolution of music. Palgrave Communications, 5(1).

[^3]: Muscato, C. and Clayton, J., 2020. _Music During The Enlightenment Period_. [online] Study.com. Available at: <https://study.com/academy/lesson/music-during-the-enlightenment-period.html> [Accessed 5 November 2020].

[^4]: Percino, G., Klimek, P. and Thurner, S., 2014. Instrumentational Complexity of Music Genres and Why Simplicity Sells. _PLoS ONE_, 9(12), p.e115255.

[^5]: Developer.spotify.com. 2020. _Get Audio Features For A Track | Spotify For Developers_. [online] Available at: <https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/> [Accessed 6 November 2020].

[^6]: dzone.com. 2020. _What Is P-Value (In Layman Terms)? - Dzone Big Data_. [online] Available at: <https://dzone.com/articles/what-is-p-value-in-layman-terms> [Accessed 8 November 2020].
