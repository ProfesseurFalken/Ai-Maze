Unzip and run using the following command line

Sample 1
python maze.py maze1.txt

Sample 2
python maze.py maze2.txt

Sample 3
python maze.py maze3.txt

For each samples, change the frontier in def solve(def) to try DFS / BFS Ai:


BFS_Ai
    def solve(self):
        """Finds a solution to maze, if one exists."""

        # Keep track of number of states explored
        self.num_explored = 0

        # Initialize frontier to just the starting position
        start = Node(state=self.start, parent=None, action=None)
        # frontier = StackFrontier() DFS
        frontier = QueueFrontier() #BFS
        frontier.add(start)

        # Initialize an empty explored set
        self.explored = set()

DFS_Ai
    def solve(self):
        """Finds a solution to maze, if one exists."""

        # Keep track of number of states explored
        self.num_explored = 0

        # Initialize frontier to just the starting position
        start = Node(state=self.start, parent=None, action=None)
	frontier = StackFrontier() DFS
        # frontier = QueueFrontier() #BFS
        frontier.add(start)

        # Initialize an empty explored set
        self.explored = set()

A png will be generated each time you run the maze.py showing the Ai research.
