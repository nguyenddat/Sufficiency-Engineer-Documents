---
title: "Annotation-free facts recognition"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Annotation-free facts recognition

[[Initial thesis index|Index]] · [[04-survey-about-home-experiment-system|← Previous chapter]] · [[06-annotation-based-facts-recognition|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Annotation-free facts recognition

In this chapter the annotations-free recognition process is detailed,
explaining the elements required such as the signature extractors and
the modalities to use them : as predefined or customized. Examples
of facts and their possibility to be detected under this approach are
presented. Conditions for utilizing this approach are also presented.

### 5.1 Conditions for utilizing Annotation-free recognition of facts

In a residential apartment, contexts might be very diverse : couples, families, roommates,
disabled, single and elderly people, with different ways of living. There are multiple life events
(some of them are simultaneous), occurring in different zones and there are several inhabitants.
All this diversity influences the complexity of establishing the relationship between indoor impacts
(such as energy consumption) and its causes (facts).
(Schoofs et al., 2010) have proposed the use of a combination of sensors to detect the operation
of appliances. They presented work on "signature generation". A signature built from several sen-
sors, rather than just one, can reduce false positives. For example, the duration of use of a kettle can
be detected by measuring vibration, temperature and noise levels. If only the temperature level had
been used, the estimated running time would have been incorrect, as the temperature would have
remained high even after the kettle had been switched off. (Morales and Akopian, 2017), develop
a reflection on the ease of recognition of activities based on information collected from different
types of sensors. They mention that this depends on the activities to be recognized : actions such as
standing, walking or transitions, for example between sitting and standing, can be estimated with
motion sensors, but more complex activities such as working, may require additional data such
as GPS signals, indoor positioning signal and audio. They expressed that the relevance of signals
depends on the activities to be classified. For instance using barometer data and accelerometer
data increase accuracy in the recognition of walking down the stairs by 20%. Their findings about
the activities that can be directly inferred from the sensors measurements raised several questions
about the recognition and how to identify when there is a need of annotations in an experiment.
When discussing annotation-free recognition of facts, it is understood from the outset that no
details of the characterization, as presented in Chapter 2, can be recognized solely by using sen-
sor data. This is because sensors can only provide measurements information associated with the
specific moment in which the data was captured. Consequently, answers to the following ques-
tions cannot be derived using only sensor measurements : Why, How, Who, What, Where and
Performance. This information is important to be given by the inhabitants in the form of text.
And when this information is required, an annotation-based recognition is executed and not an
annotation-free recognition.
However defining when a fact happens, can actually be deduced from sensors data after sense
is given to the measurements using "signature extractors". A signature extractor is an algorithm
that integrate a knowledge model and perform filtering operations. These extractors are therefore
functions, possibly parameterized that treat a stream of data as input and produces a stream of
categorical data as output.
In the process of annotation-free recognition, no annotations provided by the inhabitants, are
necessary. The moments of start and end of the facts are detected though signature extractors. Si-
gnature extractors are also a way to translate a question from its natural language into an algorithm
that can be computerized by the system. We call signature to the output of the signature extractor.

Annotation-free recognition is applicable when an explanation can be given of how to reco-
gnize a fact from a signature, therefore an algorithm can be programmed to detect the beginning
and end of a particular fact. A fact that can be recognized using only sensors information contains
the next characteristics :
1. The set of sensors that are affected by the fact are identified, they reveal the effects of
the fact. Sensors detect and record a specific type of information. To be able to extract a
signature, the appliances used and the environment sensors to observe should be correctly
identified and installed, otherwise the recognition would turn incorrect or even impossible.
For instance the fact "watching tv" affects the sensor measuring the power consumption of
the TV. One cannot recognize the fact "watching tv" by observing the power consumption
of the oven or the temperature in the kitchen. The set of sensors that are affected by the

fact are selected during the configuration of an experiment. The correct sensors are selected
when programming the experiment. If sensors are missing or they are not selected for an
experiment, there is a risk of giving inaccurate results or the task might turn impossible. It
should be considered that different inhabitants have different options to carry out activities.
Therefore an analysis with pre-selected set of sensors might have incorrect conclusions.
2. The signature stands out accurately the main properties of a sensor measurement : patterns
characterizing facts can be easily identified in available measurements, such as the beginning
and the end of a fact and randomness of events can be handled or have a non significant effect
in the sensor measurements.
3. Requesting inhabitants to add a label is not necessary for the identification of the fact.
A list of facts and its possibility to be recognized automatically is presented next.

### 5.2 Examples of facts and their possibility to be detected using annotations-

free recognition

Fact/activity        Available sen-   Measure           Possible to re-    Difficulty
sor                                cognize activity
from sensors

Open/close           Contact sensor   Contact           Yes                No difficulty,
windows         or                                                         activity     ob-
doors                                                                      served     from
contact sensor

Cooking using        Energy meter     Power             Yes                No difficulty,
electric      ap-                     consump-                             activity obser-
pliances (stove,                      tion                                 ved from power
oven,      micro-                                                          consumption
wave, toaster,                                                             sensor
kettle...)

Cooking    not       Motion sensor,   Motion      and   No                 Not      possible
using electric       CO2sensor        CO2 could pro-                       to specify the
appliances                            vide presence                        activity     "co-
information                          oking"     using
only      motion
and co2 sensors

TABLE 5.1 – Examples of facts and their possibility to be detected using annotations-free recog-
nition

Fact/activity     Available sen-   Measure           Possible to re-    Difficulty
sor                                cognize activity
from sensors

Wash     dishes   Energy meter     Power             Yes                No          diffi-
using machine                      consump-                             culty, activity
tion                                 observed
from      energy
consumption
Clear On/Off
state in device

Wash    dishes    Motion sensor,   Motion      and   No                 Not possible to
without dish-     CO2 sensor       CO2 could pro-                       specify the ac-
washing   ma-                      vide presence                        tivity "washing
chine                              information                          dishes"    only
from     motion
and CO2 sen-
sors

Fridge usage      Energy meter,    Power             No                 Power
Motion sensor,   consump-                             consumption of
CO2 sensor       tion, Motion,                        the fridge can
CO2                                  be in cycles.
No associated
to a specific
activity.      A
contact sensor
could be added
in the door of
the fridge to
observe       the
moments        in
which the door
is open and the
amount of time
it stays open.

Eating            Motion sensor,   Motion      and   No                 Only presence
CO2 sensor       CO2 could pro-                       can be es-
vide presence                        timated       by
information                          motion       and
CO2 sensors.
Not possible to
specify the acti-
vity "eating"

TABLE 5.2 – Examples of facts and their possibility to be detected using annotations-free recog-
nition

Fact/activity     Available sen-   Measure           Possible to re-    Difficulty
sor                                cognize activity
from sensors

Guests            Motion sensor,   Motion      and   No                 Only presence
CO2 sensor       CO2                                  can be estima-
ted by motion
and CO2 level
sensors.    Not
possible      to
specify      the
activity "recei-
ving     guests"
or "number of
people present"

Entertainment :   Energy meter,    Power             Yes                No          diffi-
Watching          Motion sensor,   consump-                             culty, activity
TV/video          CO2 sensor       tion, Motion,                        observed
games/Music                        CO2                                  from      energy
player                                                                  consumption
Clear On/Off
state in de-
vice. Presence
known by mo-
tion and CO2
level sensors

Personal care     Energy meter,    Power             Yes                No          diffi-
using electric    Motion sensor,   consump-                             culty, activity
devices   (for    CO2 sensor       tion, Motion,                        observed
example hair-                      CO2                                  from      energy
dryer)                                                                  consumption.
Clear On/Off
state in de-
vices. Presence
known by mo-
tion and CO2
level sensors.

TABLE 5.3 – Examples of facts and their possibility to be detected using annotations-free recog-
nition

Fact/activity      Available sen-   Measure          Possible to re-    Difficulty
sor                               cognize activity
from sensors

Washing/ dryer     Energy meter     Power            Yes                No          diffi-
clothes machine                     consump-                            culty, activity
tion                                observed
from      energy
consumption
Clear On/Off
state in device

Working : Use      Energy meter,    Power            Yes                No          diffi-
of    computer,    Motion sensor,   consump-                            culty, activity
printer, scanner   CO2 sensor       tion, Motion,                       observed
CO2                                 from      energy
consumption
Clear On/Off
state in device.
Presence can
be     estimated
by motion and
CO2 level sen-
sors

One       energy   Energy meter     Power            No                 Activity      not
source     feeds                    consump-                            able to be de-
more than one                       tion                                fined directly
activity    (wa-                                                        form       energy
ter heater for                                                          consuming
shower, kitchen                                                         device. Power
and      washing                                                        desegrega-
machine)                                                                tion might be
necessary       if
activities    are
simultaneous
and use the
same sensors
to       measure
impacts.

TABLE 5.4 – Examples of facts and their possibility to be detected using annotations-free recog-
nition

### 5.3 Signature extractors classification

In an energy management system based on "experiments" and occupants questions, it will
be important that the questions of the inhabitants can be answered and that they can visualize the
information they are interested in. In certain cases, as explained in the previous section, annotations
are required but in other cases, the recognition of facts can be free from annotations.
To carry out an annotations-free recognition, it is proposed to use what we call signature
extractors, defined in section 5.1. Signature extractors can be fixed, parameterized or composed
(See examples in table 5.5) :

1. Fixed, There is no parameter to tune. Information such as dates and times allows the system
to automatically select relevant sensor data based on the hour of the day, day of the week,
holiday periods, or specific dates. No parameters need to be manually configured to obtain
meaningful data, as dates are interpreted directly. Information about, for instance, dates and
time that help the system to select sensors information in terms of hour of the day, a day of
the week, vacations period or a specific date. There are no parameters to set. Experts have all
the knowledge to program it. In this signature extractor a single flux of data measurements
is treated as input, and a categorical time series, result as the output.
Notice that during the programming of the experiment, when defining the listening period
during which the experiment will be carried out, occupants can specify the days and times
of the day that are of interest for the analysis. For example, one can select to observe the
times when a device is on or off, namely weekends between 9h and 12h. This feature ex-
tractor is implemented at the beginning of the experiment to define the listening period of
the experiment.
2. Parameterized, when some parameters must be used to compute the Signature. This allows
to adapt to the proper characteristics of the appliances. Therefore, this makes the system
more adaptable to different contexts. In this signature extractor, a single stream of data
measurements is treated as input, producing a categorical data stream as an output.
3. Composed, It is a combination of the previous two types of signature extractors. It takes
several data streams as input and produces a categorical data stream as output. For instance
"presence during the weekends" can be detected thanks to motion sensor data and dates.
A parameterized Signature extractor can be used with the motion sensor data. A threshold
is defined to set a value such a way that enough motion is detected to consider there is
presence. From this sensor data and the parameterized signature extractor, a data stream is
extracted. A fixed signature extractor can be applied to the motion sensor data to filter dates
and consider only the weekends. The 2 extracted signatures are combined creating a third
one that will provide a specific information to the inhabitants, about the presence during the
weekends.

Figure 5.1 – Signatures example.

So far, the signatures extractors (see Table 5.5) have been defined and tested with real data
from sensors installed in a dwelling.

Signature extractor   Fixed / Parameteri-        Characteristics that     Parameters
name                  zed                        they help detecting

On off                parametrized               Detects when an ap-      Minimum        power
pliance is ON/OFF        consumption thre-
shold and minimum
duration to consider
the appliance ON
(example : 50W,
10min). Minimum
duration under the
minimum        power
consumption thre-
shold to consider the
appliance OFF.

Open close            fixed                      Detects when an          No parameters
window or door is
open or closed

Levels                parametrized               It discretizes a si-     Thresholds defining
gnal in different le-    the levels are para-
vels where ampli-        metrized. The first
tudes are parameteri-    level corresponds to
zed                      0 by default.

Trend                 parametrized               This extractor cal-      Size of the time win-
culates the average      dow to be conside-
trend of a sensor’s      red before the cur-
measurements over        rent time t, size of
a time window and        the time window af-
discretizes the trend.   ter the current time t.

Day of the week       parametrized               Decomposes     the       0 represents Mon-
week in each of its      day and 6 represents
days                     Sunday

Hour in day           parametrized               Decomposes a day in      Defines the mo-
time slices              ments when the data
should be conside-
red (from 8 :00am
to 16 :00pm). Time
is represented as
(hh,mm)

French Holydays       fixed                      Represents    French     No parameters
vacations

TABLE 5.5 – Fixed and parameterized signature extractors, characteristics that they detect and
parameters to consider when applicable

#### 5.3.1 Predefined and customised signature extractors

It is proposed that the signature extractors can be predefined or selected by the occupants. Two
modes are proposed. Predefined and customised signature extractors.

#### 5.3.2 Predefined signature extractors

Predefined options of signature extractors are displayed as a list from which occupants can
select one that suits the answer to the experiment. See table 5.5 for more precision on fixed and
parameterized signature extractors characteristics. These predefined options include the combina-
tions of signature extractors that allow the display of the desired answer. They are listed below :
1. Moments when appliances are On or Off (based on the On/Off parameterized signature
extractor) : single flux of data measurements as input and binary output stream.
2. Open close : single stream of data measurements as input and binary output stream.
3. Levels : single stream of data measurements as input and non binary output stream.
4. Trends : single stream of data measurements as input and non binary output stream.
5. Presence (uses the level signature extracted). Considers the minimum number of movements
in a time slot by defining a threshold to consider presence (50% of the time in a 15-minute
time slot, movement was detected) : single stream of data measurements as input and binary
output stream.
6. Energy wasted (composed signature extractor of no presence but appliances On) : several
stream of data measurements as input and non binary output stream.
7. Active energy usage (composed signature extractor when presence is detected and appliances
are On) : several stream of data measurements as input and non binary output stream.
8. Effect of use of appliances on CO2, temperature and presence by observing trends : several
stream of data measurements as input and non binary output stream. Each of the next cases
can be analysed : Use of appliance and trend increasing, use of appliance and trend decrea-
sing, no use of appliance and trend increasing, no use of appliance and trend decreasing.
9. Effect of use of doors and windows on temperature and CO2 observing trends : several
stream of data measurements as input and non binary output stream. Each of the next cases
can be analysed :Door/window opening and trend increasing, door/window opening and
trend decreasing, door /window closing and trend increasing, door/window closing and trend
decreasing.
10. Effect of use of doors and windows on the energy consumption of heating and cooling sys-
tems : several stream of data measurements as input and time series non binary output. Each
of the next cases can be analysed : Door/window opening and trend increasing, door/window
opening and trend decreasing, door /window closing and trend increasing, door/window clo-
sing and trend decreasing.
11. Energy consumption of appliances : single stream of data measurements as input and non
binary output stream.
The function of the predefined signature extractors is to point out when a particular situation
happens (binary output). However could also be possible to display what the sensors measure when
the fact happens (Non binary output), whether in a same graphical representation or in separate
graphical representations. Examples are presented later in chapter B with the use of a heat map
proposal that can show both information in one same graph.
The Moments when there is an active energy usage signature results from the usage of combi-
ned signatures extractors. See Figure 5.2 The blue line represents the raw values of the TV power
consumption. The green line is the signature that extracts the number of motions in different le-
vels (from 0 to 4). The TV usage signature corresponds to the purple line (TV on or off), while a
Moments when there is an active energy usage is represented by the red line, which combines the
two interested Signatures extracted : presence and On/Off.
The list of signature extractors, here presented, can answer to some of the questions that occu-
pants may have : to spot moments in which there is presence, moments in which an appliance is in

Figure 5.2 – TV signatures.

use, moments of active or wasteful energy use, effects of the use of doors and windows and energy
consumption of appliances. However it can be difficult to know all the possible experiments that
inhabitants might program, this is related to the wide diversity of dwellings contexts that exist.
Therefore we propose that inhabitants can customize their own signature extractors as shown next.

#### 5.3.3 Customized signature extractors

Fixed and parameterized components are provided and the occupants might decide to which
sensor data to apply them. This tool can be useful if there is no predefined signature extractor
option to recognize a specific situation. The occupants can customize themselves the combinations
of signature extractors to have a response.
It is suggested the utilisation of pluggable software components to select the information that
is interesting for the inhabitants to visualize. A prototype has been developed to do some tests for
this initiative using a library called iPOPO (a service oriented component model in Python). In this
way it is possible to customize and make combinations of signature extractors. Notice that when
using the predefined options, previously explained, only one specific scenario can be detected,
for instance the inhabitant might choose to recognize the fact "working" by observing the option
"active energy usage", but the inhabitant also knows that when he/she is working the lamp of
the desk is On, then the inhabitants could create their own mode of recognition of an activity. In
this case, the computer should be on, the lamp should be on and there should be presence. By
customizing, the inhabitant is free to add features that could help to recognize the facts.
The iPOPO library has been used to create software components with rigorous life cycle and
dependencies management that can be interconnected by defining in each one what is the input
and the scope of the components. For inhabitants to be able to use this tool, it would be important
to design an interface in which inhabitants can interconnect the components in a more intuitive
way. iPOPO requires coding skills.
Five types of components are suggested to be able to customize the signature extractors.
1. Components related to sensor measurements : this components output the raw values of the
sensors.
2. Signature extractor components : each of the previously defined fixed and parameterized
signature extractors.
3. Conditional component : sets the required condition based on the question. Once the signa-
ture is extracted, one can be interested in specific information from each of the signatures.
The condition component will result in a boolean stream : true or false. We will be inter-
ested in the "true" values (1). Condition yes : extracts the moments in which, for instance,
after applying a "levels" signature extractor, the level exceeds the established threshold.
Condition no : extracts the moments when the level is below the established threshold. For
example : using condition-yes, one can define the moments in which there is enough mo-
vement to consider that there is a presence, using condition-no one can define the moments
in which there is so little movement to consider that there is no presence. Both cases could
be interesting for the analysis of an experiment. Take for example the predefined option
"Energy wasted" that extracts the moments in which there is no presence, but there is power
consumption. Until this moment each signature is still separated, but the condition com-
ponent defines the information that will be used for the integration of the signatures in the
next step.
4. Customize component generator : allows to integrate the extracted information from the si-
gnature extractors and/or condition components. In the instants that each of the condition
components result in "true", the information is combined and the output defines the begin-
ning and end of the interested fact.
For example, to actually show the moments in which it can be considered there is presence
and a device is On (when both conditions are satisfied, i.e. the fact occurs). The on-off signa-
ture extractor (device on) is combined with the Condition yes after extracting the presence
levels (presence yes). Notice that the On-off signature extractor already defines as "true"
when the device is considered on.
When customizing extractors, the objective is to point out when the fact happens (binary

output). Besides it could also be possible to visualize what the sensors measure when the
fact happens (Non binary output).
It is important to mention that recognition based on more than 1 scenario could be possible
by developing another component which could be customized. Meaning that for example
the activity "working" could be detected, if there is presence and the computer is On or
the lamp is On or ...or... However this option was no tested in this thesis. However it is a
possible option that could be explored.
In the example presented in Figure 5.3. The inhabitant is interested in the effects of a fact :
"the power consumption of the computer when there is no presence". The values of the
power consumption are also integrated in order to extract the power consumption in the
moments when the fact "no presence and computer On" takes place. This results in a non
binary output, by providing the information of the energy consumption as an output.
5. Graphical outputs component : allowed to plot the components in order to visualize the
outputs.
The following figures (see below Figure 5.3 and Figure 5.4) were generated using our proto-
type.
Let’s say an inhabitant is interested in customizing the signature extractors to know the power
consumed by his computer when there is no presence in order to estimate the energy waste. The
sensors selected are the motion on the desk and the power consumption of the computer. The
selected signature extractors are On Off and Levels. The On Off signature extractor is used to
detect the times when the computer is in use. The threshold considered was 10 W.
The level signature extractor finds the moments when there are low, medium and high levels
of presence, according to the following thresholds : 0.2, 0.6, 1 (percentage of movement detected
every 15 min). The Condition-no component is attached to the signature of levels. It is considered
that under medium level (level 2) of movement (less than 60 percent movement every 15 min),
there is no presence. Then in the customize component generator, it is set to show the energy
consumption records in the moments when there is no presence and the computer is On (see
Figure 5.3).

Figure 5.3 – component association

Finally, the graphs corresponding to the raw values of power consumption, On Off signature
extractor, level signature extractor and the resulting customize component the resulting custom
component are plotted, as shown in Figure 5.4 below. In addition, the visualization of the measu-
rements of each sensor can also be observed.
Note that the power consumption in the “custom” graph (the last graph from top to bottom) is
only shown when the "no presence" and "computer on" conditions are respected.

Figure 5.4 – Graphic representation of custom signature extractors. In the first graph from top
to bottom the raw power consumption values, then the On Off signature extractor, then the levels
extractor and finally the resulting customized component
.

### 5.4 Chapter conclusions

This chapter proposes possible methods to recognize facts inspired by (Schoofs et al., 2010)
who did studies in the combination of information from different sensors to detect the use of
certain appliances. In this way they create "signatures" that help to recognize more accurately the
use of appliances. We intended to use similar ideas but for the recognition of facts. In the beginning
of the chapter it is explained in which cases the annotation-free recognition could be used. First
of all if the inhabitants are interested in responding to questions that require further information
about a fact such as : why the fact was carried out, how it was carried out, who developed it or
what objects were involved, an annotation-free recognition is not possible. This information needs
to be provided by the inhabitant. The sensor can only provide information, for instance, power
measurements, CO2 concentration, number of movements detected, temperature measurements,
etc.
However defining when a specific fact happens, can actually be deduced from sensors data
after sense is given to the measurements using "signature extractors". These latter are algorithms
that filter sensor data to provide key information of possible facts. This means that explanation
can be given of how to recognize a fact, therefore an algorithm can be programmed to detect the
beginning and end of a particular fact. We also propose that a combination of signature extractors
can be used to better recognize specific scenarios such as what (Schoofs et al., 2010) proposed for
the recognition of the use of appliances.
Notice as well that the utilisation of certain appliances are associated to a specific fact, for
instance the use of the TV is associated to the fact "watching TV". Then, sense can be given to the
sensors measurements through the use of signature extractors algorithms to define when the fact
"watching TV" starts and ends.
In other cases, when appliances are not used, motion could be recognized, or CO2 measure-
ments could be registered, but this cannot provide key information of a specific fact. Multiple facts
could be possible, in a kitchen, for instance, the inhabitants could be washing the dishes, or chop-
ping some onions, or maybe cleaning. Extracting key information from this activities could be
more difficult to define through algorithms. In this cases, predefined labels or annotation methods
might be more suitable, just to define the fact that is being carried out.
A list of predefined options of single and combined signature extractors were presented. In-
habitants could choose from this list, one of the options. Notice that it was not explored in this
thesis if a selection of multiple options could be carried out for one same experiment. The use of
signature extractors limits, for now, the recognition of one scenario at a time. It could be interes-
ting in the future to evaluate the possibility of recognizing several different scenarios for one same
experiment. This means that one fact could be recognized from different scenarios and not just
one. Also the predefined options showed here is limited to examples that we could reflect on, so
far. In the future this list could be extended.
When the signature extractors require to be parameterized, for instance to define a threshold
from which power consumption could be considered. In our tests the parameters were defined
after observing the measurement curves. It could be interesting to formalize the parameters in
a more strict level for more general cases, if possible. Or for specific cases to be able to asses
inhabitants so that they can specify the parameters that better adapt to their context. In the case of
the signature extractor of parameterized levels, more detailed studies could be carried out on the
number of levels to consider, the different thresholds for different sensors measurements, etc.
Making more observations in different dwelling contexts and experiments with the proposed
sensors and other sensors, will help expanding the possibilities and define other limitations of the
proposed approach. New contexts, for instance that include an autonomous generation of energy
with the use of solar pannels and batteries, or contexts that include sensors to measure water
consumption could bring more ideas to explore experiments.
Given that the intention in the creation of experiments is that inhabitants are free to choose

questions and explore the impacts they are interested in, we propose also a method in which,
instead of using predefined options of signature extractors, they can create their own. This idea was
tested with the utilisation of plug gable software components in a prototype. However an intuitive
interface would be necessary to design so that inhabitants can customize their signature extractors
in an easy way, given that in the way it was tested, programming skills would be required. Also in
the example provided only one scenario could be recognized, however it would be interesting to
reflect how one single fact could be recognized from different scenarios. For instance, one could
think of recognizing the "working" fact, from the use of the computer and presence in the desk,
but what if we could recognize the fact also from other scenarios, for instance, the use of a lamp in
the desk when there is presence or from the sound of phone ringing and when there is presence or
... etc. Be aware that we would be already using a combination of sensors to define each scenario,
the next step could be then to use different scenarios to define one same fact. In this way, the
inhabitants can choose if they are interested in studying a fact from one single scenario or multiple
scenarios. It will depend on the question they are interested in exploring.
In the next chapter the annotations-based recognition approach is developed. This approach
is applicable in the cases in which more information than sensors data is required. Therefore the
participation of the inhabitants is necessary to provide information that they know.

## Figures extracted from the source PDF

![[_assets/initial-thesis/05-annotation-free-facts-recognition/page-096-image-069.png]]
![[_assets/initial-thesis/05-annotation-free-facts-recognition/page-099-image-071.png]]
![[_assets/initial-thesis/05-annotation-free-facts-recognition/page-101-image-073.png]]
![[_assets/initial-thesis/05-annotation-free-facts-recognition/page-102-image-075.png]]
