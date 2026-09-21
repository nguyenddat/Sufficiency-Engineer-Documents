---
title: "General conclusions and perspectives"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# General conclusions and perspectives

[[Initial thesis index|Index]] · [[09-applying-fact-characterization|← Previous chapter]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

General conclusions and perspectives

General conclusions and perspectives

In this thesis, we have presented a concept of a Self-experimentation aiding system that intends
to provide a tool for inhabitants to learn about their behaviour and its energy and environmental
comfort impacts. The proposal has been developed in this thesis for a residential context, where
environmental sensors are installed to measure the impacts.
The objective is to include the inhabitants in the energy management process and help them
understanding about their behaviour and the effects in their dwelling, rather than provide a system
that optimizes and controls on its own, the services of the occupants space. In this thesis the
concept of facts is presented in Chapter 2. Defined as an instantiated set of meaningful events in
the dwellings, such as actions, activities, home layout, changes in the residence or specific non
habitual contexts. This is interesting given that it is proposed not to focus only on activities to
study impacts, but to realise that other life events such as a specific context can influence in the
energy consumption and comfort level.
The concept of self-experiment implemented in this work, could act as a motivator of behavior
change to reduce environmental impacts. Self-experimenting gives freedom to the user to choose
what to study. By observing the outcomes of their actions, inhabitants can identify adjustments that
may be effective for them. Study cases were presented in Chapter 8. The selection of experiments
by the inhabitants was not validated, but inhabitants showed interest in making behaviour changes
by their own initiative in the experiments they were proposed to participate. It could be interesting
to make tests in the future in which they choose what they would like to evaluate and carry out the
experiments.
The concept was found to be tested previously in health studies in which patients evaluate, for
example, impacts in their health by what they have eaten in the day. This approach can be further
studied with applications in energy management systems. The present work provides some ideas
of what could be implemented for a home energy management application, however other methods
could serve the self-experiment objective, it could also be expanded to the industry or commercial
buildings for energy management purposes, as well.
This approach is particularly valuable for exploring various options and gaining self-awareness
throughout the process. However, when it comes to "self-experimentation" systems, their effecti-
veness in encouraging behavior change relies heavily on the active participation and curiosity of
the individuals involved to initiate these experiments. Might other techniques be necessary when
using self-experimentation to keep individuals involved ? This could be observed in future work.
Self-experimentation, as presented in this thesis, allows to isolate the analysis of different
life events in the dwellings and focus on each of them separately. Programming an experiment
requires to define, fist of all, a question of interest about a cause and its impacts. For example,
does the temperature in the room reduces, when opening the window to refresh the air early in the
morning ? The sensors that are affected for each experiment can also be specified. In this way, the
analysis can be adapted to different contexts.
Several examples of questions are presented in Chapter 3. Later in 7, some of them are de-
tailed as an experiment process. In Annex B, the design of a possible app interface for "self-
experimentation" is presented using some questions examples. Questions applicable to energy
communities were not developed, but it could be a good idea to visualize how this type of system
would work in a context where several dwellings were involved sharing energy and information

recovered from the system to agree on flexibility subjects. Another case that was not explored in
this thesis was making experiments with the information from the energy distribution operators
(such as the peak hours and different energy prices), to manage flexibility in the use of energy of
the dwellings.
A survey was carried out in France to 57 people in order to know if actually, the inhabitants
have questions about the energy and comfort impacts of their activities and contexts. Although
they wonder about impacts, it was concluded that, it is better to guide them, so that they can define
questions that the system could help them to explore. In the survey, questions that the system might
not be able to answer were proposed.
The survey included as well examples to evaluate the accuracy in the sensors selection. Simi-
larly, it was concluded that before they program experiments on their own, it will be important to
first explain users how the sensors work, what they measure and to provide examples of the cases
where they could use them. In this way, inhabitants will choose more accurately the sensors they
need for their experiments. To better advise on the sensors selection, different experiments than
the ones presented here, can be carried out in multiple residences. Likewise, more in depth biblio-
graphy in this subject could be explored to define the sensors that provide interesting information
in the process of recognition.
In the survey, the respondents were asked about their interest in such a system. They were
explained that their participation, as inhabitants, would be important. 58% of the respondents
answered they were interested.
Ideas of tools to facilitate the recognition of human behavior and its association to the energy
and comfort impacts were proposed : the annotations-free and annotations-based approach. The
annotations-free recognition, explained in Chapter 4, utilises what we call "signature extractors",
to translate the questions from a natural language. Signature extractors are algorithms that have
the function of filtering the raw data from sensors, and transforms it in information that is easier to
interpret and associate to facts. Some possible predefined signature extractors are presented, also it
is proposed that a combination of them could be customized by the inhabitant. Both of this options
were developed under specific examples, it could be good to test some more cases for a more
extensive validation of the proposal. Specially the option to customize which was evaluated so far
on only one example. The latter option has been tested in a prototype by connecting pluggable
software components. An interface that permits users to select and connect the components in
a more intuitive manner, still needs to be designed. So far the tool requires programming skills.
The comprehension and interaction of the inhabitant with this part of the system should also be
evaluated in the future
Until now, the signature extractors permit recognizing a single specific context. For example,it
was presented that it was possible to recognize the fact "energy waste" by spotting the moments
in which no presence was detected, but power consumption from the computer was registered.
However an aspect not explored in this thesis was if the inhabitant wanted to recognize a fact from
several scenarios in the same experiment, rather than just one. For instance, the same fact could
be also recognized if lamp is left on but there is no presence or the heater is left on but there
is no presence. It could be interesting to test to recognize a fact not only from one scenario but
from several, in one same experiment. Specially, given that some activities may involve different
scenarios. For instance, "working" could be recognized in several ways : using the lamp, using
the computer, detecting a phone call or a meeting (with acoustic sensors). A first test could be
developed using the option to customize and its current pluggable software components prototype.
Using the annotations-free recognition method, facts can be recognized by using environmen-
tal sensors. However certain information of the context of facts cannot be recovered only using
sensors data. Specially, information as experienced psychologically by the inhabitants, such as the
intention of the fact, the objects used, the way in which they configure the appliances they use
(which could cause differences in the impacts) and the number of people involved (which is often
difficult to estimate exactly using environmental sensors). The intention is interesting to recover,

given that it is what triggers the actions, but it also gives a clue of the effects to observe.
Nowadays, there exist tools that allow to associate the human behaviour with its impacts. For
instance, the amount of energy consumption that results of the activity "cooking". However, this
power consumption may vary according to the context of each time that one same activity is carried
out. The tool proposed in this thesis permits to recover data about the context so that it provides
more information to the inhabitants and that it improves their knowledge of their behaviour and its
impacts. In this way, the inhabitants can :
1. Be more conscious of their habits.
2. Understand which are the factors in their behaviour that might affect the impacts.
3. Make informed decisions.
4. Eventually change habits towards more energy sober behaviour.
In the annotations based recognition, occupants can provide information in the form of text.
Facts are delimited in time and may be detailed by annotations using what we call "characterization
of facts" (see Chapter 2) using the (5W1H+ performance evaluation). It was observed that the six
proposed annotations could be optional. Some annotations could be left empty if the inhabitant
considers it irrelevant (according to his/her question of experiment). In the manual annotations
carried out by inhabitants in Chapter 8, some annotations were not answered given that it in some
cases it made no sense to provide certain information. For instance, the modality to insert food in
the fridge. However no annotations were left empty for reasons such lack of will/interest from the
inhabitants.
Systems assisting the annotations process are explained in Chapter 6 : The Interactive and
Cooperative Learning (ICL) processes and the a posteriori annotation system. The ICL is an al-
gorithm presented in (Silva et al., 2022) that could facilitate the annotation process by recovering
information at specific moments, for which the occupants are notified. The quality of the data-
base of the annotations is optimized by the interactive learning process. While the cooperative
learning identifies and communicates to the occupants of possible annotations errors by detecting
incoherences between past annotations associated to measured effects and new annotations.
In Chapter 6, a simulation was executed for the first time in a residential context, using a da-
tabase that contained information from sensors and labels from activities of an inhabitant in an
apartment (Lago et al., 2017). This first test was also carried out under the concept of "experi-
ments" where one specific event was studied and particular questions that inhabitants could have
were answered (for this test, only, several questions were evaluated, but let’s remember that an
experiment was defined to include one single question. This could facilitate the comprehension
and the development of the experiment for the inhabitants. If it is interesting, in the future it could
be studied if it is possible to solve multiple questions for one single experiment.)
This first test provided quite accurate results in terms of the recognition of annotated facts. We
realized as well that carrying out experiments about specific contexts and providing answers to
established questions was possible using this annotation aiding system. The next step was to test
the annotations aid algorithm in a context of facts characterized with multiple annotations (5WH+
performance evaluation). It was proposed that the "cooperative and interactive learning" process
associates the sensors information to the labels that answer to the question "how" as explained in
Chapter 9.
Specifically for this experiment, any other fact than cooking was labeled under the name of
"other activities", given that the database contained labels of multiple activities and due to there
was no real time interaction between a human and the computerized ICL (Interactive and coopera-
tive learning) system. In this way, the label "cooking" could be isolated from the rest of the activity
labels in the database.
In a system with real time interaction, the inhabitant will have to provide a label that can
indicate that there is lack of occurrence of the fact of the experience -if it is the case- . While
the system might have to automatically provide a different and specific label to indicate if the

inhabitant never answered to a request of annotation. This should be developed in future work.
(This part is applicable also to the tests carried out in Chapter 9)
In the annotation process it could also be explored in the future, an option in which the in-
habitants declare their activities by their own initiative besides answering to the requests from
the Interactive and Cooperative Learning (ICL). It is still not known how, the annotations of the
occupants initiative, could be inserted and how they could influence on the process and results
of the ICL. Another option could be to provide a system of annotations by own initiative of the
inhabitants, without using the ICL as aiding system. It can be interesting to explore this, see if
inhabitants agree with the option and evaluate the outcome.
In the annotations-based approach, it has been envisaged that the inhabitants might not be able
to answer notifications immediately. They could need to delay their response. If this happens, they
might use some help. In chapter 6 it was developed a functionality that could help the inhabitants
to remember past activities : the a posteriori annotations aiding system based in a change point
model to propose automatically the instants that could correspond to activity changes.
With the Jensen-Shannon divergence method used, the size of window in the change point mo-
del algorithm has an important impact in the results. It was proposed that the inhabitants modify
this parameter using a slider that allows increase or decrease the size of the window. A manual
adjustment option, where users define the window size based on contextual knowledge (e.g., "co-
oking" usual duration). However some times facts could have different time duration. Automating
this window size selection could be important for future work if the change point model is to be
used.
A second difficulty that the method presented was the interpretation of the points marked, to
define if a point states the end or the beginning of an activity specifically. The heat map visualiza-
tion was a useful tool for this. By discretizing sensor measurements, heat maps revealed activity
transitions and periods of inactivity, improving clarity on when facts occurred. In comparative
testing, heat maps proved effective in identifying "cooking" and "dish-washing" activities, though
ambiguities arose when sensor data overlapped between activities. Reducing such ambiguities will
be important in future research.
A main finding was that heat map visualizations alone could provide sufficient insights for
inhabitants to recall past activities, potentially eliminating the need for change point detection
methods. Further experiments are necessary to validate this across different scenarios.
This tool can be useful to help the inhabitants finding a reference on the moments of start
and end of facts to complete the postponed annotations, nonetheless the question remains. If the
annotations requested are the characterization of the facts, would the occupants remember their
intention, modality, objects used, people involved ? It will be interesting to make a real time ex-
periment to know which information could the inhabitants remember. How could we help them
to complete information they might have forgotten ? Maybe previous answers could be registered,
but would this be enough ?
Once the recognition of facts has been carried out, the inhabitants could be interested in re-
ceiving an answer to their questions. Merger options (algorithms) are presented to provide to the
inhabitants in order that they select the information that better adapts to their expected answer.
Nowadays, applications that allow the visualization of energy consumption impacts, present the
information in many different ways all at once. Here it is proposed that the inhabitants can choose
specifically what they want to see as an answer such as : average power consumption, total power
consumption, number of times an appliance is used,etc. Further study and analysis in this parts
is recommended. The options of merger can be better defined, possibly extended as well. For this,
maybe more experiments in different dwellings contexts could be carried out. The possibility of
multiple selection of the options could also be interesting. It is still important to make a test, in
which inhabitants interact with the system to select from the mergers options. The interest from the
inhabitants in this tool should be similarly studied.
Graphical representations options were presented by previous studies. Their findings revealed

that individuals can effectively articulate their visualization preferences. The tool allows users
to select their preferred visualization from a set of options. This approach could be particularly
relevant in this thesis, enabling residents to freely choose the visualization that best suits their
needs and aligns with the requirements of their experiments. This part could be studied deeper
with experts in Human-Computer Interactions It could be analysed the interest and facility for the
user to choose from different visual options, but most importantly, their level of comprehension of
the results. The best is that for them the visualization is meaningful and clear.
In this work it is intended that inhabitants actively participate in the energy management pro-
cess. The system recovers information that can help inhabitants to better comprehend the context
that causes specific impacts. Although a real time interaction with a computerized system was not
implemented, some real experiments were carried out (in Chapter 8), in which inhabitants anno-
tated manually details of the facts to analyse. Two study cases and inhabitants interviews showed
that they could better understand their behaviour and their impacts by registering information
that cannot be recovered using only sensors. The inhabitants showed also initiative to change
their behaviour.
In terms of the manual annotations process, the occupants mentioned that it was not a compli-
cated task, but it was easy to forget to annotate, it was also considered like burdensome or tedious.
This is not surprising given that the annotations were carried out manually. Digitizing the task and
implementing the annotation aiding systems could provide a more dynamic process.
It was observed that the inhabitants mainly responded to how they carry out their activities,
currently. It can be interesting to develop a feature that could invite the inhabitants to explore
different options. In this way, they could test different behaviours and measure the effects to decide
on behaviour changes.
It is considered important to show specific examples of possible annotations in the charac-
terization of different facts in order to better guide the occupants on what they could annotate.
In some cases, no annotations were provided, while in other cases, unnecessary information was
added. When designing the interface, it will be useful to introduce the system to the inhabitants by
showing predefined examples that can guide them before they can develop their own experiments,
as shown in Annex B.
In conclusion, two different profiles could be observed, both with consistent habits, but one
with more variations declared in the intentions and modalities, while the other declared less varia-
tions. This stands out the importance of avoiding predefined annotations for the inhabitants, since
the context and the habits of the occupants might be different, specially when characterizing the
facts as proposed.
It was observed that in some cases, the annotation of the performance is more convenient
just after the fact, during the listening process of the experiment and in other cases, it can be
better in the end of the experiment. For example, in the washing machine context, it is possible
to annotate the performance just after the washing machine finished the cycle. The quality of the
washed clothes or dishes can be judged. If the evaluation is postponed, the inhabitant might forget
how was the quality of the washing cycle.
However in the case of the impact on the temperature of the room when opening the window,
it is better to grade the performance at the end of the experience once the temperature of the room
has been recorded for each of the moments that the fact was executed. While the performance
could also be graded according to the comfort felt by the inhabitant after having left the window
opened for a period of time. How to grade the performance is to be better defined.
In Chapter 9, simulations of the cooperative and interactive learning were performed, with the
experiments defined in Chapter 8. Observations were made about important factors :
1. The relevance of correctly annotating the characterizations and the possibility of making
mistakes in the annotation process.
2. The parameters used in the learning process, such as the time step, the sensors selected, the
features extractors used. It was observed that the "time-step" used in the cooperative and
