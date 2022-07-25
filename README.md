# Sorting-and-Searching-Algorithms
Some searching and sorting methods are explained with examples.
<br>

## Sorting
Sorting is the action of ordering the numbers from less to most.
There are several methods to sort series. They are separated from each other
depending on the way we sort and time complexities.
<br>
## Time Complexity
Time Complexity measures the performance of the algorithms by using time. The performance
may depend on both series's lineup and the sorting's type.
Consider you have a series that is not sorted. We are looking for a number.
There are 3 cases.
<br>**Worst Case:** The number we are looking for is at the end of the series.
<br>**Average Case:** The number is in the middle of the array.
<br>**Best Case:** The number is at the beginning of the array.

### 1) Insertion Sort
One of the simplest sorting algorithms. It starts from the first index and
compares the others until it finds a number smaller than it. After, the first
integer and the smaller index change their places. Now, the algorithm looks for
the second integer. If it is greater than the first integer, the algorithm checks for the third integer.
If it is greater than the first two, it continues. However, if it is smaller than the first two integers,
it changes place one step until it's the correct place.
<br>Best Case:n
<br> Average Case:n^2
<br> Worst Case:n^2
<br><p align="center">![Alt Text](https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif) </p>
**example:**
<br>[22,27,16,2.18,6]
<ol>
  <li>Sort the array with Insertion Sort.</li>
  <li>Write Big-O Notation</li>
  <li>Write Time Complexities</li>
  <li>After the array is sorted, which case does the number 18 fall into?</li>
</ol>

<ol>
  <li>[22,27,16,2,18,6]
<br>[16,22,27,2,18,6] ->There are 2 semi steps
<br>[2,16,22,27,18,6] ->There are 3 semi steps
<br>[2,16,18,22,27,6] ->There are 2 semi steps
<br>[2,6,16,18,22,27] ->There are 4 semisteps</li>
  <li>Big-O=n^2</li>
  <li>Best Case:n
<br> Average Case:n^2
<br> Worst Case:n^2</li>
  <li>Average Case since it stands in the middle of the array.</li>
</ol>

**example:**
[7,3,5,8,2,9,4,15,6] Sort the array with Insertion Sort.

[7,3,5,8,2,9,4,15,6]
<br>[3,7,5,8,2,9,4,15,6]
<br>[3,5,7,8,2,9,4,15,6]
<br>[2,3,5,7,8,9,4,15,6]
<br>[2,3,4,5,7,8,9,15,6]
<br>[2,3,4,5,6,7,8,9,15]
### 2) Merge Sort
When we consider performance as Time Complexity Merge Sort sorts an array faster than
Insertion Sort. First, it divides the array into small pieces by dividing them by 2.
Then, it sorts every little piece and unites them as sorted.
<br>Best Case:nlog(n)
<br> Average Case:nlog(n)
<br> Worst Case:nlog(n)
<br><p align="center">![Alt Text]( https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif?20151222172210
) </p>
**example:**
<br> [16,11,21,8,12,22] Sort the array with Merge Sort
<br><p align="center">![Alt Text](merge-example.png) </p>

### 3) Quick Sort
When we sort an array with Quick Sort, the algorithm picks a random number named "pivot" as an example.
A pivot is a number in the array.
The numbers which are smaller than the pivot goes the left of the array, and the greater ones
go to the right of the array. After that, we can think of the numbers left of the pivot and the right of the pivot
as subarrays and they have their pivot. That operation continues after the array is sorted.
<br>Best Case:nlog(n)
<br> Average Case:nlog(n)
<br> Worst Case:n^2
<br><p align="center">![Alt Text](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

## Searching
Searching is the action of searching a wanted number in the array. There are some searching algorithms
to find a number we want. Time complexity may depend on both the unsorted array's lineup and the algorithm's type.
###1) Linear Search
The Linear Search algorithm starts from the first integer of the array and continues until
it finds the number.
In the Worst Case, if we want to find an integer that is at the end of the array, we have to search every
integer on the array. So, for an array that's size is n, the time complexity will be n.
When we consider that situation, the Time Complexity of the Worst Case is n.
<br><p align="center">![Alt Text](https://i.pinimg.com/originals/5a/9a/42/5a9a4231aa995d2bec0781c6972f6032.gif
) </p>
### 2) Binary Search
That searching algorithm sorts the unsorted array before searching. After sorting the array
divides the array into 2. It looks at the index that is placed in the middle of the array.
If the number is greater than the middle index, the algorithm will not search the number left part of the middle index.
The process's reverse is valid if the number is less than the middle index.
Big-O Notation of the Binary Search is Nlog(n)
<br><p align="center">![Alt Text](https://d18l82el6cdm1i.cloudfront.net/uploads/bePceUMnSG-binary_search_gif.gif
)</p>
<br>
The comparison of the Linear Search and Binary Search:
<br><p align="center">![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--PNWqc_R9--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gb49p4klebgbtdwijpak.gif)

### 3)Binary Search Tree
As its name, Binary Search Tree creates a tree and makes its search in that tree easily.
There are some steps for creating the Binary Search Tree.
<li>Sort the unsorted array
  <li>If it is the sorted middle of the array is selected as root If it's not, the first element is root..</li>
<li>Root's left contains the numbers that are smaller than root, and right contains numbers that are greater than root.
<li> Until every item in the array finds a place in the tree, the algorithm stops.</li>

<br></li></ol>
<br><p align="center">![Alt Text](https://blog.penjee.com/wp-content/uploads/2015/12/optimal-binary-search-tree-from-sorted-array.gif)
</p>

**example:**
<br>[7,5,1,8,3,6,0,9,4,2] Write the Binary-Search-Tree stages of the sequence.

<ul>
  <li>7 is the root.</li>
  <li>5 will be placed on the left of the root. 1 will be placed on the left of the 5 node </li>
  <li>8 will be placed right of the root.</li>
<li>These operations will continue until every integer finds a place in the tree.</li>
</ul>
Final Version of the tree

<br><p align="center">![Alt Text](binary-search-tree.png) </p>

