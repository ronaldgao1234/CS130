# Notes for Lecture Eggert Spring 2018

> A lot is mainly taken from lanqingwei's notes on github:
> https://raw.githubusercontent.com/lanqingwei/ucla-notes/master/cs130-eggert

## Lecture 1 March 28
What is software and why is it different?
1. Easy to change
2. Don't need to worry about manufacturing
3. Won't wear out
  - hardware failure rate (bathtub curve)
    1. break-in period: not manufactured correctly
    2. wear out: finally breaks down because of time

  - software failure rate (spikey bathtub curve)
    1. increases failure rate with each new release
    2. decreases failure rate as bugs get fixed
    3. failure rate increases overall as software gets bigger

<img src="https://www.researchgate.net/profile/Wonkeun_Youn/publication/261599262/figure/fig1/AS:296653320933376@1447739071318/Software-and-hardware-failure-rates.png" width=300 height=300>

4. No spare parts
  1. if program crashes, replacing with same new copy will not fix it
    - can revert to older version
    - use alternative


    software engineering    vs.        computer science
    =====================================================
    practical problems of            theory & methods that
     producing software               underly programs

    software engineering    vs.      system engineering
    =====================================================
    just software plus       software, hardware, firmware
     human interface                    process design
                                        policy
## Lecture 2 March 30
Just presentations
## Discussion 1 April 1
nothing
## Lecture 3 April 4
nothing
## Lecture 4 April 6
===============================
Why do we need requirements?
-----------------------------
* developers != users
* legal, contract reasons
* reliability/safety is crucial
* security (tricy in practice)

How much work to put into requirements?
How long/big is the requirements document?
-------------------------------------------
it dependes on the project
the more of the above required, the longer it will get


* one of the most common requirements document problem is that customers would
not want to read the long and obvious document because they are specifying
what the customers already know.


Requirement Engineering
------------------------
applying sound engineering principles to come up with requirements documents

                     requirements
    stakeholders <---------+--------> design
                           |
    - everybody who        |
    cares about            |
    the software           |
    - users/managers       |
                           |
    system model <---------+

    - in developers' heads


Good Requirements
------------------

- are testable (once system is implemented)
  ideally would want to make it quantifiable
  realistically turn it from something vague to something less vague
  "build a system where the UI is userfriendly"
    this is not testable
    change to something testable
    we could test them on users

- are feasible (in the indented environment)
  make sure requirements are actually doable
  do not make NP-complete requirements

- don't conflict with each other
  conflict are not obvious
  come from different parts of the requirements document
  gathered from different parts of the customer organization
  inconsistent requirements documents arise with conflicting user intentions
  conflicts may not be obvious and may reflect conflicts among users

- are attributed (to specific source)
  can go to any requirement in document and see who is responsible
  each requirement should be attributed to specific source
  should know who to ask if there is a problem in the requirements

- are bounded
  do not want to have requirement that is infinitely hard to satisfy
  should know when the requirements are satisfied
  "as fast as possible"
  do not want software engineers to develop "forever"

- are unambiguous
  ambiguous: so few requirements or so poorly stated so that they can be
             interpreted in many different ways
  should avoid the ambiguity (English is ambiguous)
  need somthing functional

- are essential
  Aristotle: get at heart/core of the story
             find out what really matters
             this is called the "essence"
  good requirements should focus on the essential part of the application
  and not trivial details

- are specified at the user level
  write in natural language that the user understands
  do not write in code-like languages such as Java, C, Shell Script

- match the system's vision
  when you try to change the world with your application, you should know what
  the world looks like after your application

- are prioritized
  an elaboration of "are essential"
  some requirements are more important than others
  in practice, some requirements conflict, but priority specifies direction

- are validated
  requirements are checked
  feasible: done a feasibility analysis
  unambiguous: gone through whole document and checked for ambiguity
  validated: we have to validate the validation process


Types of Requirements
----------------------

(A) functional
    what the software does
    behavior of software
    get support from customers about funcitonal requirements

(B) nonfunctional
    other constraints on system that are less obvious because they do not
    initially seem to have anything to do with what software does
      security
      reliability
      performance

(A) user
    imposed on system by end-users of application
    will be able to look at user applicaiton and verify

(B) system
    more detailed
    more peopled are affected here
    audience is people that want to make sure system work
      developer
      operation staff
      finance
      managers


Phases of Requirements Development
-----------------------------------

(1) inception

    some things may sound obvious but are easily done incorrectly or not done

    (a) identify stakeholders & their viewpoints
        stakeholders may not want to talk to you
          e.g. prisoners in prison
        have to indentify everyone who have something to do with the project

    (b) find agreements & disagreements
        get a good feeling on everybody who are using the system
        may have completely different opinions between departments

    (c) break the ice by asking "dumb questions"
        context free questions
        indicate that you don't understand the field
        need humility
        ask "dumb questions":
          about goals and benefits (need to know why)
            "how are you going to make money with this?"
          about the problem
          about communication activity itself
            "did I ask all questions?"
            "are there any questions I have left out?"

(2) discovery/elicitation

    (a) use a well-defined procedure
        - have meetings with agendas & prepare for the meetings
          specialized training -> requirement facilitators (bridge gaps)
        - define problems, pieces of solutions, in user-oriented way
        - write everything down
        - iterate -> multiple meetings
          come up with draft document

    (b) produce
        - scope of requirement
          specify boundary of what to do and what not to do
        - feasibility analysis
          show that requirement is feasible in document
        - justificaiton of need
          why the requirement is needed
        - stakeholder list
          characterization of stakeholders & their viewpoints
        - environment characteristics
          what the system will operate in
          where the system will be running
        - use cases
          little scenarios of where the system will be used
        - constraints
          any sort of extra high-level constraints that are not obvious
        - prototypes
          actually write some code as part of requirements discovery
          may build end-to-end prototypes
          tend to justify feasibility
          "initial testing"

    (c) software requirements document (IEEE standard for requirements)
        contains
          - glossary
            standard nomenclature for problem
          - user requirements
            "normal" requirements
          - high-level system architecture
            document understanding of system model
          - system requirements
            stated in terms of high-level system architecture
          - system models
          - system evolution
            potential changes to the requirements

