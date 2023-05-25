# Lab Report 3

The command I will be covering is "grep". The four command-line options I will be covering are -v, -i, -c, and -w.

**-v Example 1**

`maxmendelson@Maxs-MacBook-Pro docsearch % grep -v "is" technical/biomed/1468-6708-3-1.txt`      
`        Introduction                                                                     `
`        elderly [ 9 ] .                                                                  `
`          Study                                                                          `        
`          ] .                                                                            `
`          (for persons who were never in excellent, very good, or                        `
`          report results using only the simpler definition.                              `
`          findings.                                                                      `     
`        Results                                                                          `
`        likely.                                                                          `
`        from 25 to 29.9. The second column, which shows results                          `
`        under 20.                                                                        `
`        groups.                                                                          `
`        YOL or YHL.                                                                      `     
`        Discussion                                                                       `     
`          YHL.                                                                           `  
`        Conclusion                                                                       `
`        'overweight' by the NHLBI guidelines. This suggests using                        `  
`        Competing interests                                                              `                           
`        CESD Center for Epidemiologic Studies Depression                                 `
`        poor?                                                                            `                                                                                  `

Lets say we want to find all lines that don't have "a". You can use -v to find all lines in the file that do not contain "a".

**-v Example 2**

maxmendelson@Maxs-MacBook-Pro docsearch % grep -v "e" technical/911report/chapter-1.txt
"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
IMPROVISING A HOMELAND DEFENSE
    NEADS: On its way towards Washington?
    NEADS: Okay.
NATIONAL CRISIS MANAGEMENT
What If?

Let's say we want to find all lines that don't have "e". Just like the previous example, you can use -v to find all lines in the file that do not contain "e".

**-i Example 1**

`maxmendelson@Maxs-MacBook-Pro docsearch % grep -w "is" technical/government/Alcohol_Problems/DraftRecom-PDF.txt`

suggested that the recommendation be clear that it is addressing
that the patient's problem is consumption. He favored
"alcohol-related problems" because consumption is not the problem.
The problem is the consequences resulting from excessive
suggested another alternative, "problem drinking," which is
setting, where there is the question of training and the link
in isolation. He noted that little is known about effective
Referral-SBIR." Research on the individual components is important,
but the strategy for the emergency room setting is as follows:
screen, decide if a brief intervention is called for, and if not,
is a vital part of the work.
Hungerford emphasized that research on screening is needed.
However, he believed research on screening instruments that is not
a full protocol. The second recommendation, therefore, is intended
clinician who is interested in seizures or pancreatitis could
applications of interventions. If that is the goal, he thought we
large numbers of people at low cost is necessary. He believed in a
if the yield is low. He suggested that the technical aspects of
it is already used to designate small business innovation research
specified, well-described service in a clinical setting is a
an adaptation from primary care or as an innovation from the ED is
technologies)." She said this type of information is absolutely
Gordon explained that because Medicare is prohibited by statute
ironclad case that the intervention is effective, a consensus in
Recommendation #4 Research is needed to evaluate the effects of
addresses. He noted that alcohol screening in the ED is currently
Recommendation #5 Research is needed on how demographic and
profoundly influence how screening and intervention is delivered.
Recommendation #6 Research is needed to identify the factors
factors affecting that relationship. This research is crucial as
"implementation" to the recommendation. Research is needed on how
recommendation is too narrowly defined, we will encourage people to
strong a training program is, if there are no incentives for
insurmountable or the health care system is in total chaos and you
cannot find who is in charge of the department because somebody has
Peter Rostenberg noted that most trauma care is delivered in
screening works and that the sooner screening is implemented the
is appropriate for alcohol problems because they are not just
counseling is not available, screening and interventions are less
Recommendation #7 Research is needed to explore and define the
application pro-gram is oversubscribed.
For some patients, the ED visit is the only contact with the
is possible to emphasize this topic without stating that it should
and more resources if the field is to move forward.
"prioritization." It is unfortunate, but in the eyes of funders, it
is perceived as a zero sum game.
specifically for this topic. He said the way to accomplish this is
support that is commensurate with the burden of illness.
other conferences, which indicates that this issue is high on the
Interacting with the Council is an important way to influence
interventions, are on the list. NIAAA is a small institution with
Brown suggested that the recommendation remain as is, but that
Because drug use is also an important issue among ED patients, he
Gentilello acknowledged that there is a demand problem. The goal
is to help trauma surgeons and emergency physicians realize that
dealing with alcohol problems is an integral part of their job.
Research on alcohol problems is as important as research on sepsis
Longabaugh remarked that NIH is increasingly trying to

Let's say I want to find all the lines that specifically have "is" but not within another word like "his" or "this". 
You can use -w to only find lines with that exact pattern.

**-w Example 2**

`maxmendelson@Maxs-MacBook-Pro docsearch % grep -w "20" technical/plos/journal.pbio.0020001.txt`
        the 20 top ecological journals (with impact factors of 10.51–2.47) (ISI 2001a). We credited
        For the top 20 ecological journals, the American subcontinents of South, Central, and
        respectively, for 13% and 82% of the top 20 ecological publications. When we examined the
        the top 11–20 (impact factors 3.28–2.47), the Latin American countries contributed nearly
        twice as many publications to journals in the second category (8% in the top 11–20 compared
        top 11–20 journals (79%). The difference in the proportion of publications contributed by
        the United States to the top 10 and top 20 journals was even more pronounced when we
        to the top 11–20 journals.
        Nature were nearly identical to those of the top 20 ecological journals.
        versus 6% in the top 20 ecological journals, whereas the United States and Canada had 81%
        
Let's say I want to find all lines that have "20" but not "2000". Like before, you can use -w to only find lines with that exact pattern.

**-i Example 1**

maxmendelson@Maxs-MacBook-Pro docsearch % grep -i "conference" technical/government/About_LSC/Comments_on_semiannual.txt
At the Equal Justice Conference ("EJC") held in March 2001 in
the second Case Management Software pre-conference. The primary
to Justice Conference; the EJC; the National Legal Aid and Defender
conference of representatives from legal services, state courts,
series of conferences on diversity. These conferences will enable
first conference was held on March 31, 2001 in conjunction with the
2001 Equal Justice Conference, and others are planned later in
Client Conference
three-day conference in Hershey, Pennsylvania, entitled "Creating
Client-Centered State Communities of Justice". The conference
Sixteen (16) conference papers were written by legal services
the conference discussions. The conference was attended by a
Conference participants reflected a true cross section of the
LSC will publish a report on the conference in June 2001. The
the conference and serve as a possible guide to help clients and
Practices" at the March ABA/NLADA Equal Justice Conference.
during the March ABA/NLADA Equal Justice Conference. Approximately
Program Performance held a special telephonic conference for 2002

Let's say I want to find all lines that contain the word "conference" but I don't 
