Download Link: https://assignmentchef.com/product/solved-blg335e-project-1
<br>
<strong> </strong>

<h1>Overview</h1>

Breadth First Search (BFS) and Depth First Search (DFS) are well-known graph traverse algorithms. In this project, you will need to implement BFS and DFS algorithms in order to solve the given problem.




<h1>Gold Miners</h1>

In this problem, your job is to place miners next to mining sites.

<ul>

 <li>Each miner can only be attached to ​<strong>a single mining site</strong>​, there are as many miners as there are mining sites.</li>

 <li><strong>The numbers across the top and down the side</strong> tell you ​<strong>how many miner</strong> are in the respective row or column.</li>

 <li>A miner can only be placed <strong>horizontally</strong>​ ​ or ​<strong>vertically</strong>​ adjacent to a mining site.</li>

 <li>Miners are never adjacent to each other, <strong>neither vertically, horizontally, nor diagonally.</strong>​ <strong>  </strong></li>

 <li>A mining site might be next to two miners, but is ​<strong>only one miner can work on a single mining site</strong>​.</li>

</ul>




An example problem and the solution can be seen below. <img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" data-recalc-dims="1">

  </noscript>

 </noscript>

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/233.png?w=980&amp;ssl=1" data-recalc-dims="1">

  </noscript>

 </noscript>

<table width="636">

 <tbody>

  <tr>

   <td width="321">The problem given in the sample input file.</td>

   <td width="315">The solution given in the sample output file.</td>

  </tr>

  <tr>

   <td width="321">  </td>

   <td width="315">  </td>

  </tr>

 </tbody>

</table>




<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>A) Implementation</h1>

<ul>

 <li>Formalize this problem in a well-defined graph form and present your state and action representations in detail.

  <ol>

   <li>Each state can be represented as a node, and placement of a new miner may lead to a new node.</li>

   <li>You are not required to optimize the search procedure. Do ​<strong>not</strong> implement any forward checking mechanisms.</li>

   <li><strong>Upon visiting a node</strong>​, ​<strong>the constraints of the node must be checked</strong>​. If the node does not meet the constraints, the node will ​<strong>not</strong>​ be expanded.</li>

  </ol></li>

</ul>




<ul>

 <li>Run both BFS and DFS algorithms ​<strong>(graph traversal version)</strong>​, and print the following information and analyze the results in terms of:

  <ul>

   <li>the number of the visited nodes</li>

   <li>the maximum number of nodes kept in the memory</li>

   <li>the running time</li>

  </ul></li>

</ul>




<ul>

 <li>The algorithm (BFS or DFS) to be used for search, the input file name and the output file name should be chosen by a command line argument as in the given example. Sample input files and output files are given. When the solution is found, you should write the results to the specified output file in the same format as the input file.</li>

</ul>




<ul>

 <li>You must use a graph representation for the model and solve it using DFS or BFS. Any other method will not be accepted.</li>

</ul>




<ul>

 <li>All your code must be written in C++, and should be compiled and run on ITU’s Linux Server (you can access it through SSH) using g++. Otherwise your code will not be evaluated.</li>

</ul>




<strong>Your program should compile and run using the following commands:</strong><strong>  </strong>

<strong>(if you have other commands for compilation, you should state them as a comment  in your code) </strong>

<strong> </strong>

<strong>g++ sourcecode.cpp –o project1 </strong>

<strong> </strong>

<strong>./project </strong>​<strong>&lt;dfs or bfs&gt; &lt;input-file-name&gt; &lt;output-file-name&gt; </strong>

<strong> </strong>

<strong>./project1 bfs input.txt output.txt </strong>

<strong> </strong>

<strong>./project1 dfs input.txt output.txt </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>Sample Input File: (input.txt)</h1>

<ul>

 <li>The number of columns and the number of rows are given in the first row. Your code might be tested with the different number of rows or columns</li>

 <li>The numbers on the second line represents the number of miners that can be placed on the column.</li>

 <li>The numbers on the first column represents the number of miners that can be placed on the row</li>

 <li>“.” represents an empty location, “s” represents a mining site and “m” represents a miner.</li>

 <li>The columns are separated by tab(t) characters, and the rows are separated by line feed(
) characters.</li>

</ul>

<strong> </strong>

<table width="624">

 <tbody>

  <tr>

   <td width="48"><strong>8</strong></td>

   <td width="55"><strong>8 </strong><strong>2</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="24"><strong>0</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>2</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="48"><strong>1</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="234"><strong>1 </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>2</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>1</strong></td>

   <td width="55"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="24"><strong>s</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>1</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>2</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="24"><strong>s</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>s </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>0</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>3</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>0</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>3</strong></td>

   <td width="55"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="24"><strong>.</strong></td>

   <td width="24"> </td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h1>Sample Output File: (output.txt)</h1>

<strong> </strong>

<table width="624">

 <tbody>

  <tr>

   <td width="55"><strong>8</strong></td>

   <td width="48"><strong>8 </strong><strong>2</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="48"><strong>0</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="48"><strong>1</strong></td>

   <td width="48"><strong>2</strong></td>

   <td width="234"><strong>1 </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>2</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>1</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>1</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>2</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="234"><strong>s </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>0</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>3</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>0</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>. </strong></td>

  </tr>

  <tr>

   <td width="55"><strong>3</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="48"><strong>m</strong></td>

   <td width="48"><strong>.</strong></td>

   <td width="48"><strong>s</strong></td>

   <td width="234"><strong>m </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Sample Output: </strong>​The numbers may not reflect the real results.

<h1>&gt; ./project1 dfs input.txt output.txt</h1>

Algorithm: DFS

Number of the visited nodes: 21

Maximum number of nodes kept in the memory: 9 Running time: 0.34 seconds

Solution is written to the file.




<h1>B) Report</h1>

<strong> </strong>

<ul>

 <li>Present your problem formulation,

  <ol>

   <li>Describe state and action representations in detail.</li>

   <li>Write your pseudo-code.</li>

   <li>Show complexity of your algorithm on the pseudo-code.</li>

  </ol></li>

</ul>




<ul>

 <li>Analyze and compare the algorithm results in terms of: ● the number of visited nodes</li>

 <li>the maximum number of nodes kept in the memory ● the running time.</li>

</ul>




<ul>

 <li>Why should we maintain a list of discovered nodes? How this affects the outcome of the algorithms?</li>

</ul>