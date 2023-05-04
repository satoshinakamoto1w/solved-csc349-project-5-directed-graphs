Download Link: https://assignmentchef.com/product/solved-csc349-project-5-directed-graphs
<br>
<strong><u>Part 1 of 4</u></strong>

<strong><u>Note</u></strong><strong>:</strong> some  <em>LinkedList </em>class methods you may need: <em>add, remove, contains </em>to add, delete and search for the given item, <em>size() </em>to get the length of the list, and <em>get(int  x)</em> to get the element at <em>x</em> index (indexing starts at 0).

<ol>

 <li><strong>Define a class <em>DiGraph </em>to implement a directed graph as an array of Adjacency Linked Lists. </strong>Vertices are numbered by integers <strong>0 through N-1</strong> (N is the number of vertices in the graph). <em>DiGraph</em> class contains one <em>private</em> instance variable, one constructor and 5 <em>public</em> methods:

  <ol>

   <li>One <strong>private</strong> instance variable: this is an <strong>array</strong> of linked lists (<strong>use Java’s <em>LinkedList</em> class</strong>).</li>

   <li>A <strong><em>constructor</em></strong> with one <em>int</em> type parameter for N. This constructor creates and initializes the instance variable-array.</li>

   <li>A public method <strong><em>addEdge(int from, int to)</em></strong> where two parameters identify vertices representing the edge that needs to be added to the graph (<em>to </em>vertex is added as <em>from</em> vertex’s neighbor).</li>

  </ol></li>

</ol>

<strong><u>Important</u></strong>: the edge should <strong>not</strong> be added if it already exists: <strong>needs to be checked</strong> before adding.

<strong><u>Attention</u></strong>: vertex-numbers are given in <strong>natural </strong>numbering (starting with 1) so you should “turn” them to Java-indexing to reflect correct connection. <u>No need for validity check</u>.

<ol>

 <li>A public method <strong><em>deleteEdge(int from, int to)</em></strong> where two parameters identify vertices representing the edge that needs to be deleted from the graph (<em>to </em>vertex is removed as <em>from</em> vertex’s neighbor). <strong><u>Note</u>:</strong> nothing is done if such edge doesn’t exist (no error message or exception).</li>

</ol>

<strong><u>Attention</u></strong>: vertex-numbers are given in <strong>natural </strong>numbering (starting with 1) so you should “turn” them to Java-indexing to reflect correct connection. <u>No need for validity check</u>.

<ol>

 <li>A public method <strong><em>edgeCount()</em></strong>: computes and returns the number of edges in the graph.</li>

 <li>A public method <strong><em>vertexCount()</em></strong>: returns the number of vertices in the graph (it’s the array’s length)</li>

 <li>A public method <strong><em>print() </em></strong>that outputs the graph in the following format: for each vertex <em>i </em>(from 0 to N-1) outputs a line: <strong><em>i</em></strong><strong> is connected to: <em>x1</em>, …,  <em>xk </em></strong> where <em>x1,…, xk</em> are vertices that are adjacent to <em>i</em>.  <strong><em>     </em></strong><strong><em> </em></strong><u>Example</u>: for some 5-vertex graph your output may look like this:</li>

</ol>

<strong><em>                   1</em></strong><strong> is connected to: <em>2</em>,  <em>4                    2</em> is connected to: </strong>

<ul>

 <li><strong>is connected to: <em>2</em>, <em>4,  1 </em></strong></li>

 <li><strong>is connected to: <em>3 </em></strong></li>

 <li><strong>is connected to: <em>3, 1 </em></strong></li>

</ul>

<strong><em> </em></strong>

<strong><u>Attention</u></strong>: numbering of vertices in the output should be <strong>natural</strong>, i.e. <strong>starting with 1</strong>.

<strong> <u>Important:</u></strong> Separate two neighbors with a comma; <strong>do NOT</strong> put comma after the last neighbor

<ol start="2">

 <li><strong>Define an application class </strong> In <em>main </em>method of this class you need to do the following:</li>

 <li>Define a scanner object for keyboard input (i.e. connect it to <em>in</em>). You must make a scanner for <strong>System.in</strong> only once here and use it for all <strong>keyboard</strong> inputs in this <em>main</em> method. <strong>DON’T </strong>redefine this scanner or create a new scanner for<strong> <em>System.in</em> –</strong> <strong><u>it will cause problems in grading.</u></strong></li>

 <li>Prompt the user to enter the number of vertices.</li>

 <li>Input the number of vertices and define an object of <em>DiGraph</em></li>

 <li>Output a menu to the user, listing the above mentioned 5 operations that your <em>DiGraph </em>class provides. For example, your menu may look like this:</li>

</ol>

<em>Choose one of the following operations: </em>

