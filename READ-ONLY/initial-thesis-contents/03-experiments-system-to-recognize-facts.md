---
title: "An experiments system to recognize facts"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# An experiments system to recognize facts

[[Initial thesis index|Index]] · [[02-energy-consumption-centered-in-inhabitants|← Previous chapter]] · [[04-survey-about-home-experiment-system|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

An experiments system to recognize facts

In this chapter, details are given about a system that involves inha-
bitants in the energy management process by the means of "experi-
ments". The concept of experiment is presented and explained. Ex-
periments include questions from inhabitants about the energy and
comfort state impacts of their behaviour. Some examples are presen-
ted and possible questions are classified in three categories.

### 3.1 Multi-users and multi-activities recognition : state of the art

Besides the intrinsic complexity of recognizing an activity, there is a certain complexity on
recognizing multiple activities in contexts such as residences with multiple users. The activities
can be performed by different people in different times, some of them even simultaneously. To
recognize human activity, pervasive systems can be used, this means that ambient sensors are ins-
talled to collect data from human activity and environment changes. The main multi-occupancy
challenges are related with residents identification and data association but also with activity mo-
delling. The problem of data association consists of accurately relating the sensed data to the
occupant that is causing the effects on the sensors. In order to facilitate the sensors data associa-
tion, some authors have decided to use wearable sensors, given that the occupants impacts can be
better differentiated. Pervasive sensors don’t need to be carried by occupants, but the data associa-
tion to an specific occupant is more complicated (Benmansour et al., 2016).
(Li et al., 2020) mentions that ambient sensors, wearable sensors, and multi-modal sensing me-
thods can be used in multi-user activities recognition. The latter uses both, ambient sensors and
wearable senors. This can be a good approach to solve the multi-user activities recognition. More
complete systems even use cameras and microphones information. While certain sensors detect
for example movements, others, can detect localization of the people, sounds, etc. Nonetheless,
the cameras are still considered as intrusive.
In activity modelling, the interest is to define the order in which activities were carried out and
if they were carried out by 1 person or by a group of people (Benmansour et al., 2016). Just defining
the activity modality is complex and several authors have provided different classifications which
are similar, but according to their studies there exist some variations.
(Li et al., 2020) made a review on methods for multi-user activity recognition, classified by
application domain, sensing methods and recognition methods. Single user activity recognition
has been mainly studied, but multi-user activity recognition is relatively new. They mention that
there are multi-individual activities, hybrid activities and group activities. The first one is where
2 or more people execute different activities that are not related, while in the second case, there
are individual and grouped activities in the same context. The group activities is where two or
more people perform the same task. In multi users contexts such as residences, the activites can be
categorized as :
1. Simultaneous activity : multiple users perform one same activity as individual.
2. Conflicting activity : multiple users perform different activities with different goals.
3. Sequential activities : activities happen one after the other.
4. Collaborative activities : multiple users perform activities to achieve a common goal.
(Liu et al., 2016) mention that the different occupants in a dwelling perform activities si-
multaneously and that within an activity, actions can be performed sequentially, interleaved or
simultaneously. The authors also make the difference between actions and activities. Their interest
is to define general activities based on actions. Low-level actions and their temporal patterns can
be used to facilitate high-level activities recognition.
(Morveli Espinoza et al., 2022) consider temporality and durability in human activities. For
example, they define as conflicting activities the ones that cannot happen simultaneously, for ins-
tance a person cannot take a shower and cook in the same time interval. Other activities can be
partially and completely overlapped, i.e. they belong to the same time interval, but there is no
conflict between them, like talking by phone and cooking. Meaning that it is actually possible
that a person speaks while cooking, whether a person cannot be physically in two places at the
same time cooking and taking a shower. To model the time constraints, they use the Allens inter-
val algebra, a calculus for temporal reasoning. It considers a time interval and sub-events part of
the interval. The relationships (sequential or simultaneous) between sub events can be classified
in : before, meets, overlaps, starts, during, finishes and parallel. Then they use the Timed Abstract

Framework to find the relations of "attack" between activities i.e. conflicts between arguments. Ar-
guments are the data and the attack relations are demonstrated by arrows in a graph. The temporal
relationships between arguments define if there is an attack between activities. When there is a
sequential relationship, there is no attack between activities even if they are considered conflicting
activities (first cooking and later shower), since they can be performed in different times, however
conflicting activities that happen in parallel have a relation of attack (cooking and shower at the
same time). To be able to apply this method, a list of activities had to be predefined : cooking,
sleeping, talking with mom, watching TV, etc. and for each of them the sequences of actions had
to be defined. For example, to talk with mom, the sequence was grab cellular->call-> talk with
mom.

Figure 3.1 – Sequence of activities (Morveli Espinoza et al., 2022).

Different to (Morveli Espinoza et al., 2022) computational models for activities recognition
have been tested. According to (Benmansour et al., 2016), almost all the proposed models are
probabilistic based on graphical models. Probabilistic models having the structures of graphs :
Bayesian networks, Markov Models, Hidden Markov Models, etc. (Li et al., 2020) conclude that
although one of the main recognition methods for data driven approach (meaning using sensors
data is, for example, the Hidden Markov Model : a method that allows to recognize activities at
time t, based on observable variables at the same instant. It might not be suitable for multi-person
activities due to the increment of features to consider. It might not be interesting also for concurrent
activities (one person performing two or more activities simultaneously.) They recommend deep
learning technology in complex contexts and in-depth study for combined cases with multi-user
activity recognition and single activity recognition. Specially when using ambient sensors, the task
is more challenging due to the diversity of contexts and the noise in the collected data.

(Liu et al., 2016) mention that to model the temporal relationships of activities, probabilistic
graphical models have been used, for example, but the complexity of the task increases as more
activities are added, and a large amount of information to perform the learning is required. They
have developed a method based on a pattern-mining algorithm capable of identifying temporal
patterns in actions and using them to represent activities. They used body-worn sensors so that
low-level actions (sitting, standing, etc.) and actions for each hand (opening, unlocking, etc.) can
infer 5 high-level activities : relaxing, early morning, coffee time, sandwich time and cleaning. The
authors mention how statistical approaches, using models such as Bayesian networks or Hidden
Markov Models achieve good results with sequential activities, but they have difficulties to treat
parallelism between activities.

As it has been observed the variety of ways in which activities can be carried out are not
easy to define and it is complicated to try to model them with current tools. Laborious methods
have to be used just to formalize the multi activities case with activities overlapping and having
multiple users. Next in this work it will be developed a proposal to deal with this matter that we
call "experiments".

### 3.2 The concept of experiment

(Silva et al., 2022) proposed an annotation system where only one scenario at a time could
be analyzed, in an office context. But in a residence, multiple scenarios can occur. Studying the
impacts of all the life events in the dwelling might not be interesting for the occupants. It could
also need too much of their attention, which could end up being overwhelming and it won’t involve
nor engage the inhabitant in the process of energy management. It is proposed that the occupants
perform what is referred, in this thesis as an experiment. The experiment is a procedure, undertaken
by the inhabitants to make observations about their energy consumption and/or the environment
comfort impacts. The inhabitants decide the experiments that they wish to perform.
Let’s remember that in this work, the impacts are observed directly over the facts : a set of
meaningful events in the dwellings, such as actions, activities, home layout, changes in the re-
sidence or specific non habitual contexts. They potentially occur in a defined location, and at
defined moments. Facts can be characterized by labels (qualitative or quantitative), freely chosen,
using Semantic annotations. The semantic annotations are based on the 5W1H approach pro-
posed by (Kashif et al., 2011), in which the author makes an analogy between the BRAHMS
(Business redesign agent-based holistic modelling system) method and 5W1H questions (What ?,
Why ?, Who ?, When ?, Where ? and How ?) questions. BRAHMS is a descriptive language for
recording and simulating human behavior. One more annotation was proposed to evaluate the per-
formance of the fact, therefore the semantic annotations proposed in this thesis can be named
(5W1H+performance). As explained in Chapter 2 section 2.5.
During the experiments, the inhabitants define a question to specify the life event they want
to study. This approach avoids having to study all possible events in the residence, allowing the
inhabitants to be selective. For example : What is the energy impact of different washing machine
configurations (e.g., 20°C, 30°C, and 60°C) ? or What is the energy impact when cooking ? In the
first case, the focus is on the washing machine’s impact, while in the second, it is on cooking-
related energy use.
Each experiment can be analyzed separately, different sets of sensors can be specified for
each experiment (and consider the appropriate information to observe the impacts) as well as its
corresponding characterization.
The experiment question helps the user to identify the most relevant information to gather
when characterizing facts. However, inhabitants can choose to answer all the proposed semantic
annotations (5W1H) if they wish or focus solely on those most related to the experiment question.
Answering all the annotations could provide a more comprehensive context of the facts. In some
cases, annotations might be inapplicable. For instance, if only one person lives in the residence,
defining who participated in a fact’s development might be irrelevant, as there is only one possible
participant. However, if the inhabitant receives hosts, identifying who participated might become
relevant. For example, the presence of guests could influence energy consumption patterns during
activities like cooking or laundry. In such cases, noting the participants could provide a clearer
understanding of the experiment’s context.
It is proposed that the performance annotation is requested only if the inhabitants state that
their question is oriented to the evaluation of the performance. This could be maybe achieved
through a button in the interface at the beginning of the experiment. Notice that this information
does not correspond to provide a more comprehensive context, but to an evaluation of the level of
satisfaction of the intention according to the activity modality chosen. As explained in Chapter 2
section 2.5.
The experiment question also permits to define which approach can be used to provide an ans-
wer : Annotations-free recognition or annotations-based recognition. Here, they are introduced :
1. Annotation-free recognition : This type of recognition does not need annotations to identify
or categorize the human behaviour. It has been observed that certain facts information could
be recognized using only sensors data. Raw data can be transformed into information easier

to interpret and associate to a fact using what we call here signature extractors which are
algorithms that have the function of filtering the raw data from sensors, and transforms it
in information that is easier to interpret and associate to facts. For example : The use of
the washing machine, can be observed directly from the sensors data processed by signature
extractors that transform the raw data of the sensors in a binary time series output that shows
the moments when the washing machine was on or off. It is proposed that signature extrac-
tors can be predefined or customized. In the first case a list is displayed and the inhabitants
can choose from it, while in the second case, the inhabitants can create combinations of
the signatures extractors, to better adapt the options to recognize facts. More details on the
signature extractors will be provided later in Chapter 4.
2. Annotations-based recognition : This method involves the use of annotations to identify or
categorize the human behaviour. In this thesis it is proposed to use the characterization based
on semantic annotations as explained in section 2.5 to describe the facts with detail using
the 5W1H and the Performance annotation. When using annotations-based recognition, cha-
racterization based on semantic annotations provided by the inhabitants, are necessary. This
means that the recognition of facts is difficult by only using processed data by signature ex-
tractors. Annotations characterizing the facts are necessary to give a more specific answer,
such as : To know the impact of different washing machine configurations (20°C, 30°C and
60°C), the sensor won’t recognize on its own if the washing cycle was programmed at 20°C
or 30°C or 60°C. Therefore, the inhabitants should provide this informartion to the system in
a text form. For the facts that require annotations, the Interactive and Cooperative learning
(ICL) (Silva et al., 2022) approach is used during annotation retrieval to facilitate the process
of annotation and check annotation consistency. The Interactive learning, triggers the mo-
ment of interaction to request annotations. The Cooperative learning proposes annotations
for its validation or correction. The moments of start and end of the fact is defined by the
moment in which the annotation is provided by the inhabitants or classified automatically
(by the algorithm).
Also a functionality to provide annotations later in time was developed in order that the
inhabitants can complete their annotations when they are available and not only in the mo-
ment they receive a notification triggered by the ICL, requesting for their knowledge. We
call to this functionality, A posteriori annotations. More details on the annotation-based
recognition will be provided later in chapter 5

An experiment covers a period of time that needs to be specified in terms of start and end dates.
As well as specific days and time-slots (if wished). This could be defined by the inhabitants. For
instance the period of analysis can be of 1 month, starting the 30/09 and ending the 30/10, only
during week days (from monday to friday) and only in the mornings from 8 am to 11 am. We call
the period of analysis of an experiment, the listening period. In this way, the inhabitants define the
most interesting moments for the system to focus on.
The inhabitants could potentially select, as well, the sensors and appliances that are affected
by the fact (temperature sensors, CO2 concentration measurement sensors, contact sensors, power
consumption sensors, etc.). Sensors are not pre-selected in this system. If the sensors were pre-
selected, certain appliances or environmental sensors could be missing in the analysis of impacts.
It is considered that the inhabitants own the main knowledge about the sensors and appliances
involved during the facts. Besides the inhabitants knowing their intention of carrying out a certain
activity can better determine the sensors to select. If the intention of opening a window is to
lower the temperature during the summer, the important sensor to select is the one that measures
the temperatures. In this way, residents can assess the effectiveness of their actions by observing
whether the temperature has actually fallen.
During the listening period of the experiment, automatic recognition of facts is executed. After
that, the recognized facts and their corresponding impacts are recorded. Once that the listening

period is over and all required information was collected, the occupants can choose from a list of
mergers : Algorithms that execute calculations to provide an answer to the inhabitants. Then he
occupants choose from a list of possible graphical representations. This tools can help them to
better understand the results of the experiment. More details about this aspect are explained in the
next sections 7.1 and 7.2. Lastly the occupants receive an answer to their experiment.
In Chapter 5 the annotations-free approach is described in detail, in Chapter 6 the annotations-
based approach is explained and Chapter 7 focuses on the representations of the results of the
experiment and some specific examples of experiments.

Figure 3.2 – Experiment process representation

The concept of "experiment" is interesting because :
1. It associates causes and effects,while avoiding overlap of information when simultaneous
facts occur. Simultaneous facts must be in different experiments and they should involve
different sensors. For simultaneous facts that share same sensors (even if they are in a dif-
ferent experiment), it was concluded that a method of charge desegregation would still be
necessary to measure the impact of each fact. (Nuora Al Akkari, et al., 2024) tested a method
to desegregate the water consumption based on the knapsack method.
2. It collects information that cannot be recovered using sensors and facilitates the annotation
process. The freedom of adding a label as a text allows to characterize the facts, which allows
the inhabitants to observe the impact level of facts. Then, when the inhabitants observe the
results, they are capable to distinguish the behavior that caused a specific impact, and then
they can decide if changes could be made in their habits, for example to reduce their energy
consumption or improve comfort conditions in a room.
3. It helps the inhabitants to have more accurate results by specifying the devices they know
are related with facts. This matter is related to habits in each context, for instance if a person
has the habit of watching TV while cooking. When this information is not specified, the
system is not capable to know it on its own.
4. It provides more freedom to the inhabitants to select the fact they wish to analyze. Besides
it helps inhabitants resolving questions they might have about facts impact’s.
5. It facilitates the collaboration between inhabitants and the system to generate answers. Be-
sides the inhabitants focus on specific experiments only, not on all the situations happening
in the dwelling.
It can be concluded that an experiment process includes (see Figure 3.3) :
1. A question from the inhabitants that specifies what they want to analyse. In order that, for
the inhabitants it is clear the sensors to select for the experiment.
2. Two approaches for the automatic recognition of facts :

(a) Annotation-free : Using a set of sensors information processed by signature extractors
to answer the questions. Signature extractors can be :
i. Chosen from a predefined list.
ii. Customized.
(b) Annotation-based : Using a learning system that collects information from the sensors,
as well as the annotations from inhabitants participation. Defined as interactive and
cooperative learning by (Silva et al., 2022).This system allows the characterization of
facts.
i. User labeled annotations using 5W1H heuristics to better document the facts.
ii. User labeled performance annotation : valuated annotation (from 0-5 for ins-
tance).
iii. A posteriori annotation : Allows inhabitants to answer, later in time, the annota-
tions requested by the interactive learning, as well as by the cooperative learning.
3. A selection of environmental sensors’ measurements (CO2,temperature, movement, humi-
dity, contact, etc.) and power plugs sensors measurements of the appliances involved in the
event to study.
4. An answer to the occupants question in a numerical or graphical format. Selection between
the merger options and the graphical representation.
5. A listening period while the recognition is performed. The process of automatic recognition
of facts takes place during this period. Therefore the semantic annotations (5W1H+performance)
are provided during this period.
6. Archived periods in which there are no automatic recognition processes executed, however
sensors information can still be recorded.
The system can be applied to multiple residential scenarios, such as activities, home layout,
changes in the residence or specific non habitual contexts. It is also possible to raise occupant awa-
reness, and the creation of an "experiment" could reinforce the occupant’s interest in interacting
with the system. The occupant retains a central role in creating an experiment, providing its own
knowledge through the selection of the sensors that are involved in the experiment, by providing
annotations (in the case of annotations-based recognition) and analyzing its results.

Figure 3.3 – Experiment architecture process

### 3.3 Levels of questions from inhabitants in an experiment

An experiment is based on a process of selection of what the occupants wish to analyse In
the context of an experiment, it has been considered that inhabitants wonder about the functioning
of home services. Questioning the energy impact and quality of environmental comfort, as an
effect on the modification of the services in the dwellings. Different examples of questions can be
proposed (see Figure 3.4).
For the purpose of this thesis, only the questions related to a residential context are analysed,
excluding grids and energy communities cases, but presenting them gives an idea of other possible
contexts of application.

Figure 3.4 – Questions brainstorm

A classification of the type of questions is presented, depending on the interest of the question
and if the evaluation of the performance is to be carried out :
1. Question oriented to appliances impact : this level of questions intends to answer to the
impact of specific appliances. The inhabitants are interested to know for instance, the power or
energy consumption of an appliance, to compare between a set of appliances or to know which
appliance consumes the most/least energy. The impact on environmental sensors, resulting from
the usage of specific appliance can also be observed such as CO2 or temperature can also be
observed. This question could be answered using annotation-free recognition or annotations-based
recognition. In the case of using annotations-basedecognition, the 5W1H heuristics annotations,
as explained in Chapter 2 can be used. But, for this type of question, the evaluation of performance
is not required. For example :
— What is the impact on energy consumption and on the temperature when setting the air
conditioned at different temperatures set points ?
Characterization of the fact :
Why : Set a comfortable temperature in summer (optional, not compulsory)
Who : André / Edgar (optional, not compulsory)
What : Air conditioner (optional, not compulsory)
Where : living room (optional, not compulsory)
How : 19°C, 20°C, 15°C (important to add according to the question)
When : defined by the listening period as well as the moments of annotation defined by the
interactive and cooperative learning.
Performance : - (not required)

In this example, the impact on energy and on the temperature can be studied due to the
utilisation of a specific appliance. Notice that it is important (due to the question) to define
the characterization How, however specifying the rest of the annotations, is a decision of the
inhabitant depending on how in depth they wish to define the context of the fact.
— What is the energy impact of two different appliances used to prepare the same meal (boeuf
bourguignon) ?
Characterization of the fact :
Why : (optional, not compulsory)
Who : Mary / Linda (optional, not compulsory)
What : robot, stove (important to add according to the question)
Where : kitchen (optional, not compulsory)
How : cooker-robot option boeuf bourguignon, stove heating level 4 (optional, not compul-
sory)
When : defined by the listening period as well as the moments of annotation defined by the
interactive and cooperative learning.
Performance :- (not required)

In this example, the occupant may compare the energy impact of two different appliances
when preparing a same meal.
2. Question oriented to fact impact : this question is made to evaluate the energy consumption
resulting of activities or contexts where multiple appliances are involved. The impact on envi-
ronmental sensors such as CO2 or temperature can also be observed. Specific events are also
included in this type of questions, for instance hosting a person or occupants leaving the dwelling,
an occupant in a room, etc. This question could be answered using annotation-free recognition
or annotations-based recognition. In the case of using annotations recognition. The 5W1H anno-
tations, as explained in Chapter 2 could be used, but, for this type of question, the evaluation of
performance is not compulsory.

For example :
— What is the impact on energy when François or Rose cook this week ?
Characterization of the fact :
First annotation :
Why : lunch preparation (optional, not compulsory)
Who : François (important to add according to the question)
What : stove, radio, oven, microwave (optional, not compulsory)
Where : kitchen (optional, not compulsory)
How : electric stove medium heat, microwave high level (optional, not compulsory)
When : defined by the listening period as well as the moments of annotation defined by the
interactive and cooperative learning.
Performance : - (not required)

— Characterization of the fact :
Second annotation :
Why : dinner preparation (optional, not compulsory)
Who : Rose (important to add according to the question)
What : stove, radio, oven, microwave (optional, not compulsory)
Where : kitchen (optional, not compulsory)
How : oven 200°C, stove high level, radio on (optional, not compulsory)
When : defined by the listening period as well as the moments of annotation defined by the
interactive and cooperative learning.
Performance : - (not required)

As it can be seen, the evaluation of the satisfaction of the intention "lunch or dinner preparation"
could be not specified. It might not make sense to annotate the performance of food preparation.
The intention in this example defines the meal to be prepared, such as lunch dinner, breakfast. The
inhabitants could observe also which meal tends to consume more energy for its preparation.
3. Question oriented to the evaluation of performance : this question is made when the inhabi-
tants want to carry out an evaluation of the satisfaction of their intention. However, they can still
observe the energy or comfort impact of facts. The inhabitants could define in the beginning of
the experiment if they wish to add this annotation option. Notice that this option, does not provide
information of the context, but it is really an evaluation of the level of satisfaction of the intention
according to the activity modality chosen. Different modalities could be carried out to satisfy their
intention, therefore these can be tested to define the activity modality that satisfies the intention
with a lower energy impact. The evaluation of satisfaction can be based on sensors data or only on
the inhabitants perception. In some cases, the measurements of the sensors reflecting the effects
provide information to objectively evaluate the level of satisfaction. For instance, the level of CO2
can be measured by the sensors and the inhabitant can observe if this characteristic, effectively,
diminished, after opening the window. This question could be answered only using annotations-
based recognition. The 5W1H as explained in Chapter 2 should be annotated, and for this type of
question, the evaluation of performance is required.
— Opening the window actually helps to ventilate the kitchen ?
Characterization of the fact :
Why : improve room air quality∗∗ (important to add according to the question)
Who : - (optional, not compulsory)
What : window on the back of the kitchen (optional, not compulsory)
Where : kitchen (optional, not compulsory)
How : open window half (important to add according to the question)
When : defined by the listening period as well as the moments of annotation defined by the

interactive and cooperative learning.
Performance : 3 (required and important to add according to the question)

This is the performance evaluated by the inhabitant, and therefore annotated. The inhabitant can
compare the intention (improve the room air quality) with the measured effects (CO2 levels, for
instance). Note that the inhabitants can also use its perception for information that might not be
recovered by the sensors, such as odor reduction.
∗∗ There could be other reasons for which the inhabitant opened the window, for instance
"take out the cat", this can still have an impact in the air quality.

### 3.4 Self experimenting as a tool to satisfy intentional learning and

motivate behaviour change
The present work proposes a system in which experiences can be programmed by the inha-
bitants of a dwelling. This makes it possible to deal with multi-activity/facts contexts. It is also
possible to highlight the causalities of energy consumption due to the cooperation between the
inhabitants and the system. Residents annotate facts, as this enable them to better assess the effec-
tiveness of facts, based on intention. This enables residents to observe their behavior and evaluate
their effects. Similar self-experimentation methods have been tested, for example, in the health
sector.
(Fedlmeier et al., 2022) did studies on exploratory self-experimentation applied to health be-
haviour change. The self experimentation system is considered to be close to what is proposed
in this thesis. They mention how in health applications it is important to individualise since one
solution might not be applicable to everybody. Personalizing is important when seeking to beha-
viour change to be maintained in the long run. They propose giving individuals a tool to develop
"their own change behaviour plan". They suggest that individuals are supported to explore the
causes of their behaviour and the modifications that could work for them. Self experimentation
allows to embrace the problem and its solution, while users attach to the modifications. The idea
is to "find meaningful self-knowledge that matters to individuals’". This tools should leave place
to creativity to implement changes that fits to their personal needs, preferences and context. In the
self-experimentation process, "the goal is not to answer to an hypothesis, but to explore different
options and learn about themselves in the process". The users determine if the options tested hel-
ped them achieving their goal and if they were compatible with their life-style. The researchers
mention that they focus on "enabling users to reflect, make informed decisions, asses the effect of
the change and refine them in the process". After having developed a prototype they mentioned
that this could help people to self-track the progress, but could also be used as a way to remind
to continue on the behavioural change goal. This tools could evolve by allowing users to develop
their own custom tracking tools. They found out after testing 3 of this tools, (non digital), that sho-
wing examples of possible changes facilitates users to later define new changes. They propose that
digitization of tools can allow an interaction and personalizing. Further, approaches to stimulate to
stick to the change can be also implemented. In their studies they worked with people motivated to
make changes. When people is not interested, more processes before self-experimentation might
be necessary.
(Daskalova et al., 2021) have discovered that the regular use of self-monitoring data is an
incentive to change behavior. They tested digital tools as the smart phones to collect information
and allow people to self improve. In current systems that allow a visualization of certain effects
(like energy consumption for instance) tracking too many things ; not having specific goals, not

knowing what to track or how to interpret data can be a drawback. When people define their
self-experiments they start with a goal in mind on what they are interested in observing. While
the "common model is to first implement a change based on an assumption of how helpful it
will be, in self-experimentation is the opposite. First, one learn something new and then use that
as motivation for making a change". Self-tracking allows people to decide if they are willing to
change or not.
For the current project, given that users proposed request for the installation of sensors, it is
assumed that they are interested, maybe not directly on making a change, but on learning more
about their home and to explore the ways in which they use energy nowadays. We propose that
users are intentional learners, given that they make questions about their systems and the efficiency
of their usage. The theory of intentional learning states that it is a cognitive process where learning
is the final objective. Intentional learners make decisions actively to achieve their learning goal and
in the process, they even learn how to learn (Mollman and Candela, 2018). The intentional learning
requires a "conscious intention to solve the problem or reach an acceptable decision". Learning
implies to be persistently changing on what one knows or is capable to do. When learning is about
change, it is important to measure before and after beliefs, attitudes, knowledge and skills. Using
instruments that can gather this information (Spector and Kim, 2014).
(Daskalova et al., 2021) proposed that different levels of self-tracking could be developed to
facilitate users the process to correctly recover data, integrate data and understand the outcomes.
They mention that prior guidance is key for the people to better understand the process. Later,
users with more expertise can customize the parameters they are interested in analysing. Using
strategies such as scheduled interventions and automatic analysis of the results could also simplify
the process for the users. In the next pictures, we can observe how they tested 2 types of apps,
one providing guidance and another one that allowed users to have more freedom in customizing
their analysis. Figures 3.5 and 3.6 allow to study the effects of practicing meditation. Figure 3.5
is designed for new users. The interface provides a certain guidance and parameters options are
predefined. The next figure (see 3.6) is designed for users who are already familiarized with the
interface that provides guidance. In this interface, the users can customize the parameters (that
were predefined in the previous case) to better adapt the analysis to their own situation.
Figure 3.7 is another example of app for advanced users. It allows observing the impacts in
health of eating certain foods in specific amounts. The users define the food and the type of effect
they want to observe. They can also define the scale to grade the effects.

Figure 3.5 – Allowing users to explore causes (meditation) and effects (level of energy) in the
process of an experiment. c) History of the experiments d) Results of increase of energy levels
based on 6 days of self-experiment (Daskalova et al., 2021)

Figure 3.6 – Advanced self-experiment app that allows customizing parameters in and c) and
guiding users by displaying a list of possible experiments to analyse in (Daskalova et al., 2021)

Figure 3.7 – Second example of advanced self-experiment app that allows customizing parame-
ters in c) and d). Presenting an example to help with the usage of the app (Daskalova et al., 2021)

(Boulmaiz, 2024) found, citing different authours ((Arroyo et al., 2005), (Fogg, 2003),(Oi-
nas Kukkonen and Harjumaa, 2009), (Pinder et al., 2018) and (Cialdini, 1993)) that persuasive
technologies can have a role of "tool" to make the task of change easier or to help the change be
consistent. Then there is a classification of using the technology under this role of the principles
of design, whether the tool is created to suggest, to supervise, to condition using positive reinfor-
cement, etc. Two of this principles of design adapt to our proposal : the principle of "adaptation",
in which the tool appears more persuasive to the users since it adapts better to the interests, per-
sonality or context of the users. The second principle that is part of the present proposal is the
principle of "self- monitoring" or self-supervising. Using this technology allows the individuals
to self-monitor and modify their behaviour to reach their objectives. Technologies can also have
the role of a "media", which means, the technology sends a message or transmits information in
order to modify an attitude or a behaviour. Under this role, the principles of design can be based
on showing the users the causes and effects of their behaviour. In the present project, the causes
and effects are revealed to the users, in a tool that adapts to their interests and allows them to self
monitor.
(Boulmaiz, 2024) cited also (Cano et al., 2015) who showed that persuasive functions can be
classified according to their goal, whether it is helping users to understand, to decide, to act or
to protect. The function that helps users to understand focuses on the way of explaining users for
example the relations between causes and effects. This explanation part in persuasive systems is
rarely implemented according to the findings of the researcher. He mentions that it is important
that users can accurately make the association between causes and effects. Rather than the users
investigate on their own what produced a peak in the energy consumption (after the peak was
noticed), tools could be proposed to help them make accurate relation between causes and effects.

