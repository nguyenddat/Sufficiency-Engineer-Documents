---
title: "Annotation-based facts recognition: aiding systems and case of study"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Annotation-based facts recognition: aiding systems and case of study

[[Initial thesis index|Index]] · [[05-annotation-free-facts-recognition|← Previous chapter]] · [[07-functionalities-and-experiment-examples|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Annotation-based facts recognition : Aiding
systems and case of study

In this chapter, the process of experiment is presented in an study
case of a residential context. The cooperative and interactive lear-
ning is tested with information of this study case. The database used
included sensors data and facts data. However, no characterization
of the fact was included, given that the database did not contain the
information. A method of support of annotations is also developed
in this section. It was applied to the same study case. This method
permits the occupants to postpone answering to the notifications co-
ming from the system. It might be useful in case the occupants cannot
answer in the moment when the notifications are received.

### 6.1 Annotations based recognition

Notice that when it is possible to isolate the analysis of experiments and be selective on the
desired experiment to study, one can actually specify the characterization of the facts. It is proposed
that by characterizing the facts as explained in Chapter 2 (how, what, why, when, where, who and
performance), the inhabitants could recover key information of the way they develop their fact and
translate this information to answer a particular question associated to an experiment. A system of
aid to annotate the characteristics is presented in this Chapter.
The characterization of facts using annotations is also a way to translate a question from natural
language. For example the energy consumption of a washing machine might be higher when it is
programmed to wash at 60°C rather than at 20°C, but in both cases the fact is the same "wash", if
the fact is not specified by inhabitants as an annotation, the sensors information cannot define the
different options to wash on its own. Taking advantage of the occupants knowledge to annotate the
characteristics of the fact, is important in this case.
Opposite to the annotation-free recognition, the facts require annotations when :

1. The sensors effects are not enough to provide an answer.
2. An explanation cannot be given of how to recognize a fact from a signature, therefore an
algorithm cannot be programmed to distinguish a particular fact.
3. The answer requires to differentiate between the contexts of the fact. One same fact could
be carried out in different ways, which results in different possible labels to associate. The
characterization could facilitate the association of impacts to specific ways of execution of
facts.

### 6.2 Annotating is assumed to be the bothering part

Characterizing facts, using annotations, as explained in Chapter 2 allows to recover infor-
mation that can improve the comprehension of the way in which facts are developed. However,
characterizing facts, as proposed, can be tedious.
If occupants wanted to provide annotations for all the events, the task could become overwhel-
ming. For this reason, it is interesting to carry out experiments, as explained in Chapter3, it allows
to be selective with the facts to study. Let’s also remember that annotations as seen in Chapter
2 help translating the occupants question from the natural language into information that can be
treated by a computerized system.
Then, even if few experiments are being studied, annotating every time that a fact occurs,
could become an annoying task, specially if the fact is repeated frequently. Besides in some cases,
if the occupants are busy, they might not be available to add the annotations in the moment when
the fact takes place. To solve this issues it is proposed to adopt the cooperative and interactive
learning method and the A posteriori annotation approach, this methods act as an aiding system
for the annotation process in experiments. The interactive learning process reduces the number of
interactions to recover the annotations and automatizes the process of labeling by learning from the
previously provided annotations . While the cooperative learning process spots possible errors in
the learning process. It shows the annotation that could be erroneous to the occupants and request
the occupants to clarify by correcting or accepting the annotation.
The A posteriori annotation approach gives the option to the occupants to provide the anno-
tations later, after the fact has been detected. This approach provides flexibility to the user during
the process of annotation.

The processes are next explained with more detail than in Chapter 2 and some examples are
provided.

### 6.3 Interactive and Cooperative learning

#### 6.3.1 Interactive Learning

The interactive learning process, developed for occupancy estimation (Amayri et al., 2019)
consists of requesting information to the occupants. It determines when the interactions are ne-
cessary. The intention was to improve the quality of the database, so that automatic learning algo-
rithms can reach a higher accuracy with fewer training data (Silva et al., 2022). Two interaction
criteria were analyzed to minimize the number of interactions, in order to have the less labeling
errors in the learning process : density of the neighborhood and spread rate. The density of the
neighbourhood estimates if a request to the inhabitants is necessary. It is a concept used in ma-
chine learning to cluster data based on the number of points (neighborhood) in a region or space
(defined by a radius around a data point, for instance the euclidian distance ε) (Singh Chauhan,
2022). A minimum number of neighbours had to be defined to consider a region as dense. In the
algorithm and it was established that a request should happen if the number of neighbours of a
potential ask (requirement of participation of the inhabitant to provide information) in the current
time is lower than the minimum number of neighbours defined. The neighbourhood of a record is
established in a threshold between ε[0, 1] and a new record is part of the neighbourhood if the dis-
tance between the new record and a previous record is lower than ε/2. (Silva et al., 2022) defined
that the optimal parameters to use with fact labels were ε = 0.2 and 2 as the minimum number of
neighbours.
The spread rate is a more global measurement of the quality of the database. It verifies how
records are globally distributed. In the examples showed in this thesis, only the density of the
neighbour was evaluated. (Silva et al., 2022), found out that density performs better than spread
rate, when the hour of the day is considered as a feature. This feature allows to correlate also the
daily routine. This is interesting in the case of habitual facts such as "taking breakfast". At first,
the system has no records. The authors found that in the beginning there are more requests, since
there are no predefined labels and through the time the number of requests diminished.
The interactions with the occupants are the way in which labels are stored in a knowledge
database. The quality of the database is given due to the interactive learning process, which deter-
mines the moments to request labels. Then the raw values from the sensors are associated to the
labels, a classifier is used to predict the label of the current time (Silva et al., 2022).

#### 6.3.2 Cooperative Learning

Once the sensors measurements and the labels are associated, the cooperative learning pro-
cess allows to identify confusions, meaning incoherences between previous labels provided by the
occupants and new labels. Which means that whether the classifier or the human actors made a
mistake. Let’s see what are confusions and how this confusions are spotted.
The interrelated raw values and labels in the interactive learning process, are the source of
confusions as mentioned in (Awada et al., 2020). The raw values are discretized forming words
using parameterized feature generator. (Silva et al., 2022) propose that raw values are transformed
into information that can facilitate the process. For example information can be transformed in
levels : VL, L, M, H (Low, Medium, High), by limiting them with minimum and maximum raw
values. For a set of sensors, a combination of the discretized information is grouped for each time

interval. Let’s say that for a time slot t, there is a grouped of information with the discretized values
MHM (Medium, High, Medium). The first M corresponding to the energy consumption sensor, H
corresponding to motion sensor and and last M corresponding to CO2 sensor. It is the grouped
discretization MHM that is associated to the labels given by the inhabitants. The group of discrete
values from a set of sensors to be associated with the cause label is named a word.
Unions of label-word are then carried out (thanks to a random forest classifier). When 2 dif-
ferent labels, were linked to the same “word”,the system experiences a confusion.

Figure 6.1 – Confusions (Silva et al., 2022).

We say that the associations are checked by the confusion solver. With the current discretiza-
tion levels, two situations perceived differently by the user (two different labels) that, give different
sensor measurements, might, ultimately, lead to the same discretized value, and they are therefore
perceived in the same way by the system. The aim is to adjust the discretization levels (see Figure
6.2) so that the system itself perceives them as different.

Figure 6.2 – Feature generators updates to solve confusions (Silva et al., 2022).

If the confusions persist, a request of label is made to the occupants (independently from the
interactive learning process). Besides, thanks to the classifier, a label can be proposed to the users
in order that they approve it or modify it. This approved or modified label is stored as the ground
truth and associated to the corresponding raw values of the sensors.

Next we will see an example of this methodology applied to a database of a dwelling. Let’s re-

member that (Silva et al., 2022) made tests in an office context. Later in Chapter 9 an application is
presented using characterized facts semantic annotations. The cooperative and interactive learning
is to be used as an aiding system for the annotation process of the characterization of facts.

Figure 6.3 – Process proposed combining interactive and cooperative learning (Silva et al.,
2022).

### 6.4 First example using only facts labels (without annotations for the

characterization of facts)
A first test based on experiments has been carried out using data recorded by sensors and
activities labels provided by an inhabitant, in an apartment (Lago et al., 2017). The dwelling of the
experiment is a two-storey building, and one person inhabited the residence. The set of installed
sensors used for the test measure energy consumption, temperature and motions.
The procedure as tested in (Silva et al., 2022), was used. In order to validate the facts classifi-
cation in the cooperative and interactive learning, the fact tags included in the database from (Lago
et al., 2017) were used. Therefore a real-time interaction with the human actor was not performed.
It has been decided to create an "experiment" simulation about the fact "cooking". As the
database used was from (Lago et al., 2017), the semantic annotations that involve the facts charac-
terization did not exist at this time, and so, were not included. However the occupant from (Lago
et al., 2017) labeled real activities. Remember that in this thesis activities are a type of fact that
can be observed as described in Chapter 2.
For this test only, any other fact than cooking was labeled under the name of "other activities",
given that the database contained labels of multiple activities and due to there was no real time
interaction between a human and the computerized ICL (Interactive and Cooperative learning)
system. In this way, the label "cooking" could be isolated from the rest of the activity labels in

the database . Let’s remember that an experiment is dedicated to the analysis of one specific life
event. The fact "cooking" was isolated from any other fact as it would be done in the case of
an experiment. In other words, labels from different facts are not part of one same experiment.
For instance, all labels related to "washing clothes" won’t be part of the experiment associated to
"cooking".
In a system with real time interaction, the inhabitant will have to provide a label that can
indicate that there is lack of occurrence of the fact of the experience -if it is the case- when the
inhabitant is asked to provide annotations. While the system might have to automatically provide a
different and specific label to indicate if the inhabitant never answered to the request of annotation.
This should be developed in future work.
The programming of the experiment was simulated (selection of sensors and definition of the
period of listening time of the experiment). The time period of the experiment was of 7 days, from
0h on 15/11/2016 to 0h on 21/11/2016, and the time slice studied was of 30 min.
As part of the experiment, questions were defined as if the occupant wanted to answer them.
Next Table ?? shows examples of possible questions. Only for this example multiple questions
were proposed to test the possibility of answering them using the interactive and cooperative lear-
ning. Let’s remember that it was proposed that an experiment is associated to one question only.
This might facilitate the comprehension for the inhabitant and facilitate the process of experiment
programming.
Then, 2 different types of questions have been identified as explained in Chapter 3 (see Table
??).

Type of question                                 Questions

Oriented to appliances                           1.Which appliance consumes the most po-
wer, in the kitchen ?

Oriented to facts                                2.What is the total power consumption in a
week related to the fact cooking ?

Oriented to facts                                3.What is the presence level in the kitchen
during the week associated to the fact co-
oking ?

Oriented to facts                                4.What is the temperature in the kitchen du-
ring the fact cooking ?

Oriented to facts                                5.What is the total power consumption when
the fact cooking occurs ?

TABLE 6.1 – Questions type related to the experiment

The selected sensors were : energy consumption of the grill and oven and motions measure-
ments for the classification. The temperature in the kitchen was used to provide an answer to the
questions number 4 (see Table ??). The "cooking" fact was learned by the system using informa-
tion about the time of the day, presence in the kitchen and consumption of the grill and oven.

The answers to the questions (see Table ??) are next detailed. The answer to question 1 can
be obtained by comparing the total consumption of the electric grill and the total consumption of
the oven. Then the addition of the power consumption during the period of the experiment was
calculated. In (Table 6.2), it can be seen that the appliance with the highest power consumption is
the electric grill.

The answer to question number two is shown in Figure 6.5 and it is also given in numeri-
cal form. The graph shows the consumption profile of the selected appliances as a function of
time, over the total period of one week and also per day (see Figure 6.6). The numerical answer,
5.18 kWh shows the total energy consumption of the selected appliances.
The third question has been answered (see Figure 6.7), showing the profile of the presence
coefficient over the period and also per day (see Figure 6.8).
Figure 6.9 answers the fourth question. The blue dots represent the temperature in the kitchen
while the occupant was cooking, and the red dots represent the temperature in the kitchen during
another fact.
The last question is answered in Figure 6.10. The blue dots represent the occupant’s consump-
tion when cooking and the red dots represent consumption when performing another fact.

Appliances                              Electric grill   Oven

Total energy consumption in 7 days      4.33kWh          0.85kWh

TABLE 6.2 – Comparison of energy consumption of the selected appliances.

The interactive learning process of the artificial system looks as showed in the next Figure 6.4.
Consider the symbol "-" as none and [...] as continuation of the process. Ask means that labels
are requested from the inhabitants. The words are associated to the label provided. Automatic
classification is carried out when there are no Asks. When there is a confusion, the confusion
solver runs, if the confusion solver could not overcome the confusion, a request is sent to the
inhabitants for them to clarify, by adding a label.

They were observed 48 information requests to the occupants from the total of 336 timeslots
registered, meaning that in the rest 288 timeslots, the classification of the facts was automatically
performed by the artificial system. Ideally, the minimum requests of information or “notifications”
should be sent to the occupant, making the learning process efficient. The number of notifications
and confusions per day can be observed in the next Table (see Table ??).

Day                           1    2   3     4    5    6    7

Number of notifications       20   5   5     4    3    10   1

Confusions                    0    0   0     1    0    0    0

TABLE 6.3 – Number of notifications and confusions per day

Using the density algorithm, explained in (Silva et al., 2022), it was possible to estimate the
facts with the next results : when the label “cooking” was classified, it reached an accuracy of 72%,
meaning that from 18 times that the fact cooking happened, 13 times was accurately predicted by
the artificial system. The "other activities" label was predicted with an accuracy of 318 times out
of the 318 times it actually appeared. To analyze the classifier’s incorrect predictions, a confusion
matrix was displayed. The F-score is 84%.

other activities   Cooking

other activities    318                0

Cooking             5                  13

TABLE 6.4 – Confusion matrix

Predicted           Predicted

Expected     True negative       False positive

Expected     False negative      True positive

TABLE 6.5 – Generalization of the confusion matrix

Figure 6.4 – Process of the interactive and cooperative learning

Figure 6.5 – Total power consumption in a week. Answering to question 2 : what is the total
power consumption in a week, related to the fact cooking ?

Figure 6.6 – Answering to question 2 : what is the total power consumption in a week, related
to the fact cooking ? (representation per day and per hour)

Figure 6.7 – Presence percentage in a week. Answering to question 3 : what is the presence level
in the kitchen during the week, associated to the fact cooking ?

Figure 6.8 – Answering to question 3 : what is the presence level in the kitchen during the week,
associated to the fact cooking ? (representation per day and per hour)

Figure 6.9 – Temperature in the room during the fact "cooking". In blue the moments when the
fact "cooking" is carried out. Answering to question 4 : what is the temperature in the kitchen
during the fact cooking ?

Figure 6.10 – Power consumption during the fact "cooking". In blue the moments when the fact
"cooking" is carried out. Answering to question 5 : what is the total power consumption when the
fact cooking occurs ?

#### 6.4.1 Experiment simulation discussion

Notice that the presentation style of the figures showed is not to be the one used in the comple-
ted system. This are only intermediate results. A better style could be designed with professionals
of Human-Computer Interaction development.
In the confusion matrix, the F-score of 84% represents the moments when the classifier made
the fewest errors. Overall, this score is an acceptable result. In the answers to the questions (see
Figure 6.6), consumption was mainly observed in the early morning and afternoon on the first
4 days, while on the following 3 days, energy consumption was also observed around midday.
Observing the presence coefficient graph (see Figure 6.8) and the power consumption graph (see
Figure 6.6), in all cases where there was consumption, there was presence. On days 2, 5 and 6,
there was no consumption in certain time slots, but presence was recorded. An analysis of the
room temperature during the cooking fact (see Figure 6.9) reveals no significant difference from
other times when other activities are taking place. This means that cooking has not increased the
room temperature. (Figure 6.10) shows, in blue, consumption during times related to the cooking
fact. In most time slots, "other fact" was recorded as a label. In the vast majority of cases, there
is no consumption for the label "other fact". Additional red markers with higher consumption are
cases where the fact was not classified as "cooking", but there was use of the electric grill or oven.
The 5 labels which were incorrectly classified as "other fact", but which in fact corresponded to
the "cooking" fact, are included in the red markers showing energy consumption greater than zero.

#### 6.4.2 Experiment simulation conclusion

This example illustrates the programming of an experiment, using annotations based recog-
nition. The sensors and the listening time period were defined. Then the listening period of the
experiment was simulated and the interactive and cooperative learning requested the labels from
the database. The simulation was carried out using real sensors data from an apartment (for the
first time) and the fact labels were recovered by the inhabitant of the dwelling were the sensors
were installed.
The results show that implementing the "experiments" concept allowed to analyse a fact, isola-
ting it from others. This means that different facts performed at different times could be potentially
treated. However to be able to treat different facts simultaneously, should be validated in future
research work.
It could also solve the problem of the great diversity of habits, since residents themselves
declare the devices they use in the course of their facts. For example, if a resident prefers to
turn on the radio while cooking, since he/she knows he/she has this habit. If sensors utilization
is predefined, for example, the power consumption of certain appliances could be missing, which
would result in an inaccurate result of energy consumption.
The labels used in this example, provided only information of the fact that was being executed
"cooking", it provides no further explanation of its context which could be interesting for the
inhabitants to better comprehend what lead to a specific impact. However the moments in which
the ICL method triggers the interaction could be used to recover other annotations as the proposed
facts characterization (5W1H+performance) presented in Chapter 2.
The figures showed that answer to the inhabitants questions can still be improved so that for
the inhabitants the answers result is more clear. Options of the information they could receive and
different graphics can be presented to the user so that he/she can choose the presentation that better
suits to their question. A proposal is presented in Chapter 7.
For example in annex B, section "Interface for an energy management self-experimenting tool"
observing the impacts and the labels associated was proposed to be represented using a heatmap
graph.
It has been interesting to observe in this section, that the questions proposed could be answe-
red using the experiments system. In the questions oriented to appliances consumption, mainly
sensors information was needed, while in the questions oriented to facts, the knowledge from the
inhabitants is important so that the facts can be associated to the sensors measurements.
Human-Computer Interaction (HCI) techniques can be also implemented to facilitate handling
and understanding of the tool. The HCI system could include a learning phase so that residents
can understand and be guided through the system process. This includes understanding the type
of questions that can be tested, the sensors that can be selected according to the question asked,
examples of annotations, etc. (See some examples in annex B)
In terms of the notifications and confusions from the interactive and cooperative learning pro-
cesses, it was observed that with the time, the number of requests to the user diminished (see Table
??). An evaluation from users about the possibility to answer them and their experience should still
be carried out in a real-time interaction test. It can be understandable that inhabitants might not
always be able to answer immediately when the notifications are sent. For this reason, it is next
proposed that inhabitants can respond later in time.

### 6.5 A posteriori annotation

In the cooperative learning (CL) algorithms "Feature extractors" discretize the values of each
sensor data (Silva et al., 2022). Let’s call the output, feature time series. A set of feature time series
is the group of feature time series resulting from the sensors affected by a same fact.
We define then, a state-component as each of the extracted values in each time-slot tk . As
mentioned in 6.3.2, section, the group of discrete values from a set of sensors to be associated
with the label is named a word : it represents a state. In the annotations-based recognition process,
it is the "feature extractors" that generate words.
In this chapter, an interesting usage of the feature time series is developed to provide a ser-
vice of delayed annotation. Since residents are not always available to respond to the notifications
triggered by the cooperative and interactive learning processes, inhabitants can answer to the anno-
tations in the moments that they are available to do so. The a posteriori annotation tool, provides a
reference of the moments of change in sensors measurements, given that this might mean a change
of activity or context in the dwelling. It is proposed that showing the inhabitants the moments of
change can help them to remember what happened in the past.
After obtaining the feature time series resulting from the extractors, a change point detection
method is applied to the set of feature time series. The change point model is based on the window
sliding methods. "The difference between two adjacent windows that slide along a signal, is cal-
culated. When the windows record dissimilar segments, the difference increases, and it results in
a peak" (Truong et al., 2020). Change point model has already been tested for fact segmentation
purposes as shown in (Aminikhanghahi et al., 2019) and (Brdiczka, 2007).
The aim is to find instants where what happens before in the sensor measurements is different
from what happens after, as this could indicate the start or end of an fact. The detection of change
points is based on the Jensen-Shanon divergence method (Lin, 1991) for calculating the divergence
between two probability distributions. This method has been previously tested in signal segmen-
tation for recognition of changes of facts (Riqueti et al., 2023). As a weighted sum for discrete
values, it is expressed as follows :

pi                   qi
DJ S (p|q) = 1/2 ∑ pi In pi +qi + 1/2 ∑ qi In pi +qi                      (6.1)
i        2           i        2

A state component contains, what we call words, i.e. the integer values of each signature at
each precise time slot. The words of the state components are compared by a sliding window
process. The Jensen Shannon method requires information on the probability distribution (pi , qi ).
In our case, we estimate the probability distribution from the frequency of word occurrence, to
assess divergence.
The principle of this approach is as follows : we consider the frequency of word appearance
over a time window (before and after the time t under consideration) to be representative of current
fact. The Jensen Shanon divergence calculates the difference between these frequencies before and
after time t. We are therefore looking for the set of instants ti where this difference is maximum,
indicating that what happens after is very different from what happens before. These instants ti are
therefore likely to be points of change in fact. The size of the time window considered should make
it possible to construct (via the frequency of occurrence) a probability distribution representative
of the current fact. The size of this window is therefore an important parameter. A smaller window
will make the method more sensitive to minor fluctuations, which can lead to a large number of
false positives. On the other hand, a larger window will make the method less sensitive, but it may
miss some important changes. This parameter can be set directly by the user via a slider. The user
can compare the change points obtained with the sensor data visualized in the form of a heat map
(see next section).

#### 6.5.1 Example of the a posteriori annotations algorithm

The method was tested using the (Lago et al., 2017) database. This database contains infor-
mation from several sensors in a two-storey apartment with one occupant. The sensors installed
include power consumption, motion sensors, averaged sound pressure, humidity and air tempera-
ture sensors.
A test was carried out for the "cooking" fact. The sensors selected were the hotplate and oven
power consumption sensors and the movements detected in the kitchen. Power consumption was
recorded in watts (W), and movement was expressed as the percentage of time (over a 5-minute
period) during which a movement was recorded.
To obtain the feature time series of each selected sensor, a feature extractor which discretizes a
signal into different levels according to the amplitude of the measurements, was used. Thresholds
are set to transform the raw data into levels that can be defined as low, medium and high. Three
levels have been calculated (0, 1 and 2, where 0 is the lowest, e.g. negligible power consumption
or negligible detected movement).

The graph (see Figure 6.11), shows more than 10 moments when at least one sensor, of the
sensor’s set, changed state (each color change is a change of state from black to gray, for example).
It can be seen that the oven has not been used, as energy consumption was not detected, i.e. there
has been no change in sensor measurements. So that the change points can be used as a reference
for the moments when facts happen, we are then interested in observing specific moments, rather
than looking for each individual change. When the size of the comparison window is too small,
many changes are detected. This can be seen when values (values, here represent the measurement
of the change of fact between the windows before and after the time in question) are constant
around 1.3 on the y-axis in the graph (see Figure 6.12). The algorithm compared the sensors’
words every 300s (5min).

Figure 6.11 – Signature heat map for the "cooking" fact

Figure 6.12 – Change point model window size equal to 300s for the "cooking" fact

When the window is increased to 1200s (20min), the number of changes detected is reduced.

Instead of comparing each instant, it compares grouped instants, allowing changes to be observed
over a longer period (see Figure 6.13). The size of the sliding window has been adjusted to 20min
as a possible length time to cook (as a first test). When selecting 20min time length for the window
size, it was observed that the color changes in the heat map (Figure 6.11) closely aligned with the
high peaks detected by the change point model (see Figure 6.13). A change from black to grey
or white in the heat map represents a transition from “null or very low measurement values” to
“medium (grey) or high (white) measurement values,” which could indicate the start of a fact.
Conversely, a change from grey or white back to black may signify the end of a fact. However,
only until comparing with the labels provided, one can observe if this hypothesis is correct. If that
is the case, possibly, a heat map only could be used to spot the change points that represent the
beginning and end of facts.
The colored lines (see Figure 6.13) improve the visualization of moments that may correspond
to fact changes identified by the change point model that align closely with the changes observed in
the heat map. If we look only at the colored lines, it is unclear whether an activity occurs between
two lines or if it signifies a lack of activity.
By comparing with the heat map, where black represents moments with no measured values,
we can determine when "a lack of fact" is taking place. For instance it is considered that there
is lack of facts, in Figure 6.14 from 08:05 am to 11:05 am and from 12:45 pm to 13:10 pm.
While it can be suggested that a fact is likely to have occurred between 7:20 am and 7:35 am
(Activity 1), then again between 7:35 am and 8:05 am (Activity 2). Later, we detect other pro-
bable facts from 11:05 am to 12:15 pm (Activity 3), then from 12:15 pm to 12:45 pm(Activity
4), and finally one from 13:10 pm to 13:35 pm (Activity 5) (the coloured lines in Figure 6.13 are
represented in Figure 6.14 as blue arrows).
.

The change point model results, were compared with the annotated facts in the database la-
belled as : "cooking", "dish-washing", "shower", " ? ? ?" (fact not mentioned in the data base),
"working" (see Figure 6.14).
Now let’s focus on the "cooking" labels in Figure 6.14. Notice that only Activity 1 and Activity
4 corresponded closely to the moments in which the label "cooking" was annotated. The Activity
5 and Activity 2 could potentially be confused with the fact "cooking" given that presence was
detected in the kitchen as it can be seen in the heatmap (Figure 6.11), which triggered change
points, but, as annotated by the inhabitant, it was not the activity "cooking" happening, it was
actually "dish-washing".
Figure 6.11 shows the energy consumption of the hotplate from 11:00 am until 12:40. One
"cooking" annotation was provided from 11:00 am to 11:05 am. However from 11:05 am until
12:05 the label "working" was provided, rather than "cooking". This could possibly be a case
of simultaneous activities and the inhabitant privileged to annotate the label "working". If this is
right, then it can be said that the Activity 3 corresponds closely to the moments that the "cooking"
fact happened.
However from 09:50 am to 09:55 am the "cooking" label is provided, but no measurements
from sensors are observed (see Figure 6.11), therefore no change point is detected.

Figure 6.13 – Change point model window size equal to 1230s for the "cooking" fact

Figure 6.14 – Data labels in database, change points detected (blue arrows), estimated facts
numbered from 1 to 5.

#### 6.5.2 A posteriori annotations conclusions

This work proposed an a posteriori annotation tool to allow inhabitants to annotate activities
at their convenience, providing flexibility when responding to notifications. This approach aims to
help users recall the start and end of events, improving their ability to reflect on past activities.
The Jensen-Shannon change point model was tested to identify transitions in sensor data, re-
presenting potential beginnings and endings of activities. However, the method showed sensitivity
to window size selection, which posed a challenge. A manual adjustment option, where users de-
fine the window size based on contextual knowledge (e.g., "cooking" duration), was suggested.
Nonetheless, in some cases one same activity as "cooking" can have a different time duration,
while others such as a "washing cycle" could be always constant in its time duration. This could
be discussed in future research. It could also be interesting to explore the option of automatizing
the window size selection if this method is to be used.
A second difficulty that the method presented was the interpretation of the points marked, to
define if a point states the end or the beginning of an activity specifically. The heat map visua-
lization emerged as a key tool for this. Discretizing sensor measurements in a heat map visual
representation revealed activity transitions of start and end of facts (e.g., changes from "null/very
low" to "medium/high" values could represent the start of an activity while the opposite changes
"medium/high" discretization to "null/very low" could represent the end of an activity) and per-
iods of inactivity could be inferred from the periods in which "null/very low" levels are observed.
These improved clarity when facts occurred. In comparative testing, heat maps proved effective in
identifying what was annotated by the inhabitant as "cooking" and "dish-washing" , though am-
biguities arose given that the movement sensor (a common sensor for both facts) was affected by
both facts. Reducing such ambiguities will be important in future research. Possible inhabitants
knowledge could help clarifying the ambiguities. For instance, even if the heat map shows activiy
in the kitchen at 16h, the occupant might know that at that time they could not be cooking.
A notable contribution was the observation that heat map visualizations alone could provide
sufficient insights for inhabitants to recall past activities, potentially eliminating the need for
change point detection methods. Further experiments are necessary to validate this across different
scenarios.
Human-Computer Interaction (HCI) techniques can be also implemented to improve the pre-
sentation style of the graphics here showed as well as to facilitate the usage and understanding of
the a posteriori annotation tool of the tool . The graphical style used here is just an intermediate
option of representation.
The effectiveness of this tool should still be validated in future research, and it should be
evaluated if it actually helped the inhabitants to remember about their past facts. Inhabitants could
remember, for instance, that yesterday they cooked at midday, the next question to answer is how
to help them recalling the information of the context as it was proposed in the (5WH+performance)
in Chapter 2.
In the next chapter are presented options for the inhabitants to get their answers, once the
listening period of the experiments is over. This means as well that the facts recognition process is

completed.

## Figures extracted from the source PDF

![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-109-image-077.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-109-image-079.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-110-image-081.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-114-image-083.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-115-image-085.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-116-image-087.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-117-image-089.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-118-image-091.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-119-image-093.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-120-image-095.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-125-image-097.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-126-image-099.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-128-image-101.png]]
![[_assets/initial-thesis/06-annotation-based-facts-recognition/page-129-image-103.png]]
