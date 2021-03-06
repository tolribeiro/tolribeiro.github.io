---
title: "Understanding Graph Coloring (vertex): a greedy approach (Part I)"
layout: post
tag: graph
blog: true
comments: false
---

It is known that the problem of coloring a graph with the smallest number of colors needed (finding its *chromatic number*), is part of the set of NP-Complete problems.

However, there are methods that can be used to color vertices sequentially, by choosing the colors based on the colors already assigned in the vertex’s neighborhood. In other words, we can use what is called a *greedy algorithm* to solve the problem.

To explore this approach, imagine that you have a palette with 3 colors available, and the following graph to color:

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/42236450-64c68876-7eea-11e8-9e70-170ec09474c6.png" width="243" height="205" class="img-responsive center-block" />
</div>
Knowing that you cannot color vertices that are adjacent to each other with the same color, the step-by-step process to color the entire graph of Figure 1 is described below:

1. Let's say we choose the first color *blue* (ordered from left to right), to color vertex 1;
2. Intuitively, we already know that vertices 2 and 3 cannot be colored by blue anymore, because they are adjacent to 1. Thus, following the order, for vertex 2 we choose the next available color and it is *red*;
3. The next vertex to color, 3, is also adjacent to 1 and 2, and by that we know that neither blue or red can be used to color it, so the next one available is *yellow*.
4. The last vertex, 4, is only adjacent to vertex 2. This tells us that the only color we cannot choose is *red*. Then going back to the first color available, vertex 4 is colored by *blue* (it could have been yellow).

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/42236488-8602ecf0-7eea-11e8-9689-28c53d8e1b36.png" width="595" height="170"/>
</div>

One of the applications that I like the most and where graph coloring can be applied is the frequency assignment in cellular networks. In order to avoid interference (or crosstalk), different frequencies are assigned to adjacent cells, and the total number of distinct frequencies should be minimized. 

Therefore, if you instead of considering the colors blue, red and yellow, consider them as frequency 1, frenquency 2 and frequency 3, the algorithm that we manually applied to the graph above could have been very useful to configure a simple cellular network or any similar schema described as a graph.

In the next part we'll be going through a C++ implementation that generates code that can be compiled in LaTeX using Tikz, where we'll be able to see it working for generic graphs.