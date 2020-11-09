## Does Modern Day Music Lack Uniqueness Compared to Music before the 21<sup>st</sup> Century

# Introduction
Music is one of the most influential elements in the arts. It has a great impact on the way humans act and feel. Research, done by Nina Avramova, has shown that different genres of music bring about different emotions and feelings through the listener. Nonetheless, humans also have a major impact on music itself. Music and humans are mutually dependent therefore when one evolves, so does the other. 

This journal intends to progress the current understanding of if, how, and why music has changed since the 21<sup>st</sup> century. It also aims to determine if this change in music has led to a lack of uniqueness amongst the common features of a song compared to music before the 21<sup>st</sup> century.  
# Data
The data is located on Kaggle and was collected by a data scientist named Yamac Eren Ay. He collected more than 160,000 songs from Spotify that ranged from 1921 to 2020. Some of the features that this data set includes and will be used to conduct an analysis are: danceability, energy, acousticness, instrumentalness, valence, tempo, key, and loudness.  

(insert DataFrame)

**Danceability** describes how appropriate a track is for dancing by looking at multiple elements including tempo, rhythm stability, beat strength, and general regularity. The closer the value is to 0.0 the less danceable the song is and the closer it is to 1.0 the more danceable it is. **Energy** is a sensual measure of intensity and activity. Usually energetic songs feel fast, loud, and noisy. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy [5]. The closer this value is to 0.0 the less energetic the track is and the closer it is to 1.0 the more energetic the track is. **Acoustic** music refers to songs that are created using instruments and recorded in a natural environment opposed to being recorded by electronic means. The closer the value is to 0.0 the less acoustic it is and the closer it is to 1.0 the more acoustic it is. **Instrumentalness** predicts how vocal a track is. Thus, songs that contain words other than "Oh" and "Ah" are considered vocal. The closer the value is to 0.0 the less likely the track contains vocals and the closer the value is to 1.0 the more likely it contains vocals. A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry) [5]. **Valence** describes the musical positiveness expressed through a song. Tracks with high valence (closer to 0.0) sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence (closer to 1.0) sound more negative (e.g. sad, depressed, angry) [5]. **Tempo** is the overall pace of a trace measured in BPS (beats per minute). **Key** is the overall approximated pitch that a song is played in. The possible keys and their integer values are: C = 0; C# = 1; D = 2; D#, Eb = 3; E = 4; F = 5; F#, Gb = 6; G = 7; G#, Ab = 8; A = 9; A#, Bb = 10; B, Cb = 11. The overall **loudness** of a track is measured in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db [5].
# Methods
Data analysis was used to answer this papers research question. The data set was imported into Jupyter notebook using pandas, a software library built for data manipulation and analysis. The first step was cleaning the data. The data set contained 169,909 rows and 19 columns. After dropping rows where at least one column had NaN values, values that are undefined or unrepresentable, the data set still contained all 169,909 rows. Thus, the data set was cleaned by Yamac Ay. The second step in the data analysis was editing the data. The objective of this research was to compare music tracks before the 21<sup>st</sup>century to tracks after the 21<sup>st</sup>century and see if, how, and why they differ. As well as do tracks after the 21<sup>st</sup> century lack uniqueness compared to tracks that were created prior to the 21<sup>st</sup>century. 

When Yamac Ay collected the data he separated it into five comma-separated values (csv) files. The first file, titled data.csv, contained all the information that was needed to conduct a data analysis. Although, this file contained the feature "year" that was required to analyze the data based on the period of time, it still needed to be manipulated to distinguish what years were attributed to before and after the 21<sup>st</sup>century. A python script was built to create a new column titled "years_split" that sorted all rows into qualitative binary values. These values were defined as "before_21st_century" and "after_21st_century". Rows where the tracks feature "year" were between 0 and 2000 were assigned to "before_21st_century" and tracks where the feature "year" were between 2001 and 2020 were assigned to "after_21st_century". It is important to note that over 76% of the rows were attributed to "before_21st_century". Therefore, the majority of tracks collected in this dataset were released before 2001. 

# Results
The features that were analyzed were quantitative values. Thus, it was decided that histograms were the best plots for examining and comparing the data. The first feature that was analyzed is "danceability".  ![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/danceability_histogram_before_and_after_21stcentury.png)   

The histogram assigned to "before_21st_century" resembles a normal distribution. The **mean** of the histogram is 0.52 while the **mode** is 0.57. The **variance** of the data is 0.02986. The histogram assigned to "after_21st_century" closely resembles a normal distribution. The **mean** is 0.59 and the **mode** is 0.61. The **variance** of the data is 0.02997. The bulk of the data before the 21<sup>st</sup> century lies between 0.2 and 0.8. However, when looking at the data after the 21<sup>st</sup> century the majority of it lie between 0.4 and 0.9. This implies that songs have becomes more danceable but the variation of values is practically the same. 

The second feature that was analyzed is "energy". ![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/energy_histogram_before_and_after_21stcentury.png)

