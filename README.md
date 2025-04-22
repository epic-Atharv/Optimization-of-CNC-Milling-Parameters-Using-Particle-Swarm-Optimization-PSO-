# Optimization-of-CNC-Milling-Parameters-Using-Particle-Swarm-Optimization-PSO-

The optimization of CNC (Computer Numerical Control) machining processes is essential for enhancing productivity, product quality, and sustainability in manufacturing. This paper presents an approach for optimizing CNC milling parameters using Particle Swarm Optimization (PSO), incorporating multiple objective functions beyond traditional ones like surface roughness and machining time. The proposed model integrates critical parameters such as tool wear rate (TWR), cutting force, vibration index, power consumption, and surface integrity into a unified optimization framework. Experimental results demonstrate that the proposed PSO-based model minimizes machining time, improves surface finish, and optimizes power consumption and tool wear simultaneously. The findings offer valuable insights for improving the efficiency and quality of CNC machining processes in real-world industrial applications

1. Introduction



CNC machining is a cornerstone of modern manufacturing, enabling precision, flexibility, and automation across various industries. Optimizing machining parameters—cutting speed, feed rate, and depth of cut—has long been a key focus for improving machining efficiency and product quality. Traditionally, these optimization efforts have primarily targeted surface roughness or machining time. However, additional factors such as tool wear, cutting force, vibration, and power consumption significantly affect machining performance and sustainability, yet have often been overlooked in classical optimization models.
This research aims to bridge this gap by proposing an enhanced optimization model that incorporates multiple performance metrics. We utilize Particle Swarm Optimization (PSO), a population-based optimization algorithm, to minimize a composite objective function that accounts for machining time, surface roughness, tool wear rate, cutting force, vibration index, and power consumption. This multi-objective approach ensures a more holistic solution for CNC milling optimization, improving not only operational efficiency but also sustainability and product quality


4.1 Overview of Optimization Process
The optimization process in this study is implemented using Particle Swarm Optimization (PSO), a heuristic optimization technique inspired by social behavior in nature. The goal of the optimization is to minimize a composite objective function that takes into account several key machining parameters and performance indicators. These parameters include:
•	Cutting Speed (Vc): The speed at which the cutting tool moves along the workpiece.
•	Feed Rate (f): The rate at which the tool advances along the workpiece.
•	Depth of Cut (d): The thickness of the material layer removed during each pass.
•	Surface Roughness (Ra): The measure of the surface finish, affecting the quality of the workpiece.
•	Machining Time (T): The total time required for completing the milling operation.
•	Tool Wear Rate (TWR): The rate at which the cutting tool deteriorates during machining.
•	Cutting Force (Fc): The force exerted by the cutting tool during machining.
•	Vibration Index (Vi): The vibrations produced during the cutting process, which can affect both machining quality and tool life.
•	Power Consumption (P): The total energy consumed during the machining process.

4.2 Problem Formulation
The problem is formulated as a multi-objective optimization problem, where the objective function includes the weighted sum of the above parameters. The weights are determined based on their relative importance in the specific machining scenario. The goal is to optimize these parameters simultaneously in order to achieve an ideal balance between surface quality, machining efficiency, tool longevity, and energy consumption.
The objective function F(x)to be minimized is given by:
F(x)=w1⋅Ra(x)+w2⋅T(x)+w3⋅TWR(x)+w4⋅Fc(x)+w5⋅Vi(x)+w6⋅P(x)

Where:
•	x=[Vc,f,d] represents the decision vector of cutting speed, feed rate, and depth of cut.
•	w1,w2,w3,w4,w5,w6 are the weights assigned to each paramet



________________________________________
4.3 PSO Algorithm Setup
PSO is implemented with the following parameters:
•	Swarm Size: The number of particles in the swarm, set to 30 in this study.
•	Max Iterations: The maximum number of iterations for the algorithm, set to 100 for convergence.
•	Cognitive and Social Factors: The acceleration coefficients for individual and social learning, typically set to 2.0 for both. These coefficients help balance exploration and exploitation in the solution space.
•	Inertia Weight: The inertia weight controls the impact of the previous velocity in determining the next particle's velocity. It is initialized to 0.9 and gradually decreased to encourage convergence.

4.4 Constraints
The optimization problem is subject to bounds on the cutting parameters:
•	Lower Bounds: Cutting speed Vc=100Vc = 100Vc=100, feed rate f=0.05f = 0.05f=0.05, depth of cut d=0.5d = 0.5d=0.5.
•	Upper Bounds: Cutting speed Vc=300Vc = 300Vc=300, feed rate f=0.3f = 0.3f=0.3, depth of cut d=2.0d = 2.0d=2.0.
These bounds reflect practical limits in the machining process based on the type of material and the CNC machine capabilities.


4.5 Simulation Environment
The implementation was carried out in Python using the PySwarm library, which provides an efficient interface for implementing PSO. The optimization algorithm is designed to adjust the cutting parameters iteratively, evaluating the objective function at each iteration and adjusting the particle positions based on their personal best and global best positions.
The simulation also logs the objective function values at each iteration, which are plotted to show the convergence behaviour of the optimization algorithm.




![image](https://github.com/user-attachments/assets/b97faf85-d03d-4faa-9885-a100b02224fb)

5.2 PSO Optimization
PSO was implemented with the following parameters:
•	Lower bounds: [100, 0.05, 0.5]
•	Upper bounds: [300, 0.3, 2.0]
•	Swarm size: 30 particles
•	Maximum iterations: 100


