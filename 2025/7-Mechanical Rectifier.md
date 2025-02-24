# Mechanical Rectifier

- You've been assigned, from your local problem solving firm,[Mechanical Motion Consolidated] to create a system that will take in a non-constant uni-directional rotary motion, and convert it into a constant velocity uni-directional rotational output. Your system must also relay information about the input and output rotation of the system

## Requirements 
1. The system must be quickly assemblable onto and off of the aluminum breadboard. (less than 5 minutes to assemble or disassemble)
2. The system must connect to the input motor shaft, this coupling device MUST have a gearing feature on it to mesh with the encoder gear.
3. The system must have a way to measure (either in real-time or through post processing) it's input and output rotational speeds vs. time. 
4. The ouput rotational motion MUST rotate a disc with a diameter between 1-3 inches.
5. Your system will be tested at 3 different frequencies (f = 1Hz, 0.5Hz, 0.25Hz)
## Milestones
1. 3 potential solutions for the Mechanical Rectifier
    1. Sketches OR CAD are acceptable for visual representations of the mechanism
    2. A system block diagram outlining the ENTIRE system you are designing (not just the mechanism and its features)
    3. An elevator pitch for each of the potential solutions
    4. Engineering Decision Matrix

2. An initial prototype of the system
    1. The prototype is not meant to be functional, though if you wish to prototype a feature to be functional that is okay.
    2. Most of the prototype is mean to be physical visual prototype to help you understand scale, potential assembly and manufacturing issues, and detecting missing features.

3. A functional CAD model and the beginnings of your first revision of the mechanism manufactured.
    1. The CAD should be an assembly, showing the motion of the mechanism (using mates and gear-relations)
    2. Important sub-systems, sub-assemblies and critical features should be through their first manufacturing revision

4. An updated functional CAD model considering critiques from the previous milestone and a complete prototype of your mechanism.
    1. Your mechanism design must be complete
    2. Your mechanism prototype must be completed with some "kinks" to iron out
    
5. Your finalized system ready to be put to the test!

6. Final Report on the project

## Deliverables
### Journals
- I expect a journal entry for each week minimum from each member of the group
- Journal entries must discuss what was done each week, critical decisions made, critical problems and how they were solved
### Final Report
- The point of this report is to consolidate all of the work you have done for the system. Documenting all the engineering decisions made and reasoning for them. 
- Think of this report as a way to present your project to someone who has no context of the class, and also has no context regarding mechanisms and/or mechanical systems.
- Provide pictures for context where needed
- Provide graphs of data (Properly labelled!) for context where needed
- Submit videos for reference and for context where needed

## Recommended Outline
1. Introduction to project. Project criteria, requirements, deliverables, problems
2. Potential solutions your group came up with
    1. Discussion of chosen solution
3. In-depth description of the chosen solution and its features. 
4. In-depth discussion of the designing/building process.
5. Analysis of the outcomes of the system. Did the system succeed in its goal? Show proof through the analysis
6. Conclusion: TLDR your report
<div style="page-break-after: always;"></div>

## Constraints
1. Encoder Gear is a 10-tooth, 4mm Module gear. Its center is located 40mm from the center of the motor shaft
![image](../2025/images/encoder-gear.png)
<div style="page-break-after: always;"></div>

2. The motor shaft is a 6mm D-shaft
![image](../2025/images/motor-shaft.png)
<div style="page-break-after: always;"></div>

3. The aluminum breadboard is made up of a matrix of 1/4-20 threaded holes that are 0.5" apart
![image](../2025/images/aluminum-breadboard.png)
<div style="page-break-after: always;"></div>


4. An output shaft speed of 0 rad/sec is not valid.  

5. The voltage applied to the motor will follow this function:
- V = (12/255) * (150 + (100\*sin(2\*PI\*f\*t)))  
- Where 'f' is the frequency of the varying voltage signal, and 't' is time in seconds.
- Since the arduino requires a 'pwm' value to control the motor, the (12/255) conversion from pwm to voltage was added in the above function
