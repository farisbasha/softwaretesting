# Part A
## 1.What is Node/Vertex Coverage?
- Node Coverage (NC) : Test set T satisfies node coverage on graph G iff for every syntactically reachable node n in N, there is some path p in path(T) such that p visits n.
- The first (and simplest) two criteria require that each node and edge in a graph be executed



## 2.Explain the purpose of CFG: Switch-case in source code analysis
CFG analysis for switch-case statements in source code aims to map out the different control flow paths based on case options, aiding in understanding program logic and identifying potential execution paths and branching behavior.
<img width="350" alt="Screenshot 2024-04-21 at 8 16 59 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/28aeb93f-c901-4ac5-9b25-bca9f438faa3">


## 3. Explain the concept of input space partitioning in software testing ?
<img width="309" alt="Screenshot 2024-04-21 at 8 20 16 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/22d246ae-06b4-4f0f-b753-16c238e6797c">


## 4.Explain the concept of functional testing according to Howden's perspective
<img width="393" alt="Screenshot 2024-04-21 at 8 21 55 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/695d08bd-34ab-4bb6-a33a-6577aa87bd76">
<img width="333" alt="Screenshot 2024-04-21 at 8 22 14 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/6648468a-5932-4489-af7d-8e4a8bfc6fe0">

## 5.What is the purpose of equivalence class partitioning in testing? Provide a scenario where it would be applicable ?


- **Reduce Test Cases**: Minimize the number of test cases by selecting representative inputs.
- **Maximize Coverage**: Ensure comprehensive testing by covering all behaviorally equivalent inputs.
- **Identify Defects**: Efficiently uncover defects by focusing on critical areas of the input space.
- **Optimize Testing Efforts**: Streamline testing efforts by targeting inputs likely to exhibit similar behavior.

Scenario: Testing a login system for a web application.
- **Equivalence Classes**: Valid username and password, invalid username with valid password, valid username with invalid password, invalid username and password.
- **Purpose**: Efficiently validate login system behavior by testing representative inputs from each class.


# Part B

