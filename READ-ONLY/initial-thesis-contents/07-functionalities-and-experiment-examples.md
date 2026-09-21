---
title: "Functionalities to provide answers and experiments examples"
source: [[READ-ONLY/initial-thesis.pdf]]
status: foundational-reference
---

# Functionalities to provide answers and experiments examples

[[Initial thesis index|Index]] · [[06-annotation-based-facts-recognition|← Previous chapter]] · [[08-evaluating-fact-characterization|Next chapter →]]

> [!note] Foundational source
> This is a Markdown transcription of the initial thesis. It is retained as a starting point for later research development, not as a final source.

Functionalities to provide answers and experiments
examples

This chapter explores the concluding phase of an experiment, focu-
sing on features that let inhabitants select the most relevant informa-
tion and graphical representations for them. Unlike current systems,
which often display multiple metrics simultaneously, this approach
allows users to choose the data and visualizations most suited to
their needs. The concept of a "merger" is introduced, functioning as a
tool to process data after the observation phase, enabling users to ex-
tract specific insights. Then drawing inspiration from studies, which
developed tools for user-defined visualizations, this thesis advocates
for a flexible approach that empowers inhabitants to customize vi-
sual outputs for better clarity and alignment with their experimental
goals. Finally examples of experiments are presented, with a simple
representation of each of the parts of the experiment.

### 7.1 Merger

Now, we’re going to look at elements that can be used to provide the results of the experiment
to the inhabitants in a numerical or graphical format. Let’s consider, for instance, that inhabi-
tants are interested in knowing the average energy consumption of the appliances selected in an
experiment (a numerical answer). Or maybe, they are interested in displaying a graphical repre-
sentation related to their question. It is proposed to present to the inhabitants some predefined
options of answers to possible questions of the inhabitants in graphical representations and/or in a
numerical format.
In order to provide answers in a specific way, we present the tool called merger. This is a
function carried out at the end of the listening period of the experiment. The function takes one
or several data flux or times-series as inputs, leading to one or several values or one or several
sequences of timed values, as output.
In other energy management systems this features are implicitly involved in the visualization
of information. For instance in WISER ENERGY from Schneider electric (SchneiderElectric,
2021), the users can receive information such as :
— Time that appliances have been On.
— Total power consumption.
— The equivalent of the power consumption in C/h.
— Visual comparison of the energy consumption of different appliances.
— Energy consumption per day, per week, per month, per year.
— They mention that in the case of having solar panels installed they can get information about
the return on the investment based on the energy production data.
— Percentage of time that the appliance is On (per month) and comparison with other ap-
pliances.
— Estimated cost of energy in the year from the usage of an appliance.
— Solar energy consumed for a specific equipment.

Figure 7.1 – Interface proposed by WISER ENERGY from Schneider electric (SchneiderElectric,
2021). Some of the explained features are marked in orange

Figure 7.2 – Interface proposed by WISER ENERGY from Schneider electric (SchneiderElectric,
2021). Some of the explained features are marked in orange

Figure 7.3 – Interface proposed by WISER ENERGY from Schneider electric (SchneiderElectric,
2021). Some of the explained features are marked in orange

Other apps such as Smart Things from SAMSUNG (Samsung, nd) provide information such
as :
— Energy usage from specific devices in kWh and its equivalence in USD.
— Total energy consumption.
— Calculator of possible energy savings and savings rate for a set of appliances defined by the
inhabitants.
— Prediction of future energy usage from a set of devices selected by the inhabitants.
— Equivalence of carbon emissions (kg), when consuming energy, and carbon emission reduc-
tions (kg), in the case of energy savings.
Also, for example Home App from Apple (Apple, 2023), proposes a service to get a summary
of activity history detected from the openings and closing of doors.
However what if instead that the app provides many different ways of presenting information,
inhabitants could choose what they want to see as answer specifically that could be related with
their experiment question. This could be better adapted to the system here proposed.
A predefined list of merger options could be provided for the inhabitants to choose from.
Not all the experiments require this function. The inhabitants could choose to observe the data
recovered, directly using the graphical representations. The next list is proposed as some possible
examples to include (a wider version could be explored in the future) :

