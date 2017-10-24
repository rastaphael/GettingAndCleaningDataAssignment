Codebook
========
Codebook was generated at 2017-10-24 09:10:32 after generating the data (script run_analysis.R)

Source of the data
------------------

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Description of the data
-----------------------

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Variable list and descriptions
------------------------------

Variable name    | Description
-----------------|------------
subject          | ID the subject who performed the activity for each window sample. Its range is from 1 to 30.
activity         | Activity name
featDomain       | Feature: Time domain signal or frequency domain signal (Time or Freq)
featInstrument   | Feature: Measuring instrument (Accelerometer or Gyroscope)
featAcceleration | Feature: Acceleration signal (Body or Gravity)
featVariable     | Feature: Variable (Mean or SD)
featJerk         | Feature: Jerk signal
featMagnitude    | Feature: Magnitude of the signals calculated using the Euclidean norm
featAxis         | Feature: 3-axial signals in the X, Y and Z directions (X, Y, or Z)
featCount        | Feature: Count of data points used to compute `average`
featAverage      | Feature: Average of each variable for each activity and each subject

Dataset structure
-----------------


```r
str(msSet2)
```

```
## 'data.frame':	180 obs. of  68 variables:
##  $ subject                                            : int  1 1 1 1 1 1 2 2 2 2 ...
##  $ activity                                           : Factor w/ 6 levels "LAYING","SITTING",..: 1 2 3 4 5 6 1 2 3 4 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...49.56      : num  -0.997 -0.999 -1 -0.878 -0.798 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...57.64      : num  -0.996 -0.999 -1 -0.929 -0.79 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...1.16       : num  -0.989 -0.998 -1 -0.77 -0.465 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...25.48      : num  -0.994 -0.999 -1 -0.682 -0.489 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...1.8.1      : num  -0.913 -0.98 -0.998 -0.648 -0.66 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...9.16.1     : num  -0.986 -0.999 -1 -0.358 -0.627 ...
##  $ FrequencyBodyGyro.bandsEnergy...57.64              : num  -0.973 -0.999 -1 -0.965 -0.934 ...
##  $ FrequencyBodyGyro.bandsEnergy...1.16               : num  -0.966 -0.998 -1 -0.875 -0.838 ...
##  $ FrequencyBodyGyro.bandsEnergy...17.32              : num  -0.985 -1 -1 -0.734 -0.851 ...
##  $ FrequencyBodyGyro.bandsEnergy...1.8.1              : num  -0.995 -0.99 -1 -0.459 -0.615 ...
##  $ FrequencyBodyGyro.bandsEnergy...9.16.1             : num  -0.998 -1 -1 -0.932 -0.903 ...
##  $ FrequencyBodyGyro.bandsEnergy...17.24.1            : num  -0.998 -1 -1 -0.807 -0.834 ...
##  $ FrequencyBodyAcceleration.min...Z                  : num  -0.947 -0.962 -0.99 -0.824 -0.762 ...
##  $ FrequencyBodyAcceleration.sma..                    : num  -0.8916 -0.9618 -0.9887 -0.0355 0.0966 ...
##  $ FrequencyBodyAcceleration.energy...X               : num  -0.99 -0.998 -1 -0.739 -0.463 ...
##  $ FrequencyBodyAcceleration.iqr...Z                  : num  -0.954 -0.98 -0.986 -0.469 -0.344 ...
##  $ FrequencyBodyAcceleration.entropy...X              : num  -0.707 -0.88 -0.985 0.629 0.719 ...
##  $ FrequencyBodyAcceleration.entropy...Y              : num  -0.693 -0.808 -0.872 0.588 0.595 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...41.48.2: num  -0.991 -0.999 -1 -0.887 -0.765 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...49.56.2: num  -0.983 -1 -1 -0.844 -0.745 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...57.64.2: num  -0.998 -1 -1 -0.95 -0.879 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...1.24.2 : num  -0.992 -0.999 -1 -0.814 -0.727 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...25.48.2: num  -0.997 -1 -1 -0.923 -0.822 ...
##  $ FrequencyBodyGyro.Mean...X                         : num  -0.85 -0.976 -0.986 -0.339 -0.352 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...33.40  : num  -0.997 -1 -1 -0.851 -0.753 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...41.48  : num  -0.997 -1 -1 -0.79 -0.679 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...49.56  : num  -0.998 -1 -1 -0.847 -0.83 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...49.64  : num  -0.998 -1 -1 -0.844 -0.826 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...1.24   : num  -0.997 -0.999 -1 -0.59 -0.515 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...25.48  : num  -0.994 -0.999 -1 -0.629 -0.459 ...
##  $ FrequencyBodyAcceleration.kurtosis...Z             : num  -0.485 -0.514 -0.556 -0.534 -0.564 ...
##  $ FrequencyBodyAcceleration.bandsEnergy...17.24      : num  -0.995 -0.999 -1 -0.369 -0.448 ...
##  $ FrequencyBodyGyro.bandsEnergy...1.8                : num  -0.968 -0.998 -1 -0.952 -0.858 ...
##  $ FrequencyBodyGyro.bandsEnergy...25.32              : num  -0.99 -1 -1 -0.943 -0.938 ...
##  $ FrequencyBodyAcceleration.mad...Y                  : num  -0.85626 -0.94321 -0.97817 0.09465 -0.00652 ...
##  $ FrequencyBodyAcceleration.max...Y                  : num  -0.857 -0.916 -0.973 -0.306 -0.421 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...1.24.1 : num  -0.985 -0.999 -1 -0.338 -0.561 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...9.16.2 : num  -0.991 -0.999 -1 -0.881 -0.805 ...
##  $ FrequencyBodyAccelerationJerk.kurtosis...Y         : num  -0.88 -0.856 -0.912 -0.615 -0.85 ...
##  $ FrequencyBodyAccelerationJerk.bandsEnergy...1.8    : num  -0.999 -1 -1 -0.821 -0.597 ...
##  $ TimeBodyAccelerationJerk.arCoeff...Y.1             : num  0.15 0.205 0.167 -0.276 -0.215 ...
##  $ TimeBodyAccelerationJerk.arCoeff...Y.2             : num  0.0328 0.0562 0.0293 0.1841 0.1801 ...
##  $ TimeBodyAccelerationJerk.arCoeff...Y.3             : num  0.229 0.281 0.194 0.12 0.124 ...
##  $ TimeBodyAccelerationJerk.correlation...Y.Z         : num  -0.022 0.0166 0.0744 0.4906 0.116 ...
##  $ TimeBodyGyro.Mean...X                              : num  -0.0166 -0.0454 -0.024 -0.0418 -0.0351 ...
##  $ TimeBodyGyro.Mean...Y                              : num  -0.0645 -0.0919 -0.0594 -0.0695 -0.0909 ...
##  $ TimeGravityAcceleration.arCoeff...X.4              : num  0.64 0.568 0.447 0.543 0.745 ...
##  $ TimeGravityAcceleration.arCoeff...Y.1              : num  -0.3854 -0.4613 -0.394 0.0308 -0.2103 ...
##  $ TimeGravityAcceleration.arCoeff...Y.2              : num  0.3503 0.414 0.3507 0.0226 0.2307 ...
##  $ TimeGravityAcceleration.correlation...X.Z          : num  -0.0781 -0.4975 0.1378 -0.0401 -0.2974 ...
##  $ TimeGravityAcceleration.correlation...Y.Z          : num  -0.209 0.301 0.47 0.281 0.101 ...
##  $ TimeBodyAccelerationJerk.Mean...X                  : num  0.0811 0.0775 0.0754 0.074 0.0542 ...
##  $ TimeBodyGyroJerk.correlation...Y.Z                 : num  -0.09497 0.00285 -0.22817 -0.07155 -0.25142 ...
##  $ TimeBodyAccelerationMagnitude.Mean..               : num  -0.8419 -0.9485 -0.9843 -0.137 0.0272 ...
##  $ TimeBodyAccelerationMagnitude.Standard..           : num  -0.7951 -0.9271 -0.9819 -0.2197 0.0199 ...
##  $ TimeBodyAccelerationMagnitude.arCoeff..1           : num  0.0355 0.1458 0.1993 0.0888 -0.1209 ...
##  $ TimeBodyAccelerationMagnitude.arCoeff..2           : num  -0.0455 -0.1353 -0.1867 -0.134 0.0533 ...
##  $ TimeBodyAccelerationMagnitude.arCoeff..3           : num  0.0352 0.1532 0.2403 0.0886 0.1391 ...
##  $ TimeBodyAccelerationJerk.min...Z                   : num  0.93 0.985 0.989 0.434 0.348 ...
##  $ TimeBodyAccelerationJerk.iqr...X                   : num  -0.9692 -0.989 -0.9936 -0.0685 0.0339 ...
##  $ TimeBodyGyro.max...X                               : num  -0.78 -0.875 -0.874 -0.468 -0.466 ...
##  $ TimeBodyGyro.min...Z                               : num  0.7702 0.7829 0.814 0.2389 -0.0788 ...
##  $ TimeBodyGyro.arCoeff...Z.3                         : num  0.0751 0.1138 0.171 -0.172 -0.2105 ...
##  $ TimeBodyGyroJerk.Mean...X                          : num  -0.1073 -0.0937 -0.0996 -0.09 -0.074 ...
##  $ TimeBodyGyro.entropy...X                           : num  -0.245 -0.719 -0.358 0.259 0.247 ...
##  $ TimeBodyGyro.arCoeff...X.3                         : num  0.191 0.259 0.274 0.266 0.131 ...
```

