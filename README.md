Download Link: https://assignmentchef.com/product/solved-cs2040c-assignment-4-heap-and-queueing-simulation
<br>
<h1>Heap and Queueing Simulation</h1>

<h1>Two BIG Parts</h1>

<ul>

 <li>Implementing Heap

  <ul>

   <li>Basic requirement</li>

  </ul></li>

 <li>Perform a queueing simulation experiment with Priority Queue

  <ul>

   <li>Difficult</li>

   <li>Treat it as a mini project</li>

  </ul></li>

</ul>

Time to Level UP!

<h1>Something Different</h1>

<ul>

 <li>We will NOT give you the MSVC .sln or Xcode project</li>

</ul>

<ul>

 <li>It’s time for you to create your own</li>

 <li>Any problem, please refer to Lab 1 slides</li>

</ul>

<h1>Something Different</h1>

<ul>

 <li>We will tell you what you need to do

  <ul>

   <li>Namely, list of tasks</li>

  </ul></li>

 <li>However

  <ul>

   <li>You have to decide the order</li>

   <li>There may be some additional unnamed tasks you have to fill in</li>

  </ul></li>

</ul>

<h1>Something Different</h1>

<ul>

 <li>You have to learn how to NOT relying on the coursemology output</li>

</ul>

– Instead relying on your own testing cases and judgement

<h1>Given Files</h1>

<ul>

 <li>The Heap files:

  <ul>

   <li>h</li>

   <li>hpp</li>

  </ul></li>

 <li>The driver program for your tests

  <ul>

   <li>cpp</li>

  </ul></li>

 <li>Customer class, but you can ignore it for the Heap task first

  <ul>

   <li>h</li>

   <li>cpp</li>

  </ul></li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="176"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Part 1 Heap Implementation (Array)

<h1>Very First Task</h1>

<ul>

 <li>Create your own MSVC .sln or Xcode Project</li>

</ul>

<h1>Implementing Heap</h1>

<ul>

 <li>MaxHeap

  <ul>

   <li>Parents &gt; children</li>

  </ul></li>

 <li>You will implement the Heap with the array representation

  <ul>

   <li>It is <strong>NOT </strong>recommended to implement the heap by pointer/tree/node representation</li>

  </ul></li>

 <li>The following functions are provided for you –printHeapArray, printTree, _lookFor</li>

</ul>

<h1>Given Functions</h1>

<ul>

 <li>printHeapArray()

  <ul>

   <li>print out the array that stores the heap</li>

  </ul></li>

 <li>printTree()

  <ul>

   <li>print the heap in a graphical tree form… somehow</li>

  </ul></li>

</ul>

<h1>Given Functions</h1>

<ul>

 <li>The function</li>

</ul>

int Heap&lt;T&gt;::_lookFor(T x)

<ul>

 <li>It searches for the item x in the array and return the index of x in the heap array</li>

 <li>In real practice, the index of x and x should be stored in a symbol table/dictionary, thus, hash table, for fast look-up of the index of x

  <ul>

   <li>O(1) look-up time</li>

  </ul></li>

 <li>However, we just use a linear search here for our assignment

  <ul>

   <li>O(n) look-up time</li>

  </ul></li>

</ul>

<h1>Implementing Heap</h1>

<ul>

 <li>You have to implement and submit the following functions:</li>

</ul>

–insert(x): Insert an item x into the heap

–extractMax(): extract the max. item from the heap

–decreaseKey(x,y): decrease the key of item x to y

–increaseKey(x,y): increase the key of item x to y

–deleteItem(x): remove the item x

–_bubbleUp(i): bubble up the item in index i

–_bubbleDown(i) : bubble down the item in index i

<h1>Implementing Heap</h1>

<ul>

 <li></li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="240"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>You have to implement and submit the following functions:</li>

</ul>

<strong>insert(x)</strong><strong>, </strong><strong>extractMax()</strong><strong>, </strong><strong>decreaseKey(x,y), increaseKey</strong>

<strong>(x,y), deleteItem(x),_bubbleUp(i),_bubbleDown(i)</strong>

<ul>

 <li>What is the order of implementation?!</li>

</ul>

<h1>If You Implemented Correctly</h1>

<h1>If You Implemented Correctly</h1>




Queue Simulation

Second Part

<h1>Second Part: Queueing Simulation</h1>

<ul>

 <li>Queueing theory is the mathematical study of waiting lines, or queues. A queueing model is constructed so that queue lengths and waiting time can be predicted. Queueing theory is generally considered a branch of operations research because the results are often used when making business decisions about the resources needed to provide a service.</li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="64"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>




Model

