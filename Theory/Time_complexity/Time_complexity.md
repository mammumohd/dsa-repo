# Time Complexity




## Understanding Big O Notation:

- Big O notation is like a language that allows us to describe the efficiency of an algorithm
- It focuses on the rate at which the algorithm's runtime increases as the input size grows.
- Big O notation helps to find how the performance of your algorithm will change as the input size grows. But it does not tell you how fast your algorithm's runtime is.
- In a nutshell we look at the time it will take to execute each statement in the algorithm , which will gives us an idea about time complexity


## Comparing Time Complexities:

Let's look at some common time complexities and relate them to real-life scenarios:

# O(1) or Constant Time:
 
Imagine you have a recipe to make pancakes. It takes the same amount of time, regardless of the number of guests you're serving.
 
Here's a breakdown of the example:

1. Imagine you have a recipe for making pancakes, and you follow a specific set of instructions to prepare and cook them.

2. Regardless of the number of guests you're serving, the steps involved in making pancakes remain the same. You mix the ingredients, heat the pan, pour the batter, flip the pancakes, and cook them until they're done.

3. Whether you're making pancakes for one person or a hundred people, the time it takes to complete each step of the recipe remains constant.

4. The total time required to make the pancakes doesn't change as you increase the number of guests because each guest receives pancakes made in the same batch. 

This constant time complexity (O(1)) is an ideal characteristic for an algorithm since it means the runtime doesn't increase with larger inputs. It ensures that the algorithm's efficiency remains consistent regardless of the size of the problem.


# O(log n) or Logarithmic Time:

Think of finding a name in a phone book. As the number of pages doubles, the time it takes to find a name increases only slightly.

When we talk about logarithmic time complexity, we're referring to algorithms that divide the problem size in half at each step. In the case of finding a name in a phone book, the algorithm follows a logarithmic pattern.

Here's how it works:

1. Imagine you have a phone book with 1,000 pages, and you're searching for a specific name.

2. You can start by roughly dividing the phone book in half and checking the middle page. This step eliminates half of the phone book.

3. If the name you're searching for is alphabetically before the name on the middle page, you can repeat the process with the left half of the phone book.

4. Similarly, if the name is alphabetically after the middle page, you focus on the right half of the phone book.

5. By continuously dividing the remaining pages in half, you can quickly narrow down your search until you find the name you're looking for.

Now, let's see how the time complexity evolves as the number of pages doubles:

Suppose you double the number of pages to 2,000. With a logarithmic time complexity, you'd only need one extra step to find the name. It's like flipping a few more pages.

If the number of pages further doubles to 4,000, you'd require only two more steps compared to the previous case. Again, it's a minor increase in the number of steps.

The key point is that as the number of pages doubles, the number of additional steps required to find the name increases only slightly. This behavior aligns with logarithmic time complexity (O(log n)).


# O(n) or Linear Time:

Consider sorting a deck of cards. If you double the number of cards, it roughly takes twice as long to sort them.

Suppose you have a task of counting the number of elements in a list. Here's how it relates to linear time complexity:

1. Imagine you have a list of numbers, and you want to count how many elements are present in the list.

2. To accomplish this, you can iterate through the list and increment a counter for each element you encounter.

3. As the size of the list increases, the time it takes to count the elements also increases linearly.

4. Suppose it takes a certain amount of time to count the elements in a list of size 100. If you double the size of the list to 200, it would roughly take twice as long to count the elements.

5. Similarly, if you have a list four times the size (400), it would take approximately four times as long to count the elements compared to the initial list of size 100.

In this example, the time required to count the elements in the list grows in a linear fashion as the size of the list increases. The number of iterations required for counting scales linearly with the input size, resulting in a linear time complexity (O(n)).

# O ( n log n) or Linearithmic Time:

First understand a simple thing, What is log x

For simplicity lets imagine base is 2 , then the math is that 

log x = y   , IF AND ONLY IF  ,  2^y = x




Imagine you have a deck of cards that you want to sort in ascending order. You decide to use a popular sorting algorithm called Merge Sort, which has a time complexity of O(n log n).

Here's how Merge Sort works in a simplified explanation:

