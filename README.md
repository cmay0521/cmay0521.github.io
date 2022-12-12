<!DOCTYPE html>
<!-- saved from url=(0068)file:///C:/Users/Charlie%20May/Desktop/d3_project/html%20webpage.htm -->
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <title>Dr.John Snow Cholera D3 Visualization Project</title>
  <script src="./Dr.John Snow Cholera D3 Visualization Project_files/d3.js.download"></script>
    <link rel="stylesheet" href="./Dr.John Snow Cholera D3 Visualization Project_files/bootstrap.min.css">
    <script src="./Dr.John Snow Cholera D3 Visualization Project_files/bootstrap.min.js.download"></script>
    <script src="./Dr.John Snow Cholera D3 Visualization Project_files/jquery-3.2.1.slim.min.js.download"></script>
    <script src="./Dr.John Snow Cholera D3 Visualization Project_files/d3.v4.js.download"></script>
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


<div class="row">
	<div class="col-md-4 col-sm-12" id="BarGraph" style="text-align: left;font-size: medium;"></div>
</div>

<!-- <div id="canvas" style="text-align: center;"></div> -->
	<!-- <div class="col-md-4 col-sm-8" id="lineGraph" style="text-align: center;">Deaths between 19-Aug and 29-Sep</div> -->
	<!-- <div class="col-md-4 col-sm-8" id="streetMap" style="text-align: right;" >Street Map</div> -->
    <!-- <div class="col-md-4 col-sm-8" id="pieChart" style="text-align: center;"><label style="font-size: large;">Deaths by Age group</label></div> -->
    <!-- <div class="col-md-4 col-sm-8" id="BarGraph" style="text-align: center;"><label style="font-size: large;">Deaths by Gender</label></div> -->




<!-- Load d3.js -->
<script src="./Dr.John Snow Cholera D3 Visualization Project_files/d3.v4.js.download"></script>