1. Addition of the sensor’s measurements during the listening period (one or several time series
input to obtain the addition as 1 value). For instance : Adding the power consumption of all
the appliances selected in the experiment.
2. Average of the sensor’s measurements during the experiment’s listening period (one or se-
veral time series input to obtain the average as 1 value). For instance : obtaining the average
value of the power consumption of all the appliances selected in the experiment. Or obtai-
ning the average value of the CO2 in the room.

3. Average of the sensor’s measurements per day, per week or per month respecting the limits
of the experiment’s listening period (several time series input to obtain the average as a
sequence of timed values). For instance : obtaining the average power consumption per
week of all the appliances selected in the experiment. Or obtaining the average temperature
per week.
4. Count (number of times that a fact was recognized) per day, per week, per month respecting
the limits of the listening period (several input time series to obtain the count as a sequence
of timed values) For instance : in an experiment with a listening time of 1 month. A time
series of values is recovered from each week, and the output is the resulting count of the
times that the fact was recognized for each week : 3 times in week 1, 6 times in week 2, 4
times in week 3 and 5 times in week 4.
5. Equivalent in currency (C) according to electricity price (one or several time series input to
obtain a sequence of timed values). For instance : adding the power consumption of all the
appliances selected in the experiment and transform the power units into price of the energy
consumed.
6. Equivalent in carbon emissions (kg) according to electricity consumption (one or several
time series input to obtain a sequence of timed values). For instance : adding the power
consumption of all the appliances selected in the experiment and transform the power units
into carbon emissions (kg).
Receiving the information in too many formats all at once, could overwhelm inhabitants, lea-
ding to confusion and reduced effectiveness in understanding the data. However if inhabitants are
more specific in the information they want to see, they could loose the opportunity to get the in-
formation in other formats, they might not have thought as useful. Short explanations could be
provided for each of the options to help the inhabitants choosing.
It could be possible to allow inhabitants choosing multiple options that are interesting for them
rather than limiting to one single selection per experiment. Maybe also the deselection of options
could be envisaged if inhabitants change their mind on their decision. The objective is that the
information can be the most clear possible for the inhabitants.
In this thesis a limited list of mergers is presented. This list could be better defined if the
system is installed in different dwellings and the options can be improved.

### 7.2 Graphical representations

(Wambecke et al., 2023) proposed a tool that creates graphical visualizations with an explora-
tory approach. They found in previous similar studies that people are able to express their needs
of visualizations. They provided a list of possible visualisations to choose from. They associate
what they call "Insights" to visualization types. The insights show a main feature representative of
multiple visualization types. Insights are a tool for the people to define their needs of visualization,
then specific options can be selected. (See Figure 7.4)
In this thesis, we can use this study and some of the examples provided to show possible
graphic representations that the inhabitants could use for a better comprehension of the results
obtained (see Figure 7.4). As found in the research of (Wambecke et al., 2023), users have different
needs and different skills to comprehend a diversity of visualizations, some of them might fit better
to the interest and understanding of the inhabitants.
Nex are presented the insights that were considered interesting in the development of experi-
ments :
1. Comparison : compares between data.

2. Discrete : provides a discretisation of data.
3. Distribution : breaks down data according to one or several variables.
4. Extremum : provides information of maximum and minimum values.
5. Hierarchy : ranking of data in different levels (Sunburst diagram not explored).
6. Over time : data evolution over time (spiral plot not explored).
7. Pattern : repetition of structures in data (stream graph not explored).
8. Proportion : comparison of data in the form of areas.
9. Range : interval of data.
10. Variation : variation of one single variable, not specifically temporal.
Others such as Flow (data stream), location (geographical position), part of a whole (inclusion
of data in a set) and data relationship, were considered less applicable to the concept of experi-
ments in the context of energy impacts exploration.
This section might require more study and the expertise of techniques of Human-Computer
Interaction should be further implemented for this aspect in the future.

Figure 7.4 – Set of insights associated to types of visualizations to choose from (Wambecke et al.,
2023)

mergers and graphical representations

### 7.3 Experiments examples from the definition of the experiment ques-

