What is Unit Testing?
===
- all about proving correctness
  - to prove it works, must know what is a unit and what is a test

What is a Unit?
---
- Pure Unit
  - easiest and most ideal method for writing a unit test
  - unit is a function (method) that does something without calling other methods
  - a unit should not call other methods
    - sometimes this is unavoidable, but if it is avoidable don't do it
  - a unit should do only one thing
  - a unit should not have multiple code paths
    - again it may be unavoidable, but don't do it otherwise
    - a unit will not have any if or switch statements.  The body of these statements should become units
- Dependent Units
  - functions with dependencies on other classes, data, and state information
    - dependencies translate into requirements for instantiated objects, existence of data, and predetermined state
  - have preconditions that must be met
    - often times a virtual base class or something is helpful to instantiate test classes
  - dependent units are more fragile
    - may need to handle errors from functions they call
    - unit tests must be capable of simulating the errors or exceptions to ensure all code paths are executed correctly, including catch and finally blocks

What is a test?
---
- provides a useful assertion of the correctness of the unit.
  - usually in two ways
    - test how the unit behaves under normal conditions
    - test how the unit behaves under abnormal conditions

Normal Conditions testing
---
- easiest test to write
  - test the result of the function given expected inptus, whether the result of the function is a return value or a state change.
  - if the unit depends on another function or service, the test is written assuming that function or service behaved correctly

Abnormal conditions testing
---
- difficult
- must determine what the abnormal condition is (not usually obvious by inspecting the code)
- made more complicated by dependent units
- we don't know how another programmer or user might exercise the unit

Unit Tests and Other Testing Practices
---
- does not replace other testing practices
  - complements, providing additional documentation support and confidence
- other models
  - V-model of software development and testing process
    - gives good picture of what kind of testing is required for each layer of the software development process
  - waterfall model of software development (apparently the base for all other software development models)

Acceptance Test Procedures (ATP)
---
- often used as contractual requirement to prove certain functionality has been implemented
- often associated with milestones
  - milestones are often associated with payments or further project funding
- differs from a unit test because ATP demonstrates the functionality with respect to whole line-item requirement that has been implemented.
  - unit test might prove the computation works
  - ATP proves that the requirement that the computation is displayed correctly to the UI maybe.  This isn't covered by a unit test

Automated User Interface Testing
---
- I'm not sure what to write here

Usability and User Experience Testing
---
- put the application in front of users and get the UX feedback
- usability testing is not about finding bugs so it has little or nothing to do with unit tests

Performance and Load Testing
---
- measures the performance of a function, like setting execution time limits etc
- .NET languages should explicitly implement performance testing to compensate for JIT compilation the first time the code is executed.
- load tests are not suitable for unit tests, usually, but some forms of load tests can be done with unit testing
  - simulating memory constraints
  - simulating resource constraints
  -these require framework or OS API to simulate these loads for the tested application, and this affects everything.  Not desirable