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



