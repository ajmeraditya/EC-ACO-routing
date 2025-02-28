# ACO with Erasure Coding

This project simulates network performance using Ant Colony Optimization (ACO) techniques with and without erasure coding. The simulation evaluates network life, packet loss, and successful packet transmissions across multiple rounds when different routing and coding strategies are applied.

## Project Structure

- **ACO_all_nodes.py**  
  Contains the core ACO simulation logic, including:
  - **ACO_network_life**:
 calculates network life under ACO.
  - **trivial_ACO_network_life**:
 a variant of ACO network life calculation with different handling.
  - **with_erasure**:
 functions to simulate packet transmissions with and without erasure coding.
  - **plot_packet_loss**:
 used to plot simulation results for visual analysis.

- **ACO_boa_updated.py**  
  Provides an alternative implementation that compares the standard ACO approach with the BOA ACO variant:
  - **BOA_ACO_network_life**:
 computes network life for the BOA ACO variant.
  - Contains version-specific functions for routing, erasure coding, and packet loss ratio analysis.

- **Other Files**  
  - Various image files (e.g., *ACO Network Life vs BOA ACO Network Life.png*) and animations (e.g., *aco_send_data.gif*) to visualize network performance.

## How to Run

Ensure you have Python installed, then run the desired simulation script. For example, to start the ACO simulation with multiple nodes:

```sh
python ACO_all_nodes.py
```

Replace the filename if you wish to run the BOA ACO variant:


```sh
python ACO_boa_updated.py
```

## Simulation Overview
1. **Network Setup:**
The simulation sets up a network with a specified number of nodes. Each node (except the sink) participates in route establishment and data transmission.

2. **Energy and Routing:**
Functions such as trivial_ACO_network_life and BOA_ACO_network_life track node energies, adjust routes, and simulate packet loss.

3. **Erasure Coding:**
The functions with_erasure and wo_erasure_code compare the effectiveness of using erasure coding to enhance data transmission robustness.

4. **Visualization:**
The plot_packet_loss function is used to visualize the simulation outcomes like network life and packet success rates.

5. **Customization:**
You can easily adjust simulation parameters such as the number of nodes (n), energy levels, number of rounds for the simulation, and other algorithm parameters by modifying the corresponding variables within the scripts.