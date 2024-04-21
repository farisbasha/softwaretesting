# Part A
## 1.Define Prime Path Coverage?
- Prime Path Coverage is a testing approach where all unique paths through a program's control flow graph, called prime paths, are tested at least once. It ensures comprehensive testing by covering every statement in the program exactly once.

- According to prime path coverage(PPC), each prime path must be covered in test requirements.
- **! (Exclamation Mark)**: Marks the final node or endpoint of a path.
  
- **\* (Asterisk)**: Denotes a loop or cycle in the path.



## 2.What is a Control Flow Graph (CFG) in the context of source code?

A Control Flow Graph (CFG) in the context of source code:


<img width="200" alt="Screenshot 2024-04-21 at 5 04 19 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/2c92703b-8c3b-440c-b3d9-61ec808455a6">

- Graphical representation of a program's control flow.
- Nodes represent basic blocks of code.
- Edges depict the flow of control between these blocks.
- Helps analyze program structure and identify possible execution paths.
- Used in software testing to devise test cases and ensure code coverage.



## 3.Differentiate between interface-based and functionality-based approaches input domain modelling?

| Aspect                   | Interface-based                             | Functionality-based                           |
|--------------------------|---------------------------------------------|----------------------------------------------|
| Focus                    | External behavior visible to users         | Internal operations and logic                |
| Representation           | Models inputs/outputs without implementation | Models inputs, outputs, and internal processing |
| Design Considerations    | Emphasizes defining interfaces and contracts | Considers behavior, states, and transitions |
| Testing                  | Suitable for black-box testing             | Supports both black-box and white-box testing |
| Flexibility              | Easy changes to internal implementation    | May require more modifications for interface changes |
| Maintenance              | Easier due to clear interface boundaries  | Involves understanding internal logic       |

## 4.Write a short note on Black box testing?

- Tests the functionality of software without knowing its internal code structure.
- Focuses solely on the inputs and outputs of the software.
- Test cases are derived from specifications and requirements.
- Emphasizes user perspective and behavior.
- Helps ensure that software meets expected functionality.
- Can uncover issues related to usability, performance, and interoperability.

## 5.Describe the difference between pairwise coverage and T wise coverage testing techniques.
| Aspect           | Pairwise Coverage                               | T-wise Coverage                                  |
|------------------|--------------------------------------------------|--------------------------------------------------|
| Definition       | Covers all combinations of any two parameters.  | Covers all combinations of any t parameters.    |
| Example          | For any two parameters, all value combinations are covered. | For any t parameters, all value combinations are covered. |
| Specificity      | Focuses on pairs of parameters.                  | Can be tailored to cover any number of parameters together. |
| Generalization   | A special case of T-wise coverage where T equals 2. | Encompasses all lower-order combinations, including pairwise coverage. |
| Application      | Suitable for reducing the number of test cases while maintaining adequate coverage. | Offers flexibility to balance coverage and test suite size based on specific testing requirements. |


# Part B

## 6.Explain the concept of Complete Path Coverage. How does it contribute to thorough testing of software? Illustrate with an example. ?
<img width="775" alt="Screenshot 2024-04-21 at 5 20 22 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/db745e4f-e3c6-4a5b-ad63-cfe3565e6ae1">

> CPC is impossible for graph containing loops
- **Definition**: Ensures that every possible path through the software's control flow graph is executed at least once during testing.
- **Coverage**: Includes all feasible paths, including loops, conditionals, and exception handling.
- **Thoroughness**: Provides the highest level of coverage, leaving no untested paths.
- **Complexity**: Can be impractical for large or complex software due to the exponential growth of possible paths.
- **Assurance**: Offers confidence that all paths have been exercised, minimizing the risk of undiscovered defects.
- **Verification**: Validates that the software behaves as expected under all possible scenarios, enhancing reliability and robustness.

## 7.Discuss the significance of Call graphs and classes in Graph Coverage for Design Elements. How can they be utilised to improve test coverage and effectiveness?
Significance of Call Graphs and Classes:

- **Call Graphs**: 
  - Visualize method relationships and code flow.
  - Identify dependencies and invocation paths.

- **Classes**: 
  - Encapsulate related methods and attributes.
  - Promote modularity and code reuse.

Utilization for Improved Testing:

- **Identifying Critical Paths**:
  - Prioritize testing on critical paths.

- **Testing Integration Points**:
  - Validate interactions between classes.

- **Detecting Dependencies**:
  - Ensure changes in one class don't impact others.

- **Scenario-based Testing**:
  - Cover various usage patterns.

- **Refactoring and Optimization**:
  - Streamline testing efforts based on insights.



### **Example: FileADT Class**:
  - Methods: open(), close(), write().
  - Sequencing Constraints:
    - open() must precede every write().
    - open() must precede every close().
    - write() should precede every close().


  - **Use of "Must" and "Should"**:
    - "Must" implies violation is a fault.
    - "Should" implies violation is a potential fault, but not necessarily.
    
  <img width="214" alt="Screenshot 2024-04-21 at 5 35 40 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/d3e260b8-6923-439f-aa88-5e120ac63795">

  
  Above CFGs represent two units that use FileADT. We can use this graph to test the use of the FileADT class by checking for sequence viola


