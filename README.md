# 8-puzzle-solver
solving the classic 8 puzzle game using JAVA

# 8-puzzle-solver
solving the classic 8 puzzle game using JAVA

##Searching algorithm used in this project is:

A* Algorithm:

1.  Initialize the open list
2.  Initialize the closed list
    put the starting node on the open 
    list (you can leave its f at zero)

3.  while the open list is not empty
    a) find the node with the least f on 
       the open list, call it "q"

    b) pop q off the open list
  
    c) generate q's 8 successors and set their 
       parents to q
   
    d) for each successor
        i) if successor is the goal, stop search
          successor.g = q.g + distance between 
                              successor and q
          successor.h = distance from goal to 
          successor (This can be done using many 
          ways, we will discuss three heuristics- 
          Manhattan, Diagonal and Euclidean 
          Heuristics)
          
          successor.f = successor.g + successor.h

        ii) if a node with the same position as 
            successor is in the OPEN list which has a 
           lower f than successor, skip this successor

        iii) if a node with the same position as 
            successor  is in the CLOSED list which has
            a lower f than successor, skip this successor
            otherwise, add  the node to the open list
     end (for loop)
  
    e) push q on the closed list
    end (while loop)
    
## Branch and Bound Algorithm (LC Search) is another popular algorithm to solve the 8 Puzzle Problem but the most efficient and hence preferred algorithms is A* algorithm due to its heuristic search methodology -
    There are many searching algorithms such as Linear Search, Binary Search, Depth-First Search, or the Breadth-First Search. These searching algorithms fall into the category of uninformed search techniques i.e. these algorithms do not know anything about what they are searching for and where they should search for it. That’s why the name “uninformed” search. Uninformed searching takes a lot of time to search as it doesn’t know where to head and where the best chances of finding the element are.

    Informed search is exactly opposite to the uninformed search. In this, the algorithm is aware of where the best chances of finding the element are and the algorithm heads that way! Heuristic search is an informed search technique. A heuristic value tells the algorithm which path will provide the solution as early as possible. The heuristic function is used to generate this heuristic value. Different heuristic functions can be designed depending on the searching problem. So Heuristic search is a technique that uses a heuristic value for optimizing the search and hence is more efficient.
