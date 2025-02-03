# Python Examples of Computational Thinking in STEM

Computational thinking involves:
- breaking problems into smaller parts (Decomposition)
- finding recurring patterns (Pattern Recognition)
- simplifying complex problems (Abstraction)
- and designing step-by-step solutions (Algorithm Design).

Below, we analyze each code example using these key principles.

Key components: Decomposition, Pattern Recognition, Abstraction, Algorithm Design

## Physics: Modeling physical systems, simulations

```
import numpy as np
import matplotlib.pyplot as plt

g = 9.81  # gravity (m/s^2)
t = np.linspace(0, 10, 100)  # time (s)
h = 100 - 0.5 * g * t**2  # height formula

plt.plot(t, h)
plt.xlabel("Time (s)")
plt.ylabel("Height (m)")
plt.title("Free Fall Simulation")
plt.grid()
plt.show()

```

Computational Thinking Breakdown:

✔ Decomposition: Breaking the problem into components: time, gravity, height equation, and plotting.

✔ Pattern Recognition: Recognizing that motion follows a quadratic function due to acceleration.

✔ Abstraction: Using a simple mathematical formula to model real-world falling motion.

✔ Algorithm Design: Computing height at different time intervals and visualizing the motion using a graph.

## Chemistry: Molecular dynamics, data analysis

```
from rdkit import Chem

def mol_mass(smiles):
    mol = Chem.MolFromSmiles(smiles)
    return sum(atom.GetMass() for atom in mol.GetAtoms())

print(mol_mass("CCO"))  # Ethanol
```

Computational Thinking Breakdown:

✔ Decomposition: Breaking the problem into input (SMILES string), molecule parsing, and mass calculation.

✔ Pattern Recognition: Recognizing that every molecule consists of atoms with known atomic masses.

✔ Abstraction: Ignoring unnecessary molecule details and focusing only on atomic masses.

✔ Algorithm Design: Iterating over each atom in the molecule, summing up its mass, and returning the total.

## Biology: Genomics, bioinformatics, simulations

```
from Bio.Seq import Seq

seq = Seq("ATGCGTACGTTAG")
print("Reverse Complement:", seq.reverse_complement())
print("GC Content:", (seq.count("G") + seq.count("C")) / len(seq) * 100, "%")
```

Computational Thinking Breakdown:

✔ Decomposition: Breaking DNA analysis into tasks: reverse complement and GC content calculation.

✔ Pattern Recognition: Recognizing nucleotide pair rules (A-T, G-C) and counting occurrences.

✔ Abstraction: Treating DNA as a string of characters instead of biochemical structures.

✔ Algorithm Design: Creating functions that manipulate sequences using built-in string operations.

## Mathematics: Symbolic computing, optimization

```
import numpy as np

A = np.array([[3, 2], [1, 4]])
b = np.array([5, 6])
x = np.linalg.solve(A, b)

print("Solution:", x)
```

Computational Thinking Breakdown:

✔ Decomposition: Breaking the problem into matrices, solving equations, and interpreting results.

✔ Pattern Recognition: Recognizing that many real-world problems involve solving linear systems.

✔ Abstraction: Representing equations as matrices instead of writing out algebraic steps.

✔ Algorithm Design: Using a built-in numerical method to compute solutions efficiently.

## Engineering: Finite element analysis, control systems

```
import control as ctrl
import matplotlib.pyplot as plt

sys = ctrl.TransferFunction([1], [1, 2, 1])
t, y = ctrl.step_response(sys)

plt.plot(t, y)
plt.xlabel("Time (s)")
plt.ylabel("Response")
plt.title("Step Response of a Control System")
plt.grid()
plt.show()
```

Computational Thinking Breakdown:

✔ Decomposition: Breaking the problem into system definition, simulation, and visualization.

✔ Pattern Recognition: Recognizing that systems follow standard differential equations.

✔ Abstraction: Using transfer functions to simplify control system representation.

✔ Algorithm Design: Simulating a step response and plotting results to analyze system behavior.
