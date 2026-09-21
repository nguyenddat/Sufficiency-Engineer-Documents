---
title: "Applying facts characterization in the annotations aiding system: study cases"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Applying facts characterization in the annotations aiding system: study cases

[[Initial thesis index|Index]] · [[08-evaluating-fact-characterization|← Previous chapter]] · [[10-general-conclusions-and-perspectives|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Applying facts characterization in the annotations
aiding system : study cases

The annotations recovered from real study cases in the last chap-
ter, are implemented in the Cooperative and Interactive learning in
this chapter. Each of the examples allowed to evaluate important fea-
tures such as : the declaration of the moment of start and end of the
fact, the time step considered, the use of features extractors, the use
of multiple sensors as well as labels imbalance in the classification
process.

characterization of facts

### 9.1 Testing cooperative and interactive learning using the semantic

annotations for the characterization of facts
In this section, the Interactive and Cooperative Learning processes (ICL) are tested using the
recovered annotations of the sites "gamma" and "kappa", as well as the data from the installed
sensors. This tests were carried out with the intention to observe the results obtained, using the
modality label for the classification process i.e. the annotations recovered from the How ? question.
Let’s remember that in chapter 6, the ICL approaches were used with a database containing
information about activities labels. However, in this thesis, it is proposed to recover multiple la-
bels from the inhabitants, not just one. Using the semantic annotations to characterize facts, there
are 6 labels that can be associated to a fact (Why ? (intention), How ? (modality), Who ? (people
involved), What ? (objects involved), When ? (time period), Where ? (place). More over, in the
questions that evaluate also the performance, there are 7 labels. However, in this section, only the
label How ? (modality) is used for the Cooperative and Interactive learning process. Next, some
experiments are tested using this label for the learning process. It should be mentioned that this
was just a test to make observations in the classification process by using this label. This might
not be the final method to use in the ICL in a real-time interaction process.
The modality annotation was chosen, given that this is mainly linked to the measurements re-
gistered by the sensors. For instance, when using the washing machine at 60°C, the measurements
of energy consumption are different to the ones of a washing cycle of 30°C. Nonetheless they are
similar between them. Meaning that the discretization in the cooperative learning process could be
basically the same for all the cases of 30°C and basically the same for the cases of 60°C.
The labels utilized were not generated, they were actually recovered from two sites in which
inhabitants annotated manually the characterization of facts every time that the facts happened
as presented in the previous chapter. For this tests (given that there was no real time interaction
between the human and the computerized system and given the available data) in the moments in
which the fact was not annotated manually (either due to inhabitants absence or lack of occurrence
of the relevant fact of the experience) the label "no annotation" was automatically generated in the
computerized system. The objective was to provide a label at all times for the Cooperative and
Interactive learning process. In this way the system will classify between two options, when the
fact happens and when it doesn’t.
In a system with real time interaction, the inhabitant will have to provide a label that can
indicate that there is lack of occurrence of the fact of the experience -if it is the case- when the
inhabitant is asked to provide annotations. While the system might have maybe to automatically
provide a different and specific label to indicate if the inhabitant never answered to the request of
annotation. This should be developed in future work.
The labels collected from the inhabitants have been analysed previously in chapter 8. The
sensors were installed in the homes of the people who made the annotations. The hour of the day
is considered in the Cooperative and Interactive learning process.

#### 9.1.1 Uni-modal annotated facts and analysis of several factors affecting the results

When recovering the annotations from the inhabitants, in several experiments, the answer to
the question How ? (the modality) was unique (uni-modal) but repeated every time that the fact
was annotated through the experiment. This leads to tests as the the one carried out in chapter 6
when only the label of the activity cooking was used in the interactive and cooperative learning
process. However it is possible that the annotations could be provided as such ; with no variety on
the annotations responding to the question How ?
Considering this, we carried out the tests using the annotations provided by the inhabitants and
it was evaluated how several factors may affect the results, such as the time-step considered, the
correct declaration of the moment of start and end of the fact and the sensors selected.

Evaluating the declaration of the moment of start and end of the fact. Experiment 1 study
case : How much energy do I consume when I use the dishwasher in different washing pro-
grams and in different contexts ?
In the annotations provided by the occupants, they provided 2 different labels in the modality
section : half and full charge. However, during interviews with the occupants, they mentioned that
they annotated this to declare the number of objects inserted in the dishwasher. The occupants
mentioned that there is no option in the machine to configure a cycle in half or full charge. They
also mentioned that the configuration they choose all the time is "1h 60°C". In order to be more
specific, let’s use this label as modality. Half full or full charge would have worked if the machine
had this options of configuration. It is considered more accurately to use the "1h 60°C" annotation
for the test of the method. Notice that in all the moments that the fact does not occur, the label "no
annotation" is automatically provided. Any other activity could be happening, but it is not part
of the experiment. Therefore, two possible labels will be classified "1h 60°C" or "no annotations"
information.
The sensor chosen for the classification was the energy consumption of dishwasher, only.
The hour of the day was also considered, given that it was observed in the annotations of the
occupant that the fact was mainly repeated after midday around 14h or in the night around 21h.
The experiment lasted 1 month (30 days) and time slots of 30 minutes were considered for the
classification. In all the moments when no annotation were provided (meaning that the dishwasher
was not in use or that the occupant missed adding an annotation, the classification considered the
label "no annotation".
During the interactive learning process of the artificial system were observed 55 information
requests to the occupants from the total of 1464 time slots registered (1 month with time slots
every 30 minutes), meaning that in the rest 1409 time slots, the classification of the facts was auto-
matically performed by the artificial system. The ideal is that the minimum requests of information
or “notifications” are sent to the occupant, making the learning process, efficient. The number of
notifications and confusions per day can be observed in the next tables (see Table ?? and see Table
?? ).

Day            1    2    3       4   5    6     7    8       9   10   11   12   13   14   15

Notification   22   0    4       4   2    7     1    1       2   2    0    1    3    0    0

Confusions     0    0    0       0   0    1     0    0       1   0    0    0    0    0    0

TABLE 9.1 – Number of notifications and confusions per day, from day 1 to day 15

Day             16   17   18       19      20   21    22       23      24   25   26   27   28   29   30

Notification    0    0    0        1       0    0     0        0       1    1    0    0    1    0    2

Confusions      0    0    0        0       0    0     0        0       0    1    0    0    0    0    0

TABLE 9.2 – Number of notifications and confusions per day, from day 15 to day 30

After the cooperative and interactive learning phase, the learning system was able to estimate

characterization of facts

the fact. When the label “60°C-1h” was classified, it reached an accuracy of 57%, meaning that
from 42 times that the fact happened, 24 times was accurately predicted by the artificial system and
was incorrectly predicted 18 times as "no annotation" . The "no annotation" label was classified
with an accuracy of 93%, guessing 1319 times out of the 1422 times it actually appeared. To
analyze the classifier’s incorrect predictions, a confusion matrix was displayed. The F-score of
the classification of the label "60°C-1h” is 73%. These results are given by the density algorithm,
explained in (Silva et al., 2022) using a random forest classifier. Globally the accuracy reached
was of 91.73%.

No annotation    60°C-1h

No annotation    1319             103

60°C-1h          18               24

TABLE 9.3 – Confusion matrix

Predicted        Predicted

Expected    True negative    False positive

Expected    False negative   True positive

TABLE 9.4 – Generalization of the confusion matrix

Figure 9.1 – Average energy consumption in kWh every 30 minutes. In blue, the classified labels
as "60°C 1h". In red, the classified labels as "no annotation"

In the image 9.1, it can be associated the power consumption (values in the y axis) and the
labeled facts. In the x axis, the date and time. The blue points represent the power consumption
measurements classified as "60°C 1h", the modality of the washing machine, while the red points
are the measurements classified as "no annotation".
It was not a fact repeated everyday. Sometimes, in more than 2 days, the dishwasher was not
used, which lead to have many "no annotations" labels and a more limited number of the "1h
60°C" labels. When more information is provided, the classification can be more accurate. This
can explain why the label "no annotation" reached a high accuracy while the "1h 60°C" annotation
reached a lower accuracy.

characterization of facts

Figure 9.2 – Washing cycles lasting 2h. Average energy consumption in kWh every 30 minutes.
In blue, the classified labels as "60°C 1h". In red, the classified labels as "no annotation"

It was labeled by the inhabitant that the washing cycle lasted 1h, but the measurements from
the sensors show that there is power consumption during two hours (see Figure 9.2). Possibly a
mistake made by the inhabitant in the annotations.
When making the classification considering that the annotation was provided for 2h. The F1
score of the fact classification increased to 76% and accuracy was of 61%. For the no-annotation
classification, f1 score increased to 99% and accuracy was of 98%, which means that less mistakes
were made than when the annotation was considered of 2h. Notice that there are less blue dots
when there is no power consumption (see Figure 9.3) . A global accuracy of 96% was reached.

Day            1    2    3       4   5    6     7    8       9   10   11   12   13   14   15

Notification   23   2    4       4   2    7     1    2       2   2    0    1    4    0    0

Confusions     0    2    0       1   1    0     2    0       0   0    1    0    0    0

TABLE 9.5 – Number of notifications and confusions per day, from day 1 to day 15. Considering
labels of 2h

Day             16   17   18       19      20   21    22       23      24   25   26   27   28   29   30

Notification    0    0    0        1       0    0     0        0       0    1    1    0    1    2    2

Confusions      0    0    0        0       0    0     0        0       1    0    0    0    0    0    0

TABLE 9.6 – Number of notifications and confusions per day, from day 15 to day 30. Considering
labels of 2h.

No annotation    60°C-1h

No annotation   1359             23

60°C-1h         33               51

TABLE 9.7 – Confusion matrix. Considering labels of 2h.

Figure 9.3 – Classification with labels lasting 2h. Average energy consumption in kWh every 30
minutes. In blue, the classified labels as "60°C 1h". In red, the classified labels as "no annotation"

This experiment showed that if only one modality is provided as a label, the test is equivalent
to the previous test presented in chapter 6. No further information was provided from this test in
that sense. Nevertheless, it was noticed, when observing the power consumption, that the washing
cycle actually lasts 2h, while the occupant annotated it lasted 1h. In this case the occupant might
have made the mistake in each annotation. A constant mistake from the inhabitant is an aspect that
the cooperative learning algorithm cannot solve. This mistake resulted in a lower accuracy in the
learning process. More precise methods of human-machine interaction could be used to declare
the start and end of facts. Some authors used a system of buttons rather that letting to the occupants
memory the period of time that the activities took. Still they had to remember to push the button
to declare the start and end of the activities. However this method required of predefined labels,
therefore no freedom of adding different information was possible for the occupants (Thomas and
Cook, 2016). Otherwise the system could automatically detect the duration of the facts by using
a change point detection method as the one showed in chapter 6 to correct the duration of the
activity. This option was not tested in this thesis, but it could be interesting to study it.

characterization of facts

Evaluating the time step considered, the use of a binary feature extractor and the use of
multiple sensors. Experiment 2 study case : Does the room temperature drop when I open
the living room window ?

In the annotations provided by the occupants for this experiment, they actually provided no
label to respond to the How ? question for this experiment. Most probably since there are not many
different ways of opening the window. Still in one of the annotations, the occupants mentioned
"open a few". The annotation when the occupant wrote "open a few" had to be skipped, the start
time and end time was not labeled. Note that the different widths of the window opening could
have been interesting.
For study proposes, the uni-modal annotation "window opened" was used, in all the moments
of the opening window. The experiment lasted 10 days and 10 annotations were provided. In all
the moments when no annotation were provided (meaning that the fact was not carried out or that
the occupant missed adding an annotation, the classification considered the label "no annotation".
Meaning that two labels are used : "window opened" and "no annotation".
In this part, a feature extractor providing a binary output was tested, in the Cooperative and
Interactive learning, due to the type of experiment in which the inhabitant is interested about the
moments when the window is open or close.
Different time steps for the learning process were also evaluated in this study case. It was
considered that the time step should be close to the shortest period of the interested activity. (Kri-
shnan and Cook, 2014) state that using a time step smaller than the real duration of the activities,
might not contain enough information and using a long time step might consider information of
different activities.
Lastly, a test was carried out to observe the results when using a single sensor (window contact
sensor) and when using a set of sensors : the window contact sensor and the motion sensor in the
room. (Yoon et al., 2022) found that when combining information, for example, environmental
and energy consumption data, using random forest (the same classifier used in the cooperative and
interactive learning) they achieved a minimal f1 score of 0.97 for 4 out of the 7 activities studied.
In their studies, 9 days lasted the experiment, the time step was considered of one minute interval,
and 9455 observations were analysed excluding missing data or outliers.
Bear in mind that this experiment (using the contact sensor from the window) could have been
solved using the annotations-free recognition, given that the information of when the window
is opened or closed, can be recovered directly from the contact sensor. Nevertheless when the
annotations were recovered we were interested in collecting as well the information about the
"why" and "how" opening the window was described. Therefore in cases as this one, in which
more information would like to be collected, the annotations-based recognition would need to be
used.
It was asked to the inhabitants to annotate every time the window was opened. From the 13
annotations recovered, in only two occasions the inhabitant intended to reduce the temperature of
the room. The rest of the time, the main intention was to ventilate. However, the temperature could
have been impacted. This can be a typical case in winter, for instance, the temperature of the room
could be impacted even when the intention of opening the window is to ventilate the room.
The fact lasted at least 2h (according to the annotations provided). In a first test, the time
step considered for the classification was of 1 hour. In the second test, the time step is reduced to
30 minutes, and one can observe how the results are negatively impacted in the second test. The
sensor used for the first test was the contact sensor of the window. The hour of the day was also
considered for the classification, given that the window was opened mainly during the day.
Due to the interest of the question (Does the temperature lower’s when the window is open ?)
and the nature of the sensor (contact sensor), it was used a feature extractor that, rather than
discretizing the sensor measurements in different levels, such as low, medium or high, the contact
sensor will record the raw values as 1 or 0 if the window is opened or closed, respectively.

The raw data is re-sampled to determine the percentage of time a window remains open during
a given time-slot. A value of 100% indicates that the window was open for the entire duration
of the time-slot. After re-sampling, the data is processed by the feature generator. A threshold is
applied : if the window is detected as open for at least 20% of the time-slot, it is classified as "open"
(1) ; otherwise, it is classified as "closed" (0). For instance, in a 1-hour period, if the sensor records
the window as open for at least 12 minutes, it is considered "open." This approach accounts for
the delay in temperature changes after the window is opened, i.e. the temperature might not lower
down instantaneously after the window is opened.
They were observed 53 information requests to the occupants from the total of 245 time slots
registered, meaning that in the rest 192 time slots, the classification of the label was automatically
performed by the artificial system. The number of notifications and confusions per day can be
observed in the next tables (see Table ?? ).

Day              1    2         3     4   5   6    7   8   9   10

Notification     18   10        3     9   3   2    2   3   2   1

Confusions       0    0         0     1   1   0    0   2   0   0

TABLE 9.8 – Number of notifications and confusions per day, from day 1 to day 10

When the label "window opened" was classified, it reached an accuracy of 67%, meaning that
from 45 times that the window was opened, 30 times was accurately predicted by the artificial
system while it was incorrectly predicted 15 times as "no annotation" . The "no annotations"
label was classified with an accuracy of 81%, guessing 162 times out of the 199 times it actually
appeared. To analyze the classifier’s incorrect predictions, a confusion matrix was displayed. The
F-score of the label classified is 80%. These results are given by the density algorithm, explained
in (Silva et al., 2022) using a random forest classifier. Globally the accuracy reached was of 79%.

No annotation       Window opened

No annotation          162                 37

Window opened          15                  30

TABLE 9.9 – Confusion matrix

characterization of facts

In (see figure 9.4) it is plotted when the window is open (1) or closed (0). The colors of the
dots, represent the way in which labels were classified. In blue the moments classified as "window
opened" and in red the labels classified as "no annotation" given that no other annotation was
provided by the occupants. Only when the window was opened, it was annotated.

Figure 9.4 – Window open or closed. In blue, the classified labels as "window opened". In red,
the classified labels as "no annotation"

Figure 9.5 answers the question of the occupant. It can be seen the moments classified as
"window opened" in blue and "no annotation" in red. The curve of green dots represents the tem-
perature of the room. It is mainly during the night that the temperature lowered, during the day,
the temperature increased. The window was mainly opened during the day, but sometimes it was
opened in the late afternoon. In green the outdoor temperature is plotted. The data used for the out-
door temperature was retrieved from (Weather Underground, 2024). It is interesting to observe the
outdoor temperature to compare it with the internal temperature. When the internal temperature is
higher in the room, then solar gains, occupants radiated heat, building inertia, etc. influence in the
room temperature, more than the effect of air current that could refresh the air, when the window
is opened. It can be observed that the building keeps the heat at temperatures not lower than 23°C
even if outside is 15°C as in the 7th of july at 6am. This means that opening the window during
the day did not help to decrease the temperature in the room. A different option could be tested
by the occupants such as opening the window in the nights.

Figure 9.5 – Temperature of the room when opening the window. In blue, the classified labels as
"window opened". In red, the classified labels as "no annotation". In green the outdoor tempera-
tures.

The experiment was also tested using a time step for the classification of 30 minutes. No-
tice that the accuracy of classification is lower than in the first test where a time step of 1h was
considered. This might be, since 1h is closer to the real minimal duration registered for the fact
(2h).
They were carried out (in the simulation) 59 information requests to the occupants from the
total of 491 time slots registered, meaning that in the rest 432 time slots, the classification of
the label was automatically performed by the artificial system. The number of notifications and
confusions per day can be observed in the next tables (see Table ?? and see Table ?? ).

Day            1    2    3    4    5   6   7   8   9   10

Notification   19   10   5    11   2   2   2   4   2   2

Confusions     0    0    1    1    0   0   1   2   0   0

TABLE 9.10 – Number of notifications and confusions per day, from day 1 to day 10

The classification of the label "window opened" reached an accuracy of 58%, meaning that
from 106 times that the fact happened, 62 times was accurately predicted by the artificial system
while it was incorrectly predicted 44 times as "no annotation" . The "no annotations" label was
classified with an accuracy of 80%, guessing 307 times out of the 384 times it actually appeared.
To analyze the classifier’s incorrect predictions, a confusion matrix was displayed. The F-score
reached 74%. These results are given by the density algorithm, explained in (Silva et al., 2022)
using a random forest classifier. Globally the accuracy reached was of 75%.

characterization of facts

No annotation   Window opened

No annotation     307             77

Window opened     44              66

TABLE 9.11 – Confusion matrix

Lastly let’s observe the impacts when a combination of sensors information is used. The next
test was carried out using the motion sensor and the contact sensor of the window. It was stated
in the algorithm that if in at least 20% of the time in each time-step motion appeared, then it can
be considered that there is presence in the area, given that this activity, requires presence when
opening or closing the window (unless the window is automatized). This means 6 and 12 minutes
for the case of 30 minutes and 1h respectively, were considered. The next results were found :

Time-step         Motion sensor         F1-score of fact   Accuracy      of     Global   accu-
fact classifica-     racy
tion

30 minutes        Yes                   0.80               0.66                 0.81

30 minutes        No                    0.70               0.58                 0.75

1 hour            Yes                   0.80               0.67                 0.84

1 hour            No                    0.80               0.67                 0.78

TABLE 9.12 – Accuracy of classification of the "window opened" label and Global accuracy of
the test with different time-steps and using or not using motion sensor measurements.

Time-step               Motion sensor            F1-score of no anno-    Accuracy of "no an-
tation                  notation" classifica-
tion

30 minutes              Yes                      0.92                    0.85

30 minutes              No                       0.92                    0.85

1 hour                  Yes                      0.94                    0.88

1 hour                  No                       0.90                    0.81

TABLE 9.13 – Accuracy of classification of the "no annotation" label with different time-steps and
using or not using motion sensor measurements

characterization of facts

In the tables ?? and ??, it can be observed that when the motion sensor is considered for the
classification, the accuracy of the "no annotation" label increases. This leads to a better global
accuracy. The highest level of global accuracy is reached when using a time step of 1h and consi-
dering the motion sensor (84%). The classification of the label "window opened" has higher results
using a time-step of 1h. Until now one can conclude that the best configuration is reached using
1 hour of time-step and considering the motion sensor. However the number of requests and the
number of confusions, increase significantly when the motion sensor is taken into account (see
Table ??). After observing this, the configuration using 1 hour of time step and no motion sensor,
provides the best results.

Time-step     Motion sensor   Total requests   Total confusions

30 minutes    Yes             417              77

30 minutes    No              58               11

1 hour        Yes             215              38

1 hour        No              53               4

TABLE 9.14 – Total number of requests and confusions in 10 days for the different configurations
of sensors selections.

It is possible that motion is detected in several moments outside of the "window opened" fact,
which could cause the multiple requests and confusions detected by the system.

Assessing imbalance in the classification process. Experiment 4 study case : Does the energy
consumption of the fridge increase when I go shopping and put food inside the fridge ?
In the annotations provided by the occupants, they annotated the label in the modality section
"shopping storage". The latter information is therefore considered as the modality annotation for
classification. The duration of the fact was considered of 15 minutes every time for the classifica-
tion, since the time step considered was of 15 minutes to reduce the processing time. In reality the
occupant took less time to store the groceries in the fridge, as seen in the annotations.
The experiment lasted 23 days, however, during this time, only 5 labels of "shopping storage"
were annotated, meaning that in 23 days, the occupants did groceries 5 times. In all the moments
when no annotation were provided (meaning that the fact did not happen or that the occupant
missed adding an annotation), the classification considered the label "no annotation". The sensor
selected for the classification was the power consumption of the fridge. The hour of the day was
also taken into account given that the annotations provided show that this fact mainly happens in
the afternoon.
During the interactive learning process of the artificial system were observed 79 information
requests to the occupants from the total of 2193 time slots registered, meaning that in the rest 2114
time slots, the classification of the facts was automatically performed by the artificial system. The
number of notifications and confusions per day can be observed in the next tables (see Table ??
and see Table ?? ).

Day                1        2   3        4    5        6       7       8    9    10       11       12

Notification       50       5   3        5    2        2       0       3    4    0        0        1

Confusions         1        0   0        0    0        0       0       0    0    0        0        0

TABLE 9.15 – Number of notifications and confusions per day, from day 1 to day 12

Day              13       14      15       16       17       18          19   20       21       22       23

Notification     0        0       1        1        0        0           0    0        0        1        1

Confusions       0        0       0        0        0        0           0    0        0        0        0

TABLE 9.16 – Number of notifications and confusions per day, from day 13 to day 23

The poor prediction results are not very surprising due to the significant imbalance in the
number of cases between the two classes to be recognized. When the label "shopping storage" was
classified, it reached an accuracy of 0 %, meaning that from 5 times that the fact happened, 0 times
was accurately predicted by the artificial system. The "no annotations" label was classified with
an accuracy of 99.77%, guessing 2188 times out of the 2193 times it actually appeared. The fact
"shopping storage" was incorrectly predicted 5 times as "no annotation" and was accurately pre-
dicted 0 times. To analyze the classifier’s incorrect predictions, a confusion matrix was displayed.
The F-score of the label classified is 0%. These results are given by the density algorithm, explai-
ned in (Silva et al., 2022) using a random forest classifier. Globally the accuracy reached was of
99.77%, but because of the accuracy of guessing the most repeated label : no annotation. While
the "shopping storage" label was annotated only 5 times by the occupant. Too few information for
the system to make an accurate classification.

No annotation                 shopping storage

No annotation                 2188                          0

shopping storage              5                             0

TABLE 9.17 – Confusion matrix

characterization of facts

The cycles of power consumption of the fridge are shown in (see Figure 9.6).
Whether the fridge is quite efficient, or there is an issue with the sensor. It can also be noticed
that the label "shoping storage" was not classified in any moment, given that no blue dots were
plotted.
In this experiment, the number of annotations provided by the occupant are too few (only 5)
even when the duration of the experiment was of 23 days, this fact was annotated only 5 times.
When no annotation about "shopping storage" was provided, the label considered was "no anno-
tation". Given the time step considered (15 minutes) and the duration of the experiment (23 days),
2193 labels were annotated, and the great majority 2188 had the name "no annotation". In conclu-
sion, if a fact occurs with low frequency, we should either use an algorithm that is less sensitive to
imbalanced classes or perform undersampling, which refers to the process of reducing the num-
ber of examples from the majority class to balance the dataset and address class imbalance. Class
imbalance occurs when one class (category) of the data has many more examples than the other
classes, which can lead to biased or poor model performance.

Figure 9.6 – Energy consumption in kWh every 15minutes. In blue, the classified labels as "shop-
ping storage" (notice that there are no blue points). In red, the classified labels as "no annotation"

#### 9.1.2 Multi-modal annotated facts : Assessing the Impact of Experiment Duration,

Fact Duration, and Fact Frequency on Outcomes
In one of the experiments where annotations were recovered from inhabitants, the answer to
the question How ? (the modality) included several responses (multi-modal) through one same
experiment. We were interested in the outcome, which could lead to different results compared
with the previous tests in a uni-modal format.
We were interested in observing the accuracy of the classification process, when several labels
were included. More was discovered, specifically in terms of the duration of the experiment, the
frequency of occurrence of facts and the duration of the facts.

Multi-modal test using the experiment from site "kappa". Experiment 2 study case : How
much energy do I consume when I use the washing machine in different wash programs and
in different contexts ?
A test with multiple modalities is presented here using sensors data and annotations from site
kappa and the experiment related to the power consumption when using the washing machine in
different programs. In this case, only information of the power consumption of the machine was
recovered. The hour of the day is also considered when performing the classification, given that
the fact mainly happens in the morning or late in the afternoon. The measurements were registered
every hour and they were the result of the average energy consumption per hour in watt-hour
units (Wh). No motion sensors were installed. The different modalities included : "eco 30°C",
"eco 40°C", "15 minutes" and "60°C cotton". The inhabitants used this modalities given that it is
related to their habits.
The experiment lasted 14 days and a time slot of 1h was used (due to the time of measurements
recovery of the power sensor), however, during this time, only 7 labels of the different modalities
were annotated. Meaning that in 14 days, the washing machine was used 7 times. They were
provided 2 labels of the modality "15 minutes", 1 label of the modality "eco 30°C" and "60°C
cotton" and 3 labels of the modality "eco 40°C". In all the moments when no annotation were
provided (meaning that the fact didn’t happen or that the occupant missed adding an annotation,
the classification considered the label "no annotation".
During the interactive learning process of the artificial system were observed 20 information
requests to the occupants from the total of 345 time slots registered, meaning that in the rest 325
time slots, the classification of the facts was automatically performed by the artificial system.
The ideal is that the minimum requests of information (“notifications”) are sent to the occupant,
making the learning process, efficient. The number of notifications and confusions per day can be
observed in the next table (see Table ??).

Day            1    2   3   4   5   6     7   8   9   10   11   12   13   14

Notification   18   1   0   0   0   0     0   0   0   0    0    0    0    0

Confusions     0    1   0   0   0   0     0   0   0   0    0    0    0    0

TABLE 9.18 – Number of notifications and confusions per day, from day 1 to day 14

characterization of facts

After the cooperative and interactive learning phase, the learning system was able to estimate
the facts. When the label "eco 30°C", "eco 40°C", "15 minutes" and "60°C cotton" were classified,
they reached an accuracy of 0 %, meaning that from the times that the modality happened, 0 times
was accurately predicted by the artificial system. In this case, each of the modalities could have had
a different percentage of accuracy in the classification, but given the few annotations recovered,
the results were inaccurate for each of the modalities

The "no annotations" label was classified with an accuracy of 100%, guessing 335 times out
of the 335 times it actually appeared. Globally the accuracy reached was of 97%, but because
of the high accuracy of guessing the most repeated label : "no annotations". While the rest of
the modalities labels were too few information for the system to make an accurate classification.
These results are given by the density algorithm, explained in (Silva et al., 2022) using a random
forest classifier.

Figure 9.7 – Energy consumption in Wh every hour. In blue, the classified labels as "eco 30°C",
"eco 40°C", "15 minutes" and "60°C cotton". In red, the classified labels as "no annotation"

It can be concluded that when evaluating with different modalities, several labels should be
provided for each of the modalities and the accuracy of the classification of each modality could
be analysed. This means that classes as they were annotated are unbalanced. Too many labels
from the "no annotations" class and very few from the modalities labels . As in the previous
experiment it should be used an algorithm that is less sensitive to imbalanced classes or perform
an undersampling process.

Infrequent modalities lasting short periods of time could cause an important unbalance in the
data. Infrequent modalities lasting long periods of time could have a lower impact in the unbalance
of data, but this depends also on the amount of data of the rest of the classes. Similarly, too many
different modalities might cause an important unbalance in the data, given that this latter would be
dispersed between the different modalities.

### 9.2 Class imbalance : a common factor in the different experiments

Class imbalance is a main factor that could result in low accuracy results when using the
modality label (specially in multi-modal answers) as it could be seen in the experiments tested.
A quick test was carried out using information from (GeeksforGeeks, 2024). Data was gene-
rated to reproduce the characteristics of experiment "fridge". A total of 2193 data were generated
and an imbalance of 0.2 and 99.8 was applied. Then half of the data was used to test the classifi-
cation method. In the beginning the same parameters used for the random forest classifier in the
experiment, were tested with this new generated data. Only one of the parameters of the random
forest library was modified (class_weight=’balanced’) so that the classifier provided more weight
to the minority class. Results were basically the same, a zero accuracy in the classification of the
minority data class and a 99% accuracy in the majority data class.
Next a random undersampling was performed to remove data from the majority class to
achieve a more balanced distribution. According to the authors in (GeeksforGeeks, 2024) this
could improve the accuracy in classifying the minority class. The parameter of the random forest
classifier was also applied as class_weight=’balanced’. The accuracy in each of the classes resul-
ted better, the majority class prediction was reduced to 68% and the minority class results increased
from 0% to 33%. Globally (considering all data) it was achieved an accuracy of 68%. Although
results were more balanced, improvement can still be made in the general results. However the
undersampling in this exercise helped balancing the data.
In future work, a similar method could be implemented in the experiments carried out.

### 9.3 Discussion

Let’s remember that the characterization of facts includes several question as it was explained
in chapter2. Four tests were carried out using the cooperative and interactive learning algorithm
(CIL). This time using only the answers to the question How ? (modalities) label for the process.
Two type of answers were classified : the uni-modal and multi-modal answer. In the uni-modal
answer to the question How ? the same label was repeated every time that the fact happened. While
in the multi-modal type of answers, different labels were provided when the facts happened.
The modality annotation was selected because it could closely relate to the measurements re-
corded by the sensors. For example, when using a washing machine at 60°C, the energy consump-
tion readings differ from those of a cycle at 30°C, though readings within the same temperature
setting are relatively consistent. This implies that during the cooperative learning process, the sys-
tem could apply similar discretization rules for all instances of 30°C cycles and similarly for all
60°C cycles.
The objective of using this method was to observe if the classification process could be accu-
rate using the modality label. After the tests carried out in this chapter, it is concluded that class
imbalance is a main factor that could influence in low accuracy results when using the modality
label (specially in multi-modal answers). This problem should be addressed in future research
before stating that this label could be used in the Interactive and Cooperative learning process.
Notice as well that in some cases this label was left empty by the inhabitants in the experiments
presented in 8. If this method was to be used in a real time interaction, this label would need to
become compulsory to answer by the inhabitants. However, it could be convenient to not modify
the proposal that stated that no annotation is compulsory, in order to continue providing freedom
to the inhabitant and simplify the annotation process.
In order to be able to perform the tests in this chapter, the empty labels had to be annotated, for
instance in the experiment about the fridge, the label "shopping storage" was used. However in a
real time interaction with the computerized system, if the inhabitant didn’t provide the annotations,
there would be no label to classify with or as it was done here, it would need to be annotated.
Probably a solution in a real-time interaction, would be that the inhabitant responds with
"5WH+performance" when the fact is occurring or the label ""Fact not occurring"" to indicate
that the fact is not occurring. Then, the system could detect the moments in which the label (or
empty label) is different from "Fact not occurring" and use a unique label, such as "Fact anno-
tated". The ICL could classify data based on these two labels : "Fact not occurring" and "Fact
annotated". This would lead to a classification process as the one showed in Chapter 6 in which
the classification was carried out under only two labels : "cooking" and "other activity".
The "5WH" information could be used solely to display relevant details to the inhabitants when
showing the results and not for classification purposes.
Besides the system might have to automatically provide a different and specific label to indi-
cate if the inhabitant never answered to the request of annotation. This different aspects should be
developed in future work.
This proposed approach for a real-time interaction could ensures that providing "5WH" details
is optional, and probably class imbalance in the data set could be reduced. As it was seen in this
chapter. Class imbalance had an important impact in the results. Nonetheless, carrying out tests
using the modality annotation provided other interesting information, next presented.
In the three experiments of site 2 (Experiments 1, 2 and 4), the annotations for the modalities
were not varied, they were uni-modal. This is equivalent to carry out the learning processes using
one generalized activity label and one label for all the moments in which the fact does not occur. In
the tests carried out the label "no annotation" was declared automatically by the system in all the
moments that no label of the fact was provided. This was carried out specifically for this examples
due to the data available. As mentioned before the real-time interaction process would need a
different method.

In the first experiment about the dishwasher power consumption, the dishwasher was always
used in the same program "1h 60°C". When opening the window, the modality was always expres-
sed as "window opened" and for the experiment of the fridge (it was filled) as "shopping storage".
Notice that in this two last examples, it is true that there are not many different ways of carrying
out the facts. It could be possible that some experiments have this type of annotations in which the
label of the modality is repeated.
It was observed that different factors can affect the accuracy of the classification. One of the
factors is the accuracy of the declaration of start and end of the fact. In the study case 1 : How much
energy do I consume when I use the dishwasher in different washing pro-grams and in different
contexts ? The inhabitant annotated that the washing cycle lasted 1h, while when observing the
data recovered from the sensor, it showed that the cycle lasted 2h. This possibly "human error"
leaded to a low accuracy in the classification process. Should be mentioned that this error could
have happened due to the format of manual annotation in which the experiment was carried out. In
a digital system it should be envisaged an annotation process that can reduce this error. It should
be also evaluated if it was not an error in the sensor, which is less probable but still possible.
Implementing a method to detect sensors errors in the system would be very interesting too.
Other factors affecting the results are the time-step in the CIL and the sensors selected : mea-
ning that it is important to choose a time step that is close to the real duration of the facts. As
mentioned by (Krishnan and Cook, 2014) "If a very small interval is chosen, there is a possibility
that it will not contain any relevant activity information for making any useful decision. If the
time interval is too wide, then information pertaining to multiple activities can be embedded into
it and the activity that dominates the time interval will have a greater influence in the classification
decision."
In the experiment number 2 about the window opening, different configurations of parameters
and sensors were tested : time-step of 1 hour and 30 minutes and only window contact sensor
or combination of contact sensor and motion sensor. It was concluded that the configuration that
obtained the best global accuracy of classification (84%) with the less requests to the inhabitants,
was using a time-step of 1 hour and only the window contact sensor. The motion sensor might
have added noise which resulted in a high amount of requests and confusions.
It would be interesting to perform more tests to determine the set of sensors that could be
used for the different facts in order to guide the occupants in the process of sensors selection. For
instance in chapter 6 an example was presented with the activity cooking. Motion in the kitchen
and power consumption of the stove and oven were used in the classification process and an ac-
curacy of 72% reached in the classification of the label "cooking". If the motion information is
removed, the accuracy is of 72% which means that the environmental sensor of motion, provided
information, rather than noise or that the information provided by this sensor was not significant.
But at least the accuracy reached did not diminished when it was considered. Let’s notice as well
that presence is, generally, a characteristic of the cooking activity.
The last uni-modal experiment was the case of the fridge. It was observed that the amount of
annotations provided is also important (even if they are uni-modal). The annotations of the fridge
showed that "shopping storage" lasted around 5-10 minutes. For classification purposes this time
was increased to 15 minutes and the time-step used for the classification was also closed to 15
minutes to speed up the compute time. The rest of the time, when no annotation about " shopping
storage" was provided, the label was considered as "no annotation". This resulted in a very large
set of labels (2188) of "no annotation" and only 5 labels of "shopping storage". Although the total
period of the experiment was of 23 days, only 5 times, the label was annotated. This was too few
information to obtain a good accuracy in the classifications results. Meaning there was a ratio of
5/2193 (0.22%) annotations for the classification "shopping storage" out of the total 2193 time
slots (using a time step of 15 minutes during 23 days).
This number of annotations might not just be related to the annotations provided by the occu-
pant but also to the duration of the facts. For example, sleeping is a long fact, it could recover a

large set of annotations, not because the occupant annotated, but specially because it could last up
to 8 hours per day. Resulting in at least 8 annotations per day, considering a time step of 1 hour.
In the experiments tested, the fact "washing the dishes" lasts 2 hours, but the machine is not
used everyday. So, by far we can recover 2 annotations per day, using a classification time-step of
1 hour. The "window opened" fact could last minimum 2 hours and maximum 7 hours as annotated
by the occupant, besides it was carried out everyday. Then it was recovered 2 to 7 annotations per
day, using a classification time-step of 1 hour. This last experiment had the most accurate results.
In conclusion, unbalance in the classes could be expected using the self-experiment method
(this issue was seen in all the experiments here presented), it would be interesting to test in the
future an algorithm that is less sensitive to imbalanced classes or perform undersampling, an ap-
proach to reduce the number of examples from the majority class to balance the dataset and address
class imbalance.
Annotations and data from the site 1 were used to analyse a multi-modalities case. The expe-
riment observed was related to the washing machine power consumption and the different confi-
gurations that can be used. The period of the experiment was of 2 weeks, but few annotations of
each of the modalities were recovered. This lead to conclude that several annotations of each of the
modalities are required to carry out a complete analysis. Which might mean also, class imbalance.
A quick test using generated data reproduced the characteristics of the "fridge" experiment
to address class imbalance. Initial results with a random forest classifier (classweight-’balanced’)
showed low accuracy for the minority class. Applying random under-sampling to balance the data
improved results, increasing minority class accuracy from 0% to 33% and overall accuracy to
68%. Under-sampling helped to address imbalance. Future experiments could implement similar
methods for further improvements.
Notice that the presentation style of the figures showed is not to be the one used in the comple-
ted system. This are only intermediate results. A better style could be designed with professionals
of Human- Computer Interaction development.

### 9.4 Chapter conclusions

This research explored the use of modality labels in a Interactive and Cooperative Learning
(ICL) algorithm to classify energy-related facts. Tests using uni-modal and multi-modal annota-
tions revealed several challenges and opportunities in real-time interaction systems.
Main findings in this chapter included, for instance, the class imbalance insight, experiments
consistently showed that class imbalance severely affected classification accuracy, especially with
multi-modal labels. Future experiments should test advanced algorithms less sensitive to class
imbalance and apply balancing techniques like undersampling.
Tests demonstrated that choosing appropriate sensors and time-steps is important. For ins-
tance, using only the window contact sensor and a 1-hour time-step improved accuracy, while
adding other sensors introduced noise. Further tests should explore optimal sensor configurations
for various facts, ensuring sensors provide meaningful data without adding noise.
Manual annotation challenges were observed, errors in manually reporting fact duration im-
pacted classification accuracy. This error happened mainly due to the format used for this tests,
using manual annotations. The error could be reduced, when implementing the real-time interac-
tion using the ICL. This is to be observed when carrying out a real-time interaction.
Also in a real-time interaction it could be explored a streamlined labeling system that could
identify more specifically and automatically, for instance, "Fact not occurring" and "Fact anno-
tated" to simplify classification while maintaining user flexibility using the 5W1H+performance
annotation. This latter information could be used only to display relevant details to the inhabi-

tants during result presentation, rather than for classification. Additionally, the system may need
to automatically assign a specific label if the inhabitant does not respond to an annotation request
(if applicable). Tests should be carried out to evaluate what happens in the ICL process when no
answer is provided. In the tests carried out so far there have always been a label given.
Collaboration with Human-Computer Interaction experts could refine the system’s interface
and data presentation for the ICL process in a real-time interaction.
By integrating these improvements, the ICL framework could become a robust tool for real-
time energy management systems, enhancing sustainable living through adaptive learning and user
interaction.

## Figures extracted from the source PDF

![[_assets/initial-thesis/09-applying-fact-characterization/page-162-image-121.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-163-image-123.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-164-image-125.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-167-image-127.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-168-image-129.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-173-image-131.png]]
![[_assets/initial-thesis/09-applying-fact-characterization/page-175-image-133.png]]
