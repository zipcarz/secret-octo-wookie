secret-octo-wookie
==================

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>jQuery.parseHTML demo</title>
  <script src="//code.jquery.com/jquery-1.10.2.js"></script>
</head>
<body>
 
<div id="log">
  <h3>Content:</h3>
</div>
 
<script>
var $log = $( "#log" ),
  str = "hello, <b>my name is</b> jQuery.",
  html = $.parseHTML( str ),
  nodeNames = [];
 
// Append the parsed HTML
$log.append( html );
 
// Gather the parsed HTML's node names
$.each( html, function( i, el ) {
  nodeNames[ i ] = "<li>" + el.nodeName + "</li>";
});
 
// Insert the node names
$log.append( "<h3>Node Names:</h3>" );
$( "<ol></ol>" )
  .append( nodeNames.join( "" ) )
  .appendTo( $log );
</script>
 
</body>
</html>
