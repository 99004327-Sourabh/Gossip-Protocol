# Gossip and Push-Sum Simulation Project

This project simulates the Gossip and Push-Sum algorithms using the Akka actor model in F#. It explores how these algorithms perform under various network topologies to provide insights into distributed systems dynamics and the effectiveness of different communication protocols in achieving convergence.

## Installation

### Prerequisites
- .NET SDK 5.0 or later
- F# compiler

### Getting Started

To set up the project, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/99004327-Sourabh/Gossip-Protocol.git
cd Gossip-Protocol
dotnet build
Usage Instructions
To run the simulation, you need to provide the number of nodes, the chosen topology, and the algorithm. Available topologies include full, 2D, line, and imp3D, while the algorithms can be gossip or pushsum.

bash
Copy code
dotnet run -- <numNodes> <topology> <algorithm>
# Example:
dotnet run -- 100 2D gossip
Simulation Components
State Definitions
SimulatorState: Maintains the number of nodes, topology, and algorithm in use.
NodeState: Manages the state of individual nodes, including neighbors, rumor frequency, and other metrics relevant to the chosen algorithm.
Message Types
Messages are used to facilitate communication between actors, such as initiating gossip or computing and propagating sums.

Actor Definitions
Node Actor: Simulates the behavior of a network node responding to messages.
Simulator Actor: Manages the simulation setup, including node configuration and algorithm initiation.
Convergence Measurement
The simulation measures the time it takes for all nodes to reach convergence under the specified algorithm and topology, displaying the results in the console.

Key Features
Flexible Topology Setup: Allows simulation under various network topologies.
Real-Time Convergence Tracking: Monitors the progress and effectiveness of the algorithms in real-time.
Scalability: Designed to handle a significant number of nodes efficiently.
Limitations
Assumes a fully reliable network without simulating message loss.
Performance may decrease with very large networks due to overhead in actor management.
Contributing
Contributions are welcome! Please feel free to open an issue to discuss proposed changes or create a pull request with your improvements.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.

Acknowledgments
Developed as part of the coursework for COP5615 - Distributed Operating System Principles at the University of Florida.
Thanks to the Akka.NET framework and the supportive F# community for enabling this project.

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgments

- Developed as part of the coursework for COP5615 - Distributed Operating System Principles at the University of Florida.
- Thanks to the Akka.NET framework and the supportive F# community for enabling this project.