### 3.5 Chapter conclusions

In this chapter it was presented, the concept of "experiment". When carrying out an expe-
riment, the occupants are able to decide what they are interested in studying. An experiment in-
cludes a question from the inhabitants. For example "I want to know how ventilating affects the
temperature of the room by opening the window". Other examples were presented in this chapter.
The questions were classified in three main types after presenting different examples as seen in fi-
gure 3.4 . Notice that this first classification, involves experiments to carry out in a dwelling. More
options of this classification could be envisaged, for example in cases of energy communities.
The current classification includes questions oriented to appliance impacts, questions oriented
to facts impacts and questions oriented to evaluation of the performance.
Given that the inhabitants select what they are interested in studying, during the process of an
experiment. They can select the sensors that are related to the events of study. It is the occupants
who know better which appliances they use and also according to their question they can define
the effects they want to observe : the energy consumption, the temperature, the CO2, etc. They can
also select the duration of the experiments by choosing starting date and end date of the study.
Then we propose two possibilities to carry out the recognition of facts : annotation-free recog-
nition or annotations-based recognition. According to the question and the facts to study it can be
determined which of both approaches to use. In the process of annotations-based recognition, the
inhabitants collaborate with the system by providing information of the facts such as the modality,
the intention, the objects and people implied as presented in Chapter 2. Details about both types
of recognition are explained in the next chapters.
This chapter provides a general view of the different concepts involved in the system. In the
next chapters more details and evaluation of the features proposed will be discussed. In section
3.2 a list is presented of why the concept of experiments can be interesting, such as recovering
information that is not provided by sensors, focus on specific events to evaluate or a more accurate
definition of the appliances and sensors involved in the events to study. Moreover in section 3.4 it
is presented that similar methods have been tested in health contexts also with the objective of rea-
ching behaviour changes. They call this approach as "self-experimentation" or "self-monitoring"
systems. Authors mention that individualisation is important given that one single solution might
not apply to everybody. Also the tool is provided to the individuals for them to explore the causes
of their behaviour and by observing the effects they can state modifications that could work for
them. It specially can help to explore different options and learn about themselves in the process.
If "self-experimentation" systems offer a different approach to motivate behaviour changes,
the involvement and interest of the individuals is key to trigger the experiments. We propose that
having the intention of observing or testing, and not necessarily having an important intention
of changing a behaviour is already interesting and could motivate in the long term to behavior
changes. Specially this motivation would come not from an expert saying the individuals what
to do, but from the same individual who is making its own observations and determining what
could/should be modified.

## Figures extracted from the source PDF

![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-064-image-033.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-067-image-035.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-069-image-037.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-070-image-039.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-074-image-041.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-075-image-043.png]]
![[_assets/initial-thesis/03-experiments-system-to-recognize-facts/page-075-image-045.png]]
