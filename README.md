# MIT-IQuHacks-Quantum-Factorization

# **Quantum Factorization Using Shor's Algorithm**

## **🔹 Overview**
This project implements **Shor's Algorithm** for **integer factorization** using **Quantum Computing**.  
The algorithm is optimized to work on **Quantum Rings hardware** and utilizes **classical order finding**  
to enhance reliability.

### **✨ Key Features**
- ✅ **Efficient Modular Exponentiation**  
- ✅ **Classical Order Finding for Robust Factorization**  
- ✅ **Quantum Circuit Visualization & Histogram Plotting**  
- ✅ **Dynamic Base Selection for Best Results**  

---

## **🛠️ How It Works**
Shor’s Algorithm factorizes a **semiprime number** \( N = p \times q \) by:
1. **Selecting a random coprime base \( a \)**.
2. **Finding the order \( r \)** where \( a^r \equiv 1 \mod N \) using classical methods.
3. **Computing factors using \( \gcd(a^{r/2} - 1, N) \) and \( \gcd(a^{r/2} + 1, N) \)**.
4. **Executing an optimized quantum circuit for modular exponentiation**.
5. **Visualizing results using a quantum circuit diagram and a histogram**.

---

## **📂 Implementation Details**
- The quantum circuit is executed using **Quantum Rings hardware**.
- A **precomputed modular exponentiation circuit** optimizes performance.
- The **continued fractions method** refines order finding for accuracy.
- A **dynamic base selection mechanism** ensures correct factorization.

### **📌 Code Breakdown**
- `modular_exponentiation(qc, base, exponent_register, target_qubit, N)`:  
  **Optimized quantum circuit** for modular exponentiation.  
- `find_order_classically(base, N)`:  
  **Classical function** to compute the period \( r \) of \( a^r \equiv 1 \mod N \).  
- `plot_circuit(qc)`:  
  **Plots the quantum circuit diagram**.  
- `plot_histogram(counts)`:  
  **Displays a histogram with states on the y-axis and counts on the x-axis**.  

---

## **📖 Reference**
This implementation is based on concepts discussed in:  
**_"On the Various Ways of Quantum Implementation"_**,  
which explores different quantum computational techniques.  
The PDF **On_the_Various_Ways_of_Quantum_Implementation.pdf** is included in this repository.

### Setting Up the Environment

This project includes a `requirements.txt` file that lists all the Python packages and their versions used in this project. You can use this file to recreate the exact environment required to run the code.

## Free Access to Best-in-class Simulation

In order to utilize the code you would need to obtain API key for QuantumRings.

1. Register for free at [www.QuantumRings.com](https://www.quantumrings.com)
2. Confirm your email
3. Select "Manage Keys" and you should have access to free API keys.
4. Copy the key, and use it to start simulating massive circuits locally! **NB: Free API key grants 200 qubits only**

---

## **⚡ Performance & Limitations**
✅ **Successfully factorizes numbers up to** `20841207`  
✅ **Uses only 29 quantum gates for this limit**  
✅ **Extracts factors** `15727` and `13241` **accurately**  

❌ **Quantum hardware noise can affect results**  
❌ **Performance depends on base selection for efficient factorization**  
