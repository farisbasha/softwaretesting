# **Part A**

## **1.Explain the differences between Validation and Verification?**

| Aspect      | Validation                              | Verification                               |
|-------------|-----------------------------------------|--------------------------------------------|
| Objective   | "Are we building the right product?"    | "Are we building the product right?"      |
| Definition  | Ensures the software meets requirements | Confirms that the software meets standards |
| Focus       | Addresses user needs and expectations   | Emphasizes technical specifications       |
| Timing      | Done at the end of the development cycle| Performed throughout the development cycle|
| Method      | Involves testing actual software        | Involves reviewing documents and code     |
| Outcome     | Assures the right product is built      | Assures the product is built right        |


## **2.Define Ground string, Mutation score, and Mutants?**


| Term           | Definition                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ground string  | The original, unaltered version of the source code used as a reference for creating mutants. It serves as the baseline against which mutants are compared.          |
| Mutants        | Altered versions of the source code, systematically modified to introduce artificial defects. These variants help evaluate the robustness of test suites.     |
| Mutation score | A metric indicating the percentage of mutants that are killed by test cases. A higher mutation score suggests a more effective test suite in detecting faults.  |

## **3.Define Node coverage, Edge coverage and Prime path coverage in a control flow graph?**


| Coverage Type         | Definition                                                                                                                                                                              |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Node Coverage         | Node Coverage, also known as Statement Coverage, ensures that each node (or statement) in the control flow graph is executed at least once by the test cases.                        |
| Edge Coverage         | Edge Coverage, also known as Branch Coverage, ensures that each edge in the control flow graph is traversed at least once by the test cases, covering both true and false branches.  |
| Prime Path Coverage   | Prime Path Coverage aims to cover all possible prime paths in the control flow graph. A prime path is a unique path from the start node to the end node that does not include any other paths. |


## **4.Coverage Criteria**



1. **Statement Coverage/Block Coverage**:
   $\(\frac{{\text{{Number of statements executed}}}}{{\text{{Total Number of statements}}}} \times 100\)$

2. **Decision Coverage/Branch Coverage**:
   $\(\frac{{\text{{Number of decision/branch outcomes executed}}}}{{\text{{Total number of decision outcomes }}}} \times 100\)$

3. **Function Coverage**:
 $\(\frac{{\text{{Number of functions called}}}}{{\text{{Total number of functions}}}} \times 100\)$

4. **Condition Coverage/Expression Coverage**:
   $\(\frac{{\text{{Number of executed operands}}}}{{\text{{Total Number of Operands}}}} \times 100\)$


## **5.How does the cost of error correction change throughout the phases of software development**

Cost of error correction increases as software development progresses:

<img width="349" alt="Screenshot 2024-03-14 at 9 22 29 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/9aa2c167-18a6-4346-aa8e-8dc66e9b9cfd">

- **Requirements Phase**: Least expensive to fix.
- **Design Phase**: More costly, major changes possible.
- **Implementation Phase**: Moderate costs, changes in modules.
- **Testing Phase**: Costlier than previous phases, debugging needed.
- **Deployment and Maintenance Phase**: Most expensive, impacts user experience and reputation.



# **Part B**

## **6.Define software testing and explain its significance in software development. Discuss the reasons why software should be thoroughly tested**



1. **Definition of Software Testing**:
    - Software testing ensures that software works correctly by checking it against defined requirements.

2. **Significance in Software Development**:
    - **Detects defects:** Finds and fixes errors early to prevent issues later.
    - **Ensures quality:** Validates that software meets user needs and expectations.
    - **Enhances reliability:** Builds trust in the software's performance.
    - **Improves user satisfaction:** Reduces frustration by minimizing errors.
    - **Reduces costs:** Saves money by catching problems early.
    - **Aids decision-making:** Provides insights for developers and stakeholders to make informed decisions.
    - **Compliance assurance:** Ensures adherence to regulatory standards and industry best practices.

3. **Reasons for Thorough Testing**:
    - **Identify defects:** Prevents bugs from reaching users.
    - **Validate functionality:** Ensures software works as intended.
    - **Verify compatibility:** Confirms software works across different environments.
    - **Assess performance:** Evaluates speed and efficiency under various conditions.
    - **Ensure security:** Protects against vulnerabilities and data breaches.
    - **Maintain reputation:** Preserves trust and credibility with users.
    - **Meet user expectations:** Ensures software meets user needs and delivers value.
    - **Support scalability:** Tests scalability to handle increased workload or users.
    - **Reduce support burden:** Minimizes post-release issues, reducing support requests and costs.
  

## **7.Describe various types of software testing techniques and also discuss the purposes and objectives of each type of testing.**

1. **Unit Testing**:
    - **Purpose**: Test individual units of code.
    - **Objective**: Identify defects in isolated components early.

