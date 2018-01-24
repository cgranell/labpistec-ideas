# labpistec-ideas
Ideas, meetings, discussions and experiments between GEOTEC and LABPSITEC research groups

## Motivation
We (GEOTEC) want to start a prolonged colaboration with the LABPSITEC group to reach a win-win situation. On one hand, we seek our geospatial developments and toods make a real, social impact in the sense they might be used in real experiments, on the streets. On the other, LABPSITEC group can benefit from ready-to-use geospatial technology and tools for technology-driven interventions and experiments with cohorts of patients and hence considerably shorthenen times for data collection, analysis and decision making.

## Minutes

* [Meeting 2017-06-27](#meeting-2017-06-27)
* [Meeting 2017-09-18](#meeting-2017-09-18)
* [Meeting 2017-10-16](#meeting-2017-10-16)
* [Meeting 2017-10-26](#meeting-2017-10-26)
* [Meeting 2017-11-16](#meeting-2017-11-16)
* [Meeting 2017-12-12](#meeting-2017-12-12)
* [Experiment 2018-01-08](#meeting-2019-01-08)
* [Meeting 2018-01-11](#meeting-2018-01-11)
* [Focus group 2018-01-22](#focus-group-2018-01-22)

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

1. Definition of the application and the metrics in the server to cofigire the variables needed for the experiment 

2. Creation fo a mobile app, composed of:
    * Initial configuration tool, where the user (or perhaps the therapist in this case) indicates the user ID (with double confirmation), the point where the user's house is located, the radius that is defined as "area of the house" (the area from which it leaves or enters) and the date from which measures should begin to be taken.
    * Background service (which does not require interaction with the user) for monitoring regularly data and storing it.

3. A visualization tool so you can access the data. At the moment this tool will offer the best possible variables requested for the experiment with filters capabilities (by user, by date ...).

Experiment run from 25 to 28 of September. Juani/Diana provided 3-day data, Azu 1.5-day data, usign the [app](https://play.google.com/apps/testing/com.geotec.metrics.labpsitec_metrics_project). Output data resulting from the metric computation will be here (to be developed soon: @CARLOS)

### Meeting 2017-10-16
Participants: LABPSITEC (Juani, Diana), GEOTEC (Nacho, Luis, Ditsuhi, Carlos, Sven)

Presentation of two TFM projects, which may be potential candidate to use the app for data collection and the analytical platform for metric computation. Further details of TFMs [here](meeting20171016). Discussion of TFM's requirements and needs. Next, we discussed how the Ditshuhi's viz tool might be evaluated. One alternative was to use it to analyse patients' data. Another was to use it to analyse researcher's decision making process, i.e., how does the visualised data inform on the treatment (designed by the researcher)? 


### Meeting 2017-10-26
Participants. LABPSITEC (Juani, Diana), GEOTEC (Nacho, Luis, Ditsuhi, Carlos, Sven)

Presentation of results of first experiment (meeting 2017-09-18), discussion to enhace the accuracy of in/out home. Further details in [Diana's minutes](/meeting20171026/20171026minutas.pdf). In short, main limitations are:
* hard to determine IN/OUT home based only on GPS data. Signal error and low accuracy make us think about additional methods to GPS readings to respond satisfactorialy to this simple queistion: Is a patient IN/OUT home?
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
* wifi footprints are now collected and compared to double-check whether a user is at home. Further details in Spanish: Como hemos introducido es escaneo de las wifis, la configuración inicial requiere que además de introducir los datos que poniamos anteriormente, como son el usuario, la localización, días, etc, sea necesario que el usuario o paciente, una vez que llegue a su casa abra la aplicación y lo indique. Esto sirve para que podamos recoger la "huella" de las wifis que se pueden "ver" en su casa. A partir de ese momento, cuando se envíen los datos, la aplicación comprueba si el GPS está indicando que se encuentra cerca de casa (hemos establecido 30 m de radio) y en ese caso "lee" las wifis para confirmar (o en que grado) el usuario se encuentra en casa. Si el GPS indica que estamos lo suficientemente alejados de casa esa lectura no se efectúa, y de esa forma no es excesivo el gasto de bateria  para realizar esa comprobación. Solo destacar que esto que hemos introdicido es una estrategia  para confirmar que no tenemos "falsos fuera de casa" y que nos puede ayudar pero no sabemos aún la efectividad. 
* colleted data can be exported in case connection is down. Further details in Spanish: la base de datos interna se exporte automáticamente al final del experimento, eso nos ayudaría a en caso de tener problemas con los servidores (estadísticmente probable), poder recuperar los datos de los pacientes. Para realizar esta exportación hay dos formas: una manual, es decir, el terapeuta entra a la app y  en Ajustes, hace click en Exportar, y además al final del experimento (basado en las fechas introducidas de duración de experimento), la  aplicación lo debe hacer automáticamente.  Es recomendable hacerlo manualmente antes de desinstalarla para más seguridad.
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


### Meeting YYYY-MM-DD
Participants. LABPSITEC (...), GEOTEC (...)
