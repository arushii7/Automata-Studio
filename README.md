# Automata Studio

An interactive **DFA/NFA String Processing Visualizer** developed
for CSET302 – Automata Theory and Computability at Bennett University.

## Features

- Create, edit and delete automaton states.
- Add directed transitions with custom input symbols.
- Set initial and accepting states.
- Switch between DFA and NFA modes.
- Simulate input strings and check acceptance/rejection.
- Visualize active states and transitions during execution.
- Step-by-step simulation with play, pause, restart and speed controls.
- Predefined automata examples for quick testing.

## Tech Stack

- HTML5
- CSS3
- JavaScript (Vanilla)
- SVG for automaton visualization

## Getting Started

1. Clone or download this repository.
2. Open `index.html` in a modern web browser.
3. Start creating automata or load a predefined example.
4. Enter an input string and run the simulation.

No backend, installation or external dependencies required.

## Supported Automata

| Type | Support |
|------|---------|
| DFA  | Yes |
| NFA  | Yes |
| ε-NFA | No |

**Note:** The simulator currently supports single-character
input symbols. Epsilon transitions and multi-character tokens
are not supported.

## Project Structure

```text
Automata-Studio/
│
├── index.html
└── README.md