2. **Integration Testing**:
    - **Purpose**: Test interactions between integrated components.
    - **Objective**: Validate communication and data exchange.

3. **System Testing**:
    - **Purpose**: Test entire software system functionality.
    - **Objective**: Validate compliance with requirements.

4. **Acceptance Testing**:
    - **Purpose**: Validate software meets user requirements.
    - **Objective**: Ensure user satisfaction before deployment.

5. **Regression Testing**:
    - **Purpose**: Ensure existing features still work post-changes.
    - **Objective**: Prevent unintended side effects from updates.

6. **Performance Testing**:
    - **Purpose**: Evaluate software speed and scalability.
    - **Objective**: Identify and fix performance bottlenecks.

7. **Security Testing**:
    - **Purpose**: Identify vulnerabilities and protect against threats.
    - **Objective**: Ensure software resilience to security attacks.

8. **Usability Testing**:
    - **Purpose**: Evaluate user interface design and experience.
    - **Objective**: Improve user satisfaction and adoption.


## **8.Describe the role of testing in ensuring software quality and discuss its impact on overall software development processes. Provide a real-world example illustrating the importance of testing in software development.**



Testing ensures software quality by:
1. Identifying defects early.
2. Verifying functionality meets requirements.
3. Validating performance under various conditions.

**Impact on Overall Software Development Processes:**

1. **Early Detection and Prevention**: Reduces time and effort in fixing defects.
2. **Improvement of Software Quality**: Enhances user satisfaction and trust.
3. **Risk Mitigation**: Reduces project failure risks.
4. **Continuous Improvement**: Drives optimization and innovation.

**Real-World Example:**

In the Ariane 5 rocket launch failure, a software bug led to a catastrophic failure. Thorough testing could have prevented this, emphasizing the importance of testing in critical systems.


```python
def divide(x, y):
    return x / y

# Test case
divide(10, 0)  # Raises DivisionByZero error
```

In this concise example, the test case checks for the division by zero scenario, emphasizing the importance of testing to catch potential errors before deployment.



## **9.Explain the concept of unit testing and its significance in software development. Discuss the benefits of incorporating unit testing into the development process.**

**Unit Testing:**
Unit testing is a software testing technique where individual units or components of a software application are tested in isolation to ensure they work correctly.

There are two types of unit testing: Manual and Automated.

**Significance**: Unit testing is crucial as it helps identify defects early in the development process, reducing the likelihood of larger issues later on.

**Benefits:**

1. **Validates Functionality**: Confirms that individual units of code perform as expected.
2. **Identifies Defects Early**: Detects errors and bugs in the early stages of development.
3. **Improves Code Quality**: Encourages developers to write clean, modular, and maintainable code.
4. **Facilitates Refactoring**: Provides confidence to refactor code without introducing defects.
5. **Saves Time and Costs**: Reduces debugging time and costs associated with fixing defects later in the development process.
6. **Enhances Collaboration**: Encourages collaboration among team members by providing a common framework for testing and validation.


## **10.Define mutation testing and explain the concepts of mutation and mutants. Discuss the significance of mutation testing in software quality assurance.**

**Mutation Testing:**
Mutation Testing evaluates the effectiveness of existing tests and helps design new ones by making small modifications (mutations) to the codebase and checking if tests can detect these changes.

<img width="371" alt="Screenshot 2024-03-14 at 10 31 56 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/4ec9d66d-47ed-43e8-957c-a832582d469c">


**Concepts:**
1. **Mutation:** Small alterations to the codebase.
2. **Mutants:** Modified versions of the program created through mutation.

**Significance:**
1. **Identifying Weaknesses:** Reveals gaps in test coverage.
2. **Improving Test Suite Quality:** Guides enhancement of test suite effectiveness.
3. **Detecting Hidden Defects:** Uncovers defects missed by other testing methods.
4. **Measuring Code Quality:** Provides a quantitative measure of test suite effectiveness.

## **11.Discuss different types of dynamic unit testing techniques: domain testing and functional program testing. Provide examples to illustrate each technique**

**Dynamic Unit Testing Techniques:**

1. **Domain Testing:**
   - Focuses on testing specific input domains or ranges within the code.
   - Example: Testing a square root function with positive, negative, zero, large, and decimal numbers.
   <img width="347" alt="Screenshot 2024-03-14 at 10 39 12 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/3c6be806-dc9a-4ccf-a80b-da5938d1b381">


2. **Functional Program Testing:**
   - Tests the functionality of the program by executing specific program functions or methods.
   - Example: Testing a sorting function with different input arrays, including random, sorted, reverse sorted, and arrays with duplicates.
   - <img width="272" alt="Screenshot 2024-03-14 at 10 38 37 PM" src="https://github.com/farisbasha/softwaretesting/assets/72191505/31c37fe0-9037-489c-939c-1d501086d345">

