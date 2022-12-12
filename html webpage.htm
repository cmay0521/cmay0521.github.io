<!DOCTYPE html>
<html lang = "en">
<head>
  <meta charset="utf-8">
  <title>Dr.John Snow Cholera D3 Visualization Project</title>
  <script src='https://cdnjs.cloudflare.com/ajax/libs/d3/3.4.13/d3.js'></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
    <script src="https://d3js.org/d3.v4.js"></script>
  <style>
       div.tooltip {
            font: 12px sans-serif;
            text-align: center;
            position: absolute;
            padding: 2px;
            border-radius: 8px;
            border: 0px;
            pointer-events: none;
            background-color:yellowgreen;
        }
  </style>
</head>
<body>
  <button>Documentation Page</button>
  <button>Youtube Video</button>
  <h3 style="text-align: center;font-weight: bold;">Dr. John Snow's Map of 1854 Cholera Epidemic</h3>
<div style="padding-top: 30px;"></div>
<div id="canvas" style="text-align: center;"></div>
<div>
    <div style="text-align: center; padding-left: 500px">
    </div>
</div>
<!-- <div id='lineGraph' style="float: left;width: 500px;padding-left: 80px;"> -->
    <!-- <div id='slider' style='width:970px'></div> -->
<!-- </div>
<div id='streetMap'></div>
<div id='pieChart'></div> -->
<div class="row">
    </div>
    <!-- <div class="col-md-4 col-sm-12" id="BarGraph" style="text-align: center;font-size: medium;"></div>
    <div class="col-md-4 col-sm-12" id="pieChart" style="text-align: center;font-size: medium;">Deaths by Age group</div> -->

</div>
<div class="row">
	<div class="col-md-4 col-sm-12" id="BarGraph" style="text-align: left;font-size: medium;"></div>
</div>

<!-- <div id="canvas" style="text-align: center;"></div> -->
	<!-- <div class="col-md-4 col-sm-8" id="lineGraph" style="text-align: center;">Deaths between 19-Aug and 29-Sep</div> -->
	<!-- <div class="col-md-4 col-sm-8" id="streetMap" style="text-align: right;" >Street Map</div> -->
    <!-- <div class="col-md-4 col-sm-8" id="pieChart" style="text-align: center;"><label style="font-size: large;">Deaths by Age group</label></div> -->
    <!-- <div class="col-md-4 col-sm-8" id="BarGraph" style="text-align: center;"><label style="font-size: large;">Deaths by Gender</label></div> -->

<!DOCTYPE html>
<meta charset="utf-8">

<!-- Load d3.js -->
<script src="https://d3js.org/d3.v4.js"></script>

<!-- Create a div where the graph will take place -->
<div id="my_dataviz"></div>
<script>

// create 2 data_set
var data1 = [
   {group: "Male (0)", value: 283},
   {group: "Female (1)", value: 287},
];

// set the dimensions and margins of the graph
var margin = {top: 30, right: 30, bottom: 70, left: 60},
    width = 460 - margin.left - margin.right,
    height = 400 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svg = d3.select("#my_dataviz")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

// X axis
var x = d3.scaleBand()
  .range([ 0, width ])
  .domain(data1.map(function(d) { return d.group; }))
  .padding(0.2);
svg.append("g")
  .attr("transform", "translate(0," + height + ")")
  .call(d3.axisBottom(x))


// Add Y axis
var y = d3.scaleLinear()
  .domain([0, 300])
  .range([ height, 0]);
svg.append("g")
  .attr("class", "myYaxis")
  .call(d3.axisLeft(y));

// A function that create / update the plot for a given variable:
function update(data) {

  var u = svg.selectAll("rect")
    .data(data)

  u
    .enter()
    .append("rect")
    .merge(u)
    .transition()
    .duration(1000)
      .attr("x", function(d) { return x(d.group); })
      .attr("y", function(d) { return y(d.value); })
      .attr("width", x.bandwidth())
      .attr("height", function(d) { return height - y(d.value); })
      .attr("fill", "#69b3a2")
}


// Initialize the plot with the first dataset
update(data1)

</script>

<!DOCTYPE html>
<meta charset="utf-8">

<!-- Load d3.js -->
<script src="https://d3js.org/d3.v4.js"></script>

<!-- Create a div where the graph will take place -->
<div id="my_dataviz"></div>
<script>

// create 2 data_set
var data1 = [
   {group: "0-10", value: 143},
   {group: "11-20", value: 46},
   {group: "21-40", value: 58},
   {group: "41-60", value: 57},
   {group: "61-80", value: 93},
   {group: ">80", value: 173},
];

// set the dimensions and margins of the graph
var margin = {top: 30, right: 30, bottom: 70, left: 60},
    width = 460 - margin.left - margin.right,
    height = 400 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svg = d3.select("#my_dataviz")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

// X axis
var x = d3.scaleBand()
  .range([ 0, width ])
  .domain(data1.map(function(d) { return d.group; }))
  .padding(0.2);
svg.append("g")
  .attr("transform", "translate(0," + height + ")")
  .call(d3.axisBottom(x))

// Add Y axis
var y = d3.scaleLinear()
  .domain([0, 200])
  .range([ height, 0]);
svg.append("g")
  .attr("class", "myYaxis")
  .call(d3.axisLeft(y));

