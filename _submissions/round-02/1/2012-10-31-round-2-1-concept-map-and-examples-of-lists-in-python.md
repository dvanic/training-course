---
date: 2012-10-31
round: Round 2
title: 'Round 2.1 --- Concept Map and Examples of Lists (in Python)'
author: Adina Chuang Howe
permalink: /2012/10/round-2-1-concept-map-and-examples-of-lists-in-python/
tags:
  - Concept Map
---
<figure id="attachment_844" style="width: 608px;" class="wp-caption aligncenter">[<img class=" wp-image-844 " title="List-cm" src="http://files.software-carpentry.org/training-course/2012/10/Screen-Shot-2012-10-31-at-9.22.21-AM.png" alt="" width="608" height="432" />][1]<figcaption class="wp-caption-text">A concept map for lists (in Python).</figcaption></figure> 
&nbsp;

&nbsp;

A list is a data structure that maintains an ordered collection of elements.  It is mutable in that it allows you to add and remove elements from its collection.

*An illustrative example*

Tonight is Halloween and we live in a neighborhood with tons of kids.  My husband and I love to learn about human nature so we like to let the kids take as much candy as they want and analyze why the numbers vary.  Is it because their parents are with them?  Is it because they are older?  Do cuter kids take more candy?   (Note:  I would take a moderate handful, my husband would be the sucker who took only a piece).

Here's a representative list of the number of pieces of candy taken per child in order that they  came trick or treating:

>>> candy_uptake = [1, 1, 2, 1, 3, 1, 5, 1, 1, 2, 7, 1, 1, 3, 2]

How many kids took candy?  We need to know how many *elements* are in the list.

>>> len(candy_uptake)  
15

I remember that my husband made a mistake in counting the third kid's candy uptake, the kid actually took 5 pieces of candy. (With Python indexing the third kid is what *index* number?)

>>> candy_uptake[2]  
2  
>>> candy_uptake[2] = 5  
>>> print candy_uptake  
[1, 1, 5, 1, 3, 1, 5, 1, 1, 2, 7, 1, 1, 3, 2]

Now that we've fixed this error, what were the least and most candy taken?  Let's *sort* the list.

>>> sorted\_candy\_uptake = sorted(candy_uptake)  
>>> print sorted\_candy\_uptake  
[1, 1, 1, 1, 1, 1, 1, 1, 2, 2, 3, 3, 5, 5, 7]

>>> sorted\_candy\_uptake[0]  
1  
>>> sorted\_candy\_uptake[-1]  
7

*Concept reinforcement examples:*

**Find the average candy uptake.

>>> total\_candy\_uptake = sum(candy_uptake)  
>>> total\_candy\_uptake  
35  
>>> average\_candy\_uptake = ?

What were the three largest candy grabs?

>>> sorted\_candy\_uptake[?:?]

Make a list of strings and sort it.

>>> best_costumes = ['Unibomber', 'Gum on the bottom of a shoe', 'Princess Darth', 'Baby Pumpkin', 'Knight of Nee', 'Gorilla', 'Zebra']  
>>> print sorted(best_costumes)

What is this output?

>>> sorted(best_costumes)[-1]

What is this output?

*Concept extention example (iteration of lists with a for loop):*

Currently, I work at Argonne National Laboratory researching biological elements that cause intestinal diseases.  I have a lists of candidate disease-causing elements and I wanted to know how many of these elements are in a list of all observable proteins.

disease_proteins = ['virus', 'phage', 'butyrate gene']  
all_proteins = ['dna repair', 'protein synthesis', 'virus', 'recepter proteins', 'membrane proteins', 'phage']

total_disease = 0

for protein in all_proteins:  
&emsp;if protein in disease_proteins:  
&emsp;&emsp;total_disease += 1  
print 'Total disease proteins =', total\_disease, 'out of', len(disease\_proteins)  
print 'Total all proteins =', len(all_proteins)

Time taken:  2 hours

 [1]: http://files.software-carpentry.org/training-course/2012/10/Screen-Shot-2012-10-31-at-9.22.21-AM.png
