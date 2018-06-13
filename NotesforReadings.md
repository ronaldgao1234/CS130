# Notes for Readings CS130

[link to eggert spring 2018 homework page](http://web.cs.ucla.edu/classes/spring18/cs130/syllabus.html)
> I'm going to be using the following syntax:
> Mc = McConnell Chapters
> Som = Sommerville Chapters
> Went off lanqingwei's notes for relevant topics covered by sommerville cuz sommerville is too boring.
> The notes for the readings are complete for everything after the midterm. On the midterm, mostly main concepts like design pattern, architectures, UML diagrams and system perturbers were tested. So taking notes was a little bit useless.
## _Week 1 Monday 4/04/2018 Mc 1,3-3.4 Som 1,4_
============================================================
### **McConnell Chapter 1 Welcome to Software Construction**

Figure 1-1 Shows what construction really constraints
e.g. planning, integration, coding, debugging, etc.

**Construction is largely coding and debugging**

Not part of construction: requirements development, management, system testing,
etc. Page 6

#### *1.2 Why is Software Construction Important*
Page 7

### **McConnell Chapter 3-3.4 Prerequisites**
#### *3.1 Importance of Prerequisites*
- If you emphasize the end of a project you emphasize system testing.
- **If you emphasize quality in the middle of the project, you emphasize construction practices**

##### Do Prerequisites Apply to Modern Software Projects?
Yes. duh. risk reduction

##### Causes of Incomplete Preparation Page 25
1. Don't have the expertise to carry out their assignments
2. Can't resist coding as fast as possible
3. Managers are unsympathetic. Just want u to be coding.

##### Argument for doing Prerequisites
1. Appeal to Logic: good to prepare before big project
2. Building software is like building house
3. Appeal to Data page 29: Fix error = less cost

**Detect error as close to source as possible** Figure 3-1 page 30
Most people still don't detect the error early and rather catch  a large portion in debugging

#### *Determine the Kind of Software You're Working On*
Page 31 Table 3-2
Kind of Software:
1. Business Systems
  - Applications:  Games, Payroll Systems
  - Life Cycle Models: Agile, Evolutionary protoyping

2. Mission-Critical Systems
  - Applications: Games, Embedded Software, Software Tools
  - Life Cycle Models: Staged delivery, Evolutionary delivery
3. Embedded Life-Critical Systems
  - Applications: OS's, embedded
  - Staged delivery, spiral development

Very good table. For each kind of software, has the following sections relevant to each one:
planning and management, Requirements, Design, construction, Testing and QA, Deployment
Page 32

#### *Iterative Approaches' Effect on Prerequisites
2 Approaches to Prerequisites
  1. Iterative - Test as u go
  2. Sequential - Test at the very end

Cost of Iterative < Cost of Sequential
  - cost of focusing on prereq
  - cost of skipping prereq
Iterative better. Discover defect as you go.
Sequential = save for end to test for defect

** Most projects are neither completely sequential or iterative**
Rule of thumb: plan to specify about 80% of the requirements up front, and then slowly add requirements later.

#### *Choosing Iterative and Sequential Approachs*
Choose sequential when straightforward project ...
choose iterative if complex
Page 36 for more reasons

### *3.3 Problem-Definition Prerequisite*
If you can't have clear mission statement, you waste a lot of time

### *3.4 Requirements Prerequisite*
#### *Why have Official Requirements*
Explicit requirements make sure programmer and user have same vision
- helps to minimize necessary changes afterward

#### Myth of Stable Requirements
Know requirements as u go is good

#### Handling Requirements Changes During Construction
Page 40: Several things to make the best of changing requirements
1. Requirements checklist for quality
2. Dump the project if requirements are bad .
3. ...

### **Sommerville Chapter 1 Introduction**
Fundamental Software development activities:
1. Software Specification
2. software development
3. software validation
4. software evolution

#### *Software products*
1. generic - standalone. sold to any1
2. customized - made for particular customer
Page 21

General Issues that affect software:
- Heterogenity:Systems need to operate on multiple platforms like mobile and computer
- Business and social change
- security and trust
- scale

Application types: page 25
1. stand-alone
2. embedded control systems
3. interactive transaction-based applications
4. batch-processing
5. system of systems

Different level of necessary requirements for different systems. For medical you must meet requirement or some1 dies

### **Sommerville Chapter 4 Requirements Engineering**
Page 102
User requirements: written for customers
system requirements: could be between client and company

stakeholders: anyone who has a stake or claim. could be any1

Functional vs non-functional page 105

lanqingwei's notes does this part well.
#### *Requirements Elicitation*
Interviews sometimes can't do well because u can't understand the specialist

page 116 Ethnography - observational technique that can be used to understand operational processes and help derive requirements for software to support these processes
-these requirements are developed through awareness of other people's activities
-good for understanding but **can't identify new features that should be added to the system**
-problem with ethnography is that it studies existing practices which may be irrelevant
Ethnography + prototyping

#### *Requirements Specification*
writing down the requirements
lots of ways Page 121: natural language, graphical notation, etc.
Problem with natural language - unclear, **requirements almagamation** = mixing many requirements into 1
Problem with structured: too structured for business system requirements
form-based Page 124 has picture of example: literally filling out a form.
SRS
IEEE standard

#### *Requirements validation**
make sure its right
1. reviews of requirements
2. Prototyping
3. test-case

Requirements change, requirements evolution, requirements management
**systems developed incrementally typically have less detailed requirements**

## _Week 2 Wednesday 4/11/2018 Mc 2,21 Som 2-3_
============================================================
### **Mcconnell Chaper 2 Metaphors**
metaphor more like heuristic
Metaphors:
1. writing code vs writing a letter except software project invovles many people
2. Software is like farming: Plant seeds and grow crops. hard to extend past doing things incrementally. weak because it implies lack of control of direction
3. Oyster farming: slowly get more carbon to become pearl
4. Building software good metaphor. theres complexity, planning, won't build things someone else built like a fridge

### **Mcconnell Chaper 21 Collaborative Construction**
- testing is limited, code collaboration more effective
decrease development times
- pair programming costs more but takes less time than solo

> General Principle of Software Quality:
> reducing the # of defects improves development time

- Collaborative Development catches more types of errors than testing
- People write code better when they know it will be read
- Reviews help coders meet standards

**Collective Ownership**: group coding results in better code, less impact if someone leaves, defect correction more easy

#### *21.2 Pair Programming*
- don't let it turn into watching
- rotate pairs
- match pace with each others
- avoid personality conflicts
- team leader
- dont' pair newbs
- support pair programming with standards

Benefits of pair programming:
- better stress, code quality, shorter schedule

#### *21.3 Formal Inspection*
- checklists
- detect error not correct
- distinct roles
- moderator != author
- only hold meeting if every1 is prepared

Results:
- catch 60% of defects
- Design + code inspection 70-85%
- reduce overall cost

Roles during inspection page 486

General Procedure for inspection page 487
Planning , overview, preparation, inspection meeting , inspection report, rework, follow-up, third-Hour meeting: informal 1 hour meeting after

##### *Fine tuning inspection*
- don't combine stages
##### *Walk-through*
- emphasis on error detection
- Informal
- used intelligently as good as inspection. if not, it is just more trouble
- inspections are more focused

#### *Code-reading*
- less delays
- no group dynamics
- everyone only gives part of time in meeting

#### *Dog-and-Pony shows*
-show product

### **Sommerville Chapter 2 Software Process Models**

2.1 Waterfall Model page 47
2.1.2 incremental development
  3 advantages over waterfall page 50
  2 managerial disadvan
  - does not mean u incrementally reveal to customer
2.1.3 integration and configuration
reuse step included : 3 things commonly reused page 52

2.2 process activities
2.2.1 Software specification
2.2.2 Software design and implementation
2.2.3 Software validation
2.2.4 Software evolution
2.3 Coping with Change
  2.3.1 Prototyping
  - early version of a software system that is used ot demonstrate concepts...
  - test feasibility
  2.3.2 Incremental Delivery Page 64 Som
  4 advantages
  3 disadvantage
2.4 Process Improvement

### *Sommerville Chapter 3 Agile software Development*
Agile: page 76
XP: page 77
refactoring: page 80
Test-first development: page 81
Pair programming: page 83
Scrum: page 85
Scaling agile methods: page 88
Problems with agile: page 89
agile and plan-driven methods: page 91
Agile for large systems: 93

## _Week 2 Monday 4/16/2018 Som 5 19 20_
============================================================
## **Chapter 5 System modeling and engineering**
Discussion:
Types of UML Diagrams:
- behavioral modeling:
  - capture the dynamic execution of the system
    - use case, state, sequence, activity diagrams
- static/structural modeling
  - capture the fixed-code lvevel relationships in the system
    - class diagram, component diagram

UML diagramas that are covers.
1. Use case diagrams - Describe the functional behavior of the system as seen by the user
2. Class diagrams - describe the static structure of the system: Objects, Attribute, Associtation
3. Sequence diagram - describe the dynamic behavior between actors and the system between objects and the system
4. Statechart diagrams - describe the dynamic behavior of an individual object (essentiall a fini state automaton)
5. Activity Diagrams - Model the dynamic behavior of a system, in particular the workflow (flowchart)

Context Models
Interaction Model
Structural models
Behavioral Models: many business systems
Model-driven architecture
	1. CIM - computation independent model
	2. PIM - platform independent model (no implementation)
	3. PSM - platform specific model
	-Companies don't want to take MDA approach because they have to develop their own tools
	-for bigger companies, less benefit
	-adoption of agile over the times has allowed for diverting away from MDA

Just use discussion notes

Context model: page 141
Interaction Models: page 144

## **Chapter 19 Som**
Inter-disciplinary working:
		-communication problem
		-different assumption
		-professional boundaries
Sociotechnical systems: includes people and technical
	-boundaries are subjective. generally used in organizations
	-**emergent properties**: depends on system, consequence of relationship between system components
		-can only be measured after components are included
		-Reliability, Repairability, Security, Usability, Volume
		-reliability can depend on context(temperature)
	-**Non-deterministic**: don't always produce same output because of human
		-Success criteria
	-Complex relationship with organisational objectives: not only dependent on system
Conceptual Design: easy
	-feasiblity study, system structure development, system vision document
Systems procurement: make the conceptual design
	-Before procurement: decisions to be made on 1. scope of the system, 2. budget, 3. high level requirements
	-Approved set of application software; third part don't work
	-regulations can affect procurement
Systems development: make the product
	-usually plan driven because of need for parallel development of different parts of a system
	-involves different engineers
	-interface issues
	-requirements issues
System operation and evolution: start using it for its intended purpose
	- do not have to have the solution to everything since human operator. even if automated system
	-evolution is costly
	-legacy systems: existing systems that must be maintained

## **Chapter 20 Som**
System Complexity Page 584 Som
1. technical complexity
2. managerial complexity
3. governance complexity
System of systems classification
1. organizational systems
2. federal systems
3. system coalitions
Reductionism and Complex Systems
- breaks down because of inherent complexity of system of systems
Systems of systems engineering
  interface dev
  integration and deployment
System of system architecture
architectural patterns for system of systems

Basically entire chapter is about integration of systems with each other

## _Week 4 Monday 4/18/2018 Mc 3.5, Som 6 17 28_
============================================================
### **McConnell Chapter 3.5 Architectural Prerequisites** Page 44
Architecture = "high level design"
Typical Architecture Components:
	Program Organization
	Major Classes
	Business Rules
	Data Design
	UI Design
	Resource Management
	Security
	Performance
	Scalability
	Interoperability
	Internationalization/Localization
	Input/Output
	Error Processing
	Fault Tolerance
Architectural Feasibility
	Overengineering
	Buy-vs.-Build Decisions
	Reuse Decisions
	Change Strategy
	Quality

### **Sommerville 6 Architectural Design** Page 168
Architecture in the small  vs large
Advantages of architecture: Stakeholder communication, System Analysis, Large scale reuse
Contradiction between architectural model vs industrial practice because therer are 2 ways model of a program is used
1. as a way of encouraging discussion about system design
2. way of documenting an architecture that has been designed

Architecture depend on non-functional requirements of system: performance, security, safety, availability, maintainability
	obvious take and give situation going on
4+1 model: logical view, physical view, development view, process view
hofmeister adds conceptual view, designed during design processes

Argue whether or not should use UML: He likes it: useful when documenting architecture
MVC
	advan- independent change
	disadvan - may involve additional code and complexity
Layered Architecture: only adjacent layer is affected
	Advan: dependability, redundancy = authentication
	disadvan: hard to actually separate
Repository Architecture:
	Advan- independent components, backups, think github, changes can go to everyone instantly, efficient sharing
		of large amounts of data
	-Disadvant: repo is single point of failure
Client-server
	advan- servers distributed across a network
	disadvan: each service is a single point of failure so suceptible to DOS
	performance is unpredictable
Pipe and filter architecture
	advan: easy to understand
	disadvant: may have sysetm overhead because u have to have correct format of data transfer

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

#### *24.2 Software Standards*
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

# After Midterm
------------------------
## _Week 6 Monday 05/07/2018 Mc 28 Som 22_
### *Chapter 28 McConnell Managing Construction Page 661*
Good for developer to understand the issues that managers face

#### *28.1 Encouraging Good Coding*
- Don't let managers define good coding practice, let a respectable architect do it

#####Techniques for Encouraging Good coding
-Assign 2 people to every part of the project
-Review every line of code
-require code sign-offs
-Route good code examples for review
-Emphasize that code listings are public assets and not just your own
-reward good code
-easy standard: manager must be able to read the code

#### *28.2 Configuration Management*

- CM is the practice of identifying project artifacts and handling changes systematically so that a system can maintain its integrity over time.

- Despite needing CM, many people have been avoiding it for decades

- Software configuration management (SCM)
- Problem with SCM is overcontrol.
- For small number of people just do informal backups. For large projects need procedures.


##### *Requirements and Design Changes*
- Follow systematic change-control procedure
- Handle change requests in groups
- Estimate the cost of each change
- be wary of high change volumes
- Establish a change-control board or its equivalent in a way that makes sense for the project
- Watch for bureaucracy but don't let the fear of bureaucracy preclude effective change control

##### *Software Code Changes*
- version control software
- backup

#### *28.3 Estimating a Construction Schedule*
Estimation Approaches:
- Establish Objectives
- Allow time for the estimate and plan it
- Spell out software requirements ....
- page 672

Estimating the Amount of Construction:

Figure 28-2 Estimates created early in the project are usually inaccurate. they become more and more accurate as you go.

page 675: lots of influences on what a project's schedule should be

- Once you have a schedule. hard to control.

What to do when you fall behind:
- Hope you'll catch up: Never works. u fall more behind
- expand the team: usually worse. can work.
- reduce scope of the project: prioritize important

#### *28.4 Measurement*
- for any project attribute, it's possible to measure that attribute in a away that's superior to not measuring at all
- be aware of measurement side effects. people focus on work that is measured
- start collecting more measurements as the project get more complex

### *28.5 Treating Programmers as People*
top 20% programmers did 50% of the work
- found no relationship between a programmer's amount of experience and code quality or productibity
- 80% of contribution comes from 20 percent of the contributors
- pay more to get a better programmer.

Programmers have preferences so let them program with what they want.

correlation between productivity and quality of work. duh
Lots of improvement comes from a good productive environment

#### *28.6 Managing your manager*
don't be an idiot. plant an idea inside ur manager. lmao

### *Chapter 22 Developer Testing Page 499*
Software engineering differences with other Engineering
- product is intangible
- large software projects are often "one-off"
- software processes are variable and organization-specific

Lots of factors affect software projects:
- company size
- customers
- software size
- culture

Similarties between every project:
- project Planning
- risk management
- people Management
- reporting
- proposal writing

#### *22.1 Risk Management*
- project risks affect project schedule or resources like losing an architect
- product risks: failure of purchased component
- business risk

overlaps are possible of course

Steps to take:
1. risk identification
2. risk analysis
3. risk Planning
4. risk monitoring

risk management in agile development is less formal

##### 22.1.1 Risk Identification
people organizational tools, technology, estimation, requirements

##### 22.1.2 Risk Analysis
He thinks right number of risks to monitor depends on project

##### 22.1.3 Risk Planning
"what-if" questions

1. avoidance strategies
2. minimalization strategies
3. contingency plans

##### 22.1.4 Risk monitoring
do it regularly. staff morale. relationships. turnover.

#### *22.2 Managing People*
don't be a dick

##### *22.2.1 motivating people*
- give them a social space, satisfy their esteem, and give them demanding but not impossible tasks
- Maslow's model of motivation but he doesn't like that it takes an exclusively personal viewpoint on motivation. doesn't take into account they like being part of that company

#### *22.3 Teamwork*
- best size for engineering group is 4 to 6 people
- can name the group or establish territory to promote cohesion
- promote cohesion by including group members and let them be inclusive

##### *22.3.1 Selecting Group Members*
- "competing engineers problem": people start competing cuz they like their work which becomes everyone redesigning stuff and competing to rewrite each other's code.
- interaction-oriented people tend to detect tensions and dissolve them

##### *22.2.3 Group Organization*
- for large projects, best to separate technical and managerial roles
- junior staff might know more about technology than top staff because technology changes so fast
- don't adopt a model that is based on individual experts even though they can produce 25x more code. it demotivates the rest.

##### *22.3.3 Group Communications*
1. Group size
2. Group structured
3. Composition - want mixed sex group. women often more interaction-oriented than men and may act as interaction controllors or facilitators
4. etc.
5. Page 663
Barrier to this is remote members

## _Week 6 Wednesday 05/09/2018 Mc 3.6,27 Som 23_

### _3.6 Amount of Time to Spend on Upstreaam Prerequisites_
- generally 10-20% of effort and 20-30% of schedule to requirements...

### _Chapter 27 How Program Size Affects Construction_
- larger group of people means more communication issues are possible
- Typing documents is the formalized communication that people usually do

#### _27.2 Range of Project Size_
- One way of thinking about project size is thinking about the size of the project team

#### _27.3 Effects of Project Size on Errors_
**as project size increases, more errors come from requirements and design**
- On small projects, construction erors make about 75% of the errors found. 50% for larger projects
- biggest influence on program quality is the skill of the individual writing the program
- Twice as large = 2x more defects

### _27.4 Effect of Project Size on Productivity_
- at small size, only skill of individual makes the code quality better. as projects get bigger, team organization matters more
- 2 ppl for small teams, 3 ppl for large teams
- productivity on small projects can be 2-3 times as high as productivity on large projects

### _27.5 Effect of Project Size on Development Actions_
#### _Activity Proportions and Size_
**construction dominates on small projects but doesn't as much on large projects**
- "more is not better"
- usually do better if u start off small and then scale up for a large project

### _Chapter 23 Project Planning Som Page 669_
planning at 3 stages in project life Cycle
1. proposal stage
2. startup phases
3. periodically through the project

Calculate costs
- biggest cost is usually effort cost
- hardware is relatively cheap
- project plan evolves during development due to changes
- agile still needs plan

#### _23.1 Software pricing_
- "pricing to win": company has an idea of the price that a customer is willing to pay and makes a bid for the contract based on customer's expected price
- advantages for customer and developer. flexible requirements means software reuse. more budget means better planning for future project costs

#### _23.2 Plan-driven development_
Plan-driven development is an approach to where the development process is planned to detail
- problems are that early decisions have to be revised because of changes to the environments in which the software is developed and used.
- In his view, best approach to planning is plan-based and agile-development.

##### Project Plans
1. Introduction
2. Project organization
3. Risk analysis
4. Hardware and software resource requirements
5. Work breakdown
6. Project schedule
7. Monitoring and reporting mechanisms

##### 23.2.2 The planning process
- deliverables are work products that are delivered to your customers
- process enters a loop that terminates when the project is complete
- make realistic rather than optimimstic assumptions of a project plan

#### 23.3 Project scheduling
- both plan-based and agile processes need an initial project schedule
- scheduling in plan-driven projects involves breaking down the total work involved in a project into separate tasks and estimating the time required to complete each task
- max time for each task is 6 to 8 weeks
- a good rule of thumb is to estimate as if nothing will go wrong and then increase your estimate to cover anticipated problems

##### Schedule presentation
1. calendar based bar charts. gannt charts
2. activity networks show dependencies between different activities making up a project

each activity has:
- a duration
- effort estimate
- deadline
- defined endpoint

- Milestones can be multiple tasks
- milestones are short reports that are used for progress reporting, whereas deliverables are more substantial project outputs such as a requirements document or the initial implementation of a system
- if effort exceeds duration, then more than one person is working on it. if effort is smaller than duration, then people are only working part time on it.

#### _23.4 Agile Planning_
Agile methods is iterative approaches where the software is developed and delivered to customers in increments.

2 stage planning:
- release planning
- iteration planning

XP:
- relative ranking of user stories is sometimes more helpful
- effort translated from the stories
- "velocity" = # of effort point put in a day

Iteration planning:
- let developers sign up for the tasks that they made since they know their own velocity
- major difficulty in agile planning is it relies on customer availability

#### _Estimation Techniques_
1. use experience
2. algorithmic cost modeling

- startup estimates have wide margin of error
- problem with experience based technique is that project now is maybe different from one before
- impossible to say which is more accurate

##### algorithmic cost modeling
- formula: effort = A x Size^B x M
- A is constant factor that depends on practices and type of software
- size is code size
- B is complexity of software. usually between 1 and 1.5
- factor that takes into account process attributes such
- SLOC = # of source code lines
- B is exponent because it usually doesn't increase linearly but exponentially with project size
- B and M are subjective. Size is impossible to estimate in beginning because u haven't made decisions that affect size yet.

algorithmic cost modeling is complex. limited to defense and aerospace. another barrier is calibration. not enough data to calibrate.

#### COCOMO cost modeling
- best algorithmic cost modeling

Submodels:
1. application composition model: reuse, simple formula, application points
2. early design model: function points --> SLOC
3. reuse model: used with 4
4. post-architecture model: standard formula, 17 multipliers

23.6.1 application composition model
application points come from
1. \# of web pages displayed
2. \# of reports produced
3. ... page 688

23.6.2 Early design model
- make quick and approximate cost estimate
- A x Size^B x M
- B is increased effort required as size of the project increases

23.6.3 reuse model
- black-box code is code that can be reused without understanding the code or making changes to it like libraries
- white-box: reusable code that has to be adapted to integrate it with new code or other reused components
- same formula: A x Size^B x M
- AAM is estimate of additional effort required to reuse the code

23.6.4 post-architecture level
- most detailed
- SLOC - estimate of total number of lines of new code to be developed
- ESLOC -estimate of reuse costs based on equivalent number of source lines of code

Project staffing:
- adding mroe memebers decreases productivity of existing members

## _Week 7 Monday 05/14/2018 Som 10-14_
### *Chapter 10 Sommerville Dependable Systems Page 289*
Dependability:
- Availability
- Reliability
- Safety
- Security
- Resilience

Security:
- Integrity
- Confidentiality
- Relilability

critical systems need all dependability properties

trade off dependability and performance

cost gets higher as dependability gets higher

#### 10.2 Sociotechnical Systems
View as layers:
1. equipment layer
2. OS
3. communications and data management layer
4. application layer
5. business process layer
6. organizational layer
7. social layer - new law governing access to personal info

each layer can affect another layer. don't have to be the layers next to each other

#### 10.3 Redundancy and Diversity
Redundancy: spare that is used when something fails
diversity: redundant components are different types

- checking code may be redundant
- redundant servers
- don't rely on a single tool to check software: validation requires program testing, manual program inspections, etc.

Cons: Redundancy and Diversity can introduce bugs to the system by making it more complex to handle
Another approach to Redundancy and Diversity is to keep it very simple.
Generall both approaches are used together

#### 10.4 Dependable processes
- good for convincing regulator ur software is dependable
- repeatable processes means reproducable

#### 10.5 Formal methods and dependability
- formal methods are mathematical approaches to software development where you define a formal model of the software
- Advantages: as u make the model, you understand the requirements better. Can find inconsistencies...
- Another approach: refinement-based approach. here, a formal spec is refined through a series of correctness-preserving transformations
- Why ppl don't use formal: not guaranteed cost effective, some problems can't be formally defined, some engineers not trained to do this so not brought up

### _Chapter 11 Reliability Engineering_ page 307
One reason why faults may not lead to system failures is because users may adopt their behavior to not use the faulty part

3 complementary approaches to improve reliability
1. fault avoidance
2. fault detection and correction
3. fault tolerance

As number of residual errors go down, the cost to detect the error goes up. As a result some companies just accept the fault and will deal with it when it arises

#### 11.1 Availability and reliability
reliability - fail free operation probability
availability - probability that a system is operational

reliability may depend on how much of the product is used. some people just use it minimally so ur good

reliability and availability are closely related but sometimes one is more important

#### 11.2 Reliability requirements page 313
Reliability metrics:
1. POFOD
2. ROCOF / MTTF
3. AVAIL

functional vs nonfunction reliabiltiy specification
nonfunctional- use the metrics above

#### 11.3 fault-tolerant architectures
Operations to continue working even after detecting a fault
dependable servers replication
Protection system is a fail safe in case something goes wrong
self-monitoring architecture - needs diversity. good when computations have
to be correct but not availability
TMR-triple modular redudancy is what self-monitoring architectures are based on. if 2 or more things are giving same output then use it
Similar to that N-version programming is just n instead of 3.
Software diversity-have 2 teams do the same thing so that the result is diverse. to guarantee this, make them use different approaches

#### 11.4 Programming for reliability

...Rest...

## _Week 7 Monday 05/16/2018 McConnell 23-26, 31 Som 9_
### _Chapter 23 Debugging_
- Debugging is diagnosing defects.
- 20-to-1 difference in the time it takes experienced programmers to find the same set of defects found by an inexperienced progreammer
- General Principle of Software Quality: improving quality reduces development costs
- Assume the error is your fault, this helps you debug
- debugging similar to scientific method
- brute force debugging: perform full design on broken code, or throw away section of code and redesign it, etc.
- understand problem before you fix it
- set compiler warning level to highest
- treat warnings as errors
- use debuggers. he likes em

### _Chapter 24 Refactoring_
- can't just duct tape
- cardinal rule of software evolution: evolution should improve the internal quality of the program. way to ahiveve
- "tramp data" - passing data to one routine so that routine can pass it to another routine. Bad
### _Chapter 25 Code Tuning_
- performance loosely related to code speed
- can do efficiency in the long run
- Pareto Principle: you can get 80% of the result with 20% of the effort. in other words, 20% of the program's routines consume 80% of its execution time
- Reducing lines of code doesn't make it faster
- certain operations are probably faster or smaller than others. false
- you should optimize as you go. false
- a fast program is just as important as a correct one. false

Common sources of inefficiency:
- input/output operations
- paging
- interpreted languages like python are 100x slower
- errors

Measurement:
- experience doesn't help optimization
### _Chapter 25 Code Tuning Techniques_
- Loop unrolling and loop unswitching
- if else vs case statements. differ between languages
- jamming: fuse 2 loops
- sentinel values - value u put just past the end of the search range that guarantees termination of the search
- minimize work inside loops
- User int's not float's
- minimize array references
- caching
- strength reduction: use add instead of mult
- be wary of system routines

## _Week 8 Monday 5/21/2018 Mc 30, Som 27_
### McConnell 30
- 20% of tools are used 80% of the time
- Design tools - UML, architecture block diagram, hierarchy charts, etc.
- Diff tools
- Merge Tools
- Source Code Beautifiers
- Data Dictionary
- Compilers and Linkers
- execution profilers
- assembler

##_Week 8 Wednesday Mc 32, Som 29,30_
### Chapter 32 McConnell
- On large, formal projects, most of the documentation is outside the source code
- SDF(Software Development folder ) or UDF(Unit development folder) is an Informaldocument that contains notes used by a developer during construction. Unit is loosely defined.
- detailed design document is the low level design document. describes class-level stuff
- Holy Grail of legibility: self-documenting code. The code is so well written you can read it basically.

#### 32.3 To Comment or Not to Comment
- To not waste time, write the pseudocode in the comments otherwise its a waste of time.
- You can just change your code to be more readable.
- Code reviews can help establish good practice
- Poor comments are worse than no comments

Kinds of Comments
- Repeat the code
- explanation of the code. almost always better to improve the code than it is to add comments
- Marker comments ****** or !!!!!! Want standard way of marking code that needs to be fixed
- Summary of the code. Valuable!
- Decription of Code's Intent
- some stuff like copyright stuff can be commented inside too

Why commenting may be hard:
1. ur commenting style sucks
2. can't find words to describe the routine. in that case, understand what you are doing better.

Pseudocode Programming Process to reduce commenting time
- outline the code in comments before you write it

Leave commenting towards the end? bad
- takes more time to remember what you wrote
- less accurate

Performance is not good reason to avoid commenting

Optimal amount of commenting:
1 comment per 10 lines

#### 32.5 commenting techniques
- don't comment individual lines unless really need to explain or its an error

Endline comments:
1. cryptic
2. hard to maintain

When to use Endline Comments:
1. Annotate data declarations

    Ex: int boundary = 0; //upper index of sorted part of array

2. no maintenance notes
3. use it to mark ends of blocks

Key point: focus ur documentation efforts on your code itself

- Major vs minor comments: Use ellipsis in front of minor
- Justify violations of good programming
- put comment before block of statements
- comment end of control structures
- treat end-of-loop comments as warning indicating complicated code
- Problem with commenting large blocks on routines is that they discourage good factoring of code
- Describe the routine only in 1 or 2 sentences
- Document parameters where they are declared
- differentiate input and ouput data
- Put name and claim authorship of each block

### Sommerville 29 Interaction Design
Bad UI makes people not want to use something or use it wrongly
Humans factors in interface design:
1. limited short term memory
2. people are different some like text vs pictures

User interface design principles
1. familiarity
2. consistency
3. minimal surprises
4. recoverability - confirm, undo, checkpoint possibilities
5. user guidance
6. user diversity

1 and 2 can conflict. notion of Universal Design: avoid excluding any users because bad design

Interaction Styles:
1. direct manipulation -
2. menu selection
3. form fill-in
4. command language
5. natural language

LIBSYS interaction:
Document search and Document request

MVC approach is a way of supporting multiple presentations of data

Information presentation
Static vs dynamic information: static is initialised at the beginning of a session and doesn't change. dynamic changes during a session and the changes must be communicated to the system user.

Information display facotrs:
1. is the user interested in precise information or data relatinoships
2. textual vs numeric? relative numbers important?
3. ...

Digital vs Analog presentation: Digital is compact - takes little screen space, and precise values are communivated. analog u just give a glance, show relative numbers and see outliers

Common mistakes in using color in interface design is
- over use of color or use color to communicate meaning

UI design process:
1. User analysis - know what user wants to do
  1. HTA (Hiearchial Task Analysis): high level task broken down into sub tasks. Best suited for sequential tasks not concurrent
  2. HTA is good with natural language scenarios since it forces to not miss anything
  3. ethnography, interview
  4. none of these are complete ways to know what a user wants
2. system prototyping - make
  1. 2 stages: 1. paper prototyping 2. make
  2. storyboard - illustration of sequence of interactions
3. interface evaluation - test
  1. full scale evaluation is expensive.

Usability attributes:
1. learnability - how long does it take to learn the ui
2. speed of operation
3. robustness - tolerance of user error
4. recoverability - recovering from system error
5. adaptability


### Sommerville 30
Documentation starts before development
1. process documentation - plans, schedules, ...
2. product documentation - used after development. describes product beign developed

agile don't like documentation; takes too long

critical systems need not only documentation on system design but the rationale of how you made the system as well. Makes refactoring easier

Process documentation:
1. Plans
2. reports
3. Standards
4. ...
- becomes outdated. agile dont like
- some process documents help with evolution and replanning
- reduce amount of process documentation with weekly meetings

Product documentation
- has long life unlike process documentation
- End users vs system administrators: End-users just want to use the software. administrators manage the software
- several documents for ppl of different level of expertise
- if you cut product documentation, they lack 'browsability'. hard to find features that they want exactly. Also problem like they are feature oriented rather than problem-oriented.

System documentation
-small system, less documentation
-often neglected documentation maintenance

Document quality
Document structure: IEEE standard
Good writing style

Documentation Standards
1. process Standards - define approach to be taken in producing documents
2. product Standards - look it up
3. interchange standards - electronic copies how to be compatible. usually pdf

document production
1. creation
2. polishing
3. production

- problem with programming text editors is that you have to download a package to know what the preview looks like
- desktop publishing systems(DTP) like quark xpress scan stuff
- adv of publishing system is that the cost of producting high quality documents is decresed.
- disadv is that they do not automate the skills of the graphic designer
- online documentation advantages is accessibiltiy but lack browsability

....


##_Week 9 Wednesday Mc 33-35, Som 15, 26_

### McConnell 33 Personal Character
- Improvement in character has shown that the differences are on an order of 10 to 1 in speed, debugging, etc.
- no ego
- build awareness of development process
- experiment
### McConnell 34 Personal Character
- how stable your requirements have to be is up to u
- premature optimization is an error
- write programs for people first, computers second
- even if you think you are the only one reading your code, good chance you're not . One study, found that 10 generations of maintenance programmers work on an average program before it gets rewritten.
- Program in a way that maintains abstraction
- write your own assert routines
- Prohibit potential hazard by eliminating any global variables
- Conventions can help with language weaknesses,
- Work at the highest possible level of abstraction.
- Design metrics: A class with 7 member maybe a sign of bad desgin but it is definitely complicated
- Single most common cause of not finding errors was simply overlooking them. Make it hard to overlook
- Software design is heuristic process, subejct to iteration and revisions
- User mixture of methods. don't just use the latest  fad. Be eclectic

### McConnell 35 Where to Find More Information
Nope

### Sommerville 15 Software Reuse
1. System reuse
2. Application reuse
3. Component reuse
4. Object and funciton reuse

- design pattern is equal to concept reuse
- obvious advantage: cost is lower
- There is cost of knowing whether a component can be reused
- Another prob: Maintaing costs will be higher and "not invented here" syndrome

Key factors for planning reuse:
1. development schedule for the software
2. Expected software lifetime
3. The bacground, skills and experoence of the development team
4. The criticality of the software and its non-function requirements - Hard to create a security case when you didn't write the source code.
   Makes model-driven engineering impossible since MDE relies on generating code from a reusable domain-specific model of a system

- Managers may not know the risks of doing original development and don't want to trust the unknown.
- Framework provides skeleton architecture  for the application.
- Frameworks are language specific since they are implemented as a collection of concerete and abstract object classes in an object-oriented programming language.
- Most widely used application frameworks are webapplication frameworks
- MVC pattern includes the Observer pattern, the Strategy pattern , the Composite pattern.
- "callbacks" are methods that are called in reponse to events recognized by the framework
- "hook methods" are the same thing but they are linked to user functionality

3 Classes of Framework:
1. System infrastructure frameworks
2. Middleware integration frameworks
3. Enterprise application frameworks

- Frameworks are expensive to introduce inot software development processes as they are inherently complex and it can take several months to learn to use them.

Software product line is just the base of a software. or the corre.
- Engineers learn about the application domain through the software product line so become specialists who can work quckly to develop new applications.
- Software product lines usually emerge from existing applications.

Applications frameworks and software product lines have much in comon. The both support a common architecture and components and require new development to create a specific version of a system
Differences:
1. Application frameworks rely on object-oriented features such as inheritance to implement extensions. Framework is usually not modified
2. application frameworks provide general support rather than domain-specific support
3. software product lines are often controla pplications for equipment
4. software product lines are made of a family of applications

Specializations of software product line:
1. Platform
2. environment
3. functionality
4. processes

Software product lines are designed to be reconfigurable

Design-time configuration vs deployment-time configuration
- design-time configuration is used when it is impossible to use the existing deployment-time configuration facilities in a system to develop a new system version

COTS are applications system that are developed for an individual customer
configurable application systems are generic application systems that may be designed to support a particular business type, activity, or enterprise...
ERP - large-scale integrated systems designed  to support business practices such as orderin, invoicing, ...
CRM - customer relationship management

Integrated application systems include two or more applications systems or legacy systems

##_Week 10 Monday Som 21_
- top down approach is impractical for real-time systems
- responsiveness in real-time is the critical difference between embedded systems and other software systems
- in real-time system correctness depends on the output and the timing
- use shared buffer and mutual exclusion to avoid problem of processes running at different speeds
- producer of information and consumer of information processes
- can't access buffer at same time. semaphores and critical regions
- state models are used to describe real time systems
- C is fast but doesn't support concurrency
- timing constraints may not be able to use OOP for hard real-time systems
- difference between real-time and interactive software means that there are distinct architectural patterns for real-time embedded systems
- common real-time architectural patterns: Observe and React, Environmental Control,Process Pipeline
- Not design templates or else you'll end up being inefficient
- soft-real time means no stringent requirements on timing
- most widespread is control systems
- Environment control is used when user intervention is not requireed or where ethe rate of control is so high that a display would not be meaningful
- Process pipeline is moving data in sequence from one end of pipeline to another
- high speed data acquisition system uses process pipeline. used in scientific experiments
- many systems only use periodic system
- key factors in timing: deadlines, frequency, execution time = time required to process stimuli and produce response
- Windows and linux not designed to allow fine grain control of processes so they are not used as execution platform for real-time systems.
- bare-metal systems are used and built on top of RTOS
- RTOS has to manage 2 priority levels: clock level and interrupt level which is the highest priortiy level
- a further priority level may be allocated to background processes
- preemptive vs non preemptive 
