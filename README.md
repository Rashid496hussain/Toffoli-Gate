# Toffoli Gate Example with Qiskit

## Overview
This project contains a simple Qiskit program demonstrating the use of a Toffoli gate (CCNOT), a three-qubit gate where the target qubit flips only if both control qubits are in the |1> state.

## Prerequisites
- Python 3.8+
- Qiskit library (`pip install qiskit`)
- Optional: Matplotlib for histogram visualization (`pip install matplotlib`)

## File
- `toffoli_gate.py`: Implements a quantum circuit with a Toffoli gate, simulates it, and displays the measurement outcomes.

## How to Run
1. Ensure Qiskit is installed:
   ```bash
   pip install qiskit

   Save the code in a file named toffoli_gate.py.
   
Run the script:
bashpython toffoli_gate.py

The program will:

Create a 3-qubit quantum circuit.
Apply a Toffoli gate with qubits 0 and 1 as controls and qubit 2 as the target.
Simulate the circuit using Qiskit's Aer simulator.
Print the measurement outcomes and circuit diagram.


Expected Output

The initial state is |000>, so the Toffoli gate does not flip the target qubit, resulting in the output '000' (with 1024 shots).
To observe the Toffoli gate's effect, add qc.x(0) and qc.x(1) before the Toffoli gate to set the control qubits to |1>, which will flip the target qubit, resulting in '110'.
The circuit diagram is printed in a text-based format.

Measurement outcomes: {'000': 1024}
     ┌─┐
q_0: ┤M├
     ├─┤
q_1: ┤M├
     ├─┤
q_2: ┤M├
     └─┘
c: 3/═══
