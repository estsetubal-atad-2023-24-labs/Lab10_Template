# Algorithms and Abstract Data Types

## Lab 10 | Exercises + Template  

This repository was created from:

- <https://github.com/estsetubal-atad/CProgram_Template> 

Refer to the README if you have any questions about its usage.

----

**Objectives**:

- Use of the **linked list** data structure to implement the *ADT Stack* and *ADT Queue*.
- Awareness and comparison of algorithmic complexities obtained with implementations based on *array list* and *linked list*.

**References**:

- TP Class \[17, 18 & 20\].
- "Abstract Data Types - C Language. Bruno Silva", available on Moodle.

---

### Project Organization in VS Code

The files related to the *ADT Stack* and *ADT Queue* are located in the `stack` and `queue` folders, respectively. The respective implementations based on *array list* are already present and complete.

The program associated with the test of each implementation allows to verify if the respective access policy is being respected and then performs a *stress* test with the insertion and removal of `100,000` elements. This will allow you to check the required execution time and will be closely related to the algorithmic complexity of the implemented operations.  

There is a single *makefile* (see its contents) that compiles the necessary program with the chosen data structure, e.g.:

```console
$> make stack
# or
$> make stack_array
# to execute the compiled program, always use:
$> ./prog
```

### Level 1 - ADT Stack (Estimated Duration: 25min)

The implementation in `stackLinkedList.c` is partially complete, but the implementation of the `push`, `pop`, `peek`, and `print` operations is missing, which will depend on the approach chosen to obtain the LIFO access policy. In general terms, the insertion/removal of elements must be done at the "same end" of the data structure.

1. Provide the remaining implementation of the `push`, `pop`, `peek`, and `print` functions, considering the top of the stack at the "beginning" of the data structure, i.e., at node `stack->header->next`.

2. Compile and execute the program, checking if the LIFO access policy is being respected and the execution time of the stress test (a fast execution is expected).

### Level 2 - ADT Stack (Estimated Duration: 10min)

How does this implementation compare to the more efficient one based on *array list*?

3. Fill in the following table, analyzing the respective implementations of each data structure and the execution times of the stress test?

| Operation    | Array List | Linked List |
|--------------|------------|-------------|
| `create`     | &nbsp;     | &nbsp;      |
| `destroy`    | &nbsp;     | &nbsp;      |
| `size`       | &nbsp;     | &nbsp;      |
| `isEmpty`    | &nbsp;     | &nbsp;      |
| `clear`      | &nbsp;     | &nbsp;      |
| `push`       | &nbsp;     | &nbsp;      |
| `pop`        | &nbsp;     | &nbsp;      |
| `peek`       | &nbsp;     | &nbsp;      |
| `print`      | &nbsp;     | &nbsp;      |
| Exec. time ? | &nbsp;     | &nbsp;      |

4. Which implementation would you choose in the real world usage context? Justify. 

### Level 3 - ADT Queue (Estimated Duration: 25min)

The implementation in `queueLinkedList.c` is practically empty. But note that, if we are going to use the same data structure, e.g., *linked list*, then the definition of this data structure, as well as the "general" operations, e.g., `create`, `destroy`, `size`, `isEmpty`, and `clear`, are identical. 

5. Resolve the *forward declaration* when defining the content of `struct queueImpl`.

6. Implement the `create`, `destroy`, `size`, `isEmpty`, and `clear` operations.

### Level 4 - ADT Queue (Estimated Duration: 25min)

We will have to obtain a FIFO access policy with the manipulation of the *linked list* data structure. In general terms, the insertion/removal of elements must be done at "opposite ends" of the data structure.

7. Implement the `enqueue`, `dequeue`, `front`, and `print` operations.

8. Compile and execute the program, checking if the FIFO access policy is being respected and the execution time of the stress test.


| Operation   | Array List | Linked List |
|-------------|------------|-------------|
| `create`    | &nbsp;     | &nbsp;      |
| `destroy`   | &nbsp;     | &nbsp;      |
| `size`      | &nbsp;     | &nbsp;      |
| `isEmpty`   | &nbsp;     | &nbsp;      |
| `clear`     | &nbsp;     | &nbsp;      |
| `enqueue`   | &nbsp;     | &nbsp;      |
| `dequeue`   | &nbsp;     | &nbsp;      |
| `front`     | &nbsp;     | &nbsp;      |
| `print`     | &nbsp;     | &nbsp;      |
| Exec. time? | &nbsp;     | &nbsp;      |

10. Which implementation would you choose in the real world usage context? Justify. 

### Level 5 - ADT Stack + Queue (Estimated Duration: 10min)

11. Verify the correct management of dynamic memory in both your implementations (ADT Stack and ADT Queue), using *valgrind* for this purpose.

---

```markdown
@bruno.silva
(EOF)
``` 