<ul>

 <li><em>add edge (enter a) </em></li>

 <li><em>delete edge (enter d) </em></li>

 <li><em>edge count (enter e) </em></li>

 <li><em>vertex count (enter v) </em></li>

 <li><em>print graph (enter p) – Quit (enter q) </em></li>

</ul>

<strong><u>Important:</u></strong> <strong>must use </strong><strong><em>a, d, e, v, p, q</em> letters for menu choices (do NOT change these letters) </strong>

1




Dr. Hasmik Gharibyan

CSC/CPE 349

<ol start="5">

 <li>For as long as the user does not choose to quit, do the following:</li>

</ol>

<ul>

 <li>Prompt the user to enter a menu choice (do <strong>NOT</strong> print the menu here; the menu should be output <strong>only once,</strong> in step 3 above, <strong>before</strong> entering this loop).</li>

 <li>Input user’s choice and analyze it (you are recommended to use a <em>switch</em> statement with <em>default</em> case which will be executed for invalid menu choices). Arrange the execution of the requested operation; if input values are necessary (for <em>add edge </em>and<em> delete edge </em>menu choices), prompt the user to enter two integers and input them (<u>no need for validity check</u>). For every request, after executing it, <strong>output feedback</strong>: e.g. if you are adding/deleting an edge, output a message saying for example that the edge (x, y) was added/deleted; if you are giving some returned answer (e.g.</li>

</ul>

number of edges), precede it with an informative message (e.g. “Number of edges is: ”); or before printing the graph, output a sentence “The graph is the following:”

<strong><u>Note</u>:</strong> in all communications with the <strong>user</strong> the vertex numbering is <strong>natural</strong>, i.e. <strong>starting with 1</strong>.




<ol start="3">

 <li><strong>Edit, compile and execute <em>DiGraphTest </em>class, test it thoroughly. </strong>When running the program, first provide the graph by inputting N (number of vertices) and then <strong>one by one adding vertices</strong> (with ‘a’ menu option). Extensively test the functionality of your program: request different menu choices and check their execution; then add and delete edges to change the graph and repeat the testing for the modified graph. Finish testing when you are absolutely sure all the functionality of the program is correct.</li>

</ol>




<strong> </strong>

<strong><u>Part 2 of 4</u></strong><strong> (15 points):  </strong>

<strong> </strong>

<ol>

 <li><strong> Make additions in the <em>DiGraph</em> class to include the implementation of the </strong><strong>Topological Sort algorithm including a supporting routine for computing vertex <em>indegrees</em>.</strong></li>

</ol>

<strong> </strong>

Add the following content to the <em>DiGraph</em> class’s definition.

<ol>

 <li>A <strong><em>private</em></strong> method <strong><em>indegrees</em></strong>: returns an array of integers representing the indegrees of all vertices in the graph: the i-th integer in the resulting array is the indegree of the i-th vertex.</li>

 <li>A <em>public</em> method <strong><em>topSort</em></strong>: returns an array containing the list of topologically sorted vertices (values in the array should represent <strong>natural</strong> vertex-numbers, i.e. <strong>starting with 1</strong>).</li>

</ol>

<strong><u>Important:</u></strong> If the graph is <strong><u>cyclic</u></strong>, this method must throw <em>IllegalArgumentException</em> type exception (read the <em>note</em> on top of the last page of your <em>Topological Sort</em> lecture handout).




<strong><u>Attention:</u></strong> In <em>topSort</em> you need a regular queue and <strong><u>NOT</u> </strong>a priority queue. To implement a queue in Java, you can simply use an object of <strong><em>LinkedList</em></strong> class (for integers). Your list will function like a regular <strong>queue</strong> if you always add an element to the end using <em>addLast</em> method, and delete an element from the front using <em>removeFirst </em>method.

<strong>    </strong>

<ol start="2">

 <li><strong>Make additions to the <em>DiGraphTest</em> class’s <em>main</em> method to incorporate <u>one</u> additional service. </strong></li>

</ol>

<strong> </strong>

Add one <strong>new</strong> menu-choice for outputting the topologically sorted list of vertices of the graph and arrange the execution of that <strong>new</strong> service.




<strong> </strong>

<strong><u>Attention</u>: </strong>1. Use <strong><em>t</em></strong> letter for the new menu choice (<strong><em>t</em></strong> – <strong>t</strong>opological sort).

<ol start="2">

 <li>Numbering of vertices in the output should be <strong>natural</strong> (<strong>starts with 1</strong>).</li>

 <li>The list should be output on <strong><u>one</u></strong> line, with vertex-numbers separated by <strong><u>commas</u>. Important:</strong> there should <strong>NOT</strong> be a comma after the last vertex.</li>

</ol>

<strong> </strong>

<ol start="3">

 <li><strong>Edit, compile and execute <em>DiGraphTest </em>program, testing the new service very thoroughly.</strong></li>

</ol>

<strong> </strong>