Show a few rows of the dataset
------------------------------


```r
head(msSet2)
```

```
##     subject           activity
## 1         1             LAYING
## 31        1            SITTING
## 61        1           STANDING
## 91        1            WALKING
## 121       1 WALKING_DOWNSTAIRS
## 151       1   WALKING_UPSTAIRS
##     FrequencyBodyAcceleration.bandsEnergy...49.56
## 1                                      -0.9968434
## 31                                     -0.9992440
## 61                                     -0.9999436
## 91                                     -0.8778689
## 121                                    -0.7980321
## 151                                    -0.9451035
##     FrequencyBodyAcceleration.bandsEnergy...57.64
## 1                                      -0.9964651
## 31                                     -0.9989115
## 61                                     -0.9999739
## 91                                     -0.9287484
## 121                                    -0.7903131
## 151                                    -0.9504819
##     FrequencyBodyAcceleration.bandsEnergy...1.16
## 1                                     -0.9891654
## 31                                    -0.9982591
## 61                                    -0.9999612
## 91                                    -0.7703158
## 121                                   -0.4645445
## 151                                   -0.7847287
##     FrequencyBodyAcceleration.bandsEnergy...25.48
## 1                                      -0.9939361
## 31                                     -0.9992246
## 61                                     -0.9999032
## 91                                     -0.6821271
## 121                                    -0.4890609
## 151                                    -0.8896339
##     FrequencyBodyAcceleration.bandsEnergy...1.8.1
## 1                                      -0.9132222
## 31                                     -0.9795867
## 61                                     -0.9983638
## 91                                     -0.6484280
## 121                                    -0.6603970
## 151                                    -0.4033196
##     FrequencyBodyAcceleration.bandsEnergy...9.16.1
## 1                                       -0.9861262
## 31                                      -0.9987483
## 61                                      -0.9997769
## 91                                      -0.3576428
## 121                                     -0.6272106
## 151                                     -0.8482673
##     FrequencyBodyGyro.bandsEnergy...57.64
## 1                              -0.9725660
## 31                             -0.9991539
## 61                             -0.9999245
## 91                             -0.9648468
## 121                            -0.9336095
## 151                            -0.9665481
##     FrequencyBodyGyro.bandsEnergy...1.16
## 1                             -0.9655680
## 31                            -0.9981225
## 61                            -0.9998419
## 91                            -0.8754482
## 121                           -0.8383352
## 151                           -0.8822803
##     FrequencyBodyGyro.bandsEnergy...17.32
## 1                              -0.9847917
## 31                             -0.9996512
## 61                             -0.9999461
## 91                             -0.7339138
## 121                            -0.8511138
## 151                            -0.9355608
##     FrequencyBodyGyro.bandsEnergy...1.8.1
## 1                              -0.9947051
## 31                             -0.9901874
## 61                             -0.9997098
## 91                             -0.4586102
## 121                            -0.6154074
## 151                            -0.2020209
##     FrequencyBodyGyro.bandsEnergy...9.16.1
## 1                               -0.9983642
## 31                              -0.9997574
## 61                              -0.9999567
## 91                              -0.9318743
## 121                             -0.9032415
## 151                             -0.9485038
##     FrequencyBodyGyro.bandsEnergy...17.24.1
## 1                                -0.9977716
## 31                               -0.9997993
## 61                               -0.9999857
## 91                               -0.8070904
## 121                              -0.8340458
## 151                              -0.9336654
##     FrequencyBodyAcceleration.min...Z FrequencyBodyAcceleration.sma..
## 1                          -0.9470158                     -0.89158521
## 31                         -0.9624612                     -0.96181319
## 61                         -0.9898383                     -0.98873969
## 91                         -0.8241520                     -0.03547449
## 121                        -0.7620255                      0.09656391
## 151                        -0.8976861                     -0.25895738
##     FrequencyBodyAcceleration.energy...X FrequencyBodyAcceleration.iqr...Z
## 1                             -0.9897356                        -0.9536027
## 31                            -0.9983408                        -0.9798091
## 61                            -0.9999590                        -0.9857957
## 91                            -0.7392362                        -0.4689636
## 121                           -0.4631486                        -0.3440136
## 151                           -0.7885199                        -0.6837052
##     FrequencyBodyAcceleration.entropy...X
## 1                              -0.7066715
## 31                             -0.8797242
## 61                             -0.9851326
## 91                              0.6294205
## 121                             0.7187189
## 151                             0.4420472
##     FrequencyBodyAcceleration.entropy...Y
## 1                              -0.6929238
## 31                             -0.8079809
## 61                             -0.8717285
## 91                              0.5876419
## 121                             0.5945783
## 151                             0.4177606
##     FrequencyBodyAccelerationJerk.bandsEnergy...41.48.2
## 1                                            -0.9914364
## 31                                           -0.9994937
## 61                                           -0.9996696
## 91                                           -0.8871184
## 121                                          -0.7646908
## 151                                          -0.9636543
##     FrequencyBodyAccelerationJerk.bandsEnergy...49.56.2
## 1                                            -0.9832265
## 31                                           -0.9995361
## 61                                           -0.9995502
## 91                                           -0.8436982
## 121                                          -0.7454550
## 151                                          -0.9635252
##     FrequencyBodyAccelerationJerk.bandsEnergy...57.64.2
## 1                                            -0.9982833
## 31                                           -0.9998254
## 61                                           -0.9998132
## 91                                           -0.9496113
## 121                                          -0.8791880
## 151                                          -0.9835915
##     FrequencyBodyAccelerationJerk.bandsEnergy...1.24.2
## 1                                           -0.9922768
## 31                                          -0.9993441
## 61                                          -0.9998329
## 91                                          -0.8141406
## 121                                         -0.7272801
## 151                                         -0.9227556
##     FrequencyBodyAccelerationJerk.bandsEnergy...25.48.2
## 1                                            -0.9971799
## 31                                           -0.9997474
## 61                                           -0.9998401
## 91                                           -0.9225912
## 121                                          -0.8216472
## 151                                          -0.9807865
##     FrequencyBodyGyro.Mean...X
## 1                   -0.8502492
## 31                  -0.9761615
## 61                  -0.9863868
## 91                  -0.3390322
## 121                 -0.3524496
## 151                 -0.4926117
##     FrequencyBodyAccelerationJerk.bandsEnergy...33.40
## 1                                          -0.9969586
## 31                                         -0.9995051
## 61                                         -0.9999123
## 91                                         -0.8509754
## 121                                        -0.7534584
## 151                                        -0.9432277
##     FrequencyBodyAccelerationJerk.bandsEnergy...41.48
## 1                                          -0.9973905
## 31                                         -0.9995257
## 61                                         -0.9998978
## 91                                         -0.7904480
## 121                                        -0.6793909
## 151                                        -0.9214666
##     FrequencyBodyAccelerationJerk.bandsEnergy...49.56
## 1                                          -0.9977340
## 31                                         -0.9997069
## 61                                         -0.9999231
## 91                                         -0.8473816
## 121                                        -0.8301353
## 151                                        -0.9536931
##     FrequencyBodyAccelerationJerk.bandsEnergy...49.64
## 1                                          -0.9977341
## 31                                         -0.9996671
## 61                                         -0.9999219
## 91                                         -0.8435591
## 121                                        -0.8256258
## 151                                        -0.9524734
##     FrequencyBodyAccelerationJerk.bandsEnergy...1.24
## 1                                         -0.9968131
## 31                                        -0.9994802
## 61                                        -0.9999631
## 91                                        -0.5898445
## 121                                       -0.5151824
## 151                                       -0.8289207
##     FrequencyBodyAccelerationJerk.bandsEnergy...25.48
## 1                                          -0.9937447
## 31                                         -0.9993739
## 61                                         -0.9998777
## 91                                         -0.6292478
## 121                                        -0.4589435
## 151                                        -0.8848956
##     FrequencyBodyAcceleration.kurtosis...Z
## 1                               -0.4853672
## 31                              -0.5143127
## 61                              -0.5557945
## 91                              -0.5338147
## 121                             -0.5640978
## 151                              0.2820412
##     FrequencyBodyAcceleration.bandsEnergy...17.24
## 1                                      -0.9953485
## 31                                     -0.9990174
## 61                                     -0.9999316
## 91                                     -0.3689556
## 121                                    -0.4478219
## 151                                    -0.7922985
##     FrequencyBodyGyro.bandsEnergy...1.8
## 1                            -0.9681661
## 31                           -0.9980475
## 61                           -0.9998429
## 91                           -0.9521085
## 121                          -0.8576697
## 151                          -0.8940281
##     FrequencyBodyGyro.bandsEnergy...25.32
## 1                              -0.9897104
## 31                             -0.9997711
## 61                             -0.9999622
## 91                             -0.9427608
## 121                            -0.9383740
## 151                            -0.9740367
##     FrequencyBodyAcceleration.mad...Y FrequencyBodyAcceleration.max...Y
## 1                        -0.856260899                       -0.85743161
## 31                       -0.943206733                       -0.91609143
## 61                       -0.978165208                       -0.97335798
## 91                        0.094650805                       -0.30590329
## 121                      -0.006524166                       -0.42106736
## 151                      -0.130576928                       -0.04335502
##     FrequencyBodyAccelerationJerk.bandsEnergy...1.24.1
## 1                                           -0.9854256
## 31                                          -0.9991209
## 61                                          -0.9997670
## 91                                          -0.3382463
## 121                                         -0.5606562
## 151                                         -0.7746218
##     FrequencyBodyAccelerationJerk.bandsEnergy...9.16.2
## 1                                           -0.9906347
## 31                                          -0.9994809
## 61                                          -0.9997847
## 91                                          -0.8809250
## 121                                         -0.8048144
## 151                                         -0.9521591
##     FrequencyBodyAccelerationJerk.kurtosis...Y
## 1                                   -0.8796357
## 31                                  -0.8556566
## 61                                  -0.9119207
## 91                                  -0.6152643
## 121                                 -0.8501573
## 151                                 -0.7636985
##     FrequencyBodyAccelerationJerk.bandsEnergy...1.8
## 1                                        -0.9985240
## 31                                       -0.9997805
## 61                                       -0.9999899
## 91                                       -0.8207592
## 121                                      -0.5966515
## 151                                      -0.8407847
##     TimeBodyAccelerationJerk.arCoeff...Y.1
## 1                                0.1504213
## 31                               0.2049490
## 61                               0.1670493
## 91                              -0.2755097
## 121                             -0.2146633
## 151                             -0.3684657
##     TimeBodyAccelerationJerk.arCoeff...Y.2
## 1                               0.03281382
## 31                              0.05623699
## 61                              0.02928544
## 91                              0.18413286
## 121                             0.18008640
## 151                             0.09956520
##     TimeBodyAccelerationJerk.arCoeff...Y.3
## 1                               0.22873536
## 31                              0.28057755
## 61                              0.19443601
## 91                              0.11964226
## 121                             0.12407152
## 151                             0.08028114
##     TimeBodyAccelerationJerk.correlation...Y.Z TimeBodyGyro.Mean...X
## 1                                  -0.02201220           -0.01655309
## 31                                  0.01656442           -0.04535006
## 61                                  0.07443266           -0.02398773
## 91                                  0.49055492           -0.04183096
## 121                                 0.11603402           -0.03507819
## 151                                 0.31290970            0.05054938
##     TimeBodyGyro.Mean...Y TimeGravityAcceleration.arCoeff...X.4
## 1             -0.06448612                             0.6401484
## 31            -0.09192415                             0.5680201
## 61            -0.05939722                             0.4466577
## 91            -0.06953005                             0.5426353
## 121           -0.09093713                             0.7453184
## 151           -0.16617002                             0.7707991
##     TimeGravityAcceleration.arCoeff...Y.1
## 1                              -0.3853901
## 31                             -0.4612740
## 61                             -0.3939920
## 91                              0.0308226
## 121                            -0.2103374
## 151                            -0.4969284
##     TimeGravityAcceleration.arCoeff...Y.2
## 1                               0.3503157
## 31                              0.4140068
## 61                              0.3506950
## 91                              0.0225500
## 121                             0.2307304
## 151                             0.5203897
##     TimeGravityAcceleration.correlation...X.Z
## 1                                 -0.07809749
## 31                                -0.49745395
## 61                                 0.13784963
## 91                                -0.04008333
## 121                               -0.29744534
## 151                               -0.37282873
##     TimeGravityAcceleration.correlation...Y.Z
## 1                                  -0.2091177
## 31                                  0.3014193
## 61                                  0.4698583
## 91                                  0.2812603
## 121                                 0.1013046
## 151                                -0.1780037
##     TimeBodyAccelerationJerk.Mean...X TimeBodyGyroJerk.correlation...Y.Z
## 1                          0.08108653                       -0.094974300
## 31                         0.07748252                        0.002847985
## 61                         0.07537665                       -0.228165476
## 91                         0.07404163                       -0.071551364
## 121                        0.05415532                       -0.251421071
## 151                        0.10137273                       -0.240762605
##     TimeBodyAccelerationMagnitude.Mean..
## 1                            -0.84192915
## 31                           -0.94853679
## 61                           -0.98427821
## 91                           -0.13697118
## 121                           0.02718829
## 151                          -0.12992763
##     TimeBodyAccelerationMagnitude.Standard..
## 1                                -0.79514486
## 31                               -0.92707842
## 61                               -0.98194293
## 91                               -0.21968865
## 121                               0.01988435
## 151                              -0.32497093
##     TimeBodyAccelerationMagnitude.arCoeff..1
## 1                                 0.03545197
## 31                                0.14584735
## 61                                0.19925257
## 91                                0.08881873
## 121                              -0.12089368
## 151                              -0.33909830
##     TimeBodyAccelerationMagnitude.arCoeff..2
## 1                                -0.04554509
## 31                               -0.13525983
## 61                               -0.18667025
## 91                               -0.13399373
## 121                               0.05326677
## 151                               0.24879433
##     TimeBodyAccelerationMagnitude.arCoeff..3
## 1                                 0.03519635
## 31                                0.15324102
## 61                                0.24034954
## 91                                0.08856821
## 121                               0.13907453
## 151                              -0.13735975
##     TimeBodyAccelerationJerk.min...Z TimeBodyAccelerationJerk.iqr...X
## 1                          0.9302030                      -0.96916741
## 31                         0.9847152                      -0.98902343
## 61                         0.9894274                      -0.99360623
## 91                         0.4339613                      -0.06845488
## 121                        0.3484437                       0.03392950
## 151                        0.7013882                      -0.37320836
##     TimeBodyGyro.max...X TimeBodyGyro.min...Z TimeBodyGyro.arCoeff...Z.3
## 1             -0.7801817           0.77020356                 0.07506247
## 31            -0.8754239           0.78285404                 0.11381816
## 61            -0.8737757           0.81397251                 0.17100238
## 91            -0.4680432           0.23891810                -0.17202986
## 121           -0.4664805          -0.07883265                -0.21049517
## 151           -0.4098683           0.42151589                -0.11683705
##     TimeBodyGyroJerk.Mean...X TimeBodyGyro.entropy...X
## 1                 -0.10727095               -0.2446240
## 31                -0.09367938               -0.7193059
## 61                -0.09960921               -0.3581497
## 91                -0.08999754                0.2592242
## 121               -0.07395920                0.2470139
## 151               -0.12223277                0.1294998
##     TimeBodyGyro.arCoeff...X.3
## 1                    0.1905997
## 31                   0.2587339
## 61                   0.2743048
## 91                   0.2661756
## 121                  0.1314289
## 151                  0.1919801
```

Summary 
-------


```r
summary(msSet2)
```

```
##     subject                   activity 
##  Min.   : 1.0   LAYING            :30  
##  1st Qu.: 8.0   SITTING           :30  
##  Median :15.5   STANDING          :30  
##  Mean   :15.5   WALKING           :30  
##  3rd Qu.:23.0   WALKING_DOWNSTAIRS:30  
##  Max.   :30.0   WALKING_UPSTAIRS  :30  
##  FrequencyBodyAcceleration.bandsEnergy...49.56
##  Min.   :-0.9999                              
##  1st Qu.:-0.9996                              
##  Median :-0.9840                              
##  Mean   :-0.9375                              
##  3rd Qu.:-0.8979                              
##  Max.   :-0.5328                              
##  FrequencyBodyAcceleration.bandsEnergy...57.64
##  Min.   :-1.0000                              
##  1st Qu.:-0.9996                              
##  Median :-0.9857                              
##  Mean   :-0.9488                              
##  3rd Qu.:-0.9159                              
##  Max.   :-0.6730                              
##  FrequencyBodyAcceleration.bandsEnergy...1.16
##  Min.   :-1.0000                             
##  1st Qu.:-0.9993                             
##  Median :-0.9470                             
##  Mean   :-0.7915                             
##  3rd Qu.:-0.6620                             
##  Max.   : 0.3908                             
##  FrequencyBodyAcceleration.bandsEnergy...25.48
##  Min.   :-0.9999                              
##  1st Qu.:-0.9992                              
##  Median :-0.9712                              
##  Mean   :-0.8640                              
##  3rd Qu.:-0.7984                              
##  Max.   :-0.1034                              
##  FrequencyBodyAcceleration.bandsEnergy...1.8.1
##  Min.   :-0.9998                              
##  1st Qu.:-0.9932                              
##  Median :-0.8291                              
##  Mean   :-0.7620                              
##  3rd Qu.:-0.5901                              
##  Max.   : 0.1489                              
##  FrequencyBodyAcceleration.bandsEnergy...9.16.1
##  Min.   :-0.9999                               
##  1st Qu.:-0.9989                               
##  Median :-0.9584                               
##  Mean   :-0.8277                               
##  3rd Qu.:-0.7316                               
##  Max.   : 0.0653                               
##  FrequencyBodyGyro.bandsEnergy...57.64
##  Min.   :-1.0000                      
##  1st Qu.:-0.9995                      
##  Median :-0.9842                      
##  Mean   :-0.9720                      
##  3rd Qu.:-0.9515                      
##  Max.   :-0.7725                      
##  FrequencyBodyGyro.bandsEnergy...1.16
##  Min.   :-0.9999                     
##  1st Qu.:-0.9991                     
##  Median :-0.9633                     
##  Mean   :-0.9088                     
##  3rd Qu.:-0.8397                     
##  Max.   :-0.2028                     
##  FrequencyBodyGyro.bandsEnergy...17.32
##  Min.   :-1.0000                      
##  1st Qu.:-0.9995                      
##  Median :-0.9781                      
##  Mean   :-0.9090                      
##  3rd Qu.:-0.8562                      
##  Max.   :-0.2666                      
##  FrequencyBodyGyro.bandsEnergy...1.8.1
##  Min.   :-0.9999                      
##  1st Qu.:-0.9981                      
##  Median :-0.9664                      
##  Mean   :-0.8679                      
##  3rd Qu.:-0.8310                      
##  Max.   : 0.5497                      
##  FrequencyBodyGyro.bandsEnergy...9.16.1
##  Min.   :-1.0000                       
##  1st Qu.:-0.9997                       
##  Median :-0.9938                       
##  Mean   :-0.9514                       
##  3rd Qu.:-0.9378                       
##  Max.   :-0.4454                       
##  FrequencyBodyGyro.bandsEnergy...17.24.1 FrequencyBodyAcceleration.min...Z
##  Min.   :-0.99999                        Min.   :-0.9920                  
##  1st Qu.:-0.99981                        1st Qu.:-0.9792                  
##  Median :-0.99723                        Median :-0.9147                  
##  Mean   :-0.95592                        Mean   :-0.9059                  
##  3rd Qu.:-0.95074                        3rd Qu.:-0.8374                  
##  Max.   : 0.03864                        Max.   :-0.7140                  
##  FrequencyBodyAcceleration.sma.. FrequencyBodyAcceleration.energy...X
##  Min.   :-0.9894                 Min.   :-1.0000                     
##  1st Qu.:-0.9646                 1st Qu.:-0.9993                     
##  Median :-0.6275                 Median :-0.9476                     
##  Mean   :-0.5043                 Mean   :-0.7969                     
##  3rd Qu.:-0.0581                 3rd Qu.:-0.6732                     
##  Max.   : 0.6164                 Max.   : 0.3401                     
##  FrequencyBodyAcceleration.iqr...Z FrequencyBodyAcceleration.entropy...X
##  Min.   :-0.9876                   Min.   :-0.9851                      
##  1st Qu.:-0.9732                   1st Qu.:-0.8308                      
##  Median :-0.8596                   Median :-0.1432                      
##  Mean   :-0.7185                   Mean   :-0.1289                      
##  3rd Qu.:-0.4695                   3rd Qu.: 0.5684                      
##  Max.   : 0.1403                   Max.   : 0.8462                      
##  FrequencyBodyAcceleration.entropy...Y
##  Min.   :-0.9702                      
##  1st Qu.:-0.7787                      
##  Median :-0.1121                      
##  Mean   :-0.1192                      
##  3rd Qu.: 0.5388                      
##  Max.   : 0.7349                      
##  FrequencyBodyAccelerationJerk.bandsEnergy...41.48.2
##  Min.   :-0.9997                                    
##  1st Qu.:-0.9991                                    
##  Median :-0.9884                                    
##  Mean   :-0.9339                                    
##  3rd Qu.:-0.9012                                    
##  Max.   :-0.4617                                    
##  FrequencyBodyAccelerationJerk.bandsEnergy...49.56.2
##  Min.   :-0.9996                                    
##  1st Qu.:-0.9989                                    
##  Median :-0.9816                                    
##  Mean   :-0.9226                                    
##  3rd Qu.:-0.8771                                    
##  Max.   :-0.4346                                    
##  FrequencyBodyAccelerationJerk.bandsEnergy...57.64.2
##  Min.   :-0.9999                                    
##  1st Qu.:-0.9996                                    
##  Median :-0.9923                                    
##  Mean   :-0.9676                                    
##  3rd Qu.:-0.9477                                    
##  Max.   :-0.6550                                    
##  FrequencyBodyAccelerationJerk.bandsEnergy...1.24.2
##  Min.   :-0.9999                                   
##  1st Qu.:-0.9992                                   
##  Median :-0.9790                                   
##  Mean   :-0.8860                                   
##  3rd Qu.:-0.8059                                   
##  Max.   :-0.1739                                   
##  FrequencyBodyAccelerationJerk.bandsEnergy...25.48.2
##  Min.   :-0.9999                                    
##  1st Qu.:-0.9996                                    
##  Median :-0.9946                                    
##  Mean   :-0.9551                                    
##  3rd Qu.:-0.9323                                    
##  Max.   :-0.5624                                    
##  FrequencyBodyGyro.Mean...X
##  Min.   :-0.9931           
##  1st Qu.:-0.9697           
##  Median :-0.7300           
##  Mean   :-0.6367           
##  3rd Qu.:-0.3387           
##  Max.   : 0.4750           
##  FrequencyBodyAccelerationJerk.bandsEnergy...33.40
##  Min.   :-0.9999                                  
##  1st Qu.:-0.9996                                  
##  Median :-0.9804                                  
##  Mean   :-0.9086                                  
##  3rd Qu.:-0.8612                                  
##  Max.   :-0.4019                                  
##  FrequencyBodyAccelerationJerk.bandsEnergy...41.48
##  Min.   :-0.99991                                 
##  1st Qu.:-0.99952                                 
##  Median :-0.97769                                 
##  Mean   :-0.88688                                 
##  3rd Qu.:-0.82368                                 
##  Max.   :-0.07642                                 
##  FrequencyBodyAccelerationJerk.bandsEnergy...49.56
##  Min.   :-0.9999                                  
##  1st Qu.:-0.9997                                  
##  Median :-0.9884                                  
##  Mean   :-0.9364                                  
##  3rd Qu.:-0.8964                                  
##  Max.   :-0.4424                                  
##  FrequencyBodyAccelerationJerk.bandsEnergy...49.64
##  Min.   :-0.9999                                  
##  1st Qu.:-0.9997                                  
##  Median :-0.9877                                  
##  Mean   :-0.9340                                  
##  3rd Qu.:-0.8895                                  
##  Max.   :-0.4278                                  
##  FrequencyBodyAccelerationJerk.bandsEnergy...1.24
##  Min.   :-1.0000                                 
##  1st Qu.:-0.9996                                 
##  Median :-0.9668                                 
##  Mean   :-0.8224                                 
##  3rd Qu.:-0.6801                                 
##  Max.   : 0.2385                                 
##  FrequencyBodyAccelerationJerk.bandsEnergy...25.48
##  Min.   :-0.9999                                  
##  1st Qu.:-0.9993                                  
##  Median :-0.9714                                  
##  Mean   :-0.8394                                  
##  3rd Qu.:-0.7612                                  
##  Max.   : 0.1319                                  
##  FrequencyBodyAcceleration.kurtosis...Z
##  Min.   :-0.9074                       
##  1st Qu.:-0.6656                       
##  Median :-0.5029                       
##  Mean   :-0.4885                       
##  3rd Qu.:-0.3507                       
##  Max.   : 0.3863                       
##  FrequencyBodyAcceleration.bandsEnergy...17.24
##  Min.   :-0.99993                             
##  1st Qu.:-0.99946                             
##  Median :-0.97166                             
##  Mean   :-0.83954                             
##  3rd Qu.:-0.73150                             
##  Max.   : 0.08288                             
##  FrequencyBodyGyro.bandsEnergy...1.8 FrequencyBodyGyro.bandsEnergy...25.32
##  Min.   :-0.9999                     Min.   :-1.0000                      
##  1st Qu.:-0.9991                     1st Qu.:-0.9997                      
##  Median :-0.9732                     Median :-0.9886                      
##  Mean   :-0.9190                     Mean   :-0.9533                      
##  3rd Qu.:-0.8543                     3rd Qu.:-0.9303                      
##  Max.   :-0.2556                     Max.   :-0.6261                      
##  FrequencyBodyAcceleration.mad...Y FrequencyBodyAcceleration.max...Y
##  Min.   :-0.99100                  Min.   :-0.9916                  
##  1st Qu.:-0.95167                  1st Qu.:-0.9465                  
##  Median :-0.56098                  Median :-0.6444                  
##  Mean   :-0.47264                  Mean   :-0.6252                  
##  3rd Qu.:-0.03382                  3rd Qu.:-0.3328                  
##  Max.   : 0.62985                  Max.   : 0.1239                  
##  FrequencyBodyAccelerationJerk.bandsEnergy...1.24.1
##  Min.   :-0.99987                                  
##  1st Qu.:-0.99895                                  
##  Median :-0.95043                                  
##  Mean   :-0.78960                                  
##  3rd Qu.:-0.61957                                  
##  Max.   : 0.04776                                  
##  FrequencyBodyAccelerationJerk.bandsEnergy...9.16.2
##  Min.   :-0.9998                                   
##  1st Qu.:-0.9992                                   
##  Median :-0.9809                                   
##  Mean   :-0.8859                                   
##  3rd Qu.:-0.8117                                   
##  Max.   :-0.1559                                   
##  FrequencyBodyAccelerationJerk.kurtosis...Y
##  Min.   :-0.9119                           
##  1st Qu.:-0.8713                           
##  Median :-0.8440                           
##  Mean   :-0.8198                           
##  3rd Qu.:-0.7941                           
##  Max.   :-0.3058                           
##  FrequencyBodyAccelerationJerk.bandsEnergy...1.8
##  Min.   :-1.0000                                
##  1st Qu.:-0.9999                                
##  Median :-0.9730                                
##  Mean   :-0.8437                                
##  3rd Qu.:-0.7823                                
##  Max.   : 0.2930                                
##  TimeBodyAccelerationJerk.arCoeff...Y.1
##  Min.   :-0.40603                      
##  1st Qu.:-0.26356                      
##  Median :-0.09719                      
##  Mean   :-0.08829                      
##  3rd Qu.: 0.08570                      
##  Max.   : 0.27588                      
##  TimeBodyAccelerationJerk.arCoeff...Y.2
##  Min.   :-0.188049                     
##  1st Qu.: 0.006348                     
##  Median : 0.062627                     
##  Mean   : 0.074525                     
##  3rd Qu.: 0.149392                     
##  Max.   : 0.433814                     
##  TimeBodyAccelerationJerk.arCoeff...Y.3
##  Min.   :-0.0716                       
##  1st Qu.: 0.1017                       
##  Median : 0.1702                       
##  Mean   : 0.1702                       
##  3rd Qu.: 0.2332                       
##  Max.   : 0.4544                       
##  TimeBodyAccelerationJerk.correlation...Y.Z TimeBodyGyro.Mean...X
##  Min.   :-0.31108                           Min.   :-0.20578     
##  1st Qu.:-0.04482                           1st Qu.:-0.04712     
##  Median : 0.05496                           Median :-0.02871     
##  Mean   : 0.08490                           Mean   :-0.03244     
##  3rd Qu.: 0.18125                           3rd Qu.:-0.01676     
##  Max.   : 0.60828                           Max.   : 0.19270     
##  TimeBodyGyro.Mean...Y TimeGravityAcceleration.arCoeff...X.4
##  Min.   :-0.20421      Min.   :0.3353                       
##  1st Qu.:-0.08955      1st Qu.:0.5128                       
##  Median :-0.07318      Median :0.6326                       
##  Mean   :-0.07426      Mean   :0.6294                       
##  3rd Qu.:-0.06113      3rd Qu.:0.7486                       
##  Max.   : 0.02747      Max.   :0.9070                       
##  TimeGravityAcceleration.arCoeff...Y.1
##  Min.   :-0.6907                      
##  1st Qu.:-0.4831                      
##  Median :-0.3811                      
##  Mean   :-0.3407                      
##  3rd Qu.:-0.2093                      
##  Max.   : 0.1586                      
##  TimeGravityAcceleration.arCoeff...Y.2
##  Min.   :-0.1888                      
##  1st Qu.: 0.2123                      
##  Median : 0.3548                      
##  Mean   : 0.3297                      
##  3rd Qu.: 0.4652                      
##  Max.   : 0.6885                      
##  TimeGravityAcceleration.correlation...X.Z
##  Min.   :-0.93782                         
##  1st Qu.:-0.36721                         
##  Median :-0.07883                         
##  Mean   :-0.09704                         
##  3rd Qu.: 0.16853                         
##  Max.   : 0.90239                         
##  TimeGravityAcceleration.correlation...Y.Z
##  Min.   :-0.93050                         
##  1st Qu.:-0.06627                         
##  Median : 0.12905                         
##  Mean   : 0.09574                         
##  3rd Qu.: 0.35840                         
##  Max.   : 0.73379                         
##  TimeBodyAccelerationJerk.Mean...X TimeBodyGyroJerk.correlation...Y.Z
##  Min.   :0.04269                   Min.   :-0.499421                 
##  1st Qu.:0.07396                   1st Qu.:-0.234438                 
##  Median :0.07640                   Median :-0.109466                 
##  Mean   :0.07947                   Mean   :-0.109814                 
##  3rd Qu.:0.08330                   3rd Qu.: 0.004153                 
##  Max.   :0.13019                   Max.   : 0.289402                 
##  TimeBodyAccelerationMagnitude.Mean..
##  Min.   :-0.9865                     
##  1st Qu.:-0.9573                     
##  Median :-0.4829                     
##  Mean   :-0.4973                     
##  3rd Qu.:-0.0919                     
##  Max.   : 0.6446                     
##  TimeBodyAccelerationMagnitude.Standard..
##  Min.   :-0.9865                         
##  1st Qu.:-0.9430                         
##  Median :-0.6074                         
##  Mean   :-0.5439                         
##  3rd Qu.:-0.2090                         
##  Max.   : 0.4284                         
##  TimeBodyAccelerationMagnitude.arCoeff..1
##  Min.   :-0.56892                        
##  1st Qu.:-0.21750                        
##  Median :-0.04885                        
##  Mean   :-0.08446                        
##  3rd Qu.: 0.06548                        
##  Max.   : 0.28086                        
##  TimeBodyAccelerationMagnitude.arCoeff..2
##  Min.   :-0.235496                       
##  1st Qu.:-0.084091                       
##  Median : 0.004993                       
##  Mean   : 0.036414                       
##  3rd Qu.: 0.150350                       
##  Max.   : 0.426517                       
##  TimeBodyAccelerationMagnitude.arCoeff..3 TimeBodyAccelerationJerk.min...Z
##  Min.   :-0.24046                         Min.   :-0.08623                
##  1st Qu.:-0.05100                         1st Qu.: 0.44951                
##  Median : 0.08174                         Median : 0.85418                
##  Mean   : 0.04983                         Mean   : 0.71102                
##  3rd Qu.: 0.15324                         3rd Qu.: 0.97659                
##  Max.   : 0.28179                         Max.   : 0.99183                
##  TimeBodyAccelerationJerk.iqr...X TimeBodyGyro.max...X
##  Min.   :-0.9949                  Min.   :-0.88734    
##  1st Qu.:-0.9846                  1st Qu.:-0.86062    
##  Median :-0.8172                  Median :-0.71093    
##  Mean   :-0.5801                  Mean   :-0.62024    
##  3rd Qu.:-0.2074                  3rd Qu.:-0.40577    
##  Max.   : 0.5336                  Max.   : 0.04731    
##  TimeBodyGyro.min...Z TimeBodyGyro.arCoeff...Z.3 TimeBodyGyroJerk.Mean...X
##  Min.   :-0.4033      Min.   :-0.47800           Min.   :-0.15721         
##  1st Qu.: 0.2820      1st Qu.:-0.16170           1st Qu.:-0.10322         
##  Median : 0.6771      Median : 0.01317           Median :-0.09868         
##  Mean   : 0.5299      Mean   :-0.02356           Mean   :-0.09606         
##  3rd Qu.: 0.8048      3rd Qu.: 0.13581           3rd Qu.:-0.09110         
##  Max.   : 0.8353      Max.   : 0.27448           Max.   :-0.02209         
##  TimeBodyGyro.entropy...X TimeBodyGyro.arCoeff...X.3
##  Min.   :-0.71931         Min.   :-0.2238           
##  1st Qu.:-0.34760         1st Qu.: 0.0537           
##  Median :-0.09527         Median : 0.1352           
##  Mean   :-0.12497         Mean   : 0.1241           
##  3rd Qu.: 0.11823         3rd Qu.: 0.2155           
##  Max.   : 0.30246         Max.   : 0.3625
```
