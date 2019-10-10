# labpistec-ideas
Ideas, meetings, discussions and experiments between GEOTEC and LABPSITEC research groups

## Motivation
We (GEOTEC) want to start a prolonged colaboration with the LABPSITEC group to reach a win-win situation. On one hand, we seek our geospatial developments and toods make a real, social impact in the sense they might be used in real experiments, on the streets. On the other, LABPSITEC group can benefit from ready-to-use geospatial technology and tools for technology-driven interventions and experiments with cohorts of patients and hence considerably shorthenen times for data collection, analysis and decision making.

## Minutes

* [Meeting 2017-06-27](#meeting-2017-06-27)
* [Meeting 2017-09-18](#meeting-2017-09-18)
* [Experiment 2017-09-25](#experiment-2017-09-25)
* [Meeting 2017-10-16](#meeting-2017-10-16)
* [Meeting 2017-10-26](#meeting-2017-10-26)
* [Meeting 2017-11-16](#meeting-2017-11-16)
* [Meeting 2017-12-12](#meeting-2017-12-12)
* [Experiment 2018-01-08](#experiment-2018-01-08)
* [Meeting 2018-01-11](#meeting-2018-01-11)
* [Focus group 2018-01-22](#focus-group-2018-01-22)
* [Meeting 2018-03-02](#meeting-2018-03-02)
* [Meeting 2018-05-09](#meeting-2018-05-09)
* [Meeting 2018-07-03](#meeting-2018-07-03)
* [Meeting 2018-12-14](#meeting-2018-12-14)
* [Meeting 2019-10-04](#meeting-2019-10-04)
* [Meeting 2018-10-10](#meeting-2019-10-10)
* [Meeting 2018-10-17](#meeting-2019-10-17)



### Meeting 2017-06-27
Participants. LABPSITEC (Juani, Diana, Azu), GEOTEC (Nacho, Luis, Carlos, Sven)

Clinical studies:
* game to help patient with panic attacks / agoraphobia
* depression: start observing person, add psychological treatment, measure effect, add small serious game, measure effect
* scientific validation of app by therapists + 3 or 4 patients

Depression: how many times do a patient exit from their house, how far, how much time?
1. first track patients (8 - 14 days)
2. psychologists start treatment. App tracks: has he done something different? (does he go to new points? new paths? something outside his habits?)
3. give certain points (locations) to the user to go; does he arrive there? trajectory to go?
4. get feedback from the user (questionnaire, included in the app?)

Possible success factors:
* does the therapy work?
* does it work in a shorter time? (use of the app should shorten treatment time)

A list of potential experiments, from simpler to more complex and shophisticated, along with questions to answer [was discussed](/meeting20170627/experiments-list.pdf). It is decided to develop an app to monitor user's position and create the correspondig metric in the analytical platform to calculate: how many times do a user go out home?, and how long? Development will cover July, August and early September, in order to conduct a first experiment with Labpistec staff by late September 2017. 

### Meeting 2017-09-18
Participants. LABPSITEC (Juani, Diana), GEOTEC (Nacho, Luis, Carlos, Sven)

Released features of the first developmen are summarised as follows:

1. Definition of the application and the metrics in the server to configure the variables needed for the experiment. 

2. Creation fo a mobile app, composed of:
    * Initial configuration tool, where the user (or perhaps the therapist in this case) indicates the user ID (with double confirmation), the point where the user's house is located, the radius that is defined as "area of the house" (the area from which it leaves or enters) and the date from which measures should begin to be taken.
    * Background service (which does not require interaction with the user) for monitoring regularly data and storing it.

3. A visualization tool so you can access the data. At the moment this tool will offer the best possible variables requested for the experiment with filters capabilities (by user, by date ...).

### Experiment 2017-09-25
Participants: LABPSITEC (Juani, Diana, Azu)

First experiment run from 25 to 28 of September 2017. Juani/Diana provided 3-day data, Azu 1.5-day data, usign the [app](https://play.google.com/apps/testing/com.geotec.metrics.labpsitec_metrics_project). Output data resulting from the metric computation will be provided as part of a R package `labpsitecData` (to be released soon: @CARLOS)

### Meeting 2017-10-16
Participants: LABPSITEC (Juani, Diana), GEOTEC (Nacho, Luis, Ditsuhi, Carlos, Sven)

Presentation of two TFM projects, which may be potential candidate to use the app for data collection and the analytical platform for metric computation. Further details of TFMs [here](meeting20171016). Discussion of TFM's requirements and needs. Next, we discussed how the Ditshuhi's viz tool might be evaluated. One alternative was to use it to analyse patients' data. Another was to use it to analyse researcher's decision making process, i.e., how does the visualised data inform on the treatment (designed by the researcher)? 


### Meeting 2017-10-26
Participants. LABPSITEC (Juani, Diana), GEOTEC (Nacho, Luis, Ditsuhi, Carlos, Sven)

Presentation of results of first experiment (meeting 2017-09-18), discussion to enhace the accuracy of in/out home. Further details in [Diana's minutes](/meeting20171026/20171026minutas.pdf). In short, main limitations are:
* hard to determine IN/OUT home based only on GPS data. Signal error and low accuracy make us think about additional methods to GPS readings to respond satisfactorialy to this simple question: Is a patient IN/OUT home?
* app notifications should be drastically reduced. Provied positive message that recognises user participation.
* Augment period amid consequetive observations to avoid excessive battery drain.
* Next release of app should address the points for next experiments with real patients in the context of the two TFM projects presented durinf the last meeting. It was discussed different data collection strategies (time-based, place-based, beacon-based, etc.) since distinct psychological problems drive the ways to collect data and the ways to best visualise it

### Meeting 2017-11-16
Participants. LABPSITEC (...), GEOTEC (...)


### Meeting 2017-12-12
Participants. LABPSITEC (Juani), GEOTEC (Nacho, Luis, Ditsuhi, Carlos, Sven)

Improvements of visualisation tool developed by Ditsuhi:
* a more advanced tool is available
* demonstration was given
TO DO:
* deploy the tool publicly, so everybody can access it (GEOTEC) - Update: Viz tool is [online](https://labpsitec-4097d.firebaseapp.com/auth/login) 
* updates to the tool (GEOTEC)
* check the tools, specifically usability, type of data & graphs used (LABPSITEC)
* tell us improvements (suggest additional data visualisations; change of graph type; other grouping of data; etc.)  (LABPSITEC)

Data collection app: A more advanced version is [available](https://play.google.com/apps/testing/com.geotec.metrics.labpsitec_metrics_project), with the following new features:
* user message are generic
* data is collected every 5 minutes
* wifi footprints are now collected and compared to double-check whether a user is at home. We learned that the scanning of wifis is required, the initial configuration requires that in addition to entering the data that we put previously, such as the user, the location, days, etc., it is necessary that the user or patient, once he arrives at his house, opens the application and indicates it ("I'm home!). This serves us to pick up the "footprints" of the wifis that a patient can "see" in his home. From that moment, when the data is sent, the application checks if the GPS measure indicates that it is close to home (we have established 30 m radius) and in that case "reads" the wifis to confirm (or to what degree ) the user is at home. If the GPS indicates that we are far enough from home that reading is not made, and also the battery drain is not excessive to perform that check. Just highlight that this is a strategy to confirm that we do not have "false positives away from home" and that it can help us but we do not yet know the effectiveness.
* Colleted data can be exported in case connection is down. The internal database is automatically exported at the end of the experiment, that would help us in case of having problems with the servers (statistically probable), to be able to recover the data of the patients. To perform this export there are two ways: a manual way, that is, the therapist enters the app and in "Settings", click "Export", and also at the end of the experiment (based on the entered dates of experiment duration), the application will should do automatically. It is advisable to do it manually before uninstalling it for more security.
* start date of experiment can be configured (before the experiment started inmediatedly) 

TO DO:
* solve remaining issues/bugs (GEOTEC)
* use the application and report issues/bugs (LABPSITEC)
* look at the interaction flow at setup (therapist enters data; user captures home location) & provide feedback (LABPSITEC)


Experiment:
* Ditsihu needs to submit her master thesis 1 February & needs some type of validation
* different possibilities for experiments (validation) were discussed: 
  * therapist use the tool and perform a questionnaire aimed at showing improved ability to understand data, improved time of interpreting the data, better insight in data, ability to better tailor therapy, etc. (LABPSITEC input appreciated)
  * use of the tool with real patients, if possible. (Different options: 1 group of patients, all using both the tool and previous paper-based approach; 2 groups of patients, 1 new tool & 1 paper based). Similar analysis can be done as in previous point (questionnaire), but additional analyses are possible (e.g., compare paper-based collection with tool-based collection) (LABPSITEC input appreciated)
* exact experiment (to serve as validation for thesis Ditsuhi) not decided (LABPSITEC input appreciated)
* later (after 20 January), additional experiments are possible

TO DO:
* define a realistic (regarding time) experiment that can be performed (finished) by January 20. (LABPSITEC & GEOTEC)

### Experiment 2018-01-08

On Jan 8th, the last release of the app is being tested by a total of 8 therapists during one week (8-15 Jan). They will be using the tool and giving feedback regarding the app functioning and the collected data from the therapy's point of view (a final questionnaire will be defined to get structured feedback). This represents the fist, serious validation study of the tool (data collection app) 

### Meeting 2018-01-11
Participants. LABPSITEC (Diana, Juani), GEOTEC (Nacho, Ditsuhi, Carlos, Sven)

Two objectives: pne shorter (Ditsuhi; evaluation of visualisation of results; thesis submission date 01/02/2018) and one longer term (Luis & Nacho; evaluation of the whole system via the ongoing experiment).

As regards the revision of Ditsihu's visualisation tool, it is proposed:
* Therapist/participants (N=9 + Diana and Juani) use/test the tool + sign informed consent.
* Each one fills in usability questionnaire (prior to open discussion to avoid biased response)
* a (recorded) focus group to run an open discussion to evaluate pros and cons (e.g. compared to the traditional way of working) in a more qualitative manner.
* Each one fills in tnhe second questionaire on th eeffectiveness of the tool (in terms of clinical use)

The resutls of the evaluation are 1/ a set of questionnaires and 2/ notes/summary/transcriptions of the open discussion (once we watch again footage)?  

Date (focus group): 18 Jan?

### Focus group 2018-01-22
Participants. LABPSITEC (8 participants + Diana as master of ceremony), GEOTEC (Nacho, Ditsuhi, Sven as observers)

The focus group was aimed to collect qualitative information from participants' experience (N=8) of using Ditsuhi's data visualisation web app. The application shows input and processed data by mans of a set of map-based and chart-based visualisations. Discussion was centred on whether or not the applicaiton might be useful in the context of clinical psychology, as for example:
* Depression: how many times has a patient left home? How long has he spent away from home? What if he has not left home in all week?
* Agoraphobia: How close have you been to the mall (i.e crowded places) where the patient should be exposed? Or how much has he managed to get away from his area of security/comfort?
* Pathological game: Have the patient approached a play area? How long has he been there? How many times has he visited that place?

### Meeting 2018-03-02
Participants. LABPSITEC (Juani, Laura, Adriana, Diana), GEOTEC (Nacho, Sven, Carlos)

The meeting was aimed to decide on the scope, search terms and search strategy of the review. Keywords per discipline were defined. Main data sources were also identified: WoS, Scopus, and Medline. Specialised databases might be used too, especially [psynet](http://psycnet.apa.org/search/basic). 

### Meeting 2018-05-09
Participants. GEOTEC members only

Notes on the geobreakfast meeting where Menhdi presented his work on the trajectory package. This package contains classes and methods for spatio-temporal analysis of trajectories. This package might be used for comparing patients' trajectories in the health use case. Hoewver, time dimension seems to be an impediment for the health use case because time (up to now) is not relevant. In addition, interactions between trajectories (i.e patients) are independent, we do not intent to study behaviour/interactions between patients across time because each patient's trajectory is studied in isolation. 

### Meeting 2018-07-03
Participants. LABPSITEC (Juani, Laura, Diana), GEOTEC (Nacho, Sven, Carlos)

The meeting was aimed to discuss the categories and dimensions to extract key bits of useful information from the set of eligible papers. It was also discussed the required steps of the second stage of the reviewing process. A plan for next activities was agreed to make progress in the refinement of the dimensions/categories adn the preliminary assessment of 10% of the eligible papers.


### Meeting 2018-12-14
Participants. LABPSITEC (Diana), GEOTEC (Nacho, Alberto, Carlos)

Since [Symptoms](http://geotec.uji.es/projects/symptoms/) tool requires users’ long-term engagement to yield meaningful analysis, we  think that one of the best ways to engage users is to make the tool intuitive and comfortable for use. Thus we step back and realise that the project has to take into account design research:

### Meeting 2019-10-04
Participants. LABPSITEC (Diana), GEOTEC (Sven, Alberto, Nacho, Carlos)

That was a long meeting to primary discuss usability aspects of a new user interface (mock-up) of the Symptoms platform. This is a summary of the proposed changes: 
* Table of patients
  * each column must have the ability to be ordered
  * hide inactive patients, add a new filter in the top of the table (active/inactive patients)
  * End date of the treatment. A therapists can leave it open, or set a date which can be modified later if required
  * Add total number of days to the column "# days treatment in use" like this: "4/15" means fourth day out of 15
  * Delete "New patient" button
  * Reorder columns by priority: ID, alerts, watch treatment, Protocol, # days in use, Installation date, "..."
  * "Watch treatment" is a new column with the graph icon in it
  * Move "edit" icon to the view of "comments" when it's clicked on the "plus" icon
  * Put "ON/OFF" (active/inactive patient) as part of the actions of "..."
* Left panel
  * "Plantillas" -> "Protocolo"
  * "Ver plantillas" -> "Ver protocolos"
  * "Nueva plantilla" remains the same but hideen for basic users. So, two user profiles: therapist, coordinator
  
During the second part of the meeting, we focused on the "plantillas" (protocols). The basic idea is to provide a predefined set of analytical tools / units to therapists associated with a particular disorder. Then, there will be a "plantilla" of depression, phobias, etc. We begin to discuss the case of depression. For example, there are two key places: "home" and "work" that influence on the computation of the real-time outside home (and work). So, time away from home = total time away - time at work. Then, it was commented having several days at the beginning of a treatment as a calibration phase ("baseline") to determine the patient's behavior. At some point, the treatment is really activated by introducing more interaction, evaluation and intervention. In summary, a treatment for depression includes a part of evaluation (data collection) + intervention (interaction). During the intervention, when things are going well, the patient receives a form of content or another form of content when things are not so well as expected.
  
We continued the discussion with a well-known technique related to the phobias to certain places ("plantilla fobias"). It is called "exposure" and basically means forcing a patient to visit a place that produces a high level of fear, for example. It is expected that continuous expositions accompanied with in situ interventions can change the patient’s behaviour and lead to a drastic reduction of “fear” while being exposed in that place.In addition, all relevant places are not equally important during treatment; There is a hierarchy of places that organizes them from easy to difficult places to face (like the stages of a game). SO, the follosign analytica units are importante:
* selection of relevant places
* rank places. A patient starts the treatment with "easy" places, and as she advances, she's confronted with "difficult" ones. 
* define (clinical) decision tree during the event of exposure in a place (the decision tree can be the same for all places, what changes is the psyco-educational content to deliver). In other works, the tree is the sequence of interventions while the patient is in the place.

**Action**: Diana to create a detailed (clinical) decision tree of the event of exposure in the treatment of phobias

*My thoughts (carlos): That “exposure” pattern may fit pretty well with graph models. During an event of exposure, a patient is in a place and she’s asked about the level of fear on a regular basis or just after an intervention (psyco-education content, encouraging messages, etc.) is delivered to the patient. So, assuming an event of exposure takes a short period of time (e.g 30 min), a patient is asked the same question various times (level of “fear”), and each question-answer does generate a new relationship between the patient node and the place node with the level of emotion recorded.*

In summary, many questions arise such as how to model the decision tree of an event of exposure? how to store all the steps and interactions that happedn during the event? how to visualise it to patiene in a didactic manner?

(Below Carlos' topic while in UNB)

Finally, a brief discussion on how to measure the emotional perception of a patient in relation to a place. To start off, I (carlos) put psychologists in context by explaining the “social” approach developed during my stay in UNB to better understand emotions related to places. At UNB, we acknowledged that measuring emotions is something subjective and complex. And no taxonomy was available. For this reason, we looked at social theories (Sense making theory) to create questionnaires aligned with these theories to take into account and collect the complexity of emotional perceptions. Their response was clear: 

On one hand, lots of literature works use devices/sensors to monitor physiological characteristics/measurements (e.g. heart beats, etc.). In their view, these works attempt to objectively measure/identify emotions, but this is still not viable in clinical practice. Certain (co)relations may be computed but the level of confidence is still pretty low to be used in real treatments. On the other hand, social psychology theories (like sense making) are interesting and account for the complexity of subjective emotions (in theory) but it is extremely difficult to translate them to real, clinical settings. Indeed, that was the initial idea discussed in Fredericton: to create questionnaires considering the concepts of Sense making theory to collect emotions. Therefore, from a clinician perspective, I was simply told that **the best way to get the level of an emotion is to ask directly to the patient**. They told me that we (engineers, etc.) often do not trust on a subjective value provided by a person and seek for an objective, single number to summarise the level of emotion using alternative devices (sensors, etc.) and sophisticated analytics. This does not work (yet). The best way (as of today) is to ask “What is your level of fear right now?” in case a therapist is interested in knowing the emotion of fear perceived by a patient. And the patient just picks one value from 1 to 10 when she’s prompted with the question. There is a whole branch in psychology called psychometric that focuses on exploring the best scale for measuring emotions.

In summary:
* There is no taxonomy of emotions. Psychologists reviewed again literature prior to the meeting.
* Measuring emotions makes sense only in a particular type of disorder. For example, we can measure “fear” in the disorder of phobias, but levels of the same emotion (fear) are interpreted differently in another type of disorder. So, the interpretation of the levels of emotion varies from disorder to disorder.
* Ask directly the level of “fear”

### Meeting 2019-10-10
Participants. LABPSITEC (Juani, Adri), GEOTEC ()


### Meeting 2019-10-17
Participants. LABPSITEC (Diana, Adri), GEOTEC ()


### Meeting YYYY-MM-DD
Participants. LABPSITEC (...), GEOTEC (...)
