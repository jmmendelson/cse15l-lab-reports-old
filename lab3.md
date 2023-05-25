# Lab Report 3

The command I will be covering is "grep". The four command-line options I will be covering are -v, -w, -i, and -c.

---

**-v Example 1**

```
maxmendelson@Maxs-MacBook-Pro docsearch % grep -v "is" technical/biomed/1468-6708-3-1.txt      
        Introduction                                                                       
        elderly [ 9 ] .                                                                    
          Study                                                                                   
          ] .                                                                              
          (for persons who were never in excellent, very good, or                          
          report results using only the simpler definition.                                
          findings.                                                                             
        Results                                                                            
        likely.                                                                            
        from 25 to 29.9. The second column, which shows results                            
        under 20.                                                                          
        groups.                                                                            
        YOL or YHL.                                                                             
        Discussion                                                                              
          YHL.                                                                               
        Conclusion                                                                         
        'overweight' by the NHLBI guidelines. This suggests using                            
        Competing interests                                                                                           
        CESD Center for Epidemiologic Studies Depression                                   
        poor?
```      

Lets say we want to find all lines that don't have "a". You can use -v to find all lines in the file that do not contain "a".

**-v Example 2**

```
maxmendelson@Maxs-MacBook-Pro docsearch % grep -v "e" technical/911report/chapter-1.txt
"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
IMPROVISING A HOMELAND DEFENSE
    NEADS: On its way towards Washington?
    NEADS: Okay.
NATIONAL CRISIS MANAGEMENT
What If?
```

Let's say we want to find all lines that don't have "e". Just like the previous example, you can use -v to find all lines in the file that do not contain "e".

Also, I took out the blank lines for both examples because they took up a lot of lines.

---

**-i Example 1**

```
maxmendelson@Maxs-MacBook-Pro docsearch % grep -w "is" technical/government/Alcohol_Problems/DraftRecom-PDF.txt

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
```

Let's say we want to find all the lines that specifically have "is" but not within another word like "his" or "this". 
You can use -w to only find lines with the specific word "is".

**-w Example 2**

```
maxmendelson@Maxs-MacBook-Pro docsearch % grep -w "20" technical/plos/journal.pbio.0020001.txt
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
```
        
Let's say I want to find all lines that have "20" but not "2000". Like before, you can use -w to only find lines with the exact number "20".

---

**-i Example 1**

```
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
```

Let's say I want to find all lines that contain the word "conference" even if its uppercase. You can use -i to ignore case differences so you can find lines that start with "Conference".

**-i Example 2**

