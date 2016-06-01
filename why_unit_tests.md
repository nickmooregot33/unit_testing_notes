Why Unit Tests 
===
- To prove correctness
  - only happens if the unit tests are written well
  - any side effect to unit testing in the dev process must be balanced with the effort of writing and maintaining useful unit tests
- testing methods not replaced by unit tests (look these methods up as well)
  - usability testing
  - performance testing
  - load testing
  - acceptance tests (ATPs)
  - System Integration Tests
  - more


Measuring Correctness
---
- unit tests allow the degree of confidence in correct application behavior to be quantified
  - Simplest way is a coverage test
      - what percentage of the app's methods have unit tests written against them?
  - Can measure how many bugs the app has because of incomplete unit test coverage
- Unit testing is iterative (there will always be bugs)
  - can measure how many unit tests you've written against reported bugs as compared to the total number of unit tests.

Repetition
---
- regression testing
  - unit tests are written against methods as they are written and added for bugs as they are reported, all of the unit tests can be retested automatically at every change to the source, reducing testing time for modified applications

Code Coverage
---
- most useful unit tests test every single code branch that occurs in the function
