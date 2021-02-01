# Fetal-Health-Classification
Classification of Fetal Health using ML Models

# Heading 1
## Heading 2
### Heading 3
#### Heading 4

_Italics_
**Bold**
~~axe~~ 

Links:
[Google!](https://www.google.com "Google")

Images:
![Google Logo](https://blog.hubspot.com/hubfs/image8-2.jpg "Logo")

Use `for` loop

```Python
sns.distplot()
```

Tables:
|Table |Goes |Here |
|--- |--- |--- |

>Just Another Quote.

>Another another quote. 

---

Lists:
1. List one
   - sub one
   - sub two
2. List two
   1. sub one
   2. sub two
3. List three
- List four

***

Cardiotocography (CTG) is used during pregnancy to monitor fetal heart rate and uterine contractions. It is monitor fetal well-being and allows early detection of fetal distress.

CTG interpretation helps in determining if the pregnancy is high or low risk. An abnormal CTG may indicate the need for further investigations and potential intervention.

In this project, I will create a model to classify the outcome of Cardiotocogram test to ensure the well being of the fetus.

On This Dataset Cardiotocograms (CTGs) are a simple and cost accessible option to assess fetal health, allowing healthcare professionals to take action in order to prevent child and maternal mortality. The equipment itself works by sending ultrasound pulses and reading its response, thus shedding light on fetal heart rate (FHR), fetal movements, uterine contractions and more.

This dataset contains 2126 records of features extracted from Cardiotocogram exams, which were then classified by expert obstetrician into 3 classes:

Normal
Suspect
Pathological
Features

'baseline value' FHR baseline (beats per minute)
'accelerations' Number of accelerations per second
'fetal_movement' Number of fetal movements per second
'uterine_contractions' Number of uterine contractions per second
'light_decelerations' Number of light decelerations per second
'severe_decelerations' Number of severe decelerations per second
'prolongued_decelerations' Number of prolonged decelerations per second
'abnormal_short_term_variability' Percentage of time with abnormal short term variability
'mean_value_of_short_term_variability' Mean value of short term variability
'percentage_of_time_with_abnormal_long_term_variability' Percentage of time with abnormal long term variability
'mean_value_of_long_term_variability' Mean value of long term variability
'histogram_width' Width of FHR histogram
'histogram_min' Minimum (low frequency) of FHR histogram
'histogram_max' Maximum (high frequency) of FHR histogram
'histogram_number_of_peaks' Number of histogram peaks
'histogram_number_of_zeroes' Number of histogram zeros
'histogram_mode' Histogram mode
'histogram_mean' Histogram mean
'histogram_median' Histogram median
'histogram_variance' Histogram variance
'histogram_tendency' Histogram tendency

Target

'fetal_health' Tagged as 1 (Normal), 2 (Suspect) and 3 (Pathological)


I spotted outliers on our dataset. However, it is not quite a good idea to remove them yet as it may lead to overfitting. Though we may end up with better statistics.

A basic rule of thumb for the outliers in question is:

It is a measurement error or data entry error, correct the error if possible. If you can’t fix it, remove that observation. In our case, this is the outcome of a CTG report so it is unlikely that this was a data entry error.

If it is not a part of the population you are studying, you can legitimately remove the outlier. In this case, this all is about the fetus, and experts tag the classification. Let's stick with the expert opinion.

Thus assuming that these are the natural part of the population we are studying, we should not remove it.

2126 fetal cardiotocograms (CTG) were automatically processed and the respective diagnostic features measured. The CTG were also classified by three expert obstetricians and a consensus classification label assigned to each of them. Classification was both with respect to a morphologic pattern (A, B, C. ...) and to a fetal state (N, S, P). Therefore the dataset can be used either for 10-class or 3-class experiments.