```
maxmendelson@Maxs-MBP docsearch % grep -i "if" technical/911report/chapter-6.txt
            One of the 16, Raed Hijazi, had been born in California to Palestinian parents; after
                spending his childhood in the Middle East, he had returned to northern California,
                Council (NSC) Counterterrorism Coordinator Richard Clarke wrote Berger, "If George's
            In mid-December, President Clinton signed a Memorandum of Notification (MON) giving
                kill, though lethal force might be used if necessary.16Tenet would later send a
            Ahmed Ressam, 23, had illegally immigrated to Canada in 1994. Using a falsified
                Abdelghani Meskini, get training in Afghanistan if Meskini would help him maneuver
                stole a blank baptismal certificate from a Catholic church. With this document he
                appeal. Nine months later, his attorney notified the court that he could not locate
                identification, Ressam handed the Customs agent a Price Costco membership card in
                drug-related-until an inspector pried apart and identified one of the four timing
                that Hijazi had lived in California and driven a cab in Boston and that Deek was a
                government had no specific information about planned attacks.
                testified that it was her "training and experience." It
                Nawaf 's younger brother. Seeing links not only with al Qaeda but specifically with
            Though Nawaf 's trail was temporarily lost, the CIA soon identified"Khalid" as Khalid
                5, 2000.45 Other Arabs, unidentified at the time, were watched as they gathered with
            They identified one as Mihdhar. They later learned that one of his companions was
                identifier available for the third person was part of a name-Salahsae.
                lead and would let the FBI know if a domestic angle arose). The head of the Bin
                authorities could inform the United States if any of them departed from
            In early March 2000, Bangkok reported that Nawaf al Hazmi, now identified for the
                "not put too much of a dent" in Bin Ladin's network. If the United States wanted to
                "roll back" the threat, disruption would have to proceed at "a markedly different
                "if "but rather of "when"and "where."59The Principals Committee met on March 10,
                President's life. Counterterrorism officials also argued that Pakistan had not done
                proliferation, but also discussed Bin Ladin. President Clinton told us that when he
                terms of better relations with the United States, if he'd help us get Bin Ladin and
            This, too, had little if any effect. The Taliban did not expel Bin Ladin. Pakistani
                differed sharply with the CIA's managers about where it should come from. They
                in overall funds for the CIA and another supplemental appropriation specifically for
                the head of the CIA's Directorate of Operations, "said if there's going to be money
            The CIA had a very different attitude: Pavitt told us that while the CIA's Bin Ladin
                more intelligence, it remained difficult to distinguish
                surveillance, and had opened significant investigations in a number of field
                activating a special court to enable the use of classified evidence in
            But the CIA's institutional capacity for such direct action was weak, especially if
                al-Qaeda if suddenly a bunch of black ninjas rappelled out of helicopters into the
                if he lashed out in anger. Secretary of Defense William Cohen thought that the
                whereabouts. Gration and his team worked on a number of different ideas aimed at
                Predator if it proved able to lock in Bin Ladin's location. In the memo's margin,
                Berger wrote that before considering action, "I will want more than verified
                Ladin and target him for cruise missile or air attack. Even if Bin Ladin were not
                found, Clarke said, Predator missions might identify additional worthwhile targets,
                commercial vessel, specifically an oil tanker, but Bin Ladin urged them to look for
                residence. In addition, he sent his senior advisor, Mohammed Atef, to a different
                whom he identified as the big instructor (probably a reference to Bin Ladin)
                source, Bin Ladin wanted the United States to attack, and if it did not he would
                immediately sent to Yemen to investigate the attack. With difficulty, Barbara
                letting Americans openly carry long guns (rifles, shotguns, automatic weapons).
                few years earlier. To confirm the identification, the FBI agent asked the Yemenis
                the source identified Khallad from the Yemeni photograph.)
                identified Nashiri, whose links to al Qaeda and the 1998 embassy bombings were even
                Qaeda during the second half of November, identifying individual operatives whom the
                individuals to the coverage of the July 1999 Memorandum of Notification that allowed
                Afghanistan, or deliver an ultimatum to theTaliban threatening strikes if they did
                specific demands: immediate extradition of Bin Ladin and his lieutenants to a
                specifics. Intelligence gave some ambiguous indicators of al Qaeda direction of the
                enough time. If the agencies had given him a definitive answer, he said, he would
                Then it was up to the principals to decide if the case was good enough to justify
                because of their notion of how an intelligence standard of proof differed from a
                missiles would not do much good and might even help al Qaeda if the strikes failed
                the growing problems in Afghanistan." A multifaceted strategy would be needed to
                identifying, recruiting, clearing, and obtaining Senate confirmation of key
            Their policy priorities differed from those of the Clinton administration. Those
                Clinton administration had said specifically that Clarke's Counterterrorism Security
            The result, amid all the changes accompanying the transition, was significant
                arrangements. At the subcabinet level, there were significant delays in the
                formal meetings. If, however, he decided that an event or an issue called for
                administration. After Rice requested that all senior staff identify desirable major
                specifically for the Cole attack. Exchanges with the President, between the
                work. Though they made no decisions on these specific proposals, Hadley apparently
                unreliable, none of these pointed specifically to possible al Qaeda action inside
                public diplomacy, and if necessary military efforts. The State Department was to
                expanded covert action program including significant additional funding and aid to
                about al Qaeda." If Clarke was frustrated, he never
                characterize this as a dramatic shift from the previous administration."
                made to convince theTaliban to shift position and then, if that failed, the
                administration would move on the significantly enlarged covert action program. As
                strategy. First an envoy would give the Taliban a last chance. If this failed,
                developed an international coalition to undermine the regime. In phase three, if
                the idea of lifting sanctions may have seemed far-fetched, but perhaps no more so
                recall any specific guidance on the topic from the secretary. Brian Sheridan-the
                new section did not specifically order planning for the use of ground troops, or
                clarify how this guidance differed from the existing Infinite Resolve plans.
                not available and, even if the U.S. forces were sent in, it was not clear where they
                been how to do that if there had not been another attack on America. To many people,
                the beginning of 2002. On May 9, the attorney general testified at a congressional
            Ashcroft had also inherited an ongoing debate on whether and how to modify the 1995
                Thompson, issued a memorandum reaffirming the 1995 procedures with the clarification
                draft Memorandum of Notification, which included more open-ended language
                applied to reconnaissance flights) was money. A Predator cost about $3 million. If
                Force would bear the cost if a vehicle went down. Deputy Secretary of Defense
                hit tanks, not people. It needed to be designed to explode in a different way, and
                needed to continue and modifications needed to be made during the summer. Even then,
                said to us,"I would be shocked if you found anything that went faster than
                prevent specific al Qida attacks by using [intelligence] to detect them and friendly
                not been found. If the CIA was reluctant to use the Predator, Black did not mention
```
          
Let's say I want to find all lines that contain the word "if" even if its uppercase. Like before, you can use -i to ignore case differences so it includes lines that start with "If".

---

**-c Example 1**

```
maxmendelson@Maxs-MBP docsearch % grep -c "1" technical/911report/chapter-3.txt
350
```

Let's say I want just want to see how many lines contain the number "1". You can use -c to see the count of lines that contain the specific pattern.

**-c Example 2**

```
maxmendelson@Maxs-MBP docsearch % grep -c "Caulobacter" technical/plos/journal.pbio.0020053.txt
4
```

Let's say I want just want to see how many lines contain the name "Caulobacter". Like, before you can use -c to see the count of lines that contain the specific pattern.

---

The only url I used for information about the command line options was: https://man7.org/linux/man-pages/man1/grep.1.html