tion to the selection of mergers and graphical representations
Now that all the concepts of experiments have been defined, examples of experiments are
presented, in this section, with the objective to show briefly in a simple representation all the parts
involved in an experiment :
— Question of experiment to identify the life event to study.
— Choice of recognition method : annotations-free (predefined or customized)/ annotations-
based.
— Sensors selection
— Definition of the listening time of the experiment.
— Semantic annotations for the annotations-based recognition method (if applicable).
— Example of choice of a possible merger adapted to the question.
— Example of choice of possible graphical representation adapted to the question.
A possible representation of interface is also showed in the Annex B. The reader could also
give a look to this proposal if interested in have a more visual representation of a possible process
of self-experiments.
In Figure (3.4), numerous examples of questions were presented. Let’s choose some of them
and explain how it would work using the experiments system. Some cases such as energy commu-
nities** and demand response grid management*** might were not included in this thesis. Those
examples might require tests in multiple households to install the system, which was not carried
out in this thesis. .
**An energy community is a group of people, usually neighbors or residents in the same area,
who come together to produce, share, or manage energy. For example, they might install solar
panels on their roofs and share the energy they generate, making it more sustainable and cost-
effective.
*** Sometimes, grid managers encourage users to shift their energy use to less busy times. For
example, running your washing machine at night instead of during peak hours can help balance
the grid. This approach is known as demand response.
1. Experiment related to activities :
What happens when I sleep regarding the energy consumption of the heater if I variate the
temperature differently every night to observe the impacts that different temperatures might
have ?

Facts recognition method : Annotations-based
Signature extractors from list : No
Signature extractors to customize : No
Related sensors : power consumption from (radiator)
Period of time of experiment listening : start date : 02/05/24 end date : 20/05/24 form 21h
to 06h.
Annotations. Possible annotations :
-Why : sleep (optional not compulsory)
-Who : - (optional not compulsory)
-What : - (optional not compulsory)
-Where : bedroom (optional not compulsory)
-How :19C or 21C or 23C (important related to the question)
-When : While the experiment is listening and the moments annotated, as well as the mo-
ments defined by the interactive and cooperative learning classification

-Performance : - (not required) Merger : sum (energy)
Graphical representation : Pattern-heatmap

What happens when I sleep regarding the energy consumption (fixed heater temperature-No
need to specify annotations) ?

Facts recognition method : Annotation-free
Signature extractors from list : On off signature extractor
Signature extractors to customize : No
Related sensors : power consumption from (radiator)
Period of time of the experiment listening : start date : 02/05/24 end date : 20/05/24 from
21h to 06h.
Possible annotations : None
-Why : -
-Who : -
-What : -
-Where : -
-How : -
-When : -
-Performance : - (not required)
Merger : sum (energy)
Graphical representation : Overtime- line chart

2. Experiment related to special event :
What happens regarding energy consumption and air quality during Christmas celebration ?
Facts recognition method : Annotation-based
Signature extractors from list : No
Signature extractors to customize : No
Related sensors : oven, microwave, coffee maker, hotplate, fridge, heating system, CO2 li-
ving room, CO2 kitchen, multimedia.
Period of time of experiment listening : start date : 23/12/24 end date : 27/12/24 form 0h to
23h.
Annotations : Possible annotations :
-Why : christmas (important related to the question)
-Who : 20 people (important related to the question)
-What : - (optional, not compulsory)
-Where : living room and kitchen (optional, not compulsory)
-How : oven 200°C (optional, not compulsory)
-When : While the experiment is listening : moment of the annotation, moments defined by
the interactive and cooperative learning classification
-Performance : - (not required)
Merger :
Graphical representation : Overtime- line chart

3. Experiment related to analysis :
What are the most energy consuming appliances ?
Facts recognition method : Annotation-free
Signature extractors from list : Energy consumption of appliances.
Signature extractors to customize : No
Related sensors : washing machine, dish washer, oven, fridge,
Period of time of the experiment listening : start date : 02/05/24 end date : 20/05/24 from 0h

mergers and graphical representations

to 23h.
Possible annotations : None
Why : -
Who : -
What : -
Where : -
How : -
When :
Performance : -
Merger : average for each selected sensor (energy)
Graphical representation : Distribution- pie chart

4. Experiment related to building configuration :
What happens when I leave the heater of the living room on in a high set point, on a low set
point, or off during the day when I am not at home ? (With this experiment, the inhabitant
intends to define if it is worth it in terms of comfort/energy consumption to leave the heater
on during the day to keep a constant temperature in the room, even if nobody is at home.)
Facts recognition method : Annotation-based
Signature extractors from list : No
Signature extractors to customize : No
Related sensors : power consumption from heating system, temperature of living room, ex-
ternal temperature.
Period of time of experiment listening : start date : 20/11/24 end date : 20/12/24 form 8h to
18h, week-days only.

