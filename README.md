# Pokemon Cellular Automata Simulation

**Things learnt/applied** - Python, Cellular Automata Simulation, Pygame, Pattern-Visualization.

## The Idea
Welcome to the Pokemon Cellular Automata Simulation! This project demonstrates the principles of cellular automata through the interactions of Pokemon on a hexagonal grid.

![Startgame3](https://github.com/user-attachments/assets/4142380c-986c-47ff-9216-a708441eb169)


**What is Cellular Automata ?**
Cellular Automata (CA) are computational models used to simulate complex systems and processes. They consist of grid of cells and each of these cells can be in one of a finite number of states (like "dead" or "alive", "on" or "off"). The state of each cells changes according to the set of rules over discrete time steps based on the states of neighbouring cells.
One of the most famous examples of CA system is Conway's Game of Life which simulates the processes of life, death and population dynamics -- read [here](https://www.bing.com/ck/a?!&&p=8ef00c271f50e45eJmltdHM9MTcyOTkwMDgwMCZpZ3VpZD0xZDU0YjY2Yy0wNjUzLTZhMTItMGVjNC1hNDAzMDc1NTZiODYmaW5zaWQ9NTE5Nw&ptn=3&ver=2&hsh=3&fclid=1d54b66c-0653-6a12-0ec4-a40307556b86&psq=conway%27s+game+of+life+wiki&u=a1aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvQ29ud2F5JTI3c19HYW1lX29mX0xpZmU&ntb=1). While the game of life is set of simple rules it can simulate complex behaviours and has been used to explore concepts across several fields like computer science, philosophy etc. 

## Overview

This simulation models a grid-based world where Pokemon of different types interact according to predefined rules. 

![startgame1](https://github.com/user-attachments/assets/a7bc119b-afde-4d64-98ae-145c30a3dec0)

*This is how the simulation starts with random placement of each type in any cell*

Each Pokemon type has strengths and weaknesses, leading to dynamic and emergent behaviors as they move and compete for dominance. Each pokemon represents one type(written inside the hexagon) and can overpower exactly the 2 types written outside of the hexagon.

![Power_Structure4](https://github.com/user-attachments/assets/458355c2-019f-4f5e-bfbd-741710cf7a26)
*Power Structure.* 


## Features

- **Hexagonal Grid**: The simulation uses a hexagonal grid, providing a unique and visually appealing layout for the Pokemon interactions.
- **Dynamic Interactions**: Pokemon move, interact, and overpower each other based on their types, showcasing emergent behavior. (Emergent behavior in cellular automata refers to complex patterns and behaviours that arise from the simple, local interactions of individual cells. This phenomenon is fascinating because it shows how simple rules can lead to unexpected, unique and intricate outcomes.)
- **Visualization with Pygame**: The simulation is visualized using Pygame, allowing you to see the Pokemon in action.

## Cellular Automata Principles

This project is an application of cellular automata, a computational model used to simulate complex systems. Key principles include:

- **Grid-Based Structure**: The hexagonal grid represents the environment where Pokemon interact.
- **Discrete Time Steps**: The simulation evolves in discrete time steps, with each step representing a new generation of interactions.
- **Local Interaction Rules**: The behavior of each Pokemon is determined by simple rules based on the states of neighboring cells.

## Getting Started

### Prerequisites

- Python 3.x
- Pygame

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/nikhilgrad/Cellular-Automata-meets-Pokemon.git
   
   cd Cellular-Automata-meets-Pokemon
   ```

2. Install the required libraries:
   ```bash
   pip install pygame
   ```

### Running the Simulation

To run the simulation, execute the following command:
```bash
python Pokemon.py
```

## Code Structure

- `Pokemon.py`: The main script to run the simulation.
- `hexalattice/`: Contains the hexagonal grid creation logic.
- `images/`: Directory containing Pokemon images.

## How It Works

1. **Initialization**: The grid is initialized with Pokemon placed randomly.
2. **Movement and Interaction**: Pokemon move to neighboring cells and interact based on their types.
3. **Emergent Behavior**: Over time, complex patterns and behaviors emerge from the simple interaction rules.

**Some of the Structures and Patterns observed**

![endgame2](https://github.com/user-attachments/assets/7f4808e4-53d1-4633-943c-185d9755e275)

*3 type structure with infinitely changing patterns*

This type of structure is observed when each of the 3 types remaining can overpower only one of the  remaining 2 types i.e. "each one, defeat one" creating a triangular overpowering cycle resulting in an infinite loop where the simulation never ends as none of the 3 can completely win. The pattern that is created by 3 type structure's pokemon's capturing of cells shows movement across the complete hexagonal mesh till the simulation is stopped. This type of patterns that move across the cell have been termed as **spaceships** in **Conway's Game of Life**.


![endgame1](https://github.com/user-attachments/assets/e4d6a3be-3dc9-4588-b179-c42f8654a763)

*2 type structure creating Still lifes i.e. Stable patterns*

This structure is seen when any 2 pokemon types that cannot overpower each other (refer the power structure image given above) remains at the end. For e.g the fire type and electric type cannot overpower each other so they together will takeout any other that is remaining and if only this 2 remain at the end the simulation is stopped. As in this type of structure the pattern do not change over time this type of stable patterns are called as **Still Lifes** in **Conway's Game of Life**.

![endgame3](https://github.com/user-attachments/assets/4887302c-9aff-4070-96c6-2e2488ee99ac)

*Moving towards a Single-type structure*

This happens when the only one type of pokemon remains thus capturing all the cells in the hexagonal mesh. As we see in the above image the 2 types that remain are rock and fire, and if we go through the overpowering structure then we would know that in time the rock type will overpower the fire type resulting in complete capture of all grids shown in the image below. I have named this pattern as **Dominance** pattern.

![endgame4](https://github.com/user-attachments/assets/189938db-f6a6-4f9d-b6c1-7fd9e48e179a)

*Single-type structure resulting in unchanging stable patterns*  


## Future Enhancements

- **Dual-Type Pokemon**: Incorporate Pokemon with dual types for more complex interactions.
- **Evolution Mechanics**: Implement evolution rules for Pokemon to evolve into stronger forms.
- **Special status**: Add special status for e.g a fire Pokemon burns other pokemons inflicting damage, an electric type paralyzes others decreasing their speed,  a water type heals itself etc.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve the simulation.

## License

This project is licensed under the MIT License.

## Acknowledgments

Inspired by the principles of cellular automata and the dynamic world of Pokemon.
