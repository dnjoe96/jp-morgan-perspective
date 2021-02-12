# jp-morgan-perspective

<h1> Introduction</h1> 
<b> Experience Technology at JP Morgan Chase & Co</b>
<p>Try out what real work is like in the technology team at JP Morgan Chase & Co. Fast track to the tech team with your work.</p>

<h2 id="task"> Module 1 Task Overview </h2>
<p>Interface with a stock price data feed and set up your system for analysis of the data</p>
<p> <b>Aim:</b> We want to process the data feed of stock A and stock B’s price to enable us to analyse when trading for the stock should occur.</p>

<ol>
	<li>Please clone this repository to start the task</li>
	<li>Adjust the getRatio, getDataPoint and main functions</li>
	<li>Bonus: Pass all unit tests and add more to cover edge cases</li>
	<li>Upload a git patch file as the submission to this task</li>
	
</ol>

<h2 id="installation" >Set up / Installation</h2>

<p>In order to get the server and client application code working on your machine, <a href="https://insidesherpa.s3.amazonaws.com/vinternships/companyassets/Sj7temL583QAYpHXD/setup_devenv_m1_v6.pdf">follow the setup here</a></p>
<p><b>Note:</b>This is the Python 3 version of the JPM 1 exercise. The Python 2.7 version is in <a href="https://github.com/insidesherpa/JPMC-tech-task-1">this other repo</a></p>

<h2>How to Run</h2>
To start the server, run

	python server3.py

this will create random market called 'test.csv' in your working directory if one does not already exist.

If you encounter an issue with `datautil.parser`, run this command: 

	pip install python-dateutil

If you don't have pip yet, you can install it from: https://pip.pypa.io/en/stable/installing/

To start the example client, run:

	python client3.py

To unit test the example client, run:
	python client_test.py

<h2>How to request from the server using curl</h2>
<!--See also [client.py](https://github.com/texodus/exchange_simulator/blob/master/client.py)-->
Query:

	$ curl 'http://localhost:8080/query?id=1'
	{"id": "1", "top_ask": {"price": 129.18, "size": 70}, "timestamp": "2016-08-06 12:32:11.821574", "top_bid": {"price": 128.79, "size": 61}}




<h1> Introduction</h1> 
<b> Experience Technology at JP Morgan Chase </b>
<p>Try out what real work is like in the technology team JP Morgan Chase. Fast track to the tech team with your work.</p>

<h2 id="task"> Module 2 Task Overview </h2>
<p>Use JP Morgan Chase's frameworks and tools
Implement JP Morgan Chase’s Perspective open source code in preparation for data visualization</p>
<p> <b>Aim:</b>Take an incomplete setup of Perspective, i.e. a graph that updates manually, and make it work with the code from Task 1 such that it now updates automatically by continuously requesting from the server application</p>

<ol>
	<li>Please clone this repository to start the task</li>
	<li>[goal-a] In the client application, observe that when new data feed is retrieved whenever you click the 'Start Streaming Data' button, the previous entry is re-entered into the table. Update the application so that the table does not have duplicated entries</li>
	<li>[goal-b] We also want the react app to keep continuosly requesting data from the python server. Currently, the data feed is called only once every time the 'Start Streaming' button is clicked. Change the application to continuously query the datafeed every 100ms when the 'Start Streaming' is clicked.</li>
	<li>[goal-c] Currently, the Perspective element only shows the data in table view after the data loads. Add Perspective configurations so that when the data is loaded, it shows the historical data of ask_price ABC in the Y line chart.</li>
	<li>Upload a git patch file as the submission to this task</li>	
</ol>

<h2 id="installation" >Set up / Installation</h2>
<p>In order to get the server and client application code working on your machine, <a href="https://insidesherpa.s3.amazonaws.com/vinternships/companyassets/Sj7temL583QAYpHXD/setup_devenv_m2_v8.pdf">follow the setup here</a></p>

<p><b>Note</b>:This is the version of the JPM 2 exercise that uses Python 3. The Python 2.7 version is in <a href="https://github.com/insidesherpa/JPMC-tech-task-2">this other repo</a></p>

<h2>How to Run</h2>

<p>Similar to Task 1, start the data feed server by running the python server.</p> 
<p>Make sure your terminal / command line is in the repository first before doing any of this.</p>
<p>If you are using Windows, make sure to run your terminal/command prompt as administrator.</p>

<code> python datafeed/server3.py </code>

If you encounter an issue with `datautil.parser`, run this command: 

	pip install python-dateutil

If you don't have pip, you can install it from: https://pip.pypa.io/en/stable/installing/

Run <code>npm install && npm start</code> to start the React application.

It's okay to have audit warnings when installing/running the app.

If you don't have `npm` (although you should if you followed the set up / installation part), you can install the recommended version alongside NodeJS from: https://nodejs.org/en/

The recommended version are node v11.0.0 and npm v6.4.1

Open http://localhost:3000 to view the app in the browser. The page will reload if you make edits.




<h1> Introduction</h1> 
<b> Experience Technology at JP Morgan Chase </b>
<p>Try out what real work is like in the technology team at JP Morgan Chase & Co. Fast track to the tech team with your work.</p>

<h2 id="task"> Module 3 Task Overview </h2>
Display data visually for traders.
Use Perspective to create the chart for the trader’s dashboard.

<b>Aim:</b> Use Perspective to generate a chart that displays the data feed in a clear and visually appealing manner for traders to monitor this trading strategy. Basically, you have to modify the existing live chart to be able to (1) track and display the ratio between the two stock prices (2) show the historical upper and lower bounds of the stocks' ratio (3) and finally, show 'alerts'  whenever these bounds are crossed by the ratio.

<ol>
	<li>Please clone this repository to start the task</li>
	<li>From the existing live graph, update it to track the ratio between two stocks over time and NOT the two stocks’ top_ask_price over time.</li>
	<li>Update the graph to also track the historical upper and lower bounds of the stocks' ratio</li>
	<li>Trigger 'alerts' (i.e. draw red lines) on the graph whenever the bounds are crossed by the calculated ratio in a specific time period</li>
	<li>Upload a git patch file as the submission to this task</li>	
  	<li>Upload a video detailing your process and work</li>
</ol>

<h2 id="installation" >Setup / Installation</h2>
<p>In order to get the server and client application code working on your machine, <a href="https://insidesherpa.s3.amazonaws.com/vinternships/companyassets/Sj7temL583QAYpHXD/setup_devenv_m3_v3.pdf">follow the setup here</a></p>

<p><b>Note</b>:This is the version of the JPM 3 exercise that uses Python 3. The Python 2.7 version is in <a href="https://github.com/insidesherpa/JPMC-tech-task-3">this other repo</a></p>

<h2>How to Run</h2>
<p>Similar to Task 2, start the data feed server by running the python server</p>
<p>Make sure your terminal / command line is in the repository first before doing any of this.</p>
<p>If you are using Windows, make sure to run your terminal/command prompt as administrator.</p>

<code>python datafeed/server3.py</code>

If you encounter an issue with `datautil.parser`, run this command: 

	pip install python-dateutil

If you don't have pip, you can install it from: https://pip.pypa.io/en/stable/installing/

Run <code>npm install && npm start</code> to start the React application.

It's okay to have audit warnings when installing/running the app.

If you don't have `npm` (although you should if you followed the set up / installation part), you can install the recommended version alongside NodeJS from: https://nodejs.org/en/

The recommended version are node v11.0.0 and npm v6.4.1

Open http://localhost:3000 to view the app in the browser. The page will reload if you make edits.

