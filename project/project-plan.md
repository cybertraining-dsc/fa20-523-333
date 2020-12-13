# Using Spotify Data To Determine If Popular Modern-day Songs Lack Uniqueness Compared To Popular Songs Before The 21st Century

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-333/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-333/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-333/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-333/actions)
Status: in progress, Type: Project

- [ ] please follow our template
- [ ] please remove first person
- [ ] do not use I
- [ ] what is progress?
- [ ] Refernces missing

Raymond Adams, [fa20-523-333](https://github.com/cybertraining-dsc/fa20-523-333/), [Edit](https://github.com/cybertraining-dsc/fa20-523-333/blob/main/project/project.md)

{{% pageinfo %}}

## Abstract

MISSING.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** missing


## 1. Introduction

I will be looking at Spotify data, a music streaming service, to answer my research question, "Do popular modern-day songs lack uniqueness compared to popular songs before the year 2000?" Music has always been a way to express oneself. Before the new era of music began most songs seemed to have a unique sound and feel that brought the listener back for more. However, nowadays it seems that most songs that become popular have similar characteristics. The goal of this research is to study whether popular modern-day songs lack the uniqueness that songs had before January 1, 2001.

## 2. Data

The dataset that I will be using was created by Yamaç Eren Ay. He is a data scientist at EYU from İstanbul, İstanbul, Turkey. This data set was collected from Spotify's web API. It contains data on songs from 1921-2019.

The variables include:

Numerical values [**acousticness**  (Ranges from 0 to 1),  **danceability**  (Ranges from 0 to 1), energy (Ranges from 0 to 1),  **duration_ms**  (Integer typically ranging from 200k to 300k),  **instrumentalness**  (Ranges from 0 to 1),  **valence**  (Ranges from 0 to 1),  **popularity**  (Ranges from 0 to 100),  **tempo**  (Float typically ranging from 50 to 150),  **liveness**  (Ranges from 0 to 1),  **loudness**  (Float typically ranging from -60 to 0),  **speechiness**  (Ranges from 0 to 1),  **year**  (Ranges from 1921 to 2020)]

Dummy values [**mode**  (0 = Minor, 1 = Major),  **explicit**  (0 = No explicit content, 1 = Explicit content)]

Categorical [**key**  (All keys on octave encoded as values ranging from 0 to 11, starting on C as 0, C# as 1 and so on…),  **artists**  (List of artists mentioned),  **release_date**  (Date of release mostly in yyyy-mm-dd format, however precision of date may vary),  **name**  (Name of the song)]

## 3. What needs to be done to get a great grade

In order to complete the project and receive a good grade I will need complete a couple steps. First, I will import my data set through Google collab or Jupyter Notebook and create code to visualize and analyze the data. Next I will create markdown cells to explain the code and data used throughout the project. Lastly, I will create a paper report explaining my findings from the software component of my project. The most important part of this project is stating my hypothesis and answering my research question. My hypothesis is that songs after 2012 that have a popular score greater than x will have similar features such as, liveliness, loudness, tempo, and key. Whereas I suspect that popular songs before the 21st century are more differentiable among these features. 
