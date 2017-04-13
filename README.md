# willBeDeleted

part1.js
var thisApp = {}
	thisApp.testVariable="this ,test variable";
	
	thisApp.globalVar = "Global değişken denemesi"
	thisApp.sayHi = function(){
		document.getElementById("testDiv").innerHTML="<b><i>" + thisApp.globalVar + "</i></b>";
	}

part2.js
var processLib = {}
	processLib.testVariable="taskLib ,test variable";
	processLib.sayHi = function(){
		document.getElementById("testDiv").innerHTML="<pre>Hi, <br></br>I am ProcessLib new in town</pre>";
	}

part3.js
var taskLib = {}
	taskLib.testVariable = "taskLib ,test variable";
	taskLib.sayHi = function(){
		alert(globalVar);
		document.getElementById("testDiv").innerHTML="<pre>Hi, <br></br>I am tasklib,new in town</pre>";
	}

index
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,user-scalable=no,initial-scale=1">
    <title>Hello World</title>
	<!--
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.0/jquery.min.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
	 **************************************************************************************   
	 -->
	<script src="lib/app.js" type="text/javascript"></script>
	<script src="lib/partProcess.js" type="text/javascript"></script>
	<script src="lib/partTask.js" type="text/javascript"></script>
	
	<link href="lib/style.css" rel="stylesheet" type="text/css">
		
</head>
<body>
	
	<div id="testDiv" style="height:200px;" >
		sonucu burada göreceksin
	</div>
	
	<hr>
	
	<button onclick="thisApp.sayHi()"> thisApp.sayHi()</button>
	<button onclick="processLib.sayHi()"> processLib.sayHi()</button>
	<button onclick="taskLib.sayHi()"> taskLib.sayHi()</button>
	
	<br></br>
	
	<button onclick="alert(thisApp.testVariable)"> alert this test </button>
	<button onclick="alert(processLib.testVariable)"> alert process test </button>
	<button onclick="alert(taskLib.testVariable)"> alert task test</button>
	
</body>
</html>