<ul>

 <li>Customers

  <ul>

   <li>Arrival time</li>

   <li>Processing time</li>

  </ul></li>

 <li>Time need to be served</li>

 <li>Queue

  <ul>

   <li>Where customer wait, can be prioritized</li>

  </ul></li>

 <li>Server

  <ul>

   <li>Customers get served and leave</li>

  </ul></li>

</ul>

Questions

<ul>

 <li>About waiting time

  <ul>

   <li><strong>Average WT</strong></li>

   <li>Max WT</li>

   <li>Min WT</li>

   <li>or other WT</li>

  </ul></li>

 <li>For all customers</li>

</ul>

Single/Multiple Queue(s) with Multiple

Servers

What does the bank do?

<h1>Queue with “Priority”</h1>

<h1>Part 2: Queue Simulation</h1>

<ul>

 <li>First, the code customerTest() will generate 10 customers for you in customer.cpp</li>

 <li>And we assume that there is only ONE server now</li>

</ul>

<h1>Customer Behavior</h1>

<ul>

 <li>All the customers will be stored in the array custList[]</li>

 <li>To make it simple, the customer number is equal to the time they arrived in minutes</li>

</ul>

– E.g. Customer 4 will arrive 4 min after the store opens

<ul>

 <li>When the customer arrives, they will wait in the waiting queue if the server is serving another customer</li>

</ul>

<h1>Customer Behavior</h1>

<ul>

 <li>If the server is serving no one, next customer in the queue will be served (dequeued)</li>

 <li>Each customer has a processing time (PT)

  <ul>

   <li>The amount of time he will occupy the server when he left the waiting queue</li>

   <li>The server will not server the next one in the queue until he finish this current one</li>

  </ul></li>

</ul>

<h1>Waiting Time</h1>

<ul>

 <li>For each customer, his waiting time (WT) is count as the difference between</li>

</ul>

<ul>

 <li>The time he <strong>arrives </strong>and the time he <strong>starts to be served </strong>(dequeued)</li>

 <li>NOT the time he finished being served</li>

</ul>

<h1>Example (Normal Queue)</h1>

<ul>

 <li>Assume that the priority of the queue is FIFO</li>

</ul>

– Normal queue in real life

<ul>

 <li>Generate four customers (Done for you):</li>

</ul>

<table width="864">

 <tbody>

  <tr>

   <td width="288"><strong>Time at the start of…</strong></td>

   <td width="288"><strong>Customer</strong></td>

   <td width="288"><strong>Server</strong></td>

  </tr>

  <tr>

   <td width="288">0</td>

   <td width="288">C0 arrives</td>

   <td width="288">Serves C0 at time 0</td>

  </tr>

  <tr>

   <td width="288">1</td>

   <td width="288">C1 arrives</td>

   <td width="288">Serves C1 at time 1</td>

  </tr>

  <tr>

   <td width="288">2</td>

   <td width="288">C2 arrives</td>

   <td width="288">Busy with C1</td>

  </tr>

  <tr>

   <td width="288">3</td>

   <td width="288">C3 arrives</td>

   <td width="288">Busy with C1</td>

  </tr>

  <tr>

   <td width="288">4</td>

   <td width="288"> </td>

   <td width="288">Busy with C1</td>

  </tr>

  <tr>

   <td width="288">5</td>

   <td width="288"> </td>

   <td width="288">Serves C2 at time 5</td>

  </tr>

  <tr>

   <td width="288">6</td>

   <td width="288"> </td>

   <td width="288">Serves C3 at time 6</td>

  </tr>

 </tbody>

</table>

<ul>

 <li></li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="48"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Customer 2 waits for 5 – 2 = 3 min in the queue</li>

 <li>Customer 3 waits for 6 – 3 = 3 min in the queue</li>

</ul>

<h1>Output for FIFO</h1>

<ul>

 <li>Total WT = 6 min for all customers</li>

 <li>Average WT = 1.5 min for each customer</li>

</ul>

<h1>For 10 Customers (Setup)</h1>

<h1>Output for FIFO (10 Customers)</h1>

<h1>However</h1>

<ul>

 <li>If we change the queue priority

  <ul>

   <li>It will not be First Come First Served</li>

  </ul></li>

 <li>Miraculously, there is a smart scanner that can detect the processing time for the customer in the queue</li>

 <li><strong>The server will serve the customer with the LEAST processing time among the people in the queue FIRST</strong></li>

</ul>

Output For Least PT (10 Customers)

Conclusion?

<ul>

 <li>What is the difference in the average waiting time for two different policy of the priority of the queue?

  <ul>

   <li>FIFO vs Least PT</li>

  </ul></li>

 <li>Is it just coincident? Or is it always like that?</li>

</ul>

Difference

