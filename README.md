# Visual implementation of CAA algorithm with example usage
Java implementation of the Crossbar Adaptive Array (WIP) with usage

![screenshot2](https://github.com/Tanevski3/caa-experimentation/blob/master/i2.png)

![screenshot1](https://github.com/Tanevski3/caa-experimentation/blob/master/i1.png)

![screenshot3](https://github.com/Tanevski3/caa-experimentation/blob/master/i3.png)

# Requirements

 - Java 1.8
 - Maven
 
# Nice to have
 - IntelliJ

# Install
 - `git clone https://github.com/Tanevski3/caa-experimentation.git`
 - `cd ./caa-experimentation`
 - `mvn clean install`
 
# Run
 - Find `MainEntry.java` in `console` or `gui`, then right click and run
 
# Deploy
 - `cd gui`
 - `mvn jfx:jar`
 - `mv gui/target/jfx/app/caa-experimentation-gui-${version}-jfx.jar gui/target/jfx/app/caa-experimentation-gui-${version}.jar`
 - `zip gui/target/jfx/app/. caa-experimentation-gui-${version}`
 - `rm -rf dist/*`
 - `mv caa-experimentation-gui-${version}.zip ../dist/`

# Usage Guide
 
Once "File -> Open Graph" is clicked a file selection window will appear, where the user can browse through its filesystem to select a graph for loading into the software.
 
In the bottom right corner just above the Open & Cancel buttons there is a list of all supported formats for loading graphs. At the time of writing this paper, GraphML format is the only format that is supported. Once a graph is loaded into the software the working space should be filled with rendering of the graph.  

## Changing preferences
The outlook of the graph displayed in the main area can be modified through File -> Preferences. Besides, the color of the nodes & edges within Preferences edge width & vertices labels could also be modified. Additionally, some properties specific to the experiment can be modified; that is the CAA tab.
  
## Experimenting
Experimenting is divided in two menu-items:
1.	Agent Traversal
2.	Find Happy State
 
Experiments can be executed with different properties. Clicking on one of the menu items will show a popup for selecting properties of the algorithm used for a traversal. Properties are as follows:
•	Agent traversing algorithms: original & advanced
•	Experiment animation 
•	Selecting initial values.
 
Once "Find Happy State" experiment is being ran, results will be generated in a separate tab. For agent traversal there are no results.
The results relate to the graph that is being experimented on.

## Experiment Results
The experiment results split in two parts.
1.	Overall vertices traversals tab contains the following data
    a.	Vertices occurrences per generation is showing how many traversals have occurred for each vertex
    b.	"Happy" vs "Sad" generation is showing how each generation ended
    c.	"Happy to shortest" path factor is the percentage of edges that match from the happy path to the shortest path 
2.	Vertices traversals per generation tab goes more intro details about a single generation. It shows the increments, traversed edges, increments weight & traversal weight. The results are being paged depending on the number of generations.

## Viewing additional statistics & shortest path
Additionally, the software provides a visualization of the shortest path & vertices distribution. That can be done through the View menu.

# Available as JAR
 - The application is now available as a JAR file. Within the `dist/` directory of this repository the executable JAR file can be found.

Check console and generated graph for results or use the application to run own simulations or traversals

# Future
 - Increase unit test coverage for `caa-lib` to 100% (current is 90%)
 - Support for other formats then `graphml`
 - Rename `happy` & `sad` to something else