<!-- Create a div where the graph will take place -->
<div id="my_dataviz"><svg width="460" height="400"><g transform="translate(60,30)"><g transform="translate(0,300)" fill="none" font-size="10" font-family="sans-serif" text-anchor="middle"><path class="domain" stroke="#000" d="M0.5,6V0.5H370.5V6"></path><g class="tick" opacity="1" transform="translate(100.90909090909092,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">Male (0)</text></g><g class="tick" opacity="1" transform="translate(269.09090909090907,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">Female (1)</text></g></g><g class="myYaxis" fill="none" font-size="10" font-family="sans-serif" text-anchor="end"><path class="domain" stroke="#000" d="M-6,300.5H0.5V0.5H-6"></path><g class="tick" opacity="1" transform="translate(0,300.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">0</text></g><g class="tick" opacity="1" transform="translate(0,280.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">20</text></g><g class="tick" opacity="1" transform="translate(0,260.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">40</text></g><g class="tick" opacity="1" transform="translate(0,240.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">60</text></g><g class="tick" opacity="1" transform="translate(0,220.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">80</text></g><g class="tick" opacity="1" transform="translate(0,200.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">100</text></g><g class="tick" opacity="1" transform="translate(0,180.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">120</text></g><g class="tick" opacity="1" transform="translate(0,160.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">140</text></g><g class="tick" opacity="1" transform="translate(0,140.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">160</text></g><g class="tick" opacity="1" transform="translate(0,120.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">180</text></g><g class="tick" opacity="1" transform="translate(0,100.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">200</text></g><g class="tick" opacity="1" transform="translate(0,80.50000000000003)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">220</text></g><g class="tick" opacity="1" transform="translate(0,60.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">240</text></g><g class="tick" opacity="1" transform="translate(0,40.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">260</text></g><g class="tick" opacity="1" transform="translate(0,20.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">280</text></g><g class="tick" opacity="1" transform="translate(0,0.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">300</text></g></g><rect x="33.636363636363654" y="17" width="134.54545454545453" height="283" fill="rgb(105, 179, 162)"></rect><rect x="201.8181818181818" y="13" width="134.54545454545453" height="287" fill="rgb(105, 179, 162)"></rect></g></svg><svg width="460" height="400"><g transform="translate(60,30)"><g transform="translate(0,300)" fill="none" font-size="10" font-family="sans-serif" text-anchor="middle"><path class="domain" stroke="#000" d="M0.5,6V0.5H370.5V6"></path><g class="tick" opacity="1" transform="translate(35.80645161290326,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">0-10</text></g><g class="tick" opacity="1" transform="translate(95.48387096774196,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">11-20</text></g><g class="tick" opacity="1" transform="translate(155.16129032258067,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">21-40</text></g><g class="tick" opacity="1" transform="translate(214.83870967741936,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">41-60</text></g><g class="tick" opacity="1" transform="translate(274.51612903225805,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">61-80</text></g><g class="tick" opacity="1" transform="translate(334.1935483870968,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">&gt;80</text></g></g><g class="myYaxis" fill="none" font-size="10" font-family="sans-serif" text-anchor="end"><path class="domain" stroke="#000" d="M-6,300.5H0.5V0.5H-6"></path><g class="tick" opacity="1" transform="translate(0,300.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">0</text></g><g class="tick" opacity="1" transform="translate(0,270.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">20</text></g><g class="tick" opacity="1" transform="translate(0,240.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">40</text></g><g class="tick" opacity="1" transform="translate(0,210.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">60</text></g><g class="tick" opacity="1" transform="translate(0,180.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">80</text></g><g class="tick" opacity="1" transform="translate(0,150.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">100</text></g><g class="tick" opacity="1" transform="translate(0,120.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">120</text></g><g class="tick" opacity="1" transform="translate(0,90.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">140</text></g><g class="tick" opacity="1" transform="translate(0,60.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">160</text></g><g class="tick" opacity="1" transform="translate(0,30.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">180</text></g><g class="tick" opacity="1" transform="translate(0,0.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">200</text></g></g><rect x="11.935483870967772" y="85.5" width="47.74193548387097" height="214.5" fill="rgb(105, 179, 162)"></rect><rect x="71.61290322580648" y="231" width="47.74193548387097" height="69" fill="rgb(105, 179, 162)"></rect><rect x="131.29032258064518" y="213" width="47.74193548387097" height="87" fill="rgb(105, 179, 162)"></rect><rect x="190.96774193548387" y="214.5" width="47.74193548387097" height="85.5" fill="rgb(105, 179, 162)"></rect><rect x="250.6451612903226" y="160.5" width="47.74193548387097" height="139.5" fill="rgb(105, 179, 162)"></rect><rect x="310.32258064516134" y="40.5" width="47.74193548387097" height="259.5" fill="rgb(105, 179, 162)"></rect></g></svg><svg width="460" height="400"><g transform="translate(60,10)"><g transform="translate(0,360)" fill="none" font-size="10" font-family="sans-serif" text-anchor="middle"><path class="domain" stroke="#000" d="M0.5,6V0.5H370.5V6"></path><g class="tick" opacity="1" transform="translate(34.13636363636364,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">10</text></g><g class="tick" opacity="1" transform="translate(71.51010101010101,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">20</text></g><g class="tick" opacity="1" transform="translate(108.88383838383838,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">30</text></g><g class="tick" opacity="1" transform="translate(146.25757575757575,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">40</text></g><g class="tick" opacity="1" transform="translate(183.63131313131314,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">50</text></g><g class="tick" opacity="1" transform="translate(221.0050505050505,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">60</text></g><g class="tick" opacity="1" transform="translate(258.3787878787879,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">70</text></g><g class="tick" opacity="1" transform="translate(295.7525252525253,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">80</text></g><g class="tick" opacity="1" transform="translate(333.12626262626264,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">90</text></g><g class="tick" opacity="1" transform="translate(370.5,0)"><line stroke="#000" y2="6"></line><text fill="#000" y="9" dy="0.71em">100</text></g></g><g fill="none" font-size="10" font-family="sans-serif" text-anchor="end"><path class="domain" stroke="#000" d="M-6,360.5H0.5V0.5H-6"></path><g class="tick" opacity="1" transform="translate(0,360.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">0</text></g><g class="tick" opacity="1" transform="translate(0,332.8076923076923)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">1</text></g><g class="tick" opacity="1" transform="translate(0,305.11538461538464)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">2</text></g><g class="tick" opacity="1" transform="translate(0,277.4230769230769)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">3</text></g><g class="tick" opacity="1" transform="translate(0,249.73076923076923)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">4</text></g><g class="tick" opacity="1" transform="translate(0,222.03846153846152)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">5</text></g><g class="tick" opacity="1" transform="translate(0,194.34615384615384)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">6</text></g><g class="tick" opacity="1" transform="translate(0,166.65384615384616)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">7</text></g><g class="tick" opacity="1" transform="translate(0,138.96153846153845)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">8</text></g><g class="tick" opacity="1" transform="translate(0,111.26923076923077)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">9</text></g><g class="tick" opacity="1" transform="translate(0,83.57692307692304)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">10</text></g><g class="tick" opacity="1" transform="translate(0,55.884615384615415)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">11</text></g><g class="tick" opacity="1" transform="translate(0,28.19230769230768)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">12</text></g><g class="tick" opacity="1" transform="translate(0,0.5)"><line stroke="#000" x2="-6"></line><text fill="#000" x="-9" dy="0.32em">13</text></g></g><g><circle stroke="black" r="8.5" style="fill: none; opacity: 0;" cx="186.8686868686869" cy="228.73846153846154"></circle></g><g><text text-anchor="left" alignment-baseline="middle" style="opacity: 0;" x="201.8686868686869" y="228.73846153846154">x:51  -  y:4.74</text></g><path fill="none" stroke="steelblue" stroke-width="1.5" d="M0,359.16923076923075L3.737373737373738,358.89230769230767L7.474747474747476,358.33846153846156L11.212121212121213,357.5076923076923L14.949494949494952,356.4L18.686868686868685,355.0153846153846L22.424242424242426,353.0769230769231L26.16161616161616,350.8615384615385L29.898989898989903,347.53846153846155L33.63636363636364,343.66153846153844L37.37373737373737,338.95384615384614L41.11111111111111,333.13846153846157L44.84848484848485,326.2153846153846L48.58585858585859,317.9076923076923L52.32323232323232,308.7692307692308L56.06060606060606,297.96923076923076L59.79797979797981,286.33846153846156L63.535353535353536,273.32307692307694L67.27272727272728,259.4769230769231L71.01010101010101,244.8L74.74747474747474,229.56923076923076L78.48484848484848,214.06153846153848L82.22222222222221,198.55384615384617L85.95959595959596,183.32307692307694L89.6969696969697,168.64615384615385L93.43434343434345,155.0769230769231L97.17171717171718,142.61538461538464L100.9090909090909,131.53846153846155L104.64646464646464,122.12307692307692L108.38383838383838,114.64615384615385L112.12121212121212,109.10769230769228L115.85858585858587,105.78461538461539L119.59595959595961,104.1230769230769L123.33333333333333,104.67692307692303L127.07070707070707,106.61538461538458L130.8080808080808,110.49230769230772L134.54545454545456,115.4769230769231L138.2828282828283,121.84615384615384L142.02020202020202,129.04615384615386L145.75757575757575,137.07692307692307L149.49494949494948,145.66153846153844L153.23232323232324,154.79999999999998L156.96969696969697,163.93846153846155L160.70707070707073,172.79999999999998L164.44444444444443,181.93846153846155L168.1818181818182,190.79999999999998L171.91919191919192,199.10769230769233L175.65656565656565,207.41538461538462L179.3939393939394,214.89230769230767L183.13131313131314,222.09230769230768L186.8686868686869,228.73846153846154L190.6060606060606,234.83076923076925L194.34343434343435,240.36923076923077L198.08080808080808,245.07692307692307L201.8181818181818,249.5076923076923L205.55555555555557,253.66153846153847L209.29292929292927,257.26153846153846L213.03030303030306,260.5846153846154L216.76767676767676,263.3538461538461L220.5050505050505,266.12307692307695L224.24242424242425,268.3384615384615L227.97979797979798,270.55384615384617L231.71717171717174,272.7692307692308L235.45454545454544,274.4307692307692L239.19191919191923,276.36923076923074L242.92929292929293,277.75384615384615L246.66666666666666,279.4153846153846L250.40404040404042,280.8L254.14141414141415,282.18461538461537L257.8787878787879,283.2923076923077L261.6161616161616,284.4L265.35353535353534,285.7846153846154L269.0909090909091,286.89230769230767L272.8282828282828,288L276.5656565656566,289.10769230769233L280.3030303030303,290.2153846153846L284.04040404040404,291.6L287.77777777777777,292.7076923076923L291.5151515151515,293.81538461538463L295.2525252525253,295.2L298.98989898989896,296.5846153846154L302.72727272727275,297.96923076923076L306.4646464646465,299.3538461538461L310.2020202020202,301.0153846153846L313.93939393939394,302.4L317.67676767676767,304.0615384615385L321.41414141414145,305.7230769230769L325.1515151515151,307.66153846153844L328.88888888888886,309.32307692307694L332.62626262626264,311.26153846153846L336.3636363636364,313.2L340.1010101010101,315.1384615384615L343.83838383838383,317.3538461538461L347.5757575757576,319.2923076923077L351.3131313131313,321.5076923076923L355.050505050505,323.44615384615383L358.7878787878788,325.66153846153844L362.52525252525254,327.6L366.26262626262627,329.81538461538463L370,331.75384615384615"></path><rect width="370" height="360" style="fill: none; pointer-events: all;"></rect></g></svg></div>
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