<ul>

 <li>FIFO</li>

 <li>Least PT first</li>

</ul>

<h1>Given Code</h1>

class Customer { private:

int arrival_time;

// time of arrival after the shop opened in min int processing_time;

// amount of time need to be processed with the customer serivce in min

public:

Customer () {arrival_time = 0; processing_time = 0;}; void setAT(int t) {arrival_time = t;}; void setPT(int t) {processing_time = t;}; int AT() {return arrival_time;}; int PT() {return processing_time;};

bool operator&gt;(const Customer&amp; c);

// a customer is “greater” if his time is shorter

};

<h1>Comparison For Heap/PQ</h1>

<ul>

 <li>If comparisonWay = 0

  <ul>

   <li>the heap be ordered by arrival times (AT)</li>

  </ul></li>

 <li>If comparisonWay = 1

  <ul>

   <li>the heap be ordered by processing times (PT)</li>

  </ul></li>

</ul>

int comparisonWay = 0; // 0 for arrival time, 1 for processing

arrival_time &lt; c.arrival_time;

// a customer is “greater” if his time is shorter };

<h1>First Part of CustomerQueueTest()</h1>

void customerQueueTest(int n_cust) { Setting up n int current_time = 0; customers for the

int totalWaitingTime = 0;

int i;                                                  test

int WT = 0; // waiting time for each customer

Heap&lt;Customer&gt; queue;

Customer* custList = new Customer[n_cust]; cout &lt;&lt; endl &lt;&lt; endl &lt;&lt; “Setup” &lt;&lt; endl; cout &lt;&lt; “List of customers and their arrival and processing times” &lt;&lt; endl; for (i = 0; i&lt;n_cust; i++)

{ custList[i].setAT(i);

custList[i].setPT((n_cust – i) % (n_cust / 2) + 1 + (i % 2)*(n_cust /

2)); cout &lt;&lt; “Customer ” &lt;&lt; i &lt;&lt; ” will arrive at time ”

&lt;&lt; custList[i].AT() &lt;&lt; ” with PT=” &lt;&lt; custList[i].PT() &lt;&lt; endl;

} cout &lt;&lt; endl;

<h1>Following on</h1>

for (int round = 0; round&lt;2; round++) {

// you may need a big modification within this for-loop

cout &lt;&lt; endl &lt;&lt; endl; cout &lt;&lt; “Test Round ” &lt;&lt; round + 1 &lt;&lt; endl; cout &lt;&lt; (round == 0 ? “First come first serve” : “Customer with the least PT served first”) &lt;&lt; endl; comparisonWay = round; current_time = 0; totalWaitingTime = 0; queue.insert(custList[0]); cout &lt;&lt; “Customer arrives at time “You have to &lt;&lt; custList[0].AT() &lt;&lt; ” with PT=” &lt;&lt; custList[0].PT() &lt;&lt; endl;

while (!queue.empty()) {       change all the

// you should change all of the code here insidecode here!

Customer c = queue.extractMax(); cout &lt;&lt; “Customer arrives when no one is waiting” &lt;&lt; endl;

cout &lt;&lt; “Customer is served at time ” &lt;&lt; current_time &lt;&lt; ” with AT=” &lt;&lt; c.AT()

&lt;&lt; ” and PT=” &lt;&lt; c.PT() &lt;&lt; ” after waiting for “

&lt;&lt; WT &lt;&lt; ” min.” &lt;&lt; endl;

}

cout &lt;&lt; “Total Waiting Time: ” &lt;&lt; totalWaitingTime &lt;&lt; endl;

cout &lt;&lt; “Average Waiting Time: ” &lt;&lt; totalWaitingTime / (float)n_cust &lt;&lt; endl;

The purpose for giving you the code here is

for all those “cout” such that it will match the coursemology test case

Difference

<ul>

 <li>FIFO</li>

 <li>Least PT first</li>

</ul>

<h1>Real Job</h1>

<ul>

 <li>Treat the Queueing Simulation part of your assignment as a real job</li>

</ul>

– A mini project

10 ways school is different than the working world

<ul>

 <li>If you can’t do the work, you’re out.</li>

 <li>We grade on a curve.</li>

 <li>…</li>

 <li>We hate slackers.</li>

 <li>You have to fight for recognition.</li>

 <li>We realWe really, really, really want you to be able to write y, really, really want you to be able to write properly.<strong>CODE </strong>properly</li>

 <li>We really, really, really want you to be able to do math.</li>

 <li>If you can’t make money for us, we won’t hire you.</li>

</ul>

<a href="https://www.cbsnews.com/news/10-ways-school-is-different-than-the-world-of-work/">https://www.cbsnews.com/news/10-ways-school-is-different-than-the-world-of-work/</a>