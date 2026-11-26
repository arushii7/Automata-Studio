# Automata Studio
### DFA/NFA String Processing Visualizer

**Course:** CSET302 – Automata Theory and Computability  
**University:** Bennett University, School of Computer Science and Engineering Technology  
**Group ID:** 4
**Batch:** 12
---

## 1. Overview

Automata Studio is a browser-based interactive simulator for constructing, editing and testing Deterministic Finite Automata (DFA) and Nondeterministic Finite Automata (NFA).

It allows users to create states, define transitions, mark initial and accepting states, and visualize how input strings are processed through step-by-step simulation.

The application is completely self-contained and runs locally without a backend.

## 2. Supported Features

- Create, rename, move and delete states.
- Create, edit and delete directed transitions.
- Define initial and accepting states.
- Switch between DFA and NFA modes.
- Validate automaton definitions and input strings.
- Simulate strings and display ACCEPTED or REJECTED results.
- Visualize active states and transitions.
- Step forward and backward through execution.
- Play, pause and restart simulations.
- Adjust simulation playback speed.
- Load predefined automata examples:
  - DFA accepting binary strings ending in `01`.
  - DFA accepting strings containing an even number of `0`s.
  - NFA accepting strings containing substring `01`.
  - NFA demonstrating multiple possible transitions.

## 3. Technology Stack and Dependencies

| Technology | Version / Specification | Purpose |
|---|---|---|
| HTML | HTML5 | Application structure |
| CSS | CSS3 | Interface styling and layout |
| JavaScript | Vanilla JavaScript (ES6+) | Automaton logic and simulation |
| SVG | SVG 1.1-compatible browser support | Automaton visualization |
| Browser | Modern Chromium-based browser recommended | Application execution |

**External dependencies:** None.

No frameworks, package managers, databases or backend services are required.

## 4. Installation

1. Clone the repository:

   ```bash
   git clone [INSERT REPOSITORY URL]
   ```

2. Navigate to the project directory:

   ```bash
   cd Automata-Studio
   ```

3. Verify that `index.html` is present.

4. No additional installation or dependency setup is required.

## 5. How to Run

Open the application directly in a browser.

**Windows:**
```bash
start index.html
```

**macOS:**
```bash
open index.html
```

**Linux:**
```bash
xdg-open index.html
```

**Entry point:** `index.html`

The application runs locally without requiring a development server.

## 6. Example

### Example: DFA accepting binary strings ending in `01`

**Automaton definition:**

- States: `{q0, q1, q2}`
- Alphabet: `{0, 1}`
- Initial state: `q0`
- Accepting state: `{q2}`

**Transition table:**

| Current State | Input 0 | Input 1 |
|---|---|---|
| q0 | q1 | q0 |
| q1 | q1 | q2 |
| q2 | q1 | q0 |

**Test input:** `1101`

**Expected execution:**

```text
Initial: q0
Read 1:  q0
Read 1:  q0
Read 0:  q1
Read 1:  q2
```

**Expected output:**
```text
ACCEPTED
```

The final state `q2` is an accepting state.

Another test:

```text
Input:  1011
Output: REJECTED
```

The string does not end in `01`.

## 7. Project Structure

```text
Automata-Studio/
│
├── index.html
│   ├── HTML interface
│   ├── Embedded CSS
│   └── Embedded JavaScript
│
└── README.md
```

### Main implementation responsibilities

| Component | Responsibility |
|---|---|
| Automaton Management | State and transition creation, editing and deletion |
| SVG Renderer | Drawing states, transitions and visual highlights |
| Input Validation | Checking automaton definitions and input symbols |
| DFA/NFA Engine | Processing input and calculating active states |
| Simulation Controller | Managing execution frames and playback |
| Example Loader | Loading predefined automata |

## 8. Testing

Testing is performed manually through the simulator interface using predefined examples and custom automata.

### Test cases

| Test Case | Input | Expected Result |
|---|---|---|
| Binary strings ending in 01 | `101` | ACCEPTED |
| Binary strings ending in 01 | `1100` | REJECTED |
| Even number of zeros | `1010` | ACCEPTED |
| Even number of zeros | `010` | REJECTED |
| NFA containing substring 01 | `001` | ACCEPTED |
| NFA containing substring 01 | `1110` | REJECTED |
| Empty input | `ε` | Depends on initial state |
| Invalid alphabet symbol | `2` in binary DFA | Validation error |

**Testing procedure:**

1. Open the required predefined automaton.
2. Enter the test input.
3. Execute the simulation using Run or Step.
4. Verify intermediate states and transitions.
5. Compare the final result with the expected output.

**Test execution:** Manual, through the browser interface. No automated test framework is currently configured.

## 9. Known Limitations and Troubleshooting

### Known limitations

- Epsilon transitions are not supported.
- Only single-character input symbols are supported.
- The alphabet is inferred from transition labels.
- Complete transition coverage is required for DFA validation.
- Large automata may require additional rendering optimization.
- Automata are not persistently saved to a database or cloud service.

### Troubleshooting

| Issue | Suggested solution |
|---|---|
| Application does not open | Open `index.html` using a modern browser. |
| Simulation fails | Verify the initial state and transition definitions. |
| Invalid input message | Check that every input character belongs to the inferred alphabet. |
| DFA validation error | Ensure every state has exactly one transition for each alphabet symbol. |
| Unexpected rejection | Inspect the execution trace and accepting states. |

## 10. Team Contributions and Acknowledgements

**Group ID:** 4

| Member | Name | Student ID | Contribution |
|---|---|---|---|
| Member 1 | S24CSEU1072 | DEV SONI | Frontend and UI/UX |
| Member 2 | S24CSEU1061 | ADARSH RAJ | Automaton editor and SVG rendering |
| Member 3 | S24CSEU1069 | ARUSHI SINGH | DFA/NFA algorithms and validation |
| Member 4 | S24CSEU1050 | ISHITA SAHAI | Simulation, playback and testing |

**Acknowledgements**

We thank the faculty of the School of Computer Science and Engineering Technology, Bennett University, for their guidance and support throughout the CSET302 project.

---

**Project:** Automata Studio  
**Course:** CSET302 – Automata Theory and Computability  
**Institution:** Bennett University