## 8.Draw CFG fragment for (i) Simple if (ii) Switch-case (iii) Simple loop
![untitled](https://github.com/farisbasha/softwaretesting/assets/72191505/2557ec00-4722-4ff3-9757-b008def13eff)



### i) Simple if
<img width="350" alt="Screenshot 2024-04-21 at 5 42 30 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/aa9b619a-36b5-4fee-896a-9adc0e50f3a8">


### ii) Switch-case

<img width="350" alt="Screenshot 2024-04-21 at 5 43 25 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/3461191e-6516-4302-a10b-f9f49c9e435f">

> NOTE: You can use any simple program , this is just an example
### iii) Simple Loop

<img width="350" alt="Screenshot 2024-04-21 at 5 44 26 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/49776d53-833d-4a36-9d41-b7c24bf7e9b3">

> NOTE: You can use any simple program , this is just an example



## 9.Compare and contrast ACoC and ECC testing techniques. Provide insights into where each technique would be more appropriate to use
### Skip if possible 😮‍💨
> A very short simple answer for this is question

| Aspect               | ACoC Testing                                     | ECC Testing                                   |
|----------------------|--------------------------------------------------|-----------------------------------------------|
| Methodology          | Systematic, covering all combinations            | Ad hoc, focusing on likely error-prone areas |
| Coverage             | Exhaustive                                       | Non-exhaustive                                |
| Suitability          | Critical systems with complex interactions      | Quick identification of potential faults      |
| Efficiency           | Resource-intensive                               | Generally more efficient                      |
| Risk Mitigation      | Mitigates risks associated with complex interactions | Identifies and addresses risks early       |
| Complexity           | Can be complex for systems with numerous input categories | Generally less complex                  |
| Time                | Time-consuming due to exhaustive nature       | Typically faster due to less exhaustive approach  |


## 10.Describe Computation error and Domain error using examples.

| Aspect       | Computation Error                                          | Domain Error                                    |
|--------------------|------------------------------------------------------------|-------------------------------------------------|
| Definition         | A computation error occurs when a specific input data causes the correct path to execute, but the output value is wrong. | A domain error occurs when a specific input data causes the program to execute a wrong (i.e. undesired) path |
| Example            | Adding 0.1 and 0.2 in a programming language results in 0.30000000000000004 due to floating-point precision issues. | Attempting to calculate the square root of a negative number. |
| Cause              | Faulty implementation, algorithmic mistakes, or rounding errors. | Input values violating constraints or assumptions. |
| Impact             | Results in incorrect output or unexpected behavior.         | Causes program crashes or undefined behavior.   |
| Detection          | Detected during testing or validation of computations.     | Detected through boundary checking or input validation. |
| Resolution         | Requires debugging, code review, or algorithm refinement.  | Handling through input validation or error handling mechanisms. |
| Additional Types   | Overflow Error , Underflow Error                                           | Closed boundary, Open boundary, Closed domain, Open domain   |



## 11.What is the importance of Input Domain Modelling (IDM) and what are its approaches?
Importance of Input Domain Modelling (IDM) and its Approaches:

- **Definition**: IDM defines the scope of possible inputs to a program, encompassing all potential values and ranges that input parameters may take.

- **Importance**:
  - Defines all possible inputs to a program.
  - Facilitates finite set selection for testing.
  - Essential for comprehensive test coverage.
  - Guides testers in selecting representative input values, ensuring thorough testing of various scenarios.
  - Assists in identifying boundary conditions and edge cases
  - Enables efficient allocation of testing resources by focusing efforts on areas with the highest impact on system behavior.


| Approach                      | Interface-Based                                       | Functionality-Based                                   |
|-------------------------------|--------------------------------------------------------|------------------------------------------------------|
| Definition                    | Derive characteristics directly from input parameters. | Derive characteristics from the behavior of the system. |
| Focus                         | Individual input parameters.                           | Overall behavior and functionality of the system.     |
| Characteristics               | Based on properties of input domains.                  | Based on expected behavior of the system under test.  |
| Example                       | Partitioning input parameter regions (e.g., null, empty). | Analyzing system behavior (e.g., occurrences of elements in a list). |
| Usage                         | Suitable for understanding input parameter properties. | Ideal for comprehending and testing system behavior.  |


## 12.What is the "Triangle Classification Problem" or "TriTyp Problem," and what are the key aspects involved in solving it?

The Triangle Classification Problem, also known as the TriTyp Problem, involves determining the type of triangle based on the lengths of its sides
The triangle problem is the most widely used example in software testing literature

- **Problem Statement**: Given three integers \(a\), \(b\), and \(c\) representing the sides of a triangle, determine the type of triangle or if it's not a triangle based on specific conditions.

- **Inputs**:
  - Integers \(a\), \(b\), and \(c\) representing the sides of the triangle.
  - Conditions:
    - $\(1 \leq a \leq 200\)$
    - $\(1 \leq b \leq 200\)$
    - $\(1 \leq c \leq 200\)$
    - $\(a < b + c\)$
    - $\(b < a + c\)$
    - $\(c < a + b\)$

- **Outputs**:
  - If any input value fails conditions \(c1\), \(c2\), or \(c3\), output a message indicating the failure.
  - If all conditions are met:
    - If all sides are equal, output "Equilateral".
    - If exactly one pair of sides is equal, output "Isosceles".
    - If no pair of sides is equal, output "Scalene".
    - If any of conditions \(c4\), \(c5\), or \(c6\) is not met, output "NotATriangle".

- **Example Fix**:
  - For the input set (2, 2, 5):
    - The condition \(c6\) is not met, as \(c\) is greater than \(a + b\).
    - Therefore, the output should be "NotATriangle" because the values do not form a valid triangle.


