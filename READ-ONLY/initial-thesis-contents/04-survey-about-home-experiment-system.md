---
title: "Survey about the home experiment system"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Survey about the home experiment system

[[Initial thesis index|Index]] · [[03-experiments-system-to-recognize-facts|← Previous chapter]] · [[05-annotation-free-facts-recognition|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Survey about the home experiment system

In this chapter it is explained a survey that was carried out in France
to evaluate hypothesis about questions from inhabitants, their inter-
actions with a numerical system based on experiments and their in-
terest in such a tool.

### 4.1 About residents questions

A survey was carried out by the author of this thesis, in France to a population in Grenoble.
Fifty seven answers were received from people of different ages between 22 to 76 years old,
with a majority of answers from people from 22 to 34 years old. 38 people were male and 18
people were female. This latter fact was not specifically chosen as such. It randomly happened
after the survey was shared online, it was not known who was answering. They were explained
about the fact that the activities in the buildings (and specifically in the residential sector), have
an energy consumption and indoor environmental comfort impacts. We asked them to define a
question that interested them concerning the impact on energy consumption or air quality and
comfort temperature of an activity. If this task was complicated, they could skip the question.
82.5% of the people answered with an example of a question, the other 17.5% decided to skip
the question. From the people who answered, the questions were evaluated to know if they were
questions that could be answered with the system. It was concluded that 36.8% were questions
that the system could answer by carrying out experiments. The other 47.4% of the answers were
more general questions on environmental impact (and not specifically related to activities in the
buildings) or the questions were not clear. This questions were not suitable for the generation of
experiments. The rest 15.8% did not answer.

Figure 4.1 – Age of survey respondents

The intention was to observe if people ask themselves questions related to the impact of their
activities. Most of the people could express questions related to environmental impacts, but not
properly the type of questions that could be tested as it is proposed in this project.
After that, it was asked if defining a question was an easy task. 45% of the respondents said
that it was easy, 35% said it was not easy, and the rest of the respondents said it was more-less
difficult. As a good part of the respondents said that it was quite difficult, we conclude that the
task is not evident for them.
Then, we made the hypothesis that by showing some examples, the people could better un-
derstand the sort of questions that they can answer with the system. Therefore, examples of the
type of questions that can be solved with the experiments, were provided :
1. What is the total energy consumption when I cook ?
2. To cool the room during the summer to a comfortable temperature, which option consumes
less energy : leaving the air-conditioning on at an average temperature during the day, or
turning it off during the day and using it when I return, at a lower temperature ?

Figure 4.2 – Gender of survey respondents

Figure 4.3 – Type of questions given by the respondents before showing examples of questions

Figure 4.4 – Level of ease to define a question

After giving this examples it was asked if they could have more ideas of questions. 49% said
that they could actually have more ideas, 35% said they didn’t need more examples and 10%
still find the task complicated. One more person said that it was the kind of questions he/she had
thought of but was not sure that it was the kind of questions expected. Another person said he/she
did not have more questions and one last person mentioned that he would like to understand the
utility of the activities. This last answer was not very clear.

Figure 4.5 – Level of ease to define a question after seeing examples

Finally they were asked once more to provide an example of questions. This time, 61.5 percent
of the people provided an example that corresponds to questions that can actually be tested by
the system and 9.62 percent didn’t provide an answer. They considered this task of the survey
repetitive.

Figure 4.6 – Type of questions given by the respondents after showing examples of questions

The questions provided were a better fit for the system by 25 percent more than before showing
the examples. This proves that it will be important to guide the people through the process of the
generation of the experience. It will be necessary to clearly explain the objective of the concept
of experiments, whether it is by explaining or by showing predefined examples of experiments
directly in the interface.

### 4.2 About the process of selection of sensors in an experiment

It was asked to the survey respondents to imagine they’ve installed the system and the sensors
to measure the energy consumption of the various appliances in their home, as well as sensors
to measure temperature and CO2 levels. They were told that in the imaginary scenario, they pro-
grammed the next experiments :
1. How much energy do I waste when the computer is on and I’m not at my desk ?
2. How much energy do I consume when I use the dishwasher in different wash programs and
in different contexts (full load, a few plates) ?
3. Does the room temperature drop when I open the living room window ?
Then, they were asked to choose from the following list of sensors, the ones they though
would help to answer the question asked. This means that they should choose sensors related to
the electrical appliances they use in their activity, in order to obtain information on the energy
consumption of these appliances, as well as environmental sensors for temperature, movement
and CO2, if they deem it useful.
List of sensors :
1. Computer power consumption
2. Desk motion sensor
3. Desk temperature
4. Desk CO2
5. Living room temperature
6. Sensor detects opening and closing of living room window
7. Motion sensor in living room
8. Dishwasher energy consumption
9. CO2 in kitchen
10. Motion sensor in kitchen
11. Hob energy consumption
For the first example of experiment : How much energy do I waste when the computer is on
and I’m not at my desk ? It is important to measure energy and detect presence. Therefore it will
be important to select the sensors that provide power consumption information and motion and
CO2 sensors with the ones it is possible to detect presence. According to (Amayri et al., 2016), to
estimate the occupancy of an area, the best is to combine a motion detection sensor, an computer
power consumption sensor and an average acoustic pressure measurement. The CO2 also showed
to provide good information when the author compared the information gain (IG) of each sensor.
CO2 results were similar to power sensor by achieving an information gain of 0.5. Motion and
acoustic pressure reached an IG of up to 0.75 and 0.78.
35% of the respondents chose sensor 1 (computer power consumption), 26% of the respon-
dents chose sensors 1 and 2 (computer power consumption and motions sensor in the desk), 14%

chose sensors 1, 2 and 4 (computer power consumption, motions sensor in the desk and CO2
in desk). Meaning that the 35% of respondents would have missed to detect motion. Only 40%
(26% + 14%) of the respondents chose correctly the sensors and can detect presence and energy
consumption. The rest of the respondents chose only one sensor, some of them chose sensors 9
(CO2 in the kitchen) only or 8 and 11 (dishwasher energy consumption and hob energy consump-
tion) which are not related at all with the activity to analyse. 1 person answered he/she is against
the installation of sensors, other person said that the question was too complex and another person
said he/she never leaves the computer on.

Figure 4.7 – Sensors selection for question 1

In the second example of experiment : how much energy do I consume when I use the dish-
washer in different wash programs and in different contexts (full load, a few plates) ? The main
interest is to know the power consumption related to the activity. Let’s remind that during this acti-
vity, presence is not particularly part of the activity. The occupants don’t need to be present while
the dishwasher machine is working. 80% of the respondents chose the sensor number 8 which
corresponds to the measurement of the energy consumption. Two people emphasized that it would
be important to record the number of articles to wash. This is interesting given that in the proposed
system of the present thesis, these type of information could be also registered using the annota-
tions, while the sensors cannot record this information by their own. 6% chose only the sensor 6
(window contact sensor). This respondents would have known when the window is open, but they
would not know the impacts in the temperature from this activity. Other respondents chose extra
sensors like the C02 in the kitchen, motion sensor in the kitchen or hob energy consumption. One
more person decided not to answer by introducing no as an answer.

Figure 4.8 – Sensors selection for question 2

For the third example of experiment : Does the room temperature drop when I open the living
room window ? It will be important to know the moments in which the window is open and the
temperature in the room. It could also be interesting to compare with the external temperature.
Although the difference of temperature in the room before opening the window and after opening
the window could be a good indicator. 43% of the respondents chose sensors 5 and 6 (living room
temperature and contact sensor of the window). 25% chose only sensor 5 (living room temperature)
but no contact sensor of the window. 9% of the people decided to choose the same sensors but
adding the motions sensor. They did this probably to detect presence. 5% of the people chose only
sensor 6 to observe the opening and closing of the living room window. Therefore they would not
know if the cause of changes in temperature would be the opening of the window.

Figure 4.9 – Sensors selection for question 3

Lastly, one person said he/she has no need of sensors to answer this question. Maybe he/she
meant that they would grade according to the feeling of comfort in the temperature. However,
studies have showed that the human perception of heat, cold or comfort might vary and in some

cases although the temperature lowers down, people can still feel a hot environment or vice versa.
The type of activity carried out or the clothes used, can have an impact on the individuals percep-
tion(Hoyet et al., 2024).

Figure 4.10 – Temperature felt by occupants in summer 2022 and the measured changes of
temperature

### 4.3 About the interest in a home experimenting system

The last question of the survey was if the respondents would be interested in an home experi-
menting system as the one presented.
At the moment that the survey was carried out, only 2 (modality and intention) annotations
were presented to the respondents. The question was asked to the respondents in the next way :
Would you be interested in a system capable of linking your activities to their impact on energy
and environmental comfort ? To measure this impact, environmental sensors would be installed.
This system could use your help. You’ll need to add information about the modality of your activity
and your intention. The system will record your answers and learn automatically to make things
easier for you.
For example :
1. intention : "cool the room"- modality :"open the window/door".
2. intention : "wash clothes"- modality :"30°C
In the second example, you could observe whether your clothes are sufficiently clean by wa-
shing them at a low temperature (30°C). You’ll also observe the corresponding energy impact. If
you’re not satisfied with the quality of the wash, you can try a temperature of 60°C, but you’ll also
see the difference in energy impact (energy consumption could be higher). The choice is yours, but
you have the information and can assess where you can reduce your energy consumption. You’ll
also get a better idea of your environmental comfort and preferences.
We consider that :
1. Intention and modality information cannot be detected by the sensors.
2. Sharing this type of information can enable you to evaluate the effectiveness of your activity.
This means you can observe whether you were able to satisfy your intention to "cool the
room" by "opening the window".
As it can be seen in Figure 4.11, 58% of the respondents said yes, 33% of the respondents said
no and 9% did not provide an answer.

Figure 4.11 – Interest in the system

### 4.4 Chapter conclusions

A survey was performed to better understand the inhabitants questions about their energy
consumption and the impacts of their activities at home. After the survey, it was concluded that
some guidance is necessary, on the type of questions that the system can solve. Otherwise the
questions that the survey respondents proposed were not specific of the activities at home or were
hard to measure with environmental sensors. For example, some wondered of the CO2 impact of
the car usage, which is not a home activity. Another person wondered about how much heat is
radiated by a person in a room. Although this question could be calculated, the system does not
include algorithms to respond to this question.
The respondents were also evaluated on the sensors selection for specific cases. In case where
several sensors were necessary to detect different impacts for one same experiment, around 40% of
the respondents chose the necessary sensors. The rest of the people could miss some sensors that
would provide interesting information. This was to be expected given that it is not always evident
to know which sensors could provide the information needed. Definitely advice should be given to
the inhabitants on the sensors that could provide important information for different experiments.
Moreover different tests should be carried out by experts to formalize sets of sensors that would
be useful. Studies from other researchers could also be used to better define the sensors to use.
Lastly questions about their interest in the proposed system were asked. They were given
an explanation of the fact that the system could associate the human behavior and its effects
in the energy consumption or environmental comfort. They were mentioned that in some cases
they would need to provide information that cannot be recovered by sensors. With the approach
proposed they were explained that they could better understand their behaviour and their energy
consumption and comfort impacts. 58% of the respondents said they were interested, 33% answe-
red that they were not interested and the rest did not answer the question. During the survey 2% of
the respondents answered that they were against the installation of sensors.

## Figures extracted from the source PDF

![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-080-image-047.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-081-image-049.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-081-image-051.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-081-image-053.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-082-image-055.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-082-image-057.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-084-image-059.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-085-image-061.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-085-image-063.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-086-image-065.png]]
![[_assets/initial-thesis/04-survey-about-home-experiment-system/page-087-image-067.png]]
