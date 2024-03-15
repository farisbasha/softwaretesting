# **Part A**

## **1.Explain the differences between Fault, Error, and Bug?**

| Term   | Definition                                              | Example                                    |
|--------|---------------------------------------------------------|--------------------------------------------|
| Fault  | A flaw in the system's code, design, or architecture    | Missing validation check in login process  |
| Error  | Deviation from the intended behavior of the system      | Incorrect calculation in a banking system |
| Bug    | An error or fault that causes unexpected behavior       | Application crashes upon user interaction |

## **2.What are the functions of Test driver and Test stubs in dynamic unit testing?**

| Test Driver                                   | Test Stub                                     |
|-----------------------------------------------|-----------------------------------------------|
| Controls test execution and invokes functions | Simulates behavior of unavailable components |
| Provides input values to the component       | Mimics output of called components            |
| Ensures interaction with other components    | Allows testing of individual units in isolation |
| Handles test setup and teardown activities   | Simplifies integration testing                |
| Used in bottom-up integration testing         | Used in top-down integration testing         |

## **3.What are du paths and du pairs in a data flow graph?**

#### **DU Pair:**
  - A DU pair consists of a definition and use for a variable, where at least one DU path exists from the definition to the use.
  -  For instance, `x = ...` is a definition of variable `x`
  -  `y = ... x ...` is a use of `x`.

 #### **DU Path:** 
  - A DU path is a path in the Control Flow Graph (CFG) starting from a definition of a variable and leading to its use within the program.
  - It represents the flow of data from the point of definition to the point of use. 
  - Definition-clear: A DU path is considered definition-clear if the value of the variable is not replaced or modified along the path.
  - Note: Loops may create infinite DU paths between a definition and a use, requiring careful consideration during analysis.

## **4.Differences between White Box Testing & Grey Box Testing:**

| White Box Testing                               | Grey Box Testing                                     |
|-------------------------------------------------|------------------------------------------------------|
| Tests internal structures, paths, and flows     | Tests focus on functionality, inputs, and outputs   |
| Requires access to the source code              | Can be performed with or without access to the code |
| Checks for code coverage and logic correctness  | Emphasizes on user experience and system behavior   |
| Identifies potential security vulnerabilities   | Identifies integration issues and interoperability  |
| Often used for security and code review         | Commonly applied in penetration testing and QA      |

## **5. May be one common question  🙋**
pass


# **Part B**

## **6.Explain the testing process using different levels of thinking**
Testing Process with Different Levels of Thinking:

1. **Concrete Thinking:**
   - Understanding explicit requirements.
   - Creating test cases based on documented specifications.

2. **Analytical Thinking:**
   - Analyzing potential scenarios and edge cases.
   - Designing test cases to uncover hidden defects.

3. **Critical Thinking:**
   - Assessing risks and prioritizing testing efforts.
   - Identifying areas for improvement in test coverage.

4. **Creative Thinking:**
   - Innovating in test design and execution.
   - Devising unconventional test scenarios to simulate real-world usage.

5. **Systematic Thinking:**
   - Organizing testing activities systematically.
   - Developing comprehensive test plans and strategies.

6. **Holistic Thinking:**
   - Considering the overall impact of changes on the system.
   - Ensuring that testing aligns with broader project goals.

7. **Strategic Thinking:**
   - Planning testing activities to achieve long-term project objectives.
   - Aligning testing efforts with organizational strategies and priorities.
  
## **7.Define key software testing terminologies, including verification, validation, test cases, and coverage criteria. Discuss the significance of these terms in the testing process**



1. **Verification**:
   - **Definition**: Ensuring that the software product meets its specifications and requirements without necessarily executing the code.
   - **Significance**:
     - Ensures software conforms to specifications.
     - Prevents costly errors by catching them early in the development process.
   - **Types**:
     - Reviews
     - Walkthroughs
     - Inspections

2. **Validation**:
   - **Definition**: Confirming that the software product meets the customer's needs and expectations by executing the code.
   - **Significance**:
     - Ensures software meets customer expectations.
     - Confirms the software's fitness for its intended purpose.
   - **Types**:
     - User Acceptance Testing (UAT)
     - System Testing
     - Alpha/Beta Testing

3. **Test Cases**:
   - **Definition**: Detailed instructions or scenarios designed to verify specific aspects of the software functionality.
   - **Significance**:
     - Provide a systematic approach to verify software functionality.
     - Identify defects and issues early in the development process.
   - **Types**:
     - Functional Test Cases
     - Integration Test Cases
     - Performance Test Cases
     - Usability Test Cases
     - Security Test Cases
     - Regression Test Cases
     - Edge Case Test Cases
     - Negative Test Cases

4. **Coverage Criteria**:
   - **Definition**: Metrics used to measure the extent to which the software has been tested.
   - **Significance**:
     - Measures the effectiveness of testing.
     - Helps identify areas that require additional testing.
   - **Types**:
     - Code Coverage
     - Requirement Coverage
     - Path Coverage
     - Branch Coverage
     - Statement Coverage
     - Function Coverage
     - Decision Coverage



## **8.Explain the different testing methods, including black-box testing, white-box testing, and grey-box testing. Discuss the principles and techniques associated with each method.**

