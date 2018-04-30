# Notes for Readings CS130

[link to eggert spring 2018 homework page](http://web.cs.ucla.edu/classes/spring18/cs130/syllabus.html)
> I'm going to be using the following syntax:
> Mc = McConnell Chapters
> Som = Sommerville Chapters

## _Week 4 Monday 4/23/2018 Mc 4 5 6, Som 7 16 18_
============================================================


## _Week 4 Wednesday 4/25/2018 Mc 20, Som 24 25_ Quality and Change Management
=============================================================
### **McConnell Chapter 20 The Software-Quality Landscape**
>focuses on Software quality as a big picture
#### 20.1 Characteristics of Software quality
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

#### 20.2 Techniques for Improving Software Quality

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

##### Development Process
  1. Quality Assurance Activities
    1. Change-control procedures - uncontrolled change sucks
    2. Measurement of results
    3. Prototyping - can prototype parts to determine usability
##### Setting Objectives
Page 468: There was study and they found programmers will be motivated to work towards a goal if you give them one.

#### 20.3 Relative Effectivesness of Quality Techniques
##### % of Defects Detected
Leading organizations use **wide variety** to achieve 95%
1. Study told different groups to do different techniques
  -combining just one with another increased detection by factor of 2
2. Some errors humans good at finding. Others, computer is.
3. **_Defect-detection methods work better in combination than in single_**
  - Explains why disciplined defect removal in extreme programming results in high detection. Highest is 97%

##### Cost of Finding Defects
  1. Best: least cost per defect while everything else is equal. this is because which stage or other factors may affect the cost besides Defects
  2. **Inspections are cheaper than Testing**

##### Cost of Fixing Defects
- Common theme: catch the mistake at the beginning or lowest-value stage to minimize damage = **more costly to fix later** = better detection techniques fix bug earlier
- one step technique = Inspections
- two step = Testing
- **one step cheaper than two step techniques**

#### 20.4 When to do Quality Assurance
Example of how not fixing a bug earlier is harmful:
requirements error -> design or architecture error -> code error -> extra test cases
**Defects come in at all stages so do quality assurance every stage like gates**

#### 20.5 The General Principle of Software quality
**The General Principle of Software Quality: Improving quality reduces development costs** = the best way to improve quality is not have to rework code
- biggest activity is debugging so improve quality by decreasing debugging times
- **Taking medium time to code a program produces most errors**

![Figure 20-2 page 475](https://flylib.com/books/2/823/1/html/2/images/0735619670/graphics/20fig02.gif)

- Better upstream quality results in better downstream
  - So net effect is less defects, shorter development time, and lower costs

### Som Chapter 24 Quality Management
- **QM** = Quality Management_
- **Quality Assurance** is the definition of processes and standards that should lead to high-quality products and the introduction of quality processes into the manufacturing process.
- **Quality control** is the application of these quality assurance processess to weed out products that are not of the required level of quality
- QM team should not be part of software dev team to get objective Reviews
- Managers may give up quality for speed. Independent QM team keeps them in check. In practice, small companies literallly can't do this.
- write as short as possible quality plans so people will read it

#### 24.1 Software quality
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

##### 24.2.1 The ISO 9001 standards framework
ISO 9001 is framework for developing software standards
To conform to ISO 9001 means u have to define how u relate to these standards specifically

Some customers demand suppliers be 9001 compliant to get certain quality management.

Mistake: if ISO9001 certified then product must be better than company that didn't certify

Sommerville thinks ISO 9001 is inadequate because it defines quality to be the conformance to standards. Doesn't take into account the user experience defined quality. For example, a company could define test coverage standards that are bad. The user would then suffer even though it met the ISO 9001 standard.

![page 710 figure 24-6](http://slideplayer.com/slide/4646877/15/images/7/Figure+24.6+ISO+9001+and+quality+management.jpg)

#### 24.3 Reviews and Inspections
Quality reviews are based on documents that have been produced during the software development process. test plans, procedures, user manuals, etc.

Reviews are not just about conformance to standards. Also help find problems
  -formally recorded
Purpose of reviews and inspection is to improve software quality, not to assess performance of coder

Quality Reviews != Progress reviews

Progress Reviews track how on track u are with your original plans

##### The review processes
1. pre-review activities: arranging time, distributing necessary documents, etc.
2. review meeting: short. need scribe. author should walk the group through the reviews
3. Post-review: address issues

Review teams should have up to 4 people be principle reviewers. can bring in more specialized people

![review pipeline](https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-34-638.jpg?cb=1420194297)

##### Program inspections
- These are peer reviews where engineers examine the source of a system with the aim of discovering defects
- Inspections don't require implementation so may be used before implementation
- can be applied to any representation: requirements, design, configuration data, etc.
- effective

Inspection checklist:

Data faults: are all varibales init?
Control faults: each loop will terminate?
etc.

#### 24.4 Quality management and agile development
**Quality management is informal in agile**
  - relies on have a "good quality" culture
  - don't like bureaucratic ISO standards bs

##### Shared good practice
  1. Check before check-in: programmers responsible for organizing their own code reviews before actually placing it in the build systems
  2. Never break the build: never check-in code that will fail
  3. Fix problems when u see them: don't have to always go back to original developer

##### Reviews and agile methods
- informal
- in scrum, there is review after every sprint
- in XP, pair programming guarantees code is constantly being reviewed

##### Pair programming
**Advantages:**
- 2 people are responsible for code development
- code is constantly check by team member
- both programmers have to have deep knowledge
- can find bugs not found inspection process
**Weaknesses**
- can both make same mistakes
- don't want to slow other down so don't look for mistakes
- bad relationship

##### Agile QM and large systems
When we have large systems, agile qm is impractical
- informal communication hard to manage geographically
- new team members need documentation to catch up

#### Software measurement
Software measurement is concerned with deriving a quantitative value for an attribute of a software process
- allows objective comparisons
- few established Standards
- most companies don't make use of systematic measurement

**Software Metric:** Any type of measurement for systems
  - #. of lines of code is an example
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

![figure 24.10 page 718](https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-54-638.jpg?cb=1420194297)

Problems with measurement in industry:
- impossible to quantify return on investment
- no standards for software metrics
- in many companies, software processes are poorly defined
- Most work on software measurement has focused on code-based metrics and plan-driven development processes. However, more and more software is now developed by configuring ERP systems or COTS
- introducing measurement adds additional overhead to processes. this contradicts agile methods

Empirical software engineering:
- Research on empirical software engineering has not had a significant impact on software engineering practice
- difficult to relate generic research to a project different from research

##### Product Metrics
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
![figure 24.11 page 721](https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-60-638.jpg?cb=1420194297)

Theres a CK object-oriented metrics suite.

##### Software Component Analysis
System component can be analyzed separately using a range of metrics
The values of these metrics may then be compared for different components, with some past data, and if the measurements deviate from the norm they have defect.

Product measurement:
![figure 24.13 page 723](https://image.slidesharecdn.com/ch24qualitymanagement-150102101915-conversion-gate02/95/ch24-quality-management-64-638.jpg?cb=1420194297)

##### Measurement ambiguity
Can't just look at data. must also look at context to not misinterpret.

Measurement surprises:
**Reducing the number of faults in a program leads to an increased number of help desk calls**
  - program is now thought of as more reliable, so larger customer base so more calls overall.

##### Software analytics
- automated collection of user data
- github

- Software analytics still immature
- general problems of big data. knowldge depends on collected data from large companies
- small companies unlikely to invest in automated collection of data so maybe can't use analytics

### Som Chapter 25 Configuration Management
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

![figure 25.2 page 733](https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-9-638.jpg?cb=1420194310)

In large projects, it is part of software quality management. QM team checks the changes

No standard terms but heres some
![figure 25.3 page 734](https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-10-638.jpg?cb=1420194310)

#### 25.1 Version Management
process of keeping track of different versions of software components and systems in which these components are used

Codeline vs Baseline
**Codeline:** sequence of versions of source code, with later versions in the sequence derived from earlier versions.

**Baseline** definition of a specific system. already specifies what libraries used, configuration files, etc. important to recreate an individual version. may be specified with configuration language

![figure 25.4 page 736](https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-16-638.jpg?cb=1420194310 = 100x)

<img src="https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-16-638.jpg?cb=1420194310" width="200" height= "200" />

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
![figure 25.5 page 737](https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-21-638.jpg?cb=1420194310)

Integration manager:
![figure 25.7 page 739](https://image.slidesharecdn.com/ch25configurationmanagement-150102101915-conversion-gate02/95/ch25-configuration-management-26-638.jpg?cb=1420194310)


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

#### 25.3 Change Management
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
