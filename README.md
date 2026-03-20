# cross-less

This Java application allows you to visualize and manipulate graphs with embedded points. It provides functionalities to apply random layouts, clustering layouts, and minimize crossings in the graph. The application utilizes a GUI interface to display the graph and points.

## Prerequisites
- Java Development Kit (JDK) installed
- Java IDE or compiler to run the application

## Getting Started
1. Clone or download the project files from the repository.
2. Open the project in your Java IDE or compile the `App.java` file using the Java compiler.

## Usage
1. Run the application by executing the `App` class's `main` method.
2. You will be prompted to enter an instance file number. The instance file contains graph data in JSON format. Enter a valid instance file number to proceed.
3. The application will initialize with the provided graph data and display the graph and points in a separate window.
4. The number of crossings in the graph will be shown in the console.
5. If you choose to continue, the following routines will be executed:
   - **Random Layout Routine**: This routine randomly rearranges the positions of the points and displays the updated graph. The number of crossings will be shown in the console. You can export the updated graph data if desired.
   - **Force Directed Spatialization Routine**: This routine applies a force-directed graph layout algorithm (with/without (hierachical) clustering). It iteratively applies attractive and repulsive forces to the nodes to find an optimal spatialization. The resulting node labels will be displayed in the console, and the updated graph will be shown.
   - **Minimize Crossings Routine**: This routine minimizes the crossings in the graph using an optimization algorithm. You can choose to show the algorithm execution (slows down the process) and set a limit on the number of iterations. You need to provide a temperature value and a cooling rate for the optimization algorithm. The updated graph with minimized crossings will be displayed, and the number of crossings reduced will be shown in the console. You can export the updated graph data if desired.
6. If you choose to export graph data, you will be prompted to enter a file path. Enter a valid file path to export the graph data in JSON format.
7. After completing your routines, you will be asked if you want to continue. Enter 'y' to start again or 'n' to exit the application.

## File Structure
- `App.java`: Contains the main class of the application responsible for running the routines and managing user input.
- `Graph.java`: Represents the graph data structure and provides operations for counting crossings, applying random layouts, and minimizing crossings.
- `Node.java`: Represents the node data structure.
- `Edge.java`: Represents the edge data structure.
- `Position.java`: Represents a position with x and y coordinates.
- `CrossingOptimizer.java`: Implements the crossing minimization algorithm using simulated annealing.
- `Helpers.java`: Provides helper methods for user input, console clearing, and affine transformation...
- `Experiment.java`: Class to run experiments on different configuration/combination of algorithms with measurements of three metrics (time, memory and number of crossings).

## Dependencies
- Java AWT (Abstract Window Toolkit) for GUI components and graphics.
- Java IO for file input/output operations.
- Java Util for various utility classes and data structures.
- JSON-java library for parsing and creating JSON objects.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgments
The code for this application was developed by Gary KLAJER.
