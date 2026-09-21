---
title: "Energy consumption centered in inhabitants: characterization of activities"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Energy consumption centered in inhabitants: characterization of activities

[[Initial thesis index|Index]] · [[01-buildings-energy-management|← Previous chapter]] · [[03-experiments-system-to-recognize-facts|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Energy consumption centered in inhabitants :
characterization of activities

In this chapter, methodologies to understand inhabitants activities
are shown. Automatized systems and sensors are part of the methods.
Although interesting results have been shown, certain difficulties and
limitations are presented. It is also introduced the importance of en-
gaging inhabitants in the virtuous process of energy efficiency. Se-
veral projects involving the cooperation between inhabitants and the
system are explained. Lastly a proposal is presented of interesting in-
formation that could be shared by the occupants in order to construct
solutions to avoid energy waste (information that could not be reco-
vered by sensors) by observing the root causes of their activities and
their effects.

### 2.1 Activity recognition

A building is finally a set of services provided to the occupants. Inhabitants have needs, such
as the need of thermal comfort, needs of hygiene, physiological needs such as eating, etc. The
inhabitants modify the state of the services of a building, i.e. they carry out actions and activities
to fulfill their needs. Several of this activities require energy from electricity or gas, for instance.
The activities carried out have environmental impacts, by the consumption of energy resources
and other impacts such as CO2 eq. emissions and economical impacts, due to the cost of the used
resources. There is also an outcome related to the satisfaction of the occupants : whether or not
these services fulfilled their needs.
In order to better understand the occupants impacts on the environment, it is important to
relate effects such as the energy consumption to its causes, the occupants behaviour. Researchers
have worked on systems to perform an automatic activities recognition, to find out the causes of,
for example the energy consumption impact. The activities recognition has not just been applied
to energy consumption studies, health applications are also found, as well as elderly care, for
example.
In an electricity invoice, it can be seen that in some periods there is higher energy consumption
than in others. To find out the reasons of this variations one needs to look closer to the way
inhabitants fulfill their needs. So far the main questions answered have been : What activities
consume energy ? How much energy they consume and in Which moment of the day ?.
Different approaches have been tested to model the impact of behaviour over the energy
consumption and internal comfort of the buildings. One method is the data-driven approach to
estimate occupancy and/or activity recognition (Chen et al., 2012). It uses probabilistic or statis-
tical models built by machine learning from training data sets. A model predicts and classifies
information by finding patterns using data mining and machine learning techniques. This data can
be image-processing (cameras), or based on sensors positioned in the environment or portable
like those on your smartphone. Nevertheless, the use of cameras is considered intrusive, which
is why ambient or wearable sensors are increasingly being used as part of this approach (Chen
et al., 2012). Some studies based on accelerometers and gyroscopes can help understanding mo-
tions (like walking or sitting) (Marcello et al., 2019), but more complex activities can be difficult
to figure out, specially if residents can’t always take the sensors with them. People might prefer
sensors installed in their home such as motion sensors, door sensors and temperature sensors .
An impact is not necessarily measured by only one dedicated sensor. In (Amayri et al., 2016),
different types of sensor are compared to estimate the occupancy of an area. To estimate occu-
pancy, the best results were obtained by combining a motion detection sensor, an area computer
power consumption sensor and an average acoustic pressure measurement. Other sensors were
also tested, including CO2 concentration, door and window openings and closings.
Once the sensors information is collected, probabilistic approaches such as hidden Markov
models, Bayesian networks and decision trees are used to automatize the learning process (Chen
et al., 2012). (Wang et al., 2012) use a naive Bayes model to recognize activities. The aim is to
recommend music for each activity. They asked 10 people to annotate 1200 songs for the training
and to relate them to activities as running, walking, sleeping, working, studying and shopping.
In total a 30h data set was used for the 6 different activities, each activity has 30min sensor data
collected by each of the 10 participants. They also used data from gyroscopes, accelerometers,
GPS receivers, microphones and light sensors. A window size of 5 seconds seemed reasonable
for the authors. Later, 2 participants used the recommendation system for one week. If the recom-
mendation didn’t pleased the participants they could skip the song or change to manual mode. The
system updated constantly and became more accurate. After the one week adaptation phase, they
achieved 95% accuracy, but before they alreday reached 86%.
(Marcello et al., 2019) used bayes theorem considering independencies of each activities. They
intended to obtain a profile according to users habits so that they can guarantee adequate solutions.

Data from the CASAS set have been used, this data set contains environment sensors information
and annotations of people’s activities (10 different ones) : meal preparation, relaxing, eating, wor-
king, sleeping, dish washing, moving from bed to toilet, entering home, leaving home, house
keeping. Part of the data set was used to train the system and another part to test. In figure 2.1
the number of labels collected for each activity. Once known the most probable activities, each
sensor is treated as a feature and it is associated to a specific activity, like this the time steps are
defined, not fixed, but sensor-based. Meaning that the window contain equal number of sensors
events. This is considered since when an activity is executed, multiple sensors could be triggered,
while when no activity is carried out, the sensors wont register many measurements (C.Krishnan,
Narayanan, 2014). The test was performed using training time of 2 months , one week of test data
and a window of 10 sensors events. Given that some of the shortest activities had between 5 to 15
sensor events(Marcello et al., 2019).
They were able to obtain which activities are more statistically probable when events are as-
sociated with a sensor and is counted for a number of times during instances associated with one
same activity. They reached an accuracy of 80% for the activities recognition and a prediction
of the following activity with an accuracy of 60%. an accuracy of 80% and a prediction with an
accuracy of 60% None the less they point out that their system could work with only one person
carrying out activities, and besides consecutive activities. When more that one resident is to be
considered, then some changes might need to be performed. A multi activities and multi-users
context is common in the residential sector.

Figure 2.1 – Number of labels per activity
.

In energy consumption applications, the Building Energy Comfort and Management (BECM)
systems have the objective to reduce energy consumption in buildings, while fulfilling the comfort
needs of the occupants. Often they control the heating, ventilation and cooling systems, lightning,
hot water and electricity. To accurately fulfill the occupants requirements, the activities and pre-
sence of the occupants are taken into account. The BECM systems can recognize automatically
the activities to create awareness and be a decision support for the occupants, or it can "satisfy
user comfort without human intervention or interaction", controlling the different services of the
building. The effective energy and comfort management might not be reached, even if real time
information is recovered. Take the example of light systems there is a difference in the moment
of last detected motion and the moment of turning off the lights. This timeout can be adjusted
between 5-30 minutes. However if the timeout is too small, the lights could turn off while the
occupant still needs light, but if it is too long, then energy could be wasted if the lights turn off
and there is nobody in the room. The recognition of activities and preferences of occupants might
help optimizing the controlling system (Nguyen and Aiello, 2013).
Already recognizing the occupancy in buildings can help to reduce energy consumption. A
study was carried out in the university of Korea. Occupant and number of occupants recogni-
tion and prediction was studied using indirect sensing data as environmental sensors and energy

consumption combined with machine learning techniques. CO2 concentration sensors humidity
sensors, motion sensors and energy consumption of lights and appliances were used. Data col-
lection for this study took place during seven non-consecutive weekdays. Occupancy data, envi-
ronmental factors, and power consumption were recovered every 1 minute. The Classification and
Regression Tree (CART) was used for the recognition of activities. The prediction of occupancy
was carried out using Hiden Markov Models (HMM). Using the indoor and outdoor CO2 concen-
tration ratio as observation state in the HMM resulted in the most accurate results for occupancy
prediction at future states with a 93% of accuracy of prediction. Other sensors sets were tested to
define the observation states they included indoor CO2 sensor only, indoor CO2 and movement
and electric power consumption and appliances. The authors noticed that when there is high occu-
pancy the prediction was more accurate than in days of low occupancy. They considered that the
cause could be few training data on low occupancy days.The authors concluded that the CART
algorithm was well suited for occupancy detection and the HMM method was also a good choice
for the prediction of occupancy (Ryu and Moon, 2016).
(Milenkovic and Amft, 2013) state that controlling the building services based on activities
could reduce energy consumption in office buildings. The researchers investigated the possibility
of detecting activities in office buildings using sensors that are often already installed in offices
such as passive infrared (PIR) usually known as motion sensors, and power plugs meters. The
study included more than 100 hours of data from a room with one single person and a room
with three people. The training data set was divided in 1 hour sections. Presence, not presence
and computer work and desk work (without using computer) were the activities to recognize. The
number of people could also be recognized based on the presence in each desk. Layered Hidden
Markov Models (LHMM) were used for the recognition. They concluded that with around 30h of
training data a recognition of 80% can be achieved. They mention that lights could be diminished
when people are not present or when people work with the computer, while lights usage could be
increased when doing desk work. Computers could also be turned off if presence was not detected.
It would be interesting to study not only the activities recognition but also the preferences of the
occupants before programming a building control. Maybe the occupant prefers to have the lamp
on even when working with the computer if the office receives few light. Although they achieved a
robust accuracy using few sensors, in this context the number of activities that can be executed in
an office are fewer and easier to recognize compared with the number of activities of a residential
building. Presence in an office can also be easier to observe based on the usage of the computers
of each desk, while in the residence context more than 1 person can be involved in the use of one
single appliance, for example when watching TV.
Studies by (Yoon et al., 2022) have been realised in the residential sector using environmental
and energy use data to detail occupant activities. Environmental measurements, were used, since
the occupants behaviour affect the indoor environment. In addition, smart meters reflects the cor-
relation between the occupants and usage of appliances. They saw an opportunity to control and
predict usage of services in the building, by understanding the activities. The researchers argue that
knowing the activities would allow to measure the MET (metabolic equivalent tasks) to determine
the optimal temperature settings of the dwelling, for example. Besides, they say, the right environ-
ment services could be turned on in the right space or appliances could be turned off if they are
detected to not be in use. They proposed the recognition of activities using energy usage informa-
tion (several sub meters in appliances) and environment sensors : internal and external temperature,
humidity and CO2 concentration. Their research was carried out in a test-bed with characteristics
as a residence which included floor heating systems, lighting systems and appliances such as te-
levision, hot water mat and laptop. All systems and appliances could be used freely and could
be adapted to the occupant preferences. Then the accuracy of the activities prediction would be
compared with image data collected by a web camera installed in the dwelling..
The detection of 11 activities was achieved, but only 7 were used for the classification, given
that they accounted for more than 98% of all behaviours : sleeping, non-occupied (or away),

Figure 2.2 – Activities observed using camera (Yoon et al., 2022).

working, resting, cooking, eating, and exercising (see Figure 2.3).

Figure 2.3 – Main activities carried out (Yoon et al., 2022)

Three different machine learning non supervised methods were tested with different combi-
nations of environment sensors and different combinations of energy consumption of appliances :
Random Forest (RF), k-nearest neighbors (KNN) and support vector machine (SVM). When tes-
ting the RF and KNN method they found out that using three or more environment sensor measu-
rements, they reached accuracy in their results of up to 0.9 f1 score. The SVM had lower accuracy
depending on the variable combination, but when using temperature, CO2, relative humidity and
PM2.5, they could reach 0.85 f1 score. When they used only energy consumption data from ap-
pliances the accuracy of recognition was much lower with highest f1 score of 0.5 particularly when
using hot water mat, television, laptop and lighting. When combining both information environ-
mental and energy consumption data, using RF and KNN, they achieved a minimal f1 score of
0.97 for 4 out of the 7 activities, while using SVM, the accuracy was up to 0.9, but failed for the
activity "cooking". 9 days lasted the experiment, the data was recovered ant one minute interval,
and 9455 observations were analysed excluding missing data or outliers.
They could find out habits of the inhabitant like that he turned on the hot water system for floor
heating while he slept and this was confirmed due the augmentation of CO2 concentration in the
room. Other habit observed was the fact that the inhabitant watched tv while cooking or eating,
given that the tv energy consumption increased.
Their method and findings are quite interesting, they selected 7 main activities, but only one
study might not be representative to dictate that the same 7 activities will be important to observe
in other dwellings, it really depends on the life-style in every dwelling. Predefined activities might
limit the diversity of possible activities executed by occupants in a bigger population. Besides for
the classification, the images were labeled manually by monitoring the images in a 1 minute time
step.
(Thomas and Cook, 2016), focused their studies also in the energy management challenge.

They proposed a system to automatically turn off appliances when the system detects that an
activity has finished and predicts that the activity wont continue. The researchers did their study
in a smart home environment equipped with 118 sensors. These include motion sensors, magnetic
door sensors, temperature sensors and electricity usage data. In this study activity learning has two
roles : activity recognition to identify the current activities and activity prediction. In the activity
recognition the sensor data is first collected and then features are extracted. The features are then
labeled by an expert and used as data to train the system or they are used to test the trained model,
to generate new activity labels through machine learning algorithms. In their study they used a
recognition algorithm called CASAS-AR based on Support Vector Machines (SVM) as classifier
in real time (Krishnan and Cook, 2014). Meaning that the labeling happens on streaming data.
To train the activity recognition labels were provided by humans who annotated their activities.
15 activities were annotated. 14 of them were clearly defined as cook, bathe, sleep, watch TV,
etc. And if an activity was not on the list, the label "other activity" could be used. To train, the
sensors and labels data was recovered for 1 month from 3 smart buildings. The activity prediction
problem is to determine the activity in the next 10 minutes, then time windows were considered
of 10 minutes.The researchers achieved a 95% of accuracy of activities recognition after testing in
30 smart homes. Then they tested the prediction algorithm to automate the home. 3 month data of
labels and sensors were used. A set of devices is associated with each activity. The devices should
be turned off if they were not used in the present activity and in the predicted activity to occur in
the next 10 minutes. If the occupants wished to leave the device on after the algorithm detected that
it is no longer needed, buttons were installed. A double tap on the button, would leave the device
on. The activity prediction is a binary classification problem, it indicates if each activity will or
will not occur in the next 10 minutes. Activities that occur often and activities easy to predict, such
as sleep, have better prediction accuracy than the less frequent and less predictable activities. The
activities that were incorrectly detected, anticipated and automated had a negative impact on the
users comfort. In terms of energy, the system helped reducing consumption up to a 50%.
(Ahmadi-Karvigh et al., 2018) also proposed a "Real time activity recognition for energy effi-
ciency in buildings", but differently from the previous mentioned methods, they used the knowd-
lege based approach. This approach is funded on the daily living observations, the place where
the activities are carried out, the objects used, the moments of the day when they are executed.
Specially routinized activities. There is a relationship between activities and its context that may
allow inferring activities. It is usually represented by schemas or networks. The objective is to use
the semantic relationships between for example objects and activities : a tea pot is used to prepare
a tea. This approach intends to be as complete as possible due to the activities diversity, therefore a
lot of information might be necessary to build the activity models. Also this method cannot handle
uncertainty and it is difficult to adapt to changes (Bouchabou et al., 2021).
In the studies by (Ahmadi-Karvigh et al., 2018) actions are detected thanks to environmental
sensors such as energy consumption of appliances and motion in rooms. This is used to later
recognize activities (set of actions) through semantic reasoning on a constructed ontology. They
detect the activities in an "online-form", meaning that the activities are not completed, they are
being performed.
In the knowledge driven approach, ontologies are created with the activities and their contex-
tual relationships. The authors developed their own ontology (Ahmadi-Karvigh et al., 2018).They
used an unsupervised approach based on inductive and deductive reasoning. A knowledge-base
was built acccording to the possible contexts. This means that the activities should be know a
priory to develop the ontology and to be able to classify the sensors information.

Each of the actions had to be defined for each artefact (for a computer and a monitor, 3 actions
had to be established to be detected :on, off and stand-by, extracting features from the raw measu-
rements and using K-Means and EM algorithms to facilitate the classification of the actions. The
number of the actions needed to be known so that the algorithms could receive hyper parameters,

prior to clustering.
Later an algorithm performed a deductive reasoning to proceed on the activities recognition
using the developed ontology. The ontology contained classes : "scenario", "action", "artifact",
"space", "occupant". Each of this classes contained sub classes defining in detail the context. The
instances of class "scenario" represented the current activity- For an "occupant" : occupant-A wor-
king in "space" : work-station-1, using "artifact" : monitor and chair , carrying out the "actions" :
sitting-on-chair and turning-on-monitor. The information could be defined thanks to sensors infor-
mation. For example the artefacts could be known, for instance, because measurements from plug
meter and a motion sensor are given to the algorithm.

Figure 2.4 – Schema of ontology (Ahmadi-Karvigh et al., 2018).

In figure 2.4 can be observed that the ontology contained information of the space, the objects
used and the occupants implied, but it is not included the moments when the activity is carried
out, the intention of the activity or the way in which the activity is executed (one same activity
can be realised in different ways). This information could be interesting to know, but not easy to
pre-define in a system of ontologies. This information might just be recovered from the occupants
knowledge directly.
To validate the method, occupants from an office and a dwelling, annotated their activities and
the start and end of them. This method reached high percentages of accuracy : 97,6% for action
detection and 96,7% for activity recognition. This method might be very useful for activities that
are performed in general in the same way with the same appliances in the same places, which
is not always the way it happens. Or In reality, the ontology should be adapted to each dwelling
context. However, activities should not be generalized, when there is a wide diversity of life events
in complex contexts, such as residences. The number of activities to evaluate could be limited to
a specific list (part of the ontology), therefore occupants can only analyse their energy impact on
the activities programmed. Lastly the authors talked about how the ontology would work when
different occupants participate : "In a scenario where 2 different occupants perform different ac-
tivities, two instances of class "scenario" two instances need to be created for each occupant,
one sub class for each one. If one occupant performs multiple activities, multiple instances are
related to the same occupant". Nonetheless, it is not mentioned how using environmental sensors
they could differentiate from occupant A and occupant B, i.e. for example a motion sensor detects
when a person moved, but it cannot differentiate who performed the movement.
Different methods have been presented that intend to recognize activities automatically, spe-
cially with the use of sensors. Different computerized methods have been utilized to carry out an
automatic recognition of activities. Then, annotations or the use of cameras is required to evaluate
the accuracy of the method used. Often this methods are limited to the recognition of a set of
activities. Moreover, they can be limited to the context that it is studied. Nonetheless they demons-

trate the possibility of carrying out an automatic learning of the activities with high accuracy. For
health applications or elderly care, this automatic recognition is quite useful, but in the objective of
energy management this methods would hardly involve the inhabitants by automatically recogni-
zing the activities. Besides it is also true that inhabitants might have interesting information that
sensors cannot detect. (Nguyen and Aiello, 2013) realised a survey on energy intelligent buildings
based on used activity. After reading about the activities recognition methods and its application
to energy management, they concluded that wireless sensor networks are promising for future de-
velopment of technologies in energy management of buildings. They consider that cameras and
wearable sensors might not be necessary. Besides they claim that to optimize in terms of energy
efficiency and comfort, being aware of the users activities and the context of the environment is
fundamental. Moreover they strongly believe that further building context information is needed.
In the next sections this idea is explored.

### 2.2 Knowledge from system and inhabitants

The majority of the impacts of the buildings services, are not visible such as air quality, energy
flux, temperature, etc. Therefore measurements from sensors are necessary to understand the actual
state of the environment (Ploix et al., 2021). Besides, human actors carry out activities even in
unconscious ways as habits appear (Ploix et al., 2021). The lack of attention from occupants to the
activities may lead to practices that cause a waste of energy or high energy consumption results.
On the other side, if measurements are just recorded but no association to activities is carried out,
people will just understand the final outcome of their energy consumption but they won’t know
which activities have more impact. It is proposed, as shown in the next table, that complementary
information belongs to both, the inhabitants and the information systems.

Inhabitants                                        Information systems

Qualitative perception                             Can measure the effects of events

Knows expectations and intentions                  Provides a numerical representation of the
building systems

Decides over the systems and the building,
but might not be conscious of the decisions

Has the information of comfort preferences         Can record the services configurations
and needs
TABLE 2.2 – Complementary information from inhabitants and information systems, Alyafi and
Ploix in (Ploix et al., 2021).

Deeply understanding what is happening often requires to know the Beliefs, Desires and In-
tentions of inhabitants, the BDI architecture (Adam et al., 2016). It’s not enough to detect an
activity, but it’s useful to determine the underlying intentions. Additionally, when there are seve-
ral humans, they reach compromises thanks to deliberations before acting (Kashif et al., 2011).
Firstly, dwelling systems have been considered as purely technical with inhabitants represented as
disturbances, like in building energy simulations. Then the concept of humans in the loop (Jung
and Jazizadeh, 2019) appeared, which is a progress, but humans are just contributors to loops.

Here, we propose a wider position for inhabitants : we consider they are taking the most impor-
tant decisions in buildings, such as changing the configuration of the envelope or starting/stopping
appliances or starting/stopping appliances. We propose to involve and empower them. Buildings
are socio-technical systems where humans have to be considered as part of the system and not just
like external decision makers.
Buildings are socio-technical systems where humans have to be considered as part of the sys-
tem and not just like external decision makers By definition, a socio-technical system (STSs)
depends on both a technical part and the behavior of the people. It involves an interaction bet-
ween the social subsystem (members of a structure and their roles) and the technical subsystem
(mechanical and informational aspects) (Wilpert, 2015). Residences are STSs in which the inha-
bitants must be considered as central : they decide on the layout of the place, the use of electrical
equipment, the operating points of heating and ventilation systems, and the renewal of equip-
ment. They also influence their residence through their presence in a given space. Collaborative
socio-technical systems (CSTSs) are a subset of STSs, i.e. they allow the process of information
exchange between the human actors and the technical part : the data collected by sensors. We
propose that a CSTS is equipped with a decision support system offering a service to residents to
help them achieve their goals while avoiding energy waste. In the next section some examples of
CSTSs are shown.

#### 2.2.1 Annotation systems

(Matsui et al., 2020) tested an easy labeling system for elderly people. They used a system
based on push button, but therefore only a specific selection of activities could be annotated (“ba-
thing,” “cooking,” “eating”, “going out”, and “sleeping”) Besides the buttons to be pushed were
installed in locations where this activities are generally executed. A questionnaire was also provi-
ded to the inhabitants for them to confirm whether the activities were carried out and if they had
remembered to push the button. The button had to be pressed at the beginning and at the end of the
activity, but sometimes the inhabitants could forget. This system allowed to recover data over long
periods of time (2 months) and it was conceived to be easy to use. Nonetheless the number of acti-
vities to observe was limited. Other systems were compared for the annotations, one of them used
Graphical user interfaces were it was possible to collect up to 27 activities and 60 to 100 labels
per day. In total, 28 days were recorded. The annotations were marked when they were started, but
not when they were finished, which facilitated the task (Alemdar et al., 2013). Bluetooth headset
combined with speech recognition software have also been tested with 7 activities recorded, none-
theless it had to be programmed to transform speech to text and the annotations had to be spoken
specifically such as "begin take shower" (van Kasteren et al., 2008). It was found that expert an-
notation can be done by an observer of videos, which is often time consuming. PC software have
also been build to guide on the process of expert annotation. A complete interface was included
with video visualization of cameras, possibility of annotation by typing and sensors location vi-
sualisation (Rockinson, 2003). This 3 different authors developed the tools to generate data sets
that could be used later for automatic activities recognition mainly for elderly care applications,
but energy efficiency applications have also been developed.
(Herrmann et al., 2021) explored the domestic energy consumption using interactive annota-
tion. Twelve households participated in annotating their activities linked to their energy consump-
tion data, specifically when there were peaks. They found out after interviewing the participants
that the process of annotation helps the inhabitants to interpret their consumption and makes
them reflect how they are using the energy and gives some ideas of how they could reduce their
consumption. The inhabitants were able to indicate the period of time that an activity lasted and
they could also add notes, for example about the appliances they used. It was interesting for the
researchers to observe the different labels that the users annotated. Some people could specifically
observe which appliances they use the most, others annotated the activity and not the appliance

and others realized that information was missing when they annotated just the peaks : they felt cu-
rious of knowing the consumption of other appliances they used that didn’t generate a peak in the
energy consumption measurements. Moreover, the inhabitants expressed to be surprised of how
much energy some of their appliances consumed and actually decided to change some habits such
as turning off the lights or even preferred washing dishes by hand than using their dishwasher.
An annotations system with energy measurement purpose was developed by (Rollins et al.,
2014). Notifications were sent to the inhabitants through a smartphone to annotate their situa-
tion, specially when changes in energy consumption patterns appeared over a threshold of po-
wer consumption. Since every house has different appliances and have a different minimal power
consumption, they developed a clustering algorithm that could automatically estimate the thre-
shold of the change point for the context of each residence. They found out that there are devices
that represent a "background load" (devices that are connected and have a repetitive pattern). To
reduce the number of interactions for this devices, they structured an algorithm that detects if more
than 80% of the time there exists a change in the power state of the device, then this behavior is
most likely coming from the device itself and not from a inhabitant using the device. In the author
words "if a device transitions between power states in more than 19 h of the day then the device is
likely not manually controlled by the user and will not trigger notifications".
(Phan, ), proposed the utilization of a smartphone application to annotate activities. A list of
activities to study was defined based on activities with important impact on energy consumption
of the dwelling studied : personal care, drying clothes, washing dishes, washing clothes, cooking,
entertaining (computer, tv, music, etc.). The authors used ambient sensors. Sensors included : PIR
motion sensors, power consumption, door and window contact sensors, CO2 sensors, air tem-
perature and relative humidity. The proposal included building activity estimation model using
Bayesian Networks, a graphical model to represent relationships among variables and their proba-
bility distributions. It was considered the fact that activities are executed based on habits, which
means that the occupants execute their activities in similar ways and at same moments of the
day. The researchers had to know which appliances were used for different activities, which they
could recognize automatically through information gain analysis. Once the sensors were selected,
the model would only consider the appliances observed for each of the activities. The authors
mentioned that electricity consumption measurements, the hour of the day and the recognition of
presence, through movement sensors provided important information for the model to be accurate.
Accurate results were found, for example, when comparing the estimated profile for the activity
cooking with the actual profile. Although their findings were interesting, the model would need to
be adapted to every dwelling. There is a wide variety in life events and habits in the residential
sector. Different activities to the ones studied (personal care, drying clothes, washing dishes, wa-
shing clothes, cooking, entertaining) should be considered, specially if the intention is to observe
the activities with an important impact on energy consumption. As showed by (Kashif, 2016) high
energy impacts can come from low power consumption appliances as well as from high power
consumption appliances. This depends on occupants behaviour. Besides, using the same bayesian
networks of this precise model for other contexts might turn into inaccurate results, given that they
were adapted to the usage of appliances and schedules of one specific dwelling.
(Amayri et al., 2019) tested a supervised learning method, the interactive learning. This me-
thod consists of direct interactions that the system has with the occupants to request information of
the number of occupants in the room. It allows to link sensors information with the truth known by
the occupant. Their main question is when are the interactions necessary ? The researchers carried
out real time experiments with people real people answering to the systems’ intervention. The ex-
periment lasted 5 days in an office context that contained 30 environmental sensors. The occupant
inserted the required labels for the training, meaning the number of occupants. Nonetheless the
authors emphasise that the time of collecting the data depends also on the occupants interest and
commitment to provide the data 2 classifiers were tested, a decision tree and a parameterized rule
based classifier. Two interaction criteria were analyzed to minimize the number of interactions,

Figure 2.5 – Model of bayesian network of the cooking breakfast activity(Phan, ).

while having the less labeling errors in the learning process : density of the neighborhood and
spread rate. Using decision tree, they found out that 16 interactions were needed as training data
to build an acceptable estimator with an average error of 0.03. The authors concluded that this
method was more accurate and less intrusive than when cameras are used and labels are added
manually which resulted in an average error of around 0.2. As the time passed it was observed that
the number of questions diminished, meaning that less intervention is needed from the occupants.
The first day, 10 interactions were necessary, the second day 5, then the last interaction happened
until day 5. In days 3 and 4 no interactions were necessary. It should be mentioned that the partici-
pants could choose to reject the question and not answer, therefore the time of collecting the data
depends also on the occupants interest and commitment. The system cannot perceive this, but the
number of questions could hardly be reduced through time, if no answers are provided .
(Awada et al., 2020) introduced the method of co-definition or Cooperative-learning. In au-
tomated labeling systems, the labels provided by the occupants are associated to information of
the sensors. The author mentions that in any system that recognizes activities using sensors, there
can be a difference between the activities that the sensor might end up recognizing and the real
experience of the occupants, like errors in the classification of an activity label to the wrong mea-
surements. In a first case, if the system already contains labels, the system will provide to a new
measurement of the sensors one of the existent labels (based on sensor data similarities), but this
might be an incorrect labeling. In a second case the occupants may annotate one same activity
in different ways : "working" and for the same activity the label "reading", therefore, if sensor
measurements are similar, the system might not know which of both labels to choose to make the
classification. In a third case the occupant might have annotated the same label, while the system
recognizes 2 different measurements. In a fourth case, the time period of the activity recognized
by the system, might not be the same as the occupant actually experienced it.
Notice that the computerized system along with the sensors might have a mistaken perception,
but also the occupant might have made a mistake when providing a label. The proposal of the
author allows to align the different perceptions based on a cooperation between the system and the
human actor.
The system uses a supervised learning method which requires the inhabitants to label their
activities. With the intention of recording accurately the information. The occupants can correct
what the system detects wrongly and when the system finds incoherent information between new
labels and past labels, the system notifies this to the occupants and asks for a verification. There is a
symmetrical interaction between the system and the inhabitant to improve the learned knowledge.
The authors included features generators to discretize the raw values from the sensors. When
the information was recorded and discretized from the sensors in a time slot, it was associated to
a label. If later, the same values of sensor measurements in a different time t1 are associated to a
different label, the computerized system experiences a "confusion". It cannot define autonomously
which of both labels it should choose : the label that has been previously recorded or the new label

Figure 2.6 – Co-definition and perception alignment (Awada et al., 2020)

just given by the inhabitant that is different to the one registered. This cooperative method can
also help the inhabitant to correct possible human mistakes in the labeling process. However the
cooperative interaction was defined to happen only once a day, therefore inhabitants will have to
remember what happened in the past and read the proposed labels by the system to decide if they
should be considered or corrected (Silva et al., 2022)
(Silva et al., 2022) tested a CSTS implementing interactive and cooperative learning in one
same system for occupancy and activities recognition in an office. They proposed the methodology
to learn about occupancy and activities in the office. Besides including the characteristics of the
two previous learning systems mentioned, the authors had access to a ground truth database to test
the process of search for confusions. They did not perform on-line labeling, they used information
obtained from cameras.

Figure 2.7 – Process proposed combining interactive and cooperative learning (Silva et al.,
2022).

The sensors used were motion, acoustic pressure and power consumption. Two different types
of labels were generated, numerical and non numerical. Numerical labels, included numbers from
0 to 3 and non numerical labels included "absence", "working", "meeting" and "visio". Nume-
rical labels were collected from 15 days while non numerical labels were collected for 3 days.
The authors concluded that non numerical labels are harder for the system to distinguish, which
leads to more need of confusions solving and updates, but the results are still reliable. The longer
the length of the labels data set result in the same affection, and besides the global accuracy of
the model decreases, for which the number of labels should not be very numerous. Results were
promising after analyzing the two criteria : density of the neighborhood and spread rate for the
interactive learning. The results are satisfactory in an office-type zone, without any parallelism
in activities, but this solution as it was presented, is not suitable for a residential context, where
multiple activities can be performed in parallel, in different zones.

### 2.3 Theory of planned behaviour and BDI Architecture

According to (Ajzen, 2005). A person has an intention before it turns into an action. In daily
routines, people might be rarely aware of the intentions of their actions, "habits are established
when people have frequent opportunities to perform a behaviour under identical or very similar
circumstances". However even in this cases, research suggests that intentions are good predictors
of behaviour. When people has control over their behaviour, they act according to their intentions.
In the theory of planned behaviour (Ajzen, 2005), the intention is dictated by three main rea-
sons :
1. The individual’s attitude towards the behavior : Evaluation (positive or negative) that an
individual makes of performing a particular behaviour.
2. The subjective norm : The person’s perception of social pressure and norms.

3. Perceived behavioural control : The individual evaluates its ability to perform a certain
behaviour.
In general, the theory of planned behaviour states that "People intend to perform a behaviour
when they evaluate it positive, they experience social pressure to perform it and when they believe
they have the means and opportunities to do so" (Ajzen, 2005).
In the figure 2.8, The dotted line represents the concept that individuals who feel they lack
the resources or opportunities to perform a behavior are unlikely to engage in it, even if they have
a positive attitude towards the behavior and believe that others would approve of it the dotted
line is represented given that people who believe that they have neither the resources, nor the
opportunities to perform a behaviour will most likely not engage in the behaviour, regardless if
they have a positive attitude towards it and if others would approve the behaviour (Ajzen, 2005).

Figure 2.8 – Theory of planned behaviour (Ajzen, 2005).

The BDI of Michael Bratman’s is a theory of human practical reasoning also referred as Belief-
Desire-Intention. In this theory, agents are situated in a environment that changes continuously, and
they have also a constant perception, then they take actions to affect their environment, based on
their internal state. The theory is based on common sense in terms of psychology, to explain and
predict behaviour and psychological state of people (Smitha Rao M.S and Jyothsna.A.N, 2013) :
1. Beliefs : Represent the information about the environment, its current state and messages
from other agents, as well as its own internal information.
2. Desire : It is related to motivation and goals.
3. Intention : This is related to the means to achieve the agents desires. Represented as plans,
and chosen actions.
In the theory of planned behaviour, before passing to the actions, there is an intention, actions
that the person is convinced he/she will help them to achieve a goal. In the BDI architecture
this is related to the also called "intention" aspect, which is defined after having evaluated the
information in the "beliefs" aspect and once the "desire" is defined. Both theories coincide. In
the present thesis the knowledge of the intention is important since it is the "root cause" of the
activities performed. Inhabitants can have a diversity of options to satisfy an intention and different
inhabitants in different living contexts will proceed differently when carrying out their activities.
In the next section it will be showed the importance of this information that, in general cannot be
collected from sensors.

### 2.4 Facts definition

Households have access to a range of services to ensure their comfort, based on devices win-
dow openings and closings, shading devices, artificial lighting, electrical appliances, heating set
points management and domestic hot water. Inhabitants influence energy consumption through
their presence and use of services, to the point that, in high-performance buildings, the main im-
pact is due to inhabitants’ activities (Vorger, 2015). In general, these services bring a level of
satisfaction, have a monetary cost and an impact on the environment. To satisfy occupants’ de-
mands for comfort, services modify the configuration of a residence, e.g. windows are closed, the
heating set points is fixed at a specific value, or electrical appliances are used.

It is our goal to assess the impact (effects) on energy consumption and internal comfort of
causes that sometimes cannot be observed using sensor measurements. Nowadays it is possible to
measure and register the effects that are often not visible. The causes are still difficult to define.
To understand what is happening in a building, it is necessary to link environmental impacts to the
intentions, often linked to beliefs, and preferences of the inhabitants, as this is what corresponds
to their psychological experience. An activity like "opening a window" only makes sense if we
know the intention : ventilating to remove cooking smoke for example, "action that could be part
of a coherent sequence, i.e. a specific activity."

(Marcello et al., 2019) mention that preferences and habits of inhabitants are important to
understand because if a system that optimizes energy consumption does not consider this factors,
it would lead to dissatisfied inhabitants who will abandon the system. It might not be efficient
from the perspective of the occupants for example an HVAC system switching off earlier before
the users consider having reached thermal comfort.
The intentions give a meaning to the activities, and they are the drivers of them. The intentions
can be satisfied by carrying out different activities. Let’s consider an action (α) as the modification
of the state of services in dwellings. Let’s now consider an activity (A), as a sequence of actions,
performed with a particular intention knowing that a particular case is a sequence of a sole action
like "open the window". The same activity can be performed in different ways, leading to different
activity modalities (Ai ) . An activity modality refers to the way in which an activity is performed.
Modalities specify how the intentions are transformed into activities :
1. The use of a set of a specific service or appliance for an activity. For instance : people
intending to refresh the room could open the door or the window.
2. The configuration of an appliance. Example : a washing cycle at 60°C or 30°C, for a service
associated with a washing machine.
3. Details of a particular context. Example : “Receiving hosts” can have variations, it can be
someone’s birthday or the Christmas dinner.
Some intentions are associated with a comfort need that has an energy impact, some other
intentions are not at all associated with a comfort need, but the inhabitants decide to take action on
this intention. Anyways the action could have an energy impact. For example, the activity "ope-
ning the window" could be driven by the intention "letting the cat to go out" or with the intention
"need to refresh the air". The first intention is not related to comfort needs, and it can still have an
energy and comfort/ discomfort impact. The second intention is driven by the need of modifying
the internal atmosphere that could be considered "too hot" for the inhabitant. Intentions cannot
be predefined since the reasons for occupants to carry out an activity cannot be known a priory.
Although "refreshing the air" or "cooling down the room" can be provided as very possible predefi-
ned options, one cannot say that the occupants open the windows only for this two activities. There
should exist the possibility for occupants to customize by providing themselves the intention. As
seen in this example the intention could be "dry wet clothes". Now, lets consider an example of a

washing machine in which the intention is to wash different types of clothes "dirty soccer clothes",
"towels", "dog cushion". The possibilities could be wide.
Inhabitants learning from their intentions and the way they act to fulfill them is a way to explore
their habits and reactions. Instead of having a controlled environment or being told what to do to
save energy, inhabitants may gain awareness and learn of why they are executing activities, how
they are executing them and what are the effects, i.e. the impact of the activities. The effects are
defined here as measured or estimated changes in the state of appliances or services during the
performance of activities. Effects can be measured with the use of environmental sensors.
Eventually the inhabitants can decide which changes they can perform based on the awareness
gained. Moreover, they can discover, the actions that could fulfill their needs with less energy
impact. This actions would be specific for their building and their context. Changes could last
longer and be actually carried out, since the inhabitants are participating in the exploration of their
context, their needs, their intentions and habits.

### 2.5 Characterizing facts : a way to better understand the causes by

labeling based on semantic annotations

A system capable of learning human behavior through an interactive and cooperative learning
model has been tested by (Silva et al., 2022). In this system, there is an exchange of information
between occupants and an artificial system, i.e. an algorithm that classifies context-characterized
sensor data into activity-labels. Whereas in the interactive approach, the artificial system sends
a notification to gather information from a human actor, in cooperative learning, the artificial
system suggests corrections thanks to what it has already learned. Residents are then asked to
provide labels in the form of text, if they are available and wish to do so. A label for a given period
corresponds to the completion of an activity. In the present project it is proposed to go further
in the association of causes to impacts. Not only annotating activities, but to label what we call
characterization of facts.
One can go further and realise that not only actions and activities can have impacts. Therefore a
fact (ϕ) is here defined as an instantiated set of meaningful events in the dwellings, such as actions,
activities, home layout, changes in the residence or specific non habitual contexts. It is delimited
in time and may be characterized by annotations. Facts cause a perceptible modification in the
environment and provide a truth about an event. This results in meaningful recognizable sequences
of data measurements. Notice that the absence of events measurements provide information too
i.e. a process of reasoning on absence of data can also help inferring on facts. For instance not
detecting movement in the room can infer "absence in the room". Without a reasoning process,
anything could be possible "absence in the room" or "sleeping activity" or eventually "sensor
failure". Example : cooking breakfast in the kitchen the 8 October from 6 :30 to 6 :45.
Facts may include an action, an activity or a specific context. All activites and actions are facts,
but facts are not only actions or activities. A context of “kids absence at home during vacations
period” is not an activity, it is a fact that can have an impact in the energy consumption, such as
(potentially) energy savings.
The aim of CSTS is to assess the impact (effects) on energy consumption and internal comfort
even of causes that cannot be observed using sensor measurements. For us, the cause involves not
only the fact, but its characterization
The characterization of a fact can be described by : Meaningful labels (qualitative or quantita-
tive), freely chosen, using Semantic annotations. A semantic annotation specifies on the intention
of a fact, its modality, the people and objects involved and the place where it happens : its context.

annotations

The characterization based on semantic annotations allows to better describe the facts.
The semantic annotations are based on the 5W1H approach proposed by (Kashif et al.,
2011), in which the author makes an analogy between the BRAHMS (Business redesign agent-
based holistic modelling system) method and 5W1H questions (What ?, Why ?, Who ?, When ?,
Where ? and How ?) questions. BRAHMS is both a multi-agent simulator and a descriptive lan-
guage for recording and simulating human behavior. The language describes a context, mentioning
agents, geography, knowledge and object.(Kashif et al., 2011) and (Ebuy et al., 2020)have used
the BRAHMS method to study human behavior in the context of energy management studies.
It is proposed that inhabitants report the realizations of their facts and provide complementary
semantic annotations :
— Why : specializes the intention for the particular performance of a fact (qualitative label
expressed in form of text).
— How : specifies the way in which a fact is carried out (the modality). It can be a word or
words that help residents identify a particular case of an event (qualitative or quantitative
label expressed in form of text or numerical).
— Who : specifies the human actors, the people involved (qualitative or quantitative label ex-
pressed in form of text or numerical).
— What : describes the objects involved. The services of the building, the appliances used or
other objects implied (qualitative or quantitative label expressed in form of text).
— Where : specifies location of the fact (qualitative label expressed in form of text).
The question "When ?" specifies the beginning and end of the fact. This information is not
requested to the inhabitants in the form of annotation, it can be, for instance, recovered from
sensors information or the moment in which the other annotations are provided to the system.
One more annotation can be provided to evaluate the level of satisfaction of the intention ac-
cording to the fact modality chosen. The name given to this annotation is performance. This might
not be applicable for all the cases. It will depend if the inhabitant is interested in the evaluation and
the possibility to evaluate. The evaluation can be based on measurements (physical quantity such
as temperature or CO2 level) or perceptible by the inhabitants senses (quality of washing cycle
visually, amount of smoke visually and through smell, heat feeling, odor reduction). For example
if the intention of a fact is "cooling down the room", and the inhabitant decides to "open the win-
dow" to achieve his/her intention, the inhabitant can later observe if the temperature of the room
actually diminished by observing the change in temperature.
For example the fact "cooking" with the intention "preparing lunch" make less sense to eva-
luate the performance. In this work there might be no interest in evaluating for instance "preference
for the prepared meal". Though, it could be possible to make subjective evaluations if there is an
association to energy consumption or comfort impacts, such as "the quality of a specific washing
program", which has an impact in the energy consumption .
The level of satisfaction can be evaluated, for instance in a scale of 5 levels where 1 :"unsatis-
fied", 2 :"poorly satisfied", 3 : "moderately satisfied", 4 : "satified", 5 : "very satisfied". To facilitate
the task, the levels could be predefined and the inhabitants would have to choose one option of the
options proposed.
Here presented some examples of characterization :
— characterize : "cooking"
Why : christmas dinner
Who : Family
What : turkey, oven
Where : kitchen
How : oven 200°C
When : start date and time , end date and time

Performance : - (No performance to evaluate)

— characterize : "cooking"
Why : lunch
Who : Edgar
What : steak, stove
Where : kitchen
How : electric stove high heat
When : start date and time , end date and time
Performance : - (No performance to evaluate)

Note that this same activity ("to cook") has two different contexts.
— characterize : "open window"
Why : improve room air quality
Who : Rose
What : window on the back
Where : kitchen
How : open window
When : start date and time , end date and time
Performance : 3 (It is possible to evaluate the room air quality by observing sensor measu-
rements)

— characterize : "open window"
Why : refresh room
Who : André
What : window
Where : kitchen
How : open window
When : start date and time , end date and time
Performance : 4 (It is possible to evaluate the room temperature by observing sensor mea-
surements)

Note that for two different intentions (improving room air quality or refreshing the room),
the same modality can be used.

— characterize : "accommodate people"
Why : visits
Who : 2 people
What : general power consumption
Where : blue room
How : - (No specific modality)
When : start date and time , end date and time
Performance : - (No performance to evaluate)

— characterize : "go on vacations"
Why : vacations
Who : children
What : general power consumption
Where : - (No specific place implied)
How : - (No specific modality)

When : start date and time , end date and time
Performance : - (No performance to evaluate)

In this couple of examples, it is a specific context ("accommodate people" or "children in
vacations") that could have a specific impact in the energy consumption and comfort in the
environment.

— characterize : "washing clothes"
Why : washing
Who : Diana
What : sports clothes very dirty
Where : bath room
How : 40°C
When : start date and time , end date and time
Performance : 5 (It is possible to evaluate the washing quality)

— characterize : "washing clothes"
Why : washing
Who : John
What : sports clothes very dirty
Where : bath room
How : 30°C
When : start date and time , end date and time
Performance : 3 (It is possible to evaluate the washing quality)

In this example, people could observe whether their clothes are sufficiently clean by wa-
shing them at a low temperature (30°C). They will also observe the corresponding energy
impact. If they are not satisfied with the quality, they could try washing at a temperature of
60°C, but they will also see the difference in energy impact. The choice is of the inhabitants,
but they have the information and can assess in which cases they can modify their behaviour
to reduce energy consumption.

Notice that each of the examples represent 1 fact characterization. Variations of the examples
can exist, for instance another person carried out the activity, a different configuration of the
appliance could be chosen, different objects can be used, a different intention, etc.
Because the activities in a CSTS can be numerous, the ideal is for human actors to anno-
tate only if they are interested in knowing about their impact. To this end, we introduce the
concept of "experiment" developed in the next chapter.

### 2.6 Chapter conclusions

The methods presented have shown that the recognition of activities is possible with the use
of environmental and portable sensors that the inhabitants should carry with them. However, there
might be a preference for the estimation of activities based on environmental sensors, given that
other sensors need to be carried all the time by the inhabitants, which can be uncomfortable.
From the sensors information, certain activities are detected and even be predicted. Activities

should be somehow repetitive in order to accurately detect them and predict them. For instance
they should be executed at the same hour of the day, with same appliances and/or in the same order
according to other activities. However, changes in the way of executing the activities, spontaneous
or uncommon situations are hard to learn and predict. Activities with an important energy impact
could be left out of the analysis if they are not part of the usual habits. The recognition of the ac-
tivities with this methods require often the use of cameras or annotations to verify the accuracy of
the programmed detection. Due to the diversity of possible activities and the diversity of contexts
the methods would need to be adapted every time to the different life events in the dwellings,
which might not be practical.
The automatic recognition of activities does not involve the inhabitants, and it is often tested
to later control the settings and the moments of usage of the services of the dwellings. Leaving
few room for the occupants to decide or choose the moments and ways of executing an activity.
The inhabitants can end up living in an uncomfortable building and they might not understand the
saving energy benefit that the system is supposed to be providing. In this way they might abandon
the system and the interest in becoming more energy sober.
The recognition of activities can be useful when a confirmation of the execution of an activity
is necessary, for example for elderly care, to make sure that the occupants have carried of certain
activities. For the energy management, recognizing the activity is just the first step to understand
what causes a certain energy or comfort impact. For instance, if an amount of energy consumption
is associated to the activity "cooking", the inhabitants will learn that their energy consumption
when they cook is an X quantity. But the occupants have a feeding physiological need that they
wont abandon just to save energy.
In order to empower the inhabitants and make them part of the energy management, they
would need more information, for instance to understand how they perform the activity so that
they can observe their behaviour more in detail and realise if changes are possible. Even for a
same activity the impacts may variate. But what creates the difference ? In what way one same
activity was "different" to obtain a different impact outcome ?
This information cannot be collected from sensors. The ultimate goal in the energy manage-
ment is not to ask people to not carry out energy consumption activities, but to perform them in
a way that can be less consuming and to reduce energy waste, while the occupants needs are still
fulfilled.
In this thesis project, it is proposed that facts rather than activities are characterized. Since
other events, not only activities could have an impact. Facts can be described by their main fea-
tures, highlighting interesting information to better understand the way in which facts happen.
Beyond the facts themselves as a label (cook, wash, open window, vacations, hosts...), we could
be interested to know their characteristics : intention, modalities, objects and people involved,
places concerned and temporalities, to be able to learn from our behaviour. Associating not only
the activity to its effects, but the characteristics of it that resulted in an specific outcome, for ins-
tance : What appliances were used and how they were configured ? What was the context ? Why
the activity was performed in a particular way ?
While the computerized system can recover information measured with sensors of the impacts
(that are often invisible), the inhabitants have knowledge of the contexts and the intentions of their
activities. It is then proposed that an interaction can be carried out to associate the knowledge of
the occupants and the computerized system. It is to be developed in the next chapters how this
interaction help the inhabitants in the raise of awareness and consciousness in the way their facts
happen and their energy and comfort impacts.

## Figures extracted from the source PDF

![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-043-image-017.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-045-image-019.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-045-image-021.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-047-image-023.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-051-image-025.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-052-image-027.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-053-image-029.png]]
![[_assets/initial-thesis/02-energy-consumption-centered-in-inhabitants/page-054-image-031.png]]
