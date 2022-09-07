# ARMT invervention experiment flow (Healthy subject) 

[Read me Online](https://hackmd.io/@maromaSamsa/r14l1sSeo)

## Objective: 

Compare the upper limb rehabilitation performance of traditional mirror therapy and augmented reality mirror therapy (ARMT)

## Subject
:::info
Recruit from WTMH Lab and other BME lab member
:::

Find at least 10, at most 30 subjects to join the intervention experiment, All subjects should be **right-handed and should be unfamiliar with the mirror therapy**. subjects did not have musculoskeletal or neurological defect and did not have visual impairment.

## Rehearsal
:::info
**Site**: Electrical engineering classroom
:::
 - Check the place experiment take, set up fNIRS, run through the software and collect the raw data. 
 - If fNIRS is not been used in the period by other labs, left it to stand by in the electrical engineering classroom.

### Selected date
- [ ] **2022/9/13 ::: 13:10 - 17:00**
- [ ] **2022/9/14 ::: 13:10 - 17:00**
- [ ] **2022/9/16 ::: 13:10 - 17:00**
> Discuss with professor Su's Lab which day is prefer.

## Period of formal intervention
:::warning
This schedul have **not** discuss with professor Su yet, may be changed in the future
:::
---


**September 2022**
- [ ] 9/20 (W2)
- [ ] 9/21 (W3)
- [ ] 9/27 (W2)
- [ ] 9/28 (W3)
- [ ] 9/30 (W5)

**October 2022**
- [ ] 10/4 (W2)
- [ ] 10/5 (W3)
- [ ] 10/7 (W5)
- [ ] 10/11 (W2)
- [ ] 10/12 (W3)
- [ ] 10/14 (W5)
- [ ] 10/18 (W2)
- [ ] 10/19 (W3)
- [ ] 10/21 (W5)
- [ ] 10/25 (W2)
- [ ] 10/26 (W3)
- [ ] 10/28 (W5)

:::info
**[Time: 13:10 - 17:10]**
**[At: Electrical engineering classroom]** 
**[Two subjects per day]**

 - **At least choose 10 day, 10 subject**, each healthy subject will have twice intervention, one is traditional mirror therapy, the other one is ARMT.
 - The interval between the two intervention times needs to be **more than one week**, as the cleaning period.
:::

---

## Intervention

```mermaid
graph TD;

A[Select subjects]
B[1:1 Randomization]
C1[MT <br> Once, 10 min fNIRS + 20 min therapy]
C2[ARMT <br> Once, 10 min fNIRS + 20 min therapy]
E1[ARMT <br> Once, 10 min fNIRS + 20 min therapy]
E2[MT <br> Once, 10 min fNIRS + 20 min therapy]

G1[Group1]
G2[Group2]

A --> B
B --> G1 --> C1
B --> G2 --> C2
C1 --One week washout--> E1
C2 --One week washout--> E2

INFO[Evaluated by fNIRS, pre-test and post-test]

E1 --- INFO
E2 --- INFO
```

### Select subjects
:::info
Recruit from WTMH Lab and other BME lab member
:::

Find at least 10, at most 30 subjects to join the intervention experiment, All subjects should be **right-handed and should be unfamiliar with the mirror therapy**. subjects did not have musculoskeletal or neurological defect and did not have visual impairment.

### Evaluation 
#### Pre-test and post-test
:::success
This part will be handled by Dr. Xu
:::
1. Pinch-holding-up-activity test, PHUA test
2. Semmes-Weinstein monofilament, SWM
3. Two-point Discrimination Test, 2PD)
4. Purdue Pegboard Test
5. Minnesota Manual Dexterity Test, MMDT


#### fNIRS
According to the literature research and Dr. Xu's IRB proposal, the following cortex regions will be selected:
1. brain prefrontal cortex
2. premotor cortex
3. primary motor cortex
4. supplementary motor cortex
5. sensorimotor cortex
6. secondary sensory cortex


![image](https://github.com/maromaSamsa/fNIRS-experiment/blob/main/fOLD/fOLD.png)
https://github.com/maromaSamsa/fNIRS-experiment/blob/main/fOLD/fOLD.png
> The fNIRS chennel will be set with reference to this chart


![image](https://github.com/maromaSamsa/fNIRS-experiment/blob/main/PNG/fNIRS.png)
https://github.com/maromaSamsa/fNIRS-experiment/blob/main/fOLD/fOLD.png
> Subject schematic

### Intervention schedule for single subject
Each healthy subject will have **twice intervention**, one is the traditional mirror therapy, the other one is ARMT.

#### Experimental procedure
 - Pre-test will take place in NCKU Hospital Rehabilitation Department
 - Next, for the purpose of collecting fNIRS signal, there will have ten minutes intervention will take place in NCKU BME Electrical Engineering Classroom.
 - In the ten minutes recording fNIRS time, the subject will only be asked to perform finger pinching, **by their non-dominant hand**. 
 - Depending on the group to which they were assigned, subjects **were asked to observe with their eyes a mirrored hand (their dominant hand)** generated through a mirror or VR headset.
 - After finish recording, subject will back to NCKU Hospital Rehabilitation Department to do the post test.


```graphviz
digraph {
    node[shape=record]
    splines = false
    rankdir = "LR"
    
    subgraph cluster01 {
        label="Experimental procedure (90 minutes)"
        pre [label = "Pre-test | <p>NCKU Hospital | <t> 20 minutes"]
        setup [label = "Setup | <p>BME EE classroom | <t> 10 minutes"]
        trans1 [label = "Transfer | <t> 5 minutes"]
        inter1 [label = "Intervention (fNIRS) | <p>BME EE classroom | <t> 10 minutes", fillcolor = "Turquoise", style = filled]
        trans2 [label = "Transfer | <t> 5 minutes"]
        inter2 [label = "Intervention | <p>NCKU Hospital | <t> 20 minutes"]
        post [label = "Post-test | <p>NCKU Hospital | <t> 20 minutes"]
        
        pre->trans1->setup->inter1
        inter1->trans2->inter2->post
    }
}
```


```graphviz
digraph {
    node[shape=record]
    splines = false
    rankdir = "LR"
    
    subgraph cluster01 {
        label="fNIRS Intervention (10 minutes)"
        rest1 [label = "Rest | <s>eyes close | <t> 30 seconds", fillcolor = "gainsboro", style = filled]
        pinch1 [label = "Pinching | <s>eyes open | <t> 30 seconds", fillcolor = "coral", style = filled]
        rest2 [label = "Rest | <s>eyes close | <t> 30 seconds", fillcolor = "gainsboro", style = filled]
        pinch2 [label = "Pinching | <s>eyes open | <t> 30 seconds", fillcolor = "coral", style = filled]
        rest3 [label = "Rest | <s>eyes close | <t> 30 seconds", fillcolor = "gainsboro", style = filled]
        pinch3 [label = "Pinching | <s>eyes open | <t> 30 seconds", fillcolor = "coral", style = filled]
        DOT[shape = plaintext, label = "..."]
        
        rest1->pinch1->rest2->DOT->pinch2->rest3->pinch3
    }
}
```
> Each trail box switch between resting and pinching, triggered by an auditory cue.
> **In the resting state**, subjects will be asked to let their minds go empty with closing their eyes
> **During the pinching state**, the subjects were asked to observe their mirrored hand.




 

