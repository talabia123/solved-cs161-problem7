Download Link: https://assignmentchef.com/product/solved-cs161-problem7
<br>



<ol>

 <li>Consider the graph <em>G </em>below.</li>

</ol>

<ul>

 <li><strong> </strong>What MST does Prim’s algorithm return? In what order does Prim’s algorithm add edges to the MST when started from vertex <em>C</em>?</li>

 <li><strong> </strong>What MST does Kruskal’s algorithm return? In what order does Kruskal’s algorithm add edges to the MST?</li>

</ul>

<h2>[We are expecting: For both, just a list of edges. No justification is required.]</h2>

<table>

 <tbody>

  <tr>

   <td width="95"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<ol start="2">

 <li><strong> </strong>At a Thanksgiving dinner, there are <em>n </em>food items <em>f</em><sub>0</sub><em>,…,f<sub>n</sub></em><sub>−1</sub>. Each food item has a tastiness <em>t<sub>i </sub>&gt; </em>0 (measured in units of deliciousness per ounce) and a quantity <em>q<sub>i </sub>&gt; </em>0 (measured in ounces). There are <em>q<sub>i </sub></em>ounces of food <em>f<sub>i </sub></em>available to you, and for any real number <em>x </em>∈ [0<em>,q<sub>i</sub></em>], the total deliciousness that you derive from eating <em>x </em>ounces of food <em>f<sub>i </sub></em>is <em>x </em>· <em>t<sub>i</sub></em>. (Notice that <em>x </em>here doesn’t have to be an integer).</li>

</ol>

Unfortunately, you only have capacity for <em>Q </em>ounces of food in your belly, and you would like to maximize deliciousness subject to this constraint. Assume that there is more food than you can possibly eat:

<sup>P</sup><em>i q<sub>i </sub></em>≥ <em>Q</em>.

(a) <strong> </strong>Design a greedy algorithm which takes as input the tuples (<em>f<sub>i</sub>,t<sub>i</sub>,q<sub>i</sub></em>), and outputs tuples (<em>f<sub>i</sub>,x<sub>i</sub></em>) so that 0 ≤ <em>x<sub>i </sub></em>≤ <em>q<sub>i</sub></em>, <sup>P</sup><em><sub>i </sub>x<sub>i </sub></em>≤ <em>Q</em>, and <sup>P</sup><em><sub>i </sub>x<sub>i</sub>t<sub>i </sub></em>is as large as possible. Your algorithm should take time <em>O</em>(<em>n</em>log(<em>n</em>)).

<h2>[We are expecting: Pseudocode and a short English explanation. ]</h2>

(b) <strong> </strong>Fill in the inductive step below to prove that your algorithm is correct.

<ul>

 <li><strong>Inductive hypothesis: </strong>After making the <em>t</em>’th greedy choice, there is an optimal solution that extends the solution that the algorithm has constructed so far.</li>

 <li><strong>Base case: </strong>Any optimal solution extends the empty solution, so the inductive hypothesis holds for <em>t </em>= 0.</li>

</ul>

<h2>• Inductive step: <em>(you fill in)</em></h2>

<ul>

 <li><strong>Conclusion: </strong>At the end of the algorithm, the algorithm returns an set <em>S</em><sup>∗ </sup>of tuples (<em>f<sub>i</sub>,x<sub>i</sub></em>) so that <sup>P</sup><em><sub>i </sub>x<sub>i </sub></em>= <em>Q</em>. Thus, there is no solution extending <em>S</em><sup>∗ </sup>other than <em>S</em><sup>∗ </sup>itself. Thus, the inductive hypothesis implies that <em>S</em><sup>∗ </sup>is optimal.</li>

</ul>

<strong>[We are expecting: A proof of the inductive step: assuming the inductive hypothesis holds for </strong><em>t </em>− 1<strong>, prove that it holds for </strong><em>t</em><strong>.]</strong>

<h1>Problems</h1>

You may talk with your fellow CS161-ers about the problems. However:

<ul>

 <li>Try the problems on your own <em>before </em></li>

 <li>Write up your answers yourself, in your own words. You should never share your typed-up solutions with your collaborators.</li>

 <li>If you collaborated, list the names of the students you collaborated with at the beginning of each problem.</li>

</ul>

<ol>

 <li><strong> </strong>Consider the problem of <strong>making change. </strong>Suppose that coins come in denominations <em>P </em>= {<em>p</em><sub>0</sub><em>,…,p<sub>m</sub></em>} cents (for example, in the US, this would be <em>P </em>= {1<em>,</em>5<em>,</em>10<em>,</em>25}, corresponding to pennies, nickels, dimes, and quarters). Given <em>n </em>cents (where <em>n </em>is a non-negative integer), you would like to find the way to represent <em>n </em>using the fewest coins possible. For example, in the US system, 55 cents is minimally represented using three coins, two quarters and a nickel.</li>

</ol>

(a)Suppose that the denominations are <em>P </em>= {1<em>,</em>10<em>,</em>25} (aka, the US ran out of nickels). Your friend uses the following greedy strategy for making change:

