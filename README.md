# Multi-controlled-U-gate

This project builds a Qiskit circuit for a multi-controlled single-qubit unitary gate $C^n(U)$. 
The circuit applies a given $2\times2$ unitary matrix $U$ to a target qubit only if all $n$ control qubits are $|1\rangle$.

This project builds a Qiskit circuit for a multi-controlled single-qubit unitary gate $C^n(U)$. The notebook writes a Qiskit function that takes two inputs: a positive integer $n$ and a matrix $U \in \text{U}(2)$ and outputs a quantum circuit on $n + 1$ qubits, with further ancillas, that implements a multi-controlled $U$ gate, $C^nU$, that is

$$C^nU|x\rangle_n|y\rangle_1 = \begin{cases} 
|x\rangle_n U|y\rangle_1, & \text{if } x = (1,1,\dots,1), \\ 
|x\rangle_n|y\rangle_1, & \text{otherwise.} 
\end{cases}$$

The construction may use any number of ancillas, arbitrary 1-qubit gates, $CX$, and Toffoli gates. 
