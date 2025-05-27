# ASSIGNMENT-8-COMPSCI-230-solution

Download Here: [ASSIGNMENT 8 COMPSCI 230 solution](https://jarviscodinghub.com/assignment/assignment-8-compsci-230-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Problem 1 (15+2 points)
Let T = (V, E) be a tree with n vertices and at least one edge. For any positive integer k, let yk
denote the number of vertices with degree k.
(a) (10+1 points) Prove that the following equality holds:
y1 = 2 +
nX−1
k=3
(k − 2) · yk.
(b) (5+1 points) Use part (a) to prove the following: if T is a rooted full binary tree, then T has
(n + 1)/2 leaves. (Recall that a leaf of a rooted tree is a node with zero children. Also, in a
rooted full binary tree, every node has zero or two children.)
Problem 2 (15+1 points)
Let G1 = (V1, E1) and G2 = (V2, E2) be undirected graphs. We say that G2 contains a copy of G1
if there exists a function f : V1 → V2 that satisfies the following property:
∀u, v ∈ V1. {u, v} ∈ E1 implies {f(u), f(v)} ∈ E2.
In other words, the function f should map adjacent vertices in G1 to adjacent vertices in G2.
Let T be an arbitrary tree with k vertices. Prove the following: if G is a graph whose minimum
degree is at least k − 1, then G contains a copy of T.
Hint: Recall that any tree has at least one leaf, i.e., a vertex with degree 1. Removing this
vertex (and its single incident edge) yields a tree with fewer vertices. Using this fact, proceed with
induction on k.
Problem 3 (15+1 points)
Let G = (V, E) be a directed graph, and let u, v be two vertices of G. We say that v is reachable
from u if there exists a directed path from u to v in G. Furthermore, u and v are strongly connected if v is reachable from u and u is reachable from v. Now recall that the relation {(u, v) :
u and v are strongly connected} is an equivalence relation on V , and we call each equivalence class
induced by this relation a strongly connected component of G.
Let C be a strongly connected component of G. We say that C is a source component if C does
not contain a vertex that is reachable from a vertex outside C. Now recall that when we run DFS on
G, every vertex u is assigned two positive integers pre(u) and post(u).
Prove the following: in any run of DFS on G, the vertex with the largest post-value belongs to
a source component of G.
Hint: Consider the DAG formed by the strongly connected components of G.
Problem 4 (20 points)
Programming: In Lecture 16, we gave the “cycle property” regarding minimum spanning trees
(MSTs): the heaviest edge of any cycle in the graph is not in the MST. Thus, one way to find an
MST is the following: while there exists a cycle C in the graph, remove the heaviest edge of C from
the graph. Repeat this process until the graph is acyclic, and return this final graph.
For this problem, you will implement the algorithm above as function findMST(M) where M
is a weighted adjacency matrix. As in the programming assignment of Homework 6, we assume
that the vertex set of the input is of the form {0, 1, 2, . . . , n − 1}. The weighted adjacency matrix
representation of an n-vertex undirected graph G is an n × n symmetric matrix where M[i][j]
is None if there is no edge between vertex i and vertex j in G, and otherwise it is the weight of
the edge (i, j) in G. (Recall that M is symmetric means M[i][j] = M[j][i] for every pair of
vertices i and j.) See the example graph G and its corresponding matrix M below.
To implement findMST(M), you are to use the given function findCycle(M) which returns
None if there is no cycle contained in the graph G represented by M, otherwise it returns a cycle
C represented by a list of vertices (integers between 0 and n − 1, inclusive) such that every pair
of consecutive vertices are adjacent in G, as well as the first and last vertices in C. For example,
findCycle(M) for the matrix M below might return [0,3,1], [2,3,4,0], or any other such
cycle in G represented by M. In addition, we also provide the functions isConnected(M),
isSymmetric(M), and createExampleGraph(), whose details are in the skeleton file and
may be useful when implementing or testing your solution. (The skeleton contains other functions
as well, but you should not be calling them directly, so you can ignore them.)
0
1
2
3
4
12
3
-8
5
11
-5
4
Above, the 5-vertex graph G represented by the matrix M below. The thick edges denote the
(unique) MST in G which is represented by findMST(M) below.
M =






None 12 −5 3 4
12 None None −8 None
−5 None None 5 None
3 −8 5 None 11
4 None None 11 None






findMST(M) =






None None −5 3 4
None None None −8 None
−5 None None None None
3 −8 None None None
4 None None None None






For more details, see the skeleton file and the documentation of each function.