The histogram assigned to "before_21st_century" does not resemble a normal distribution. The **mean** of the histogram is 0.44 while the **mode** is 0.25. The **variance** of the data is 0.06819. The histogram assigned to "after_21st_century" also does not resemble a normal distribution. The **mean** is 0.65 and the **mode** is 0.73. The **variance** of the data is 0.05030. The data before the 21<sup>st</sup> century is skewed right while the data after the 21<sup>st</sup> century is skewed left. This indicates that tracks have become much more energetic since the 21<sup>st</sup> century. Songs before 2001 on average have an energy level of 0.44 but there are still a good amount of song with high energy levels. Where as, songs after 2001 on average have an energy level of 0.65 but there are very few songs with low energy levels. 

The third feature that was analyze was "acousticness". ![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/acousticness_histogram_before_and_after_21stcentury.png)

When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is 0.57 while the **mode** is 0.995. The **variance** of the data is 0.13687. The histogram assigned to "after_21st_century" also does not resemble a normal distribution. The **mean** is  0.26 and the **mode** is 0.114. The **variance** of the data is 0.08445 . The graph shows that music made before the 21<sup>st</sup> century varied from non-acoustic to acoustic. However, when analyzing music after the 21<sup>st</sup> century the graph shows that most music is created using non-acoustic instruments. It is assumed that this change in outlet of sounds is due to music production transitioning from acoustic to analog to now digital. However, more in depth research would need to be completed to confirm this assumption. 



The fourth histogram to be anaylzed was "instrumentalness". ![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/instrumentalness_histogram_before_and_after_21stcentury.png)

When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is 0.19 while the **mode** is 0.0. The **variance** of the data is 0.10699. The histogram assigned to "after_21st_century" **mean** is  0.07 and the **mode** is 0.0. The **variance** of the data is 0.04786 . By analyzing the graph it appears that the instrumentalness for before and after the 21<sup>st</sup> century are relatively similar. Both histograms are skewed right  but the histogram attributed to after the 21<sup>st</sup> century has much less songs that are instrumental compared to song before the 21<sup>st</sup> century. 

The fifth histogram that was analyzed is "valence" 

![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/valence_histogram_before_and_after_21stcentury.png)

When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is 0.54 while the **mode** is 0.961. The **variance** of the data is 0.07035. The histogram assigned to "after_21st_century" **mean** is  0.49 and the **mode** is 0.961. The **variance** of the data is 0.06207. By analyzing the graph we can see that the valence before and after the 21<sup>st</sup> century has remained fairly the same in terms of shape. However, the average value of valence after the 21<sup>st</sup> century decreased by 0.05. Thus, songs have become less positive but there are still a good amount of positive songs being created.

The sixth histogram that was analyzed is "tempo". 

![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/tempo_histogram_before_and_after_21stcentury.png)

When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is 115.66. The **variance** of the data is 933.57150. The histogram assigned to "after_21st_century"  **mean** is 121.19. The **variance** of the data is 955.44287. This indicates that tracks after the 21<sup>st</sup> century have increased tempo by a little over 6 BPM. 

The seventh histogram that was analyzed is "key". 

![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/key_histogram_before_and_after_21stcentury.png)

When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is 5.19 The **variance** of the data is 12.22468. The histogram assigned to "after_21st_century"  **mean** is 5.24. The **variance** of the data is 12.79017. The key of song have mostly stayed the same hoever, there are less songs after the 21<sup>st</sup> century being created in C, C#, and D compared to songs before the 21<sup>st</sup> century. 



The eighth histogram that was analyzed is "loudness". 

![](/Users/rayadams/Documents/GitHub/fa20-523-333/images/loudness_histogram_before_and_after_21stcentury.png)



When analyzing the histogram assigned to "before_21st_century" the **mean** of the histogram is -12.60 while the **mode** is -11.82. The **variance** of the data is 29.17625. The histogram assigned to "after_21st_century" **mean** is  -7.32 and the **mode** is -4.80. The **variance** of the data is 20.35049. The shapes of both histograms are the same, however the histogram attributed to after the  21<sup>st</sup> century shifted to the right by 5.28. This is  an important statstic because music has become much louder and our ears are not meant to be exposed to this amount of loudness. 

# Conclusion 



# References
[1] Nina Avramova, C., 2020. How Music Can Change The Way You Feel And Act. [online] CNN. Available at: <https://www.cnn.com/2019/02/08/health/music-brain-behavior-intl/index.html> [Accessed 5 November 2020].

[2] Savage, P., 2019. Cultural evolution of music. Palgrave Communications, 5(1).

[3] Muscato, C. and Clayton, J., 2020. _Music During The Enlightenment Period_. [online] Study.com. Available at: <https://study.com/academy/lesson/music-during-the-enlightenment-period.html> [Accessed 5 November 2020].

[4] Percino, G., Klimek, P. and Thurner, S., 2014. Instrumentational Complexity of Music Genres and Why Simplicity Sells. _PLoS ONE_, 9(12), p.e115255.

[5] Developer.spotify.com. 2020. _Get Audio Features For A Track | Spotify For Developers_. [online] Available at: <https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/> [Accessed 6 November 2020].

[6] dzone.com. 2020. _What Is P-Value (In Layman Terms)? - Dzone Big Data_. [online] Available at: <https://dzone.com/articles/what-is-p-value-in-layman-terms> [Accessed 8 November 2020].