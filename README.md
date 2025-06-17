# Eigenvector-Preparation-Erdos-QC-Bootcamp

Implementing the Eigenvector Preparation Quantum circuit - mini-project 2 for Erdos Quantum Computing Bootcamp (in collaboration between Aayush Vijayvargia and Sandeep Joy)

1. Function create_qpe_oracle creates the Grover oracle using Quantum Phase Estimation.

    Args:
            n: The number of main qubits (for the eigenvector).
            d: The number of ancilla qubits (for phase estimation).
            U_diagonals: The diagonal elements of the unitary U.
            t: The target phase value, t, such that $e^{2*pi*i*theta(x)} = e^{2*pi*i*t}$.
    
    Returns:
            A QuantumCircuit object representing the oracle.


2. Funtion create_diffuser creates the Grover diffuser (amplitude amplification) circuit.

    Args:
            n: The number of qubits to apply the diffuser to.
    
    Returns:
            A QuantumCircuit object representing the diffuser.

3. Function prepare_eigenvector constructs the full quantum circuit to find and prepare the eigenvector |x>.

    Args:
        U_diagonals: The diagonal elements of the unitary U. 
        n: The number of main qubits. 
        d: The number of ancilla qubits for QPE precision. 
        t: The target phase value. 

    Returns:
        The final quantum circuit that prepares the state |x>.

In the main code we also test the function with an example for n=3, d=3. A target |x> and target t, that uniquely corresponds to the phase can be chosen and tested by printing the probabilities of the statevector. We demonstrate it for x = 5 and t = theta(5) = 5 / 2^3 = 5/8.
