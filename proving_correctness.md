Proving Correctness
===
- outside of unit testing,"proving correctness" normall is in the context of veracity of a computation
- regarding unit testing there are 3 broad categories in "proving correctness"
  - verifying inputs to a computation are correct
  - verifying a function call results in the desired result (computational aspect), in 4 typical processes:
    - data transformation
    - data reduction
    - state change
    - state correctness
  - external error handling and recovery

How Unit tests prove Correctness
---
- proving correctness involves
  - verifying the contract
  - verifying the computational results
  - verifying data transformation results
  - verifying external errors are handled correctly

Prove Contract is implemented
---
- most basic form of unit testing
- verify a developer has written a method that clearly states the contract between the caller and the method being called
- usually means the test verifies that bad inputs to a function results in an exception being thrown.
- one of the weakest unit tests that can be done

Prove Computational Results
---
- stronger than verifying contract
- categorize the functions into 3 forms of computation
  - data reduction
  - data transformation
  - state change
- Data Reduction 
  - using assert statements
  - example as a division function (takes two arguments and returns one)
  - simplest form of USEFUL unit testing
- Data Transformation
  - tend to operate on sets of values
  - still using assertions
  - list transformations
    - separate list transformations into 2 tests
      - verify the core transformation is correct
      - verify the list operation is correct
      - the example was confusing.  I'm not sure what they were arguing
- State Change
  - classes often keep track of state (with bools etc)
  - these test whether the state actually is the correct state in various situations

Prove a Method Correctly Handles an External Exception
---
