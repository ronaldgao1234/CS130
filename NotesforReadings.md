# Notes for Readings CS130

[link to eggert spring 2018 homework page](http://web.cs.ucla.edu/classes/spring18/cs130/syllabus.html)
> I'm going to be using the following syntax:
> Mc = McConnell Chapters
> Som = Sommerville Chapters

## _Week 4 Monday 4/23/2018 Mc 4 5 6, Som 7 16 18_
---


## _Week 4 Wednesday 4/25/2018 Mc 20, Som 24 25_ Quality and Change Management
------------------------------------------------------
### **McConnell Chapter 20 The Software-Quality Landscape**
=========================================================================
>focuses on Software quality as a big picture
#### *20.1 Characteristics of Software quality*
External Characteristics: users are aware of it
1. Correctness
2. Usability or ease of use
3. efficiency
4. reliability
5. Integrity
6. ...

Users only care about this. Don't care whether it's easy for you to modify. don't care about code

_Programmers care about internal and external qualities_
Internal Characteristics:
1. maintainability
2. flexibility - how much u can modify for your new environment
3. reusability
4. readability

**Difference between internal and external qualities not completely clear because internal can affect external**
  - if your code isn't flexible might affect usability
  - choosing characteristics becomes trade-off

  ![Figure 20-1](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR6Idk_mt5Y1UNRKXOqLZNLRAO9wSpzP526xYqonx2vE4-4GBBX)

#### *20.2 Techniques for Improving Software Quality*

  1. Set Objectives
  2. Make quality a priority - most of the times whoever finishes first is rewarded which isn't good
  3. Testing
  4. Guidelines
  5. Informal Technical Reviews
  6. Formal Technical Reviews: Quality gates - gates that are stages code has to pass to go to next stage of software development
    1. Gates can be an audit or inspection.
    2. gates are between stages like architecture and construction
      - Common theme: catch the mistake at the beginning or lowest-value stage to minimize damage.
  7. External audit

##### *Development Process*
  1. Quality Assurance Activities
    1. Change-control procedures - uncontrolled change sucks
    2. Measurement of results
    3. Prototyping - can prototype parts to determine usability
##### *Setting Objectives*
Page 468: There was study and they found programmers will be motivated to work towards a goal if you give them one.

#### *20.3 Relative Effectivesness of Quality Techniques*
##### *% of Defects Detected*
Leading organizations use **wide variety** to achieve 95%
1. Study told different groups to do different techniques
  -combining just one with another increased detection by factor of 2
2. Some errors humans good at finding. Others, computer is.
3. **_Defect-detection methods work better in combination than in single_**
  - Explains why disciplined defect removal in extreme programming results in high detection. Highest is 97%

##### *Cost of Finding Defects*
  1. Best: least cost per defect while everything else is equal. this is because which stage or other factors may affect the cost besides Defects
  2. **Inspections are cheaper than Testing**

##### *Cost of Fixing Defects*
- Common theme: catch the mistake at the beginning or lowest-value stage to minimize damage = **more costly to fix later** = better detection techniques fix bug earlier
- one step technique = Inspections
- two step = Testing
- **one step cheaper than two step techniques**

#### *20.4 When to do Quality Assurance*
Example of how not fixing a bug earlier is harmful:
requirements error -> design or architecture error -> code error -> extra test cases
**Defects come in at all stages so do quality assurance every stage like gates**

#### *20.5 The General Principle of Software quality*
**The General Principle of Software Quality: Improving quality reduces development costs** = the best way to improve quality is not have to rework code
- biggest activity is debugging so improve quality by decreasing debugging times
- **Taking medium time to code a program produces most errors**

![Figure 20-2 page 475](https://flylib.com/books/2/823/1/html/2/images/0735619670/graphics/20fig02.gif =200x)


- Better upstream quality results in better downstream
  - So net effect is less defects, shorter development time, and lower costs

### **Som Chapter 24 Quality Management**
==============================================================================
- **QM** = Quality Management_
- **Quality Assurance** is the definition of processes and standards that should lead to high-quality products and the introduction of quality processes into the manufacturing process.
- **Quality control** is the application of these quality assurance processess to weed out products that are not of the required level of quality
- QM team should not be part of software dev team to get objective Reviews
- Managers may give up quality for speed. Independent QM team keeps them in check. In practice, small companies literallly can't do this.
- write as short as possible quality plans so people will read it

#### *24.1 Software quality*
**Impossible to objectively say if a system has fulfilled a requirement**
because:
  1. hard to write unambiguous requirements
  2. sometimes have to give up requirements to fulfill others
  3. hard to measure something like maintainability

Therefore, quality assurance is largely subjective -> rating them depends on non-functional requirements like safety, security, ....

Not possible to optimize all non-functional requirements. Ex: Security -> loss in performance.

Define the most important quality instead

Traditional view: Quality of development process -> quality product Quality
  - largely due to manufacturing processes being like this. However, manufacturing processes were easily standardized and calibrated for higher performance. Software is designed so more individualistic. Having these standard processes can stifle creativity.

  **Solution:** Develop "high quality culture"

#### 24.2 Software Standards
  They are important because:
  1. based on company values
  2. provide framework for quality
  3. Actually a good reason: help the new guy know what standards to uphold.

**Product standards: ** Documentation standards like commenting
**Process standards: ** Good coding like design, validation processes, process support tools

More specialized standards for more critical systems

How to convince engineers why to follow good quality:
1. Involve engineers in selection of product Standards
2. Change to reflect changing technology
3. make sure support tool is available. For example a syntax-directed editing tool like the one i just downloaded in atom that makes function definition comments automatically

##### *24.2.1 The ISO 9001 standards framework*
ISO 9001 is framework for developing software standards
To conform to ISO 9001 means u have to define how u relate to these standards specifically

Some customers demand suppliers be 9001 compliant to get certain quality management.

Mistake: if ISO9001 certified then product must be better than company that didn't certify

Sommerville thinks ISO 9001 is inadequate because it defines quality to be the conformance to standards. Doesn't take into account the user experience defined quality. For example, a company could define test coverage standards that are bad. The user would then suffer even though it met the ISO 9001 standard.


<img src="http://slideplayer.com/slide/4646877/15/images/7/Figure+24.6+ISO+9001+and+quality+management.jpg" width=400 height=300>

#### *24.3 Reviews and Inspections*
Quality reviews are based on documents that have been produced during the software development process. test plans, procedures, user manuals, etc.

Reviews are not just about conformance to standards. Also help find problems
  -formally recorded
Purpose of reviews and inspection is to improve software quality, not to assess performance of coder

Quality Reviews != Progress reviews

Progress Reviews track how on track u are with your original plans

##### *The review processes*
1. pre-review activities: arranging time, distributing necessary documents, etc.
2. review meeting: short. need scribe. author should walk the group through the reviews
3. Post-review: address issues

Review teams should have up to 4 people be principle reviewers. can bring in more specialized people

<img src="https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-34-638.jpg?cb=1420194297" width=400 height=300>

##### *Program inspections*
- These are peer reviews where engineers examine the source of a system with the aim of discovering defects
- Inspections don't require implementation so may be used before implementation
- can be applied to any representation: requirements, design, configuration data, etc.
- effective

Inspection checklist:

Data faults: are all varibales init?
Control faults: each loop will terminate?
etc.

#### *24.4 Quality management and agile development*
**Quality management is informal in agile**
  - relies on have a "good quality" culture
  - don't like bureaucratic ISO standards bs

##### *Shared good practice*
  1. Check before check-in: programmers responsible for organizing their own code reviews before actually placing it in the build systems
  2. Never break the build: never check-in code that will fail
  3. Fix problems when u see them: don't have to always go back to original developer

##### *Reviews and agile methods*
- informal
- in scrum, there is review after every sprint
- in XP, pair programming guarantees code is constantly being reviewed

##### *Pair programming*
**Advantages:**
- 2 people are responsible for code development
- code is constantly check by team member
- both programmers have to have deep knowledge
- can find bugs not found inspection process
**Weaknesses**
- can both make same mistakes
- don't want to slow other down so don't look for mistakes
- bad relationship

##### *Agile QM and large systems*
When we have large systems, agile qm is impractical
- informal communication hard to manage geographically
- new team members need documentation to catch up

#### *Software measurement*
Software measurement is concerned with deriving a quantitative value for an attribute of a software process
- allows objective comparisons
- few established Standards
- most companies don't make use of systematic measurement

**Software Metric:** Any type of measurement for systems
  - \# of lines of code is an example
  - allows software to be quantified
  - may be used to predict product attributes or control processess
  - may be used to find defective components

  Types of metrics:
  1. time taken for completion
  2. resources needed
  3. number of occurrences of an event - Ex. number of bugs found during inspection

Use of measurements:
- to assign a value to system quality attributes like maintainability
- to identify the system components whose quality is substandard

Metric assumptions:
- software property can be measured accurately
- relationship exists between what we measured and what we know. We can only measure internal attributes but are often more interested in external software attributes
- May be difficult to relate what can be measured to desirable external quality attributes

<img src="https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-54-638.jpg?cb=1420194297" width=400 height=300>

Problems with measurement in industry:
- impossible to quantify return on investment
- no standards for software metrics
- in many companies, software processes are poorly defined
- Most work on software measurement has focused on code-based metrics and plan-driven development processes. However, more and more software is now developed by configuring ERP systems or COTS
- introducing measurement adds additional overhead to processes. this contradicts agile methods

Empirical software engineering:
- Research on empirical software engineering has not had a significant impact on software engineering practice
- difficult to relate generic research to a project different from research

##### *Product Metrics*
A quality metric used as a predictor of product quality

Classes:
1. **Dynamic metrics** - collected by measurements made during execution.
  1. help assess efficiency and reliability.
  2. Ex. time taken to complete execution.
  3. Dynamic metrics are closely related to software quality attributes. like response time
2. **Static metrics** - collected by measurements made of representations of the system.
  1. Ex. design, program,documentation.
  2. help assess complexity, understandability, and maintainability
  3. not closely related. need to derive relationship between metric and properties such as complexity, understandability,...

Some static metrics:

<img src="https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-60-638.jpg?cb=1420194297" width=400 height=300>

Theres a CK object-oriented metrics suite.

##### Software Component Analysis
System component can be analyzed separately using a range of metrics
The values of these metrics may then be compared for different components, with some past data, and if the measurements deviate from the norm they have defect.

Product measurement:

<img src="https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-64-638.jpg?cb=1420194297" width=400 height=300>

##### Measurement ambiguity
Can't just look at data. must also look at context to not misinterpret.

Measurement surprises:
**Reducing the number of faults in a program leads to an increased number of help desk calls**
  - program is now thought of as more reliable, so larger customer base so more calls overall.

##### *Software analytics*
- automated collection of user data
- github

- Software analytics still immature
- general problems of big data. knowldge depends on collected data from large companies
- small companies unlikely to invest in automated collection of data so maybe can't use analytics

### **Som Chapter 25 Configuration Management**
============================================================================
Configuration Management(CM) is converned with the policies, processes and tools for managing changing software systems.

- you need CM because it is easy to lose track of what changes and component versions have been incorporated into each system version
- CM is necessary because u need to control different changes from different developmers

CM activities:
- Version Management
- System building: process of assembling components, data and libraries to create executable system
- Change Management: keeping track of changes and their properties
- Release management: preparing software for external release and keeping track of system versions

CM can be simple bug tracking to integrated environments that support all CM activities

Agile needs CM - shared repo. everyone pull. everyone makes changes

software product phases:
1. development phases
2. system testing phase
3. release phase

Often, several differnt versions of software being worked on at the same time

<img src="https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-9-638.jpg?cb=1420194310" width=400 height=300>

In large projects, it is part of software quality management. QM team checks the changes

#### *25.1 Version Management*
process of keeping track of different versions of software components and systems in which these components are used

Codeline vs Baseline
**Codeline:** sequence of versions of source code, with later versions in the sequence derived from earlier versions.

**Baseline** definition of a specific system. already specifies what libraries used, configuration files, etc. important to recreate an individual version. may be specified with configuration language

<img src="https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-16-638.jpg?cb=1420194310" width="400" height= "300" />

X.1.2 is component version. X is identifier

VC system types:
1. **Centralized:** single master repo maintains all versions
2. **Distributed:** Multiple versions of the repo exist at same time. Git

Key features of both
1. Version and release identification
2. Change history recording
3. Independent development (done differently in Central vs distributed)
4. Project support
5. Storage management

"master" branch for baseline

Independent development (done differently in Central vs distributed):

Central:
Say Alice works on C and Bob works on C at same time. Alice checks out C so C.0 is given to her. she checks in C.1. Bob checks out C.1 for a new version so when he checks in it won't overwrite hers and it will be C.2.

  - disadvantage:
    - To integrate versions, there is manager who pulls your changed code from your own public repo individually. he pushes to the main repo.

How check in and check out looks

<img src="https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-21-638.jpg?cb=1420194310" width=400 height= 250>

Integration manager:

<img src="https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-26-638.jpg?cb=1420194310" width=400 height= 250>

Distributed:
"master", pull , commit, push
  - Advantages
    - provides backup for repo
    - allows offline working
    - dev's can compile and test entire system on local machine before uploading changes

When VC first developed, storage management was one of the most important functions. disk space was expensive. So peole just kept a **delta**, a list of changes.
  - disadvantage: took long time to apply deltas

#### 25.2 Sytem Building
System building: process of creating a complete, executable system by compiling and linking the system components, external libraries, Configuration files, etc.
  - lots of stuff so use automated tool

Tools for system integration:
1. build script generation
2. version control system Integration
3. minimal recompliation
4. executable system creation
5. test automation
6. reporting
7. documentation generation

built script is definition of system to be built. includes dependencies, etc.

3 different building places
1. dev system (local)
2. build server
3. target environment

Agile uses very frequent system builds

Steps in continuous integration: 25.2
1. extract mainline system from vc systems
2. build system and run testing
3. make changes
4. ...

Jenkins is a tool to support **continuous integration**
Advantage of continuous integration:
- Allows conflicting changes between dev to be solved ASAP
- Not always implementable
  - too large system = too long to build and test
  - dev platform different from target

For large systems, use **daily build system**:
1. dev need to deliver component by 2pm
2. new version buillt
3. sent to testing teams
4. back to dev team

Advantages of daily build:
  - chances of finding bugs early is incr.


To not have to recompile nontouched code, master version and your changed version have signatures and they compare them

2 types of **signatures**:
1. Modification timestamp
  - can't edit at same time because only recently saved version is kept. if u modify Comp.Java ur gonna get Comp.class. if 2 dev work at same time its 2 Comp.class so one guys work is lost
2. source code checksum
  - Advantage: allows many different versions of object code maintained at same time. source code and object code have same signature. Unlike modification timestamp, it doesn't overwrite object code, just generates new object code file and tags with source code signature.

#### *25.3 Change Management*
Process of analyzing costs and benefits of proposed changes, approving the good ones, and tracking what changes have been made

Differs between size of company and what kind of product

Tools can be simple or complex

Starts when stakeholder submits a **CRF**:
stakeholder can be dev, manager, customer, anyone
CRF has details about the change.

1. checker from support team checks CRF
2. for valid change requests, then change assessment and costing. Cost estimated.
3. Decide if cost-effective to change. In military often called Change Control Board (CCB). in industry its called product development group.
4. accepted change passed back to dev team

Things that will influence whether or not to implement a change:
1. consequence of not making it
2. benefits
3. costs
4. product release cycle. if just released new version, then delay implementation of change until next planned release.

Change management for software product is handled differently from custom systems
  - in software product, customer not directly involved. changes come from dev team or marketing team based on customer opinions

if change daily, no need for formal process.

in some agile methods, customers directly involved with change.

refactoring, continually improving software, is necessary

**derivation history of component:** list of changes the component went through

#### 25.4 Release Management
2 Types:
1. major release - new functionality
2. minor release - just fix bug

software release is not just code. may include documentation, installation program, etc.
page 751 shows what else it includes

marketing is involved with mass-market release

Release creation: creating a release by gathering all necessary files
Page 751 has step by step instructions

documentation is important. especially for military and those with complex machine

to document, record specific versions of the source code, os and hardware

**new releases of a system cannot rely on previous installations** -> sometimes customers won't install a particular release

**Software as a service** (SaaS) - simplifies all these problems since the developer is responsible for updating. problem might be that all servers must update at same time.

## _Week 5 Monday 4/30/2018 Mc 22,29 Som 8_ Testing
------------------------------------------------------

### **McConnell Chapter 22 Developer Testing**
============================================================================
1. Unit testing - tested in isolation from complete system. Can be done by 1 or more ppl
2. Component testing - tested in isolation from complete system. Only done in team(s)
3. Integration testin - testing how 2 component work together. Adds more and more until u get complete system
4. Regression testing - Redo previous test case to find defect
5. System testing - final test. test everything.

**Black Box testing:** can't see inner workings of item being tested
**White Box testing:** Can see. Ex. test your coder

**Debugging:** fix known error
**Testing:** detect error

### *Role of Developer Testing in Software Quality*

Why do testing when mixture of collaborative development practices find higher % of errors?

Why ppl don't like testing:
1. Counter to goal. Goal is now to find error, not build program.
2. doesn't solve completely
3. does not improve software Quality
4. makes u assume u will find erors in your program. but since u wrote it, u won't.

~~Testing = 50% of time~~ Why Wrong?
1. usually misleadingly includes testing and Debugging
2. not the time that *should* be spend
3. Usually includes *independent* and *developer* testing

<img src="https://flylib.com/books/2/823/1/html/2/images/0735619670/graphics/22fig01.gif" width="400" height= "200" />

> As project size increase, developer testing takes smaller % of total development time

Testing helps:
1. reveal common errors
2. shows how reliable

### *Testing During Construction*
- Testing with glass box: Know internally how the code is going allows you to test more thoroughly
- Check *routine* completely before mixing with others

## 22.2 Recommended Approach to Developer Testing
Things to test: requirements, design, checklist of errors.

**basis testing** - adding detailed test cases to those that test the requirements and desiign

### *Test Before Writing Code? Yes.*
- minimize amount of time to detect defect
- force u to think

### *Limitations of Developer Testing*
- Developer tests tend to be **clean tests** (test for if code works vs **dirty tests** which test how code breaks)
- Devs usually optimistic
- tend to skip sophisticated kinds of test

## *Bag of Testing Tricks*
Not possible to test if code is correct: Has to test *all* possible value. Which is impossible.

### *Incomplete Testing*
Pick test cases likely to give errors

### *Structured Basis Testing*
test each statement in the program at least once
If two "if" statements, 4 possible outcome, only test 2

**code coverage or logic coverage** are approachs to test all paths through a program. doesn't mean most minimal set.

Straightforward way of creating minimum nuber of test cases: page 506
- minimum != cover all bases

### *Data-Flow Testing*
Based on the idea that data usage is at least as error-prone as control flow
Add on to Structured basis testing, test cases for the data flow too

(ASIDE)
Data flow is where the data is going
Control flow is what operations are executed in what order
Intertwined. Depending on how control flow goes determines what data flow goes.

Data can exist in 3 states
1. Defined (initialized)
2. used
3. Killed

Control Flow: Enter and exit

### *Combination of Data states to treat with CAUTION*
1. Defined- defined
2. Defined-Exited
3. ...

### *Equivalence Partitioning*
Don't keep test cases that test same thing

### *Error Guessing*
Guess where errors already

### *Boundary Analysis*
Test the boundaries

### *Compound boundaries*
Boundaries for more variables: multiply 2 large numbers

### *Classes of Bad Data*
negative salary

### *Classes of Good Data*
Save an empty document. Group of one employee
If max is 500. Test group of 500 ppl.

### *Use Test Cases that Make Hand-Checks Convenient*
Output: Salary = 123456789. Probably something wrong with that salary....

## *Typical Errors*
> Natural to assume defects are ditributed throughout your code evenly. WRONG.
> Usually concentrated

*Why not surprising?*
1. 20% of routines is 80% of cost
2. Error-prone routines are highly expensive to fix
> General Principle of Software Quality: improving quality improves the developent schedule

### *Errors by Classification Page 519*
1. Most contrstruction erorr are programmers fault
2. Typos are common
3. Misunderstand design
4. Most errors easy to fix

### *Proportion of Errors Resulting from Faulty Construction*
- Most are construction errors. As project size increases as well too

### *How many Errors should you expect to find?  Page 521*
> Another Version of GPSQ(General Principle of Software Quality): Cheaper to build high-quality software than it is to build and fix low-quality software

## 22.5 Test-Support Tools

### *Building Scaffolding to Test Individual Classes*
**scaffolding** comes from building construction. Scaffolding is built so workers can reach parts of a building they couldn't reach otherwise. Software scaffolding is built for the sole purpose of making it easy to exercise code.

*Types:*
1. **Mock object or stub object:** class thats dummied up so that it can be used by another class thats being tested
for routines its just called **stub routine**

2. **driver:** calls the routine being tested
3. **dummy file:** small version of the real thing that has the same types of components as real deal

### *Test-Data Generators*
You can write code to test individual pieces of programs. Generate ton of random data. Random data can make a combination youve never thought of to introduce an error

### *Coverage Monitors*
Shows which parts of the code are being executed. So if not all your code is executed during testing, then you have not tested well

### *Data Recorder/Logging*
Log sophisticated

### *Symbolic Debuggers*
Supplement to code walk-throughs and inspections. step through code line by line

### *System Perturbers*
Simulate low memory or slowly filling memory or rearranging memory

### *Error Databases*
Data base of errors allows you to check for recurring errors

### *22.6 Improving Your Testing*

1. plan to test
2. retesting (regression testing)
3. automate testing

### *22.7 Keeping Test Records*
Basically keep track of details of an error so you can esitmate whether your project is going somewhere
1. Hours to fix defect
2. How severe the defect

## **McConnell Chapter 22 Developer Testing**
==============================================================================

**definitely look at each chart for each type of integration**

### *29.1 Importance of the Integration Approach*
Some Benefits of Integration carefully each step:
- less Defects
- less scaffolding
...

### 29.2 *Integration Frequency-Phased or Incremental*
#### *Phase Integration*
1. unit development
2. system integration
3. test and debug
Problems mix. Not good approch. maybe work for small project
#### Incremental Integration
1. make small functional parts
2. design code test
3. integrate with skeleton

#### *Benefits of Incremental Integration*
- Erors are easy to locate
- System succeeds early in  the project means higher morale
- progress monitoring
- units of the system tested more full

### *29.3 Incremental Integration Strategies*
Phase integration - since all are stupidly integrated at same time, don't need to order the integration
Incremental Integration - integrate in some order

#### *Top-Down Integration*
Benefits:
1. control logic is tested early
2. have partially working system soon

Problems:
1. leaves doing system interfaces last
2. large \# of stubs so more likely to contain errors
3. hard to implement purely
4. sometimes no top exists

#### Aternative *vertical slice*
top down by sections

#### *Bottom-Up Integration*
you write test drivers to exercise the low-level classes initially and add classes to the test-driver scafolding as they are developed
Benefit: easy to locate error
Problem: leaves integration of system interface until last, need to completely design system before starting integration

#### *Sandwich Integration*
do top then bot then mid

#### *Risk-Oriented Integration* Page 699
Do hardest part first.
top-level interface usually hardest so they do that first.
kind of like sandwich

#### *Feature-Oriented Integration*
integrate one feature at a time. good if features are independent
Adv:
1. eliminates almost all scaffolding
2. Shows progers
3. Is good with object oriented design

#### *T-shaped Integration*
do each slice from left to right

### *29.4 Daily Build and Smoke Test*
everything is compiled and has to pass a smoke test
1. reduces risk of low qualit
2. quality problems are prevented
3. easier to find defects

disadvantage: Can accumulate unseen error

1. Build daily
2. Check for broken buiilds
3. smoke test Daily
4. keep the smoke test current
5. ... Page 704

can do large builds

#### Continuous Integration
at least daily build
helps u stay in sync with group

## **Sommerville Chapter 8 Software Testing**
==============================================================================

validation testing - does it perform correctly to test cases
defect testing - test cases to expose defects

- validation: Are we building the right product?
- Verifiction: Are we building the product right?
- page 228

testing can reveal of prescence of errors NOT their abscence

Inspections > testing
1. during testing, errors can hide other erros
2. incomplete versions can be inspected without additional cost
3. inspection can consider broader quality attributes of the program
4. Inspections do not require execution of a system
^inspections not good for integration testing. thats where testing is good
Inspections can't check non-funcional requirements

stages of testing:
1. development testing
2. Release testing
3. User testing

### *8.1 Development testing*
Development testing includes all testing activiteies that are carried out by the team developing the system
Stages of development testing:
1. unit Testing
2. component testing
3. system testing

#### *8.1.1 Unit Testing*
Test methods or object classes
Inheritance makes it so that you have to test subtypes too. pain
state model
should automate. parts of automating page 234
2 Types
- normal operation
- abnormal input like neg. salary

#### *8.1.2 Choosing unit test cases*
1. **Partition testing**: find groups of inputs with common attribute and test how they are processed.
2. **guideline-based testing**: test based on guideline

Similar classes = **equivalent partitions**.
 - can be for input or output groups. once u find partition ust choose test cases from theses groups

#### *8.1.3 Component testing*
Component = several objects together
1. Parameter Interface: data or function refernce pass from one component to another
2. shared memory interface: share a block of memory
3. procedural interface: one component encapsulates a set of procedurces that can be called by other components
4. message passing interface: web shit

Types of errors
1. interface misuse
2. Misunderstanding
3. timing

#### *8.1.4 System testing*

ASDFASDFSAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