Annotations : Possible annotations :
Why : warm up room (optional, not compulsory)
Who : 2 people (optional, not compulsory)
What : - (optional, not compulsory)
Where : living room (optional, not compulsory)
How : 20C, 15C, Off (important related to the question)
When : While the experiment is listening : moment of the annotation, moments defined by
the interactive and cooperative learning classification
Performance : - (not required)
Merger :
Graphical representation : Pattern-heatmap

5. Experiment related to appliances impacts :
How many times I use the kettle per week ?
Facts recognition method : Annotation-free
Signature extractors from list : Moments when appliances are On or Off (based on the
On/Off signature extractor)
Signature extractors to customize : No
Related sensors : kettle, motion in kitchen
Period of time of the experiment listening : start date : 07/06/24 end date : 23/09/24 from 0h
to 23h.
Possible annotations : None
Why : -
Who : -
What : -
Where : -

How : -
When :
Performance : -
Merger : count
Graphical representation : Discrete-histogram

Note : The period of time of experiment listening is configured by the inhabitant, in the
beginning of the experiment, for all the cases.
For this last example, let’s see the representation of the signature extractors and the graphical
representation to answer the question.

Figure 7.5 – Image to exemplify the signature extractors applied to the example of usage of the
kettle

Figure 7.6 – Image to exemplify the graphical representation of the number of times a kettle is
used per week

### 7.4 Chapter conclusions

In this chapter were presented, the features of the last part of an experiment. These, allow
the inhabitants to select the information they wish to receive and the graphical representation that
better adapts to the experiment.
It was observed that in nowadays systems, different forms of presenting the information are
provided to the inhabitants all at once. One can get the results of total energy consumption, the
average energy consumption per week, per, month, per year and its equivalence in price and CO2
impacts, as well as the prediction of future energy usage of one same appliance, etc. But maybe
inhabitants are interested in observing 1 or 2 of these metrics, while the rest could just not be in-
teresting or maybe even confusing. We propose that instead of pre-programming the visualization

of many different forms of results, the inhabitants can choose from a list, the ones that are more
interesting for their experiment.
Then we introduce in this section the concept of merger, which is a function that treats the
information after the listening period of the experiment, i.e. by this time, the recognition of facts
is finished. This last treatment, could allow the inhabitants to choose from a list of merger options
and receive an specific information, such as the average power consumption of the facts detected
during the experiment.
Later studies were from (Wambecke et al., 2023) who proposed a tool that creates graphical
visualizations with an exploratory approach. They found that people are able to express their needs
of visualizations. They developed a tool for people to define their visualization of preference from
a list of options they call Insights. In this thesis this approach could be interesting so that inhabi-
tants can also be free to choose the visualization that is more clear for them and adapted to their
experiment needs.
Both initiatives would require to provide some key information to the inhabitants from the dif-
ferent options proposed, to help the inhabitants choosing. It would also be interesting that multiple
selection is possible, if the inhabitants wish so. The options presented in this part, should still be
tested as well as the process of selection from the inhabitants. While the results could be more
clear, the process of selection of the information to visualize and the format of visualization could
require the investment of inhabitants time.
In the last part of the chapter, some examples of experiments are presented to help visualizing
how different experiments could be carried out from the definition of the experiment question to
the selection of mergers and graphical representations. Although we can see that the development
of experiments can be possible with the presented approach, the functional automatized system
would allow to know how interesting, useful and accurate, the proposition is. Also it could be
better evaluated the involvement of the inhabitants and the easiness of use of the system. However,
for now, this thesis is limited to a proposal of different features that a self-experimenting system
could include in an energy management context.
In the next chapter study case experiments are developed and real annotation process for each
of the experiments is analyzed.

## Figures extracted from the source PDF

![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-133-image-105.png]]
![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-134-image-107.png]]
![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-135-image-109.png]]
![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-138-image-111.png]]
![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-142-image-113.png]]
![[_assets/initial-thesis/07-functionalities-and-experiment-examples/page-142-image-115.png]]
