# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

Using the values of Good, Big, and Small, we can see that there are 4 scenarios within the median of three method. First, the simple one where are values are Good (GGG). Next, we have 2 Good values, and one Big value (BGG, GBG, GGB). Third we have 2 Good values and one Small (SGG, GSG, GGS). And lastly, where they are all different (GBS, GSB, SGB, BGS, BSG, SBG). Using the 1/2 base probability, we can calculate the overall probability based on each scenario above. On the first scenario, there is 1/2 chance for each value, or $$(1/2)^3 = 1/8$$. Next, we can use both scenario 2 and 3 together, since they are very similar. So instead of using 1/2, we can use 1/4. This is equal to $$((1/2)^2 * (1/4)) * 6 = 3/8$$. Lastly, only one value is considered good so it is equal to $$((1/2) * (1/4)^2) * 6 = 3/16$$. We can then add all of the final values together to get an answer of 11/16 or 68.75%. Using this method, we can see that the median of three method would in fact be better than the 50% chance of the first value being a good pivot.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