1. Divide: You start by dividing the deck of cards into smaller, roughly equal-sized piles.

2. Sort: For each smaller pile, you repeat the process of dividing it further until you end up with individual cards. At this point, individual cards are already considered sorted.

3. Merge: You then start merging the smaller piles back together, but in a sorted manner. You compare the top cards from each pile, place them in order, and repeat the process until all piles are merged into a single sorted pile.

Now, let's see how Merge Sort exhibits O(n log n) time complexity:

1. Suppose you have a deck of 16 cards. With Merge Sort, you would divide it into two piles of 8 cards each, then further divide those piles into four piles of 4 cards each, and so on, until you end up with individual cards.

2. The number of divisions required (log n) grows logarithmically with the input size. In this case, log base 2 of 16 is 4, meaning you perform the division process four times.

3. During the merge phase, you merge the piles in a sorted manner. For each division, you compare and merge cards, and the number of comparisons required grows linearly with the input size (n).

4. The total number of comparisons and operations performed is the product of the number of divisions (log n) and the number of comparisons per division (n). In this case, log base 2 of 16 multiplied by 16 equals 4 * 16 = 64.

Therefore, in this example, Merge Sort with O(n log n) time complexity requires a total of 64 comparisons and operations to sort a deck of 16 cards.


# O(n^2) or Quadratic Time:

Imagine you have a group of people, and you want to arrange everyone in pairs for a group photo. Let's go through the process step by step:

1. Pairing the First Person: You start by selecting the first person and pairing them with another person. This process is relatively simple because there is only one person involved, so it takes constant time (O(1)).

2. Pairing the Second Person: Now, you have two people. To pair the second person, you need to consider all the available options in the group. Since there is one person already paired, you have (n-1) remaining people to choose from. Pairing the second person requires checking all the possibilities, which takes linear time (O(n)).

3. Pairing Subsequent People: As you continue pairing each person, the number of available options decreases. For each remaining person, you need to consider all the unpaired people and select one as their pair. This process takes linear time (O(n)) for each person.

Total Time Complexity: Since you have n people in the group, the total time required to arrange everyone in pairs can be calculated by adding up the time taken for each person. As a result, the time complexity becomes O(n) + O(n) + O(n) + ... (repeated n times) = O(n^2).

Now, let's analyze how the time complexity increases when the number of people doubles:

Suppose it initially takes t units of time to organize a group photo with n people.
When the number of people doubles to 2n, the time required would increase to (2n)^2 = 4n^2.
As you can see, the time required quadruples when the number of people doubles, resulting in quadratic growth.


# O(2^n) or Exponential Time

Imagine you have a puzzle that you want to solve by trying every possible combination. Let's break down the process and understand the implications:

1. Brute Force Approach: To solve the puzzle, you consider all possible combinations or permutations of the puzzle's elements. This means trying every possible configuration until you find the correct solution.

2. Doubling the Puzzle Size: Now, let's say the puzzle initially has n elements. As you add just one more element to the puzzle, the size increases to (n+1). With each additional element, the number of possible combinations or permutations doubles.

3. Time Required: Since you're trying every possible combination, the time required to solve the puzzle increases exponentially. As the size of the puzzle increases by just one element, the time required doubles.

4. Relationship to O(2^n): The time complexity of this brute force approach can be represented as O(2^n) because the number of possible combinations doubles with each additional element, resulting in an exponential growth pattern.

To illustrate further, let's consider an example:

Suppose you have a puzzle with 4 elements. With a brute force approach, you need to consider all 2^4 = 16 possible combinations.

If you increase the puzzle size by just one element to 5, the number of possible combinations becomes 2^5 = 32. So, by adding a single element, the number of combinations doubles.

This doubling effect continues as you add more elements. For a puzzle with 6 elements, you have 2^6 = 64 combinations, and for 7 elements, you have 2^7 = 128 combinations, and so on.

Exponential time complexity (O(2^n)) indicates that the time required to solve the puzzle grows exponentially with the size of the input. As the size of the puzzle increases by just one element, the number of possible combinations doubles, resulting in an exponential increase in time required.