<h2>Algorithm 1: makeChange(<em>n</em>) Input: <em>n </em>and <em>P</em></h2>

Your friend acknowledges that this won’t work for general <em>P </em>(for example if <em>P </em>= {2} then we simply can’t make any odd <em>n</em>), but claims that for this particular <em>P </em>it does work. That is, your friend claims that this algorithm will always return a way to make <em>n </em>out of the denominations in <em>P </em>with the fewest coins possible.

Is your friend correct for <em>P </em>= {1<em>,</em>10<em>,</em>25}?

<h2>[We are expecting: Your answer, and either a proof or a counterexample. If you do a proof by induction, make sure to explicitly state your inductive hypothesis, base case, inductive step, and conclusion.]</h2>

(b)<strong> </strong>Your friend says that additionally their algorithm should work for any <em>P </em>of the form <em>P </em>= {1<em>,</em>2<em>,</em>4<em>,</em>8<em>,…,</em>2<em><sup>s</sup></em>}.

Is your friend correct for <em>P </em>= {1<em>,</em>2<em>,</em>4<em>,…,</em>2<em><sup>s</sup></em>}?

<h2>[We are expecting: Your answer, and either a proof or a counterexample. If you do a proof by induction, make sure to explicitly state your inductive hypothesis, base case, inductive step, and conclusion.]</h2>

<ol start="2">

 <li><strong> </strong>On Thanksgiving day, you arrive on an island with <em>n </em>turkeys. You’ve already had thanksgiving dinner (and maybe you prefer tofurkey anyway), so you don’t want to eat the turkeys; but you do want to wish them all a Happy Thanksgiving. However, the turkeys each have very different sleep schedules. Turkey <em>i </em>is awake only in a single closed interval [<em>a<sub>i</sub>,b<sub>i</sub></em>]. Your plan is to stand in the center of the island and say loudly “Happy Thanksgiving!” at certain times <em>t</em><sub>1</sub><em>,…,t<sub>m</sub></em>. Any turkey who is awake at one of the times <em>t<sub>j </sub></em>will hear the message. It’s okay if a turkey hears the message more than once, but you want to be sure that every turkey hears the message at least once.</li>

</ol>

<ul>

 <li>Design a greedy algorithm which takes as input the list of intervals [<em>a<sub>i</sub>,b<sub>i</sub></em>] and outputs a list of times <em>t</em><sub>1</sub><em>,…,t<sub>m </sub></em>so that <em>m </em>is as small as possible and so that every turkey hears the message at least once. Your algorithm should run in time <em>O</em>(<em>n</em>log(<em>n</em>)).</li>

</ul>

<strong>[We are expecting: Pseudocode and an English description of the main idea of your algorithm, as well as a short justification of the running time.]</strong>

<ul>

 <li>Prove that your algorithm is correct.</li>

</ul>

<h2>[We are expecting: A proof by induction]</h2>

<ol start="3">

 <li><strong> </strong>Let <em>G </em>be a connected weighted undirected graph. In class, we defined a minimum spanning tree of <em>G </em>as a spanning tree <em>T </em>of <em>G </em>which minimizes the quantity</li>

</ol>

<em>X </em>= <sup>X</sup><em>w<sub>e</sub>,</em>

<em>e</em>∈<em>T</em>

where the sum is over all the edges in <em>T</em>, and <em>w<sub>e </sub></em>is the weight of edge <em>e</em>. Define a “minimum-maximum spanning tree” to be a spanning tree that minimizes the quantity <em>Y </em>= max<em>w<sub>e</sub>. </em><em>e</em>∈<em>T</em>

That is, a minimum-maximum spanning tree has the smallest maximum edge weight out of all possible spanning trees.

(a) Prove that a minimum spanning tree in a connected weighted undirected graph <em>G </em>is always a minimum-maximum spanning tree for <em>G</em>.

<em>[HINT: Suppose toward a contradiction that T is an MST but not a minimum-maximum spanning tree, and say that T</em><sup>0 </sup><em>is a minimum-maximum spanning tree. Let </em>(<em>u,v</em>) <em>be the heaviest edge in T. Then deleting </em>(<em>u,v</em>) <em>from T will disconnect it into two trees, A and B. Now use A and B and T</em><sup>0 </sup><em>to come up with a cheaper MST than T (and hence a contradiction).]</em>

<h2>                       [We are expecting:        A proof. ]</h2>

(b) Show that the converse to part (a) is not true. That is, a minimum-maximum spanning tree is not necessarily a minimum spanning tree.

<h2>[We are expecting: A counter-example, with an explanation of why it is a counterexample. ]</h2>

(c) Give a deterministic <em>O</em>(<em>m</em>) algorithm to find a minimum-maximum spanning tree in a connected weighted undirected graph <em>G </em>with <em>n </em>vertices and <em>m </em>edges.

<h2>[We are expecting: Pseudocode, along with an English description of the idea of the algorithm, and an informal justification of correctness and running time.]</h2>