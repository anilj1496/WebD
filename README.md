<!doctype  html>
<html>
<head>
<title>Countdown Timer</title>
<style>

#header {
	background-color:black;
	color:white;
	height:100px;
	text-align:center;
	padding:5px;
}
#timer {
	background-color:darksalmon;
	color:darkblue;
	height:30px;
	width:100px;
	text-align:center;
	border:solid black 2px;
	border-radius:25px;
}
</style>
</head>
<body>
<div id="header">
<h1>Countdown Timer</h1>
</div>
<p>
Enter the starting time...
</p>
<input id="numb" type="number">
<button type="button" onclick="start()">Start</button>
<button type="button" onclick="reset()">Reset</button>
<button type="button" onclick="clearInterval(t)">Stop</button>
<p id="timer" style="text-align:center;"></p>
<script>
var x;
var t;
var s;
var z;
Number(x).toFixed(2);
s=document.getElementById('timer');
function start() {
x=document.getElementById('numb').value;
Number(x).toFixed(2);
s.innerHTML=Number(x).toFixed(2);
down();
}
function down() {
if(x<=0){
s.innerHTML="Time's Up";
return;
}
x=x-0.01;
s.innerHTML=Number(x).toFixed(2);
t=setTimeout("down()",1000);
}
function reset() {
x=document.getElementById('numb').value;
s.innerHTML=x;
clearInterval(t);
}
</script>
</body>
</html>

