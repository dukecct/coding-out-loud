Doctors of Dr. Who
================
Mine Çetinkaya-Rundel + Evan Dragich
11/30/2021

``` r
library(tidyverse)
library(here)
```

``` r
knitr::opts_chunk$set(
  fig.width = 8,
  fig.asp = 0.618,
  fig.retina = 3,
  dpi = 300,
  out.width = "90%"
)
```

``` r
episodes <- read_csv(here::here("01-dr-who", "data/episodes.csv"))
imdb <- read_csv(here::here("01-dr-who", "data/imdb.csv"))
```

## Task 1: Recreate

Recreate the following plot (Source:
<https://www.independent.ie/entertainment/doctor-who-suffers-lowest-ratings-since-2005-revival-39028919.html>).

[<img src="https://image.assets.pressassociation.io/v2/image/production/3fe8f7647e7f1e4f6e5b298f1fa288c0Y29udGVudHNlYXJjaCwxNTgzODU3MjQy/2.51242519.jpg?w=1280" width="500" />](https://www.independent.ie/entertainment/doctor-who-suffers-lowest-ratings-since-2005-revival-39028919.html)

## Task 2: Improve

Improve the plot above.

## Task 3: Doctors and seasons

In the revived era there have been five doctors, see
[here](https://en.wikipedia.org/wiki/List_of_Doctor_Who_episodes_(2005%E2%80%93present)#Regular_seasons)
for which doctors were in which seasons. Recreate the previous
visualization, this time including doctor information.

``` r
doctors <- tribble(
  ~season_number, ~doctor_no, ~doctor_name,
               1,          9, "Christopher Eccleston",
               2,         10, "David Tennant",
               3,         10, "David Tennant",
               4,         10, "David Tennant",
               5,         11, "Matt Smith",
               6,         11, "Matt Smith",
               7,         11, "Matt Smith",
               8,         12, "Peter Capaldi",
               9,         12, "Peter Capaldi",
              10,         12, "Peter Capaldi",
              11,         13, "Jodie Whittaker",
              12,         13, "Jodie Whittaker",
)
```

## Task 4: Episode descriptions

Visualize the common words in episode descriptions.