// A function that create / update the plot for a given variable:
function update(data) {

  var u = svg.selectAll("rect")
    .data(data)

  u
    .enter()
    .append("rect")
    .merge(u)
    .transition()
    .duration(1000)
      .attr("x", function(d) { return x(d.group); })
      .attr("y", function(d) { return y(d.value); })
      .attr("width", x.bandwidth())
      .attr("height", function(d) { return height - y(d.value); })
      .attr("fill", "#69b3a2")
}

// Initialize the plot with the first dataset
update(data1)

</script>

<!DOCTYPE html>
<meta charset="utf-8">

<!-- Load d3.js -->
<script src="https://d3js.org/d3.v4.js"></script>

<!-- Create a div where the graph will take place -->
<div id="my_dataviz"></div>
<script>

// set the dimensions and margins of the graph
var margin = {top: 10, right: 30, bottom: 30, left: 60},
    width = 460 - margin.left - margin.right,
    height = 400 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svg = d3.select("#my_dataviz")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

//Read the data
d3.csv("https://raw.githubusercontent.com/holtzy/D3-graph-gallery/master/DATA/data_IC.csv",function(data) {

  // Add X axis --> it is a date format
  var x = d3.scaleLinear()
    .domain([1,100])
    .range([ 0, width ]);
  svg.append("g")
    .attr("transform", "translate(0," + height + ")")
    .call(d3.axisBottom(x));

  // Add Y axis
  var y = d3.scaleLinear()
    .domain([0, 13])
    .range([ height, 0 ]);
  svg.append("g")
    .call(d3.axisLeft(y));

  // This allows to find the closest X index of the mouse:
  var bisect = d3.bisector(function(d) { return d.x; }).left;

  // Create the circle that travels along the curve of chart
  var focus = svg
    .append('g')
    .append('circle')
      .style("fill", "none")
      .attr("stroke", "black")
      .attr('r', 8.5)
      .style("opacity", 0)

  // Create the text that travels along the curve of chart
  var focusText = svg
    .append('g')
    .append('text')
      .style("opacity", 0)
      .attr("text-anchor", "left")
      .attr("alignment-baseline", "middle")

  // Add the line
  svg
    .append("path")
    .datum(data)
    .attr("fill", "none")
    .attr("stroke", "steelblue")
    .attr("stroke-width", 1.5)
    .attr("d", d3.line()
      .x(function(d) { return x(d.x) })
      .y(function(d) { return y(d.y) })
      )

  // Create a rect on top of the svg area: this rectangle recovers mouse position
  svg
    .append('rect')
    .style("fill", "none")
    .style("pointer-events", "all")
    .attr('width', width)
    .attr('height', height)
    .on('mouseover', mouseover)
    .on('mousemove', mousemove)
    .on('mouseout', mouseout);


  // What happens when the mouse move -> show the annotations at the right positions.
  function mouseover() {
    focus.style("opacity", 1)
    focusText.style("opacity",1)
  }

  function mousemove() {
    // recover coordinate we need
    var x0 = x.invert(d3.mouse(this)[0]);
    var i = bisect(data, x0, 1);
    selectedData = data[i]
    focus
      .attr("cx", x(selectedData.x))
      .attr("cy", y(selectedData.y))
    focusText
      .html("x:" + selectedData.x + "  -  " + "y:" + selectedData.y)
      .attr("x", x(selectedData.x)+15)
      .attr("y", y(selectedData.y))
    }
  function mouseout() {
    focus.style("opacity", 0)
    focusText.style("opacity", 0)
  }

})

</script>
<!DOCTYPE html>
<meta charset="utf-8">

<!-- Load Leaflet -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.4/dist/leaflet.css" integrity="sha512-puBpdR0798OZvTTbP4A8Ix/l+A4dHDD0DGqYW6RQ+9jxkRFclaxxQb/SJAWZfWAkuyeQUytO7+7N4QKrDh+drA==" crossorigin=""/>
<script src="https://unpkg.com/leaflet@1.3.4/dist/leaflet.js" integrity="sha512-nMMmRyTVoLYqjP9hrbed9S+FzjZHW5gY1TWCHA5ckwXZBadntCNs8kEqAWdrb9O7rxbCaA4lKTIWjDXZxflOcA==" crossorigin=""></script>

<!-- Create an element where the map will take place -->
<div id="mapid"></div>

<style>
#mapid { height: 400px; }
</style>

<script>

// Initialize the map
// [50, -0.1] are the latitude and longitude
// 4 is the zoom
// mapid is the id of the div where the map will appear
var mymap = L
  .map('mapid')
  .setView([50, -0.1], 4);

// Add a tile to the map = a background. Comes from OpenStreetmap
L.tileLayer(
    'https://blog.rtwilson.com/wp-content/uploads/2012/01/SnowMap_Points.png', {
    attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a>',
    maxZoom: 6,
    }).addTo(mymap);


</script>

<body>
  <p>Dr. John Snow's map of London's 1854 cholera epidemic was a true master piece. It was the first time that anyone had established a link between contaminated water and cholera. The visualization provided compelling evidence and made the case for public health policies to improve water sanitation. The map remains one of the most remarkable and insightful visualizations ever created. This project uses D3 to give a today version of Dr. Snow's work.
<script>
