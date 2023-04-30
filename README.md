Download Link: https://assignmentchef.com/product/solved-cs301-homework-1-asymptotic-growth-and-recurrences
<br>
Problem 1 (Asymptotic Growth) Rank the following functions by nondecreasing order of growth; that is, find an arrangement <em>g</em><sub>1</sub><em>,…,g</em><sub>10 </sub>of the functions satisfying <em>g</em><sub>1 </sub>= <em>O</em>(<em>g</em><sub>2</sub>), <em>g</em><sub>2 </sub>= <em>O</em>(<em>g</em><sub>3</sub>), …, <em>g</em><sub>9 </sub>= <em>O</em>(<em>g</em><sub>10</sub>). All the logs are in base 2.

Problem 2 (Recurrences) Give an asymptotic tight bound for <em>T</em>(<em>n</em>) in each of the following recurrences. Assume that <em>T</em>(<em>n</em>) is constant for <em>n </em>≤ 2.

<ul>

 <li><em>T</em>(<em>n</em>) = 2<em>T</em>(<em>n/</em>2) + <em>n</em><sup>3</sup></li>

 <li><em>T</em>(<em>n</em>) = 7<em>T</em>(<em>n/</em>2) + <em>n</em><sup>2</sup></li>

</ul>

√

<ul>

 <li><em>T</em>(<em>n</em>) = 2<em>T</em>(<em>n/</em>4) + <em>n</em></li>

 <li><em>T</em>(<em>n</em>) = <em>T</em>(<em>n </em>− 1) + <em>n</em></li>

</ul>

Problem 3 (Binary Search – Python) Consider the two algorithms for binary search, shown in Figures 1 and 2.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> Each algorithm takes a sorted list of numbers, alist, and a number, item, and returns true if and only if item is an element of alist. The algorithm shown in Figure 1 is iterative whereas the algorithm shown in Figure 2 is recursive.

def binarySearch(alist,item): first = 0 last = len(alist)-1 found = False

while first&lt;=last and not found: midpoint = (first + last)/2 if alist[midpoint] == item:

found = True

else:

if item &lt; alist[midpoint]:

last = midpoint-1

else:

first = midpoint+1

return found

Figure 1: Iterative binary search

def binarySearch(alist,item):

if len(alist) == 0:

return False

else:

midpoint = len(alist)/2 if alist[midpoint] == item:

return True

else:

if item&lt;alist[midpoint]:

return binarySearch(alist[:midpoint],item)

else: return binarySearch(alist[midpoint+1:],item)

Figure 2: Recursive binary search

In the following, <em>n </em>is len(alist).

<ul>

 <li>According to the cost model of Python, the cost of computing the length of alist of size <em>n </em>using the function len is <em>O</em>(1), and the cost of extracting a slice of a list using : (e.g., alist[0:n/2]) is <em>O</em>(<em>n</em>). Based on this cost model:

  <ul>

   <li>What is the asymptotic running time of the iterative binary search algorithm shown in Figure 1? (State the running time and give an upper bound for it.)</li>

   <li>What is the asymptotic running time of the recursive binary search algorithm shown in Figure 2? (State a recurrence and solve it.)</li>

  </ul></li>

 <li>Implement these two algorithms using Python. For each algorithm, determineits scalability experimentally by running it with different sized sorted lists of numbers in the worst case. For instance, you can generate a sorted list of <em>n </em>numbers ranging between 1 and 10<sup>7 </sup>(using range function of Python) and search for 1.

  <ul>

   <li>Fill in following table with the running times in seconds.</li>

  </ul></li>

</ul>

<table width="0">

 <tbody>

  <tr>

   <td width="77">Algorithm</td>

   <td width="65"><em>n </em>= 10<sup>4</sup></td>

   <td width="65"><em>n </em>= 10<sup>5</sup></td>

   <td width="65"><em>n </em>= 10<sup>6</sup></td>

   <td width="65"><em>n </em>= 10<sup>7</sup></td>

  </tr>

  <tr>

   <td width="77">Iterative</td>

   <td width="65"> </td>

   <td width="65"> </td>

   <td width="65"> </td>

   <td width="65"> </td>

  </tr>

  <tr>

   <td width="77">Recursive</td>

   <td width="65"> </td>

   <td width="65"> </td>

   <td width="65"> </td>

   <td width="65"> </td>

  </tr>

 </tbody>

</table>

Specify the properties of your machine (e.g., CPU, RAM, OS) where you run your programs.

<ul>

 <li>Plot these experimental results in a graph.</li>

 <li>Discuss the scalability of the algorithms with respect to these experimental results.</li>

 <li>Determine whether the experimental results confirm the theoretical results you found in (a).</li>

</ul>

<ul>

 <li>For each algorithm, determine its average running time experimentally by running it with randomly generated sorted lists of <em>n </em>numbers, and randomly generated keys. For instance, for each randomly generated list of size <em>n</em>, you can generate 50 different keys.

  <ul>

   <li>Fill in following table with the average running times in seconds (<em>µ</em>), and the standard deviation (<em>σ</em>).</li>

  </ul></li>

</ul>

<table width="0">

 <tbody>

  <tr>

   <td rowspan="2" width="78">Algorithm</td>

   <td colspan="2" width="68"><em>n </em>= 10<sup>4</sup></td>

   <td colspan="2" width="68"><em>n </em>= 10<sup>5</sup></td>

   <td colspan="2" width="68"><em>n </em>= 10<sup>6</sup></td>

   <td colspan="2" width="66"><em>n </em>= 10<sup>7</sup></td>

  </tr>

  <tr>

   <td width="26"><em>µ</em></td>

   <td width="42"><em>σ</em></td>

   <td width="26"><em>µ</em></td>

   <td width="42"><em>σ</em></td>

   <td width="26"><em>µ</em></td>

   <td width="42"><em>σ</em></td>

   <td width="26"><em>µ</em></td>

   <td width="40"><em>σ</em></td>

  </tr>

  <tr>

   <td width="78">Iterative</td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="40"> </td>

  </tr>

  <tr>

   <td width="78">Recursive</td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="42"> </td>

   <td width="26"> </td>

   <td width="40"> </td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Plot these experimental results in a graph.</li>

 <li>Discuss how the average running times observed in your experimentsgrow, compared to the worst case running times observed in (b).</li>

</ul>

<ul>

 <li>How can we improve the recursive binary search algorithm so that it has thesame asymptotic running time as the iterative one? (Make sure that the algorithm is still recursive after the improvements.)</li>

</ul>

Do we observe this improvement experimentally? (Redo the experiments in (b) for the worst-case analysis, with the improved binary search algorithm. Plot the running times of the given iterative algorithm, the given recursive algorithm, and the improved recursive algorithm as a graph.)

<a href="#_ftnref1" name="_ftn1">[1]</a> These algorithms are taken from the book “Problem Solving with Algorithms and Data Structures using Python” by Miller and Ranum: http://interactivepython.org/ runestone/static/pythonds/index.html .