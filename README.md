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

### Meeting YYYY-MM-DD
Participants. LABPSITEC (...), GEOTEC (...)