<img width="417" alt="Screenshot 2024-03-14 at 11 16 24 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/199cd726-6d24-4b99-83b3-54ebb1283da0">



| Aspect            | Black-box Testing                                              | White-box Testing                                              | Grey-box Testing                                               |
|-------------------|---------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|
| **Principle**     | Focuses on external behavior without examining internal logic. | Tests internal logic and structure of the software directly.   | Combines elements of both black-box and white-box approaches.  |
| **Level of Knowledge** | Tester has no knowledge of internal code or structure.       | Tester has full access to internal code and design.           | Tester has partial knowledge of internal code and structure. |
| **Techniques**    | Equivalence partitioning, boundary value analysis, scenario-based testing. | Coverage criteria: statement, branch, and path coverage.   | Combination of black-box and white-box techniques.            |
| **Test Design**   | Based on specifications and requirements.                     | Based on code structure and implementation details.          | Combines specification-based and structure-based testing.      |
| **Dependency**    | Independent of code changes.                                   | Highly dependent on code changes.                            | Moderately dependent on code changes.                         |
| **Scope**         | Suitable for system and acceptance testing.                   | Commonly used in unit and integration testing.               | Useful for integration and system testing.                   |
| **Visibility**    | Focuses on user interactions and inputs/outputs.              | Focuses on code paths and internal data structures.          | Balances external behavior and internal structure.           |



## **9.Describe the difference between static unit testing and dynamic unit testing. Provide examples of tools or techniques used in each type of testing.**



| Aspect          | Static Unit Testing                      | Dynamic Unit Testing                  |
|-----------------|-----------------------------------------|---------------------------------------|
| **Definition**  | Analyzes code without execution.         | Executes code, evaluates behavior.    |
| **Purpose**     | Identifies defects pre-runtime.         | Validates behavior post-runtime.      |
| **Timing**      | Pre-runtime during development.          | Post-runtime after code execution.    |
| **Focus**       | Code structure, standards compliance.    | Functional behavior, performance.     |
| **Technique**    | Static analysis, code review.            | Test case execution, debugging.       |
| **Tools**  | Tools for automated code inspection (e.g., SonarQube, Checkstyle). | Test automation frameworks (e.g., JUnit, TestNG).|
| **Interactivity** | Minimal interaction with code.         | Direct interaction with code.         |
| **Scope**       | Broader view of codebase.                | Specific functionality or features.   |
| **Feedback**    | Early feedback on potential issues.      | Immediate feedback on behavior.        |




## **10.Discuss different types of dynamic unit testing techniques, including control flow testing and data flow testing Provide examples to illustrate each technique.**



| Aspect        | Control Flow Testing                | Data Flow Testing               | Path Testing                   |
|---------------|-----------------------------------|--------------------------------|--------------------------------|
| **Principle** | Tests different control flow paths| Ensures correct data flow      | Tests all possible code paths |
| **Technique** | Exercise branches, loops, decisions| Track variable data flow       | Cover every execution path     |
| **Focus**     | Testing control flow paths         | Validating data flow handling  | Ensuring comprehensive coverage|
| **Benefits**  | Identifies control flow errors    | Detects data-related issues    | Verifies comprehensive coverage|

**EXAMPLE**
 1. **Control Flow**
   <img width="297" alt="Screenshot 2024-03-14 at 11 32 17 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/3c383354-0150-4e32-b5fb-1b8728c306c1">

 2. **Data Flow**


       <img width="506" alt="Screenshot 2024-03-14 at 11 33 29 PM" 
        src="https://github.com/farisbasha/softwaretesting/assets/72191505/8f48714c-b463-4177-bc68-58a2cbeacbc7">

3. **Path Testing**


     <img width="310" alt="Screenshot 2024-03-14 at 11 35 38 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/e052dc25-0049-40f4-8ead-28d9fc383fe7">

    Example path in the above figure
   Prime Paths : [ 0, 1, 3, 0 ], [ 0, 2, 3, 0], [ 1, 3, 0, 1 ], [ 2, 3, 0, 2 ], [ 3, 0, 1, 3 ], [ 3, 0, 2, 3 ], [ 1, 3, 0, 2 ],

   



## **11.Explain the concept of JUnit and its role as a framework for unit testing in Java-based applications. Discuss the key features and benefits of using JUnit for test automation.**

**JUnit**:
- **Definition**: JUnit is an open-source testing framework for Java-based applications.
- **Key Features**:
  1. *Annotations*: Mark test methods easily.
  2. *Assertions*: Verify outcomes with built-in methods.
  3. *Test Runners*: Execute tests with different runners.
  4. *Test Fixtures*: Setup and teardown methods for test environments.
  5. *Parameterized Tests*: Run tests with different inputs.
  6. *Hamcrest Matchers*: Use expressive assertions.

**Benefits**:
- **Simplicity**: Easy syntax for writing test cases.
- **Automation**: Supports automated testing for continuous integration.
- **Reusability**: Test cases can be reused across projects.
- **Reporting**: Detailed test reports aid in issue identification.
- **Integration**: Integrates smoothly with IDEs, build tools, and CI servers.