(3) negotiation

    come up with too many requirements and can't satisfy
    ideally they are prioritized but practically not that easy
    so we have to negotiate with clients

    - want win-win situation
    - key role of written requirements

(4) validation

    list of things we want out of requirements
    check consistency, completeness, etc.

    via. reviews
         prototypes (little programs to test)
         test cases

## Lecture 5 April 11
============================================
test driven development
buggy spec, if we explore all possible test cases, we can fill in the spec
test debug the spec before writing the code
it is simpler to write tests than writing code
now we can find the bugs in our spec faster

do you use test driven development?
we don't always practice what we preach. - Paul Eggert, Ph.D

if we have real-time constraints, this needs plan driven development
safety systems also requires plan driven development

the development team gets bigger and more parts of the software are not under
your control, and you can't continuously integrate.


goals of software engineering
------------------------------
(1) understand your problem
    much of the software engineering activity is devoted to finding the
    problem that we are trying to solve, which is easiest to get wrong

(2) design is crucial
    design better be there when we are done
    we should know how the software was designed

(3) quality
    software should always be high-quality

(4) maintainability
    software has to be something that we can fix, improve, refactor

(5) work across a lot of domains
    shouldn't be good for just one thing (web, realtime, embedded, system apps)


software engineering principles (Hooker)
-----------------------------------------
(1) provide value to users
    not always obvious

(2) keep it simple stupid (KISS)
    when in doubt, use the simpler approach
    keep code as simple as possible

(3) have an architectural vision
    don't just look at little picture

(4) plan to get hit by a bus
    do not assume that your software project will have you on it
    other peoples may take over it
    somebody else may be maintaining your project
    if it's important, always write it down
    be ready to be replaced

(5) be ready to change
    designing and building software should not be like building the pyramid
    it should be able to mutated

(6) plan for reuse
    when you build your code, assume that it will be successful and you
    or other people will reuse the current code
    write code that can be reused in other systems

(7) THINK before doing
    don't just code because it feels good to type keystrokes
    think before you build the code, before it's too late

Sommerville likes 1,4,6, and

(8) worry about dependability and performance
    obvious yet important
    when you worry about dependability and performance, you are bringing to
    the table software engineering strength


Developers             Managers
------------------------------------------------------
I wanna code           ensure it does what user wants
McConnell              Sommerville

programming
textbooks
S.E. theory


software construction
----------------------

        problem definition                 corrective maintenance
        requirements definition
      --------------------------------------------------------------
                                  detailed design

      construction planning          coding          integration

                  unit testing     integration testing
      --------------------------------------------------------------
              software architecture            system testing

(1) get your prerequisites right
Plan to throw it away; you will anyhow - F. Brooks
McConnel disagrees and thinks that we should make code work
software is not authored in the usual way
software is edited (like an encyclopedia)
don't plan to throw the whole thing away

collarborative development
---------------------------
(1) focus on cost-effective defect-detection
    bugs will be the normal way of life
    will spending more time fixing defects than writing code
    reduce # of defects as many as possible

(2) collarborative practices do best on defects resistant to traditional tests
    can you break up the project


pair programming
-----------------
pay 2 people's salaries to write one program
  one programmer K has the keyboard and the house
  one programmer J just kibitzes
    find errors quickly, early when they are cheap to fix
    if we wait to review, the cost goes up
    reduces defect removal tests
    have immediate feedback
    back-and-forth is fast
    requires 2 bus hits

guidelines

(1) match pairs
    makes sure the two people are comfortable around each other

(2) rotate
    switch roles

(3) Keyboard = tactics
    Kibitzer = strategy

(4) don't let the kibitzer relax
    make pair programming sessions short

(5) don't use it for everything
    not all things are suited for pair programming


formal inspection
------------------
gold standard for software review (IBM)

(1) focus on defect detection not correction
    formal inspections are expensive
    hard part is mostly finding bugs
    so focus on hard part

(2) use a checklist to focus reviewers' attention
    use different checklists and measure how well each checklist performs
    checklist will depend on problem domain

(3) reviewers prepare for meetings
    have multiple reviewers for reviewing system
    give code ahead of time to read independently and come up with questions
    in the meeting, combine the reviews, big merge of question list

(4) all participants have roles
    moderator: requires most training, competent to organize reviewers
    scribe: keep track of what is set
    reviewers (2-5): reviews the code
    author: usually doesn't participate, but also nice to have there
    managers are not participants, inefficient

(5) time and efficiency
    100-500 lines/hour
    < 2 hours/meeting
    code reviews are very expensive


code walk-through
------------------
code readign
demos (dog & pony)
"demo or die"


software process
-----------------
the set of heuristics
developers' heads (extreme approach)

(lisp (code))
lisp code in which developers are subroutines
this doesn't work

framework for what goes on in developers' heads
dynamic perspective - phases, in some sequence
  communications (requirements)/planning/modeling/construction/deployment
practice perspective (umbrella activities)
  - quality assurance
  - reviews
  - configuration management (how system/requirements are configured)
  - project tracking (keep track of what's done/not done)


plan driven vs. agile approach