<!-- Load d3.js -->
<script src="./Dr.John Snow Cholera D3 Visualization Project_files/d3.v4.js.download"></script>

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




<!-- Load d3.js -->
<script src="./Dr.John Snow Cholera D3 Visualization Project_files/d3.v4.js.download"></script>

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



<!-- Load Leaflet -->
<link rel="stylesheet" href="./Dr.John Snow Cholera D3 Visualization Project_files/leaflet.css" integrity="sha512-puBpdR0798OZvTTbP4A8Ix/l+A4dHDD0DGqYW6RQ+9jxkRFclaxxQb/SJAWZfWAkuyeQUytO7+7N4QKrDh+drA==" crossorigin="">
<script src="./Dr.John Snow Cholera D3 Visualization Project_files/leaflet.js.download" integrity="sha512-nMMmRyTVoLYqjP9hrbed9S+FzjZHW5gY1TWCHA5ckwXZBadntCNs8kEqAWdrb9O7rxbCaA4lKTIWjDXZxflOcA==" crossorigin=""></script>

<!-- Create an element where the map will take place -->
<div id="mapid" class="leaflet-container leaflet-touch leaflet-retina leaflet-fade-anim leaflet-grab leaflet-touch-drag leaflet-touch-zoom" tabindex="0" style="position: relative;"><div class="leaflet-pane leaflet-map-pane" style="transform: translate3d(426px, 0px, 0px);"><div class="leaflet-pane leaflet-tile-pane"><div class="leaflet-layer " style="z-index: 1; opacity: 1;"><div class="leaflet-tile-container leaflet-zoom-animated" style="z-index: 6; transform: translate3d(0px, 0px, 0px) scale(1);"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(163px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(419px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(163px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(419px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(163px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(419px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-93px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(675px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-93px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(675px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-93px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(675px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-349px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(931px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-349px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(931px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-349px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(931px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-605px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(1187px, 91px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-605px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(1187px, -165px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(-605px, 347px, 0px); opacity: 1;"><img alt="" role="presentation" src="./Dr.John Snow Cholera D3 Visualization Project_files/SnowMap_Points.png" class="leaflet-tile leaflet-tile-loaded" style="width: 256px; height: 256px; transform: translate3d(1187px, 347px, 0px); opacity: 1;"></div></div></div><div class="leaflet-pane leaflet-shadow-pane"></div><div class="leaflet-pane leaflet-overlay-pane"></div><div class="leaflet-pane leaflet-marker-pane"></div><div class="leaflet-pane leaflet-tooltip-pane"></div><div class="leaflet-pane leaflet-popup-pane"></div><div class="leaflet-proxy leaflet-zoom-animated" style="transform: translate3d(2047px, 1389px, 0px) scale(8);"></div></div><div class="leaflet-control-container"><div class="leaflet-top leaflet-left"><div class="leaflet-control-zoom leaflet-bar leaflet-control"><a class="leaflet-control-zoom-in" href="file:///C:/Users/Charlie%20May/Desktop/d3_project/html%20webpage.htm#" title="Zoom in" role="button" aria-label="Zoom in">+</a><a class="leaflet-control-zoom-out" href="file:///C:/Users/Charlie%20May/Desktop/d3_project/html%20webpage.htm#" title="Zoom out" role="button" aria-label="Zoom out">−</a></div></div><div class="leaflet-top leaflet-right"></div><div class="leaflet-bottom leaflet-left"></div><div class="leaflet-bottom leaflet-right"><div class="leaflet-control-attribution leaflet-control"><a href="http://leafletjs.com/" title="A JS library for interactive maps">Leaflet</a> | Map data © <a href="https://www.openstreetmap.org/">OpenStreetMap</a></div></div></div></div>

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


  <p>Dr. John Snow's map of London's 1854 cholera epidemic was a true master piece. It was the first time that anyone had established a link between contaminated water and cholera. The visualization provided compelling evidence and made the case for public health policies to improve water sanitation. The map remains one of the most remarkable and insightful visualizations ever created. This project uses D3 to give a today version of Dr. Snow's work.
<script>
</script></p>
  </body>
</html>