## 6.Draw CFG fragment for (i) Simple if (ii) Switch case (iii) Simple loop 
![untitled](https://github.com/farisbasha/softwaretesting/assets/72191505/2557ec00-4722-4ff3-9757-b008def13eff)



### i) Simple if
<img width="350" alt="Screenshot 2024-04-21 at 5 42 30 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/aa9b619a-36b5-4fee-896a-9adc0e50f3a8">


### ii) Switch-case

<img width="350" alt="Screenshot 2024-04-21 at 5 43 25 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/3461191e-6516-4302-a10b-f9f49c9e435f">

> NOTE: You can use any simple program , this is just an example
### iii) Simple Loop

<img width="350" alt="Screenshot 2024-04-21 at 5 44 26 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/49776d53-833d-4a36-9d41-b7c24bf7e9b3">

> NOTE: You can use any simple program , this is just an example


## 7.Describe the Subsumption Relationships among Graph Coverage Criteria. How do these relationships influence the selection and implementation of testing strategies?
<img width="399" alt="Screenshot 2024-04-21 at 8 25 22 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/338c588f-5056-490d-a479-7c6f5a31499f">

- **Definition**: Subsumption relationships occur when one coverage criterion includes or is more comprehensive than another. it denote hierarchy among graph coverage criteria.
- One criterion includes another, making the narrower one redundant.
- For example, path coverage subsumes edge coverage.
- Understanding guides efficient criterion selection and testing strategy implementation.


- **Influence on Selection of Testing Strategies**:
  - **Coverage Hierarchy**: Understanding subsumption relationships helps prioritize testing criteria based on their level of comprehensiveness.
  - **Test Strategy Selection**: Testers can choose the most appropriate coverage criterion based on the testing objectives and available resources.
  - **Balancing Depth and Efficiency**: Subsuming criteria may provide deeper analysis but require more resources, while subsumed criteria may offer efficiency but less thorough coverage.

- **Influence on Implementation of Testing Strategies**:
  - **Incremental Testing**: Testers may start with less comprehensive criteria and gradually progress to more detailed ones as resources permit.
  - **Tailoring Testing Approaches**: Depending on the application's complexity and criticality, testers can customize testing strategies to prioritize certain criteria over others.
  - **Tooling and Automation**: Testing tools should support various coverage criteria, allowing testers to implement strategies efficiently.

Understanding subsumption relationships enables testers to design effective testing strategies tailored to the specific needs and constraints of the software project, balancing thoroughness with resource efficiency.


## 8.Explain simple path coverage and prime path coverage with the help of CFG given below?
<img width="277" alt="Screenshot 2024-04-21 at 8 35 45 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/a3202cb1-926b-490f-9349-deb318f0d870">

### Simple Path Coverage
**Simple Path :** A path from node ni to nj is simple if no node appears more than once, except possibly the first and last nodes are the same
– No internal loops
– A loop is a simple path

**Simple Path Coverage:** Test Requirement(TR) contains each simple path in G

In the figure, following are the simple paths:
- **Length 0**:
  Simple paths = [1], [2], [3], [4]
  - [1], [2], [3], [4] are simple paths because each node appears only once.

- **Length 1**:
  Simple paths = [1, 2], [1, 3], [2, 4], [3, 4], [4, 1]
  - Each path is simple because each node appears only once.

- **Length 2**:
  Simple paths = [1, 2, 4], [1, 3, 4], [2, 4, 1], [3, 4, 1], [4, 1, 2], [4, 1, 3]
  - Each path is simple because each node appears only once.

- **Length 3**:
  Simple paths = [1, 2, 4, 1], [1, 3, 4, 1], [2, 4, 1, 2], [3, 4, 1, 3], [4, 1, 2, 4], [4, 1, 3, 4], [1, 3, 4, 2], [2, 4, 1, 3]
  - Each path is simple because each node appears only once.

### Prime Path Coverage
**Prime Path :** A simple path that does not appear as a proper subpath of any other simple path
**Prime Path Coverage (PPC) :** Test Requirement(TR) contains each prime path in G.
All of the following simple paths are prime paths because each path:
- Is a simple path.
- Does not appear as a sub-path of any other simple path.

Prime Paths:
1. [1, 3, 4, 1]
2. [1, 2, 4, 1]
3. [3, 4, 1, 3]
4. [2, 4, 1, 2]
5. [4, 1, 3, 4]
6. [4, 1, 2, 4]
7. [3, 4, 1, 2]
8. [2, 4, 1, 3]

Each path satisfies both conditions, making them prime paths in the graph.


## 9.Explain the steps involved in input partitioning and equivalence partitioning?

### Input Partitioning
**Steps:**

1. **Identify Inputs**: Determine the input fields or parameters to be tested.

2. **Analyze Characteristics**: Understand input properties like data type, range, and constraints.

3. **Partition Inputs**: Divide inputs into subsets based on common characteristics or criteria.

4. **Define Strategy**: Choose partitioning techniques like boundary value analysis or equivalence partitioning.

5. **Assign Test Cases**: Create test cases covering each input partition.

6. **Execute Tests**: Run test cases to validate system behavior and analyze results.

### Equivalence Partitioning
Step-by-Step Process of Equivalence Partitioning:

1. **Identify Input Field**: Determine the input field to be tested, like the username field.
2. **Define Equivalence Classes**: Categorize possible input values into distinct classes based on similar behavior.
3. **Determine Representative Values**: Select values covering boundary conditions and critical scenarios within each class.
4. **Create Test Cases**: Generate test cases covering each equivalence class, including valid and invalid inputs.
5. **Execute Test Cases**: Run the test cases using defined classes to validate system behavior, recording results for analysis.

By following this process, testers can efficiently design test cases for comprehensive coverage while minimizing redundancy.




## 10.Classify black box testing, white box testing, and grey box testing from the standpoint of a software tester
| Black Box Testing | White Box Testing | Grey Box Testing |
|---------------------|---------------------|---------------------|
| Focuses on external behavior. | Examines internal code structure. | Combines external and internal perspectives. |
| Tester lacks access to source code. | Tester has access to source code. | Tester has partial access to source code. |
| Relies on specifications and requirements. | Tests based on code coverage and logic. | Uses a combination of requirements and code structure. |
| Emphasizes functional specifications. | Emphasizes code paths and structure. | Offers a balanced perspective. |
| Validates user perspectives. | Validates code implementation. | Validates both user and code aspects. |
| Examples include functional, regression, and acceptance testing. | Examples include unit, integration, and system testing. | Examples include API, usability, and security testing. |


## 11.Discuss the significance of boundary value analysis in software testing. Provide an example scenario where boundary value analysis would be crucial.


- **Significance of Boundary Value Analysis:**

1. **Error Localization**: Identifies defects at critical boundaries where triangle classification might change.

2. **Efficient Coverage**: Maximizes coverage with minimal test cases by focusing on boundary conditions.

3. **Risk Mitigation**: Reduces risks of defects in crucial areas where errors are more likely to occur.

4. **Requirement Validation**: Validates if software meets specified requirements by testing boundary conditions.

5. **Bug Prevention**: Identifies potential off-by-one errors or boundary-related issues before deployment.


**Example: Consider a system that accepts ages from 18 to 56**.

Boundary Value Analysis(Age accepts 18 to 56)

| Invalid  (min-1)  | Valid (min, min + 1, nominal, max – 1, max) | Invalid  (max + 1) |
| ------------------ | ------------------------------------------ | ------------------- |
| 17 | 1 8, 19, 37, 55, 56 |57 |



Valid Test cases: Valid test cases for the above can be any value entered greater than 17 and less than 57.


Invalid Testcases: When any value less than 18 and greater than 56 is entered.


## 12. Describe the functional testing methodology and list its types
Functional Testing Methodology:

- **Definition**: Verifies the functionality of a software system or application to ensure it behaves according to specified requirements and business needs.

- **Goal**: Validate system features, capabilities, and interactions with components to ensure it works as intended.

- **Focus**: Tests input and output, data manipulation, user interactions, and system responses to various scenarios and conditions.

Types of Functional Testing:

1. **Unit Testing**: Performed by developers to test individual components or units of an application against requirements. Ensures code coverage including line, code path, and method coverage.

2. **Smoke Testing**: Conducted after each build release to verify software stability and absence of anomalies.

3. **Sanity Testing**: Follows smoke testing to ensure major functionalities work perfectly, both independently and in combination with others.

4. **Regression Testing**: Ensures changes to the codebase do not disrupt existing functions or cause instability.

5. **Integration Testing**: Validates that functional modules work as expected when operating together, ensuring end-to-end system outcomes meet standards.

6. **Beta/Usability Testing**: Involves actual customers testing the product in a production environment to gauge interface comfort and provide feedback for further improvements.


