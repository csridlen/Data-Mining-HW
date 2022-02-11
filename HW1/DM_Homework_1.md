# Problem 1

## Which seasons have the most delays?

A delay is considered to be a departure delay length of over 9 minutes,
which is the average length of departure delays for all flights. The
table below displays the number of delayed flights per season. It
appears that Spring has the highest number of delays, while Fall
significantly has the lowest.

    ## # A tibble: 4 x 2
    ##   Season Counts
    ##   <chr>   <int>
    ## 1 Spring   6513
    ## 2 Summer   6388
    ## 3 Winter   6281
    ## 4 Fall     3185

## Does this change by destination?

We are considering only the top 10 arrival destinations for ABIA. Their
IATA codes along with the number of flights arriving there are included.

    ## # A tibble: 10 x 2
    ## # Groups:   Dest [10]
    ##    Dest      n
    ##    <chr> <int>
    ##  1 DAL    5573
    ##  2 DFW    5506
    ##  3 IAH    3691
    ##  4 PHX    2783
    ##  5 DEN    2673
    ##  6 ORD    2514
    ##  7 HOU    2319
    ##  8 ATL    2252
    ##  9 LAX    1733
    ## 10 JFK    1358

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-5-1.png)

# Problem 2

Let’s work with the `billboard` data set.

## Part A

Here, we display the top 10 most popular songs since 1958.

    ## # A tibble: 10 x 3
    ## # Groups:   performer [10]
    ##    performer                              song                             count
    ##    <chr>                                  <chr>                            <int>
    ##  1 Imagine Dragons                        Radioactive                         87
    ##  2 AWOLNATION                             Sail                                79
    ##  3 Jason Mraz                             I'm Yours                           76
    ##  4 The Weeknd                             Blinding Lights                     76
    ##  5 LeAnn Rimes                            How Do I Live                       69
    ##  6 LMFAO Featuring Lauren Bennett & Goon~ Party Rock Anthem                   68
    ##  7 OneRepublic                            Counting Stars                      68
    ##  8 Adele                                  Rolling In The Deep                 65
    ##  9 Jewel                                  Foolish Games/You Were Meant Fo~    65
    ## 10 Carrie Underwood                       Before He Cheats                    64

## Part B

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-9-1.png)
\#\# Part C

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-11-1.png)

# Problem 3

    ## # A tibble: 132 x 2
    ##    event                                       height95
    ##    <chr>                                          <dbl>
    ##  1 Athletics Women's 1,500 metres                  172 
    ##  2 Athletics Women's 10 kilometres Walk            170 
    ##  3 Athletics Women's 10,000 metres                 168.
    ##  4 Athletics Women's 100 metres                    180.
    ##  5 Athletics Women's 100 metres Hurdles            176 
    ##  6 Athletics Women's 20 kilometres Walk            173 
    ##  7 Athletics Women's 200 metres                    180 
    ##  8 Athletics Women's 3,000 metres                  170 
    ##  9 Athletics Women's 3,000 metres Steeplechase     177.
    ## 10 Athletics Women's 4 x 100 metres Relay          176 
    ## # ... with 122 more rows

## Part B

    ## # A tibble: 1 x 2
    ##   event                      max_sdheight
    ##   <chr>                             <dbl>
    ## 1 Rowing Women's Coxed Fours         10.9

## Part C

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-16-1.png)

# Problem 4

    ##    K  rmse350   rmse65
    ## 1  2 11719.18 24905.52
    ## 2  5  9959.78 22235.74
    ## 3 10 10376.27 23245.25
    ## 4 25 10925.11 22754.99
    ## 5 50 10902.29 23347.27
    ## 6 75 11107.50 27706.89

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-20-1.png)
The RMSEs out of sample for 350 Trim and 65 AMG Trim are both minimized
at K = 10. This may be because 10 is around the median value for K, and
does the best at the minimizing bias-variance tradeoff.

![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-22-1.png)![](DM_Homework_1_files/figure-markdown_strict/unnamed-chunk-22-2.png)
