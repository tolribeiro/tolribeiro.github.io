---
layout: post
title:  "Understanding Graph Coloring (vertex): a greedy approach"
description: "Using a greedy algorithm to color vertex of a graph"
date:   2015-12-21 12:48:15
categories: graph algorithms
---

It is known that the problem of coloring a graph with the smallest number of colors needed (finding its *chromatic number*), is part of the set of NP-Complete problems.

However, there are methods that can be used to color vertices sequentially, by choosing the colors based on the colors already assigned in the vertex's neighborhood. In other words, we can use what is called a *greedy algorithm* to solve the problem.

To explore this approach, think of you having a palette with 3 colors available, and the following graph to color:

// image

Knowing that you cannot color vertices that are adjacent to each other with the same color, let's explore the step-by-step process to color the entire graph of Figure 1:

1. Let's say we choose the first color *blue* (ordered from left to right), to color vertex 1. 
2. Intuitively, we already know that vertices 2 and 3 cannot be colored by blue anymore, because they are adjacent to 1. Thus, following the order, for vertex 2 we choose the next available color and it is *red*;
3. The next vertex to color, 3, is also adjacent to 1 and 2, and by that we know that neither blue or red can be used to color it, so the next one available is *yellow*.
4. The last vertex, 4, is only adjacent to vertex 2. This tells us that the only color we cannot choose is *red*. Then going back to the first color available, vertex 4 is colored by *blue* (it could have been yellow).



