# Deterministic Finite Automaton (DFA) Simulator

## Description
This project is a functional simulator designed to handle the core logic of Deterministic Finite Automata (DFA). It allows users to load an automaton definition from a file, verify its properties, and test various words to see if they are accepted by the defined language. The system ensures that the loaded automaton is strictly deterministic, providing error messages if non-deterministic transitions are detected.

## Technologies
-   **C11**
-   **Standard I/O Libraries**
-   **GCC** (GNU Compiler Collection)

## Features
-   **File-Based Loading**: Import DFA specifications including alphabets, states, and transition functions from `.txt` files.
-   **Determinism Validation**: Automatically checks if the provided specification adheres to DFA rules.
-   **Interactive Menu**: User-friendly CLI for managing memory, printing DFA info, and testing strings.
-   **Word Testing**: Real-time processing of input strings to check for acceptance or rejection.
-   **Memory Management**: Options to reset the current automaton and load new specifications without restarting the program.

## How to Run
### Compilation

Use a C compiler (like GCC) to compile the source files:

```
gcc main.c arquivo.c menu.c sistema.c -o dfa_sim

```

### Execution

Run the compiled executable:

```
./dfa_sim
```

### Instructions

1.  **Load DFA (Option 1)**: Enter the filename (e.g., `automaton.txt`). The file must follow this format:
    
    
    ```
    alfabeto={a,b,0,1}
    estados={q0,q1,q2}
    finais={q2}
    (q0,a)= q1
    (q1,b)= q2
    ```
    
2.  **Print Info (Option 2)**: Displays the alphabet, states, final states, and transition list.
    
3.  **Test Words (Option 3)**: Enter choice `1` to type a word and check if it reaches a final state.
    
4.  **Reset Memory (Option 4)**: Clears the current DFA to allow loading a different file.
    
5.  **Exit (Option 0)**: Closes the program.

## Project Structure

-   **`main.c`**: Entry point that coordinates the interaction between the menu and the simulation logic.
-   **`sistema.c / .h`**: Contains the core logic for automaton processing and word testing.
-   **`arquivo.c / .h`**: Handles file parsing and data extraction from the specification files.
-   **`menu.c / .h`**: Manages the CLI display and user input options.

## What I Learned

-   **Automata Implementation**: Translating mathematical definitions of 5-tuple automata into programmatic data structures.
-   **String Parsing**: Implementing custom logic to extract transitions and sets (alphabet/states) from formatted text files.
-   **State Machines**: Managing state transitions and processing input symbols sequentially to determine finality.
-   **Modular Programming**: Organizing a C project into separate modules (system, file handling, UI) for better maintainability.

## Future Improvements

-   **NFA Support**: Expand the simulator to handle Non-Deterministic Finite Automata and NFA-to-DFA conversion.
-   **Graphic Visualization**: Integrate a tool to generate visual diagrams of the states and transitions.
-   **Step-by-Step Debugging**: Allow users to see the state change for each character processed in a word.




