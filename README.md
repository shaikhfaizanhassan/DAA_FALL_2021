# DAA_FALL_2021


#### Shaikh Faizan Hassan
#### 11076

My name is Shaikh Faizan Hassan.Studying MSC from PAF-KIET University.Currently working as Faculty Member at Aptech Pakistan.My skills include C#,HTML/CSS,Javascript.

<html>
<head>
	<title>N-Queen Problem</title>
	<meta charset="utf-8">
	<script type="text/javascript" src="nQueen.js"></script>
		<!-- Load plotly.js into the DOM -->
	<script src='https://cdn.plot.ly/plotly-latest.min.js'></script>
</head>
<body>
	<h1>N-Queen Problem</h1>
	<h2>63742 - Saqib Ullah</h2><!--This is the group leader-->
	<h3>63744 - Adnan Siddiqui</h3><!--This is the 2nd Member of the group-->
	<h4><a href="https://daa2020.000webhostapp.com/nQueen.html" target="blank">GitHub</a></h4><!--Replace about:blank with your GitHub repository folder for assignment 1. -->
	<p> 
		<button id="btnRun" onclick="runEmAll()">Run</button>
	</p>
	<div id='myDiv'><!-- Plotly chart will be drawn inside this DIV --></div>
	<textarea id="ta_sol1" cols="50" rows="30"></textarea>&nbsp
	<textarea id="ta_sol2" cols="50" rows="30"></textarea>&nbsp
	<textarea id="ta_sol3" cols="50" rows="30"></textarea>
	
	
</body>
</html>
[12/21/2021, 5:05 PM] Ali Naeem Sheikh: function runEmAll(){
	console.log("Running All Solutions")
	taSol1.value = ""; 	taSol2.value = ""; 	taSol3.value = "";
	var start;
	var end;
	var n=4;
	var xval = [];
	var ysal1 = [];
	var ysal2 = [];
	var ysal3 = [];
	for (var k = 4; k <= 16; k++) {
		xval.push(k);
		//Runs each solution and measures performance in microseconds
		console.log("In Forloop: Line 18, k = "+k+"\n");
		start = performance.now();
		sol1(n);
		end = performance.now();
		taSol1.value+= ""+n+", "+(end-start)*1000+"\n";
		ysal1.push((end-start)*1000);
		
		start = performance.now();
		sol2(n);
		end = performance.now();
		taSol2.value+= ""+n+", "+(end-start)*1000+"\n";
		ysal2.push((end-start)*1000);
		
		start = performance.now();
		sol3(n);
		end = performance.now();
		taSol3.value+= ""+n+", "+(end-start)*1000+"\n";
		n = n * 2;
		}//end for
		
		console.log(xval);


var trace1 = {
  x: xval,
  y: ysal1,
  type: 'scatter',
  name : 'brute-force'
};

var trace2 = {
  x: xval,
  y: ysal2,
  type: 'scatter',
  name : 'back-tracking'
};


var layout = {
  title:'nQueen Problem Timing Analysis'
};

var data = [trace1, trace2];
Plotly.newPlot('myDiv', data,layout);
}//end runEmAll

function sol1(n){
	//Implement your brute-force solution here


	//console.log(([(- 1)] * 8));
	//new NQueens(8);

	//Mention reference where you got the solution
	//Ref: http://
	//Ref: If you found any paper
}//end sol1

function sol2(n){
	//Implement your recursive back-tracking solution here

	//console.log(rb_queenPuzzle(8,8));

	//Mention reference where you got the solution
	//Ref: http://
	//Ref: If you found any paper
}//end sol2

function sol3(n){
	//Implement your dynammic programming solution here

	//--This is garbage code: Remove this--//
	for (var i = 1; i <= n; i++) {
		for(var k=0;k<50;k++);
	}//end for j
	//--End of Garbage Code--//

	//Mention reference where you got the solution
	//Ref: http://
