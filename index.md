---
title       : "Indicators of Human Development"
subtitle    : (from the 2014 Human Development Report)
author      : G. Lewandowski 
framework   : io2012        
highlighter : highlight.js  
hitheme     : tomorrow       
widgets     : [bootstrap]    
mode        : selfcontained 
knit        : slidify::knit2slides
---

## What is Human Development
From the [United Nations Development Programme, 
Human Development Report Office](http://hdr.undp.org/en/humandev):  

"2015 marks 25 years since the first Human Development Report introduced a new approach for advancing human wellbeing. Human development - or the human development approach - is about expanding the richness of human life, rather than simply the richness of the economy in which human beings live. It is an approach that is focused on people and their opportunities and choices."

### Human Development Index (HDI):
Is a summary measure of three central aspects of human development:  
1. a long and healthy life (Life Expectancy)       
2. access to knowledge (Education Index)   
3. a decent standard of living (GNI Index)  

The details for the [HDI calculation](http://hdr.undp.org/sites/default/files/hdr14_technical_notes.pdf) and the full [2014 Human Development Report](http://hdr.undp.org/sites/default/files/hdr14-report-en-1.pdf) are on the [United Nations Development Program](http://hdr.undp.org/en) website.

--- .class #id 

## HD Interactive Data-Exploration Application
### Description:
Interactive exploration of the impact of a.) Life Expectancy, b). Education and c). GNI per capita on HDI.   

[2014 Human Development Report Data](http://hdr.undp.org/en/data) was obtained from the Human Development Report website.

### Application Instructions:
Select three human development indicators (X, Y, & bubble size) to generate a bubble chart.
The bubble chart shows indicator Y as a function of indicator X.  Each bubble represents a country.
The bubble color indicates world region, and the bubble size corresponds to the value of the third human development indicator.

Hover over a bubble to see the complete information for a country. The chart is moveable, zoom-able, and reactive to your choices. So, go ahead and explore as many indicator combinations as you can think of!

--- .class #id 

## R code to produce a gvisBubbleChart




```r
suppressPackageStartupMessages(library(googleVis))
# Generate a bubble chart 
M <- gvisBubbleChart(data = data,idvar= "Country", xvar= "edu.index.2013", 
                     yvar="HDI.2013",sizevar="GNI.2013", 
                     colorvar= "PrimaryRegion", options=list(width=1000, height=500,
                                chartArea = "{top:50}", bubble="{textStyle:{color: 'none'},
                                        stroke:'none', opacity:0.6}",
                                hAxis="{title:'Education Index'}",
                                vAxis="{title:'Human Development Index', maxValue:1.2}",
                                explorer="{}"
                                )
                     )
```


--- .class #id 
## Example of Bubble Chart
Hover over a bubble to display country information. The chart is also zoom-able.
<!-- BubbleChart generated in R 3.1.3 by googleVis 0.5.9 package -->
<!-- Fri Apr 24 18:39:57 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataBubbleChartID1a2439091bab () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 "Norway",
0.91,
0.944,
"Europe",
63909.45 
],
[
 "Australia",
0.927,
0.933,
"Oceania",
41523.94 
],
[
 "Switzerland",
0.844,
0.917,
"Europe",
53761.92 
],
[
 "Netherlands",
0.894,
0.915,
"European Union",
42397.2 
],
[
 "United States",
0.89,
0.914,
"North America, Latin America, Caribbean",
52308.38 
],
[
 "Germany",
0.884,
0.911,
"European Union",
43048.68 
],
[
 "New Zealand",
0.917,
0.91,
"Oceania",
32569.37 
],
[
 "Canada",
0.85,
0.902,
"North America, Latin America, Caribbean",
41886.82 
],
[
 "Singapore",
0.768,
0.901,
"Asia",
72371.23 
],
[
 "Denmark",
0.873,
0.9,
"European Union",
42880.28 
],
[
 "Ireland",
0.887,
0.899,
"European Union",
33414.4 
],
[
 "Sweden",
0.83,
0.898,
"European Union",
43201.35 
],
[
 "Iceland",
0.847,
0.895,
"Europe",
35116.46 
],
[
 "United Kingdom",
0.86,
0.892,
"European Union",
35001.63 
],
[
 "Hong Kong",
0.767,
0.891,
"Asia",
52383.45 
],
[
 "South Korea",
0.865,
0.891,
"Asia",
30345.35 
],
[
 "Japan",
0.808,
0.89,
"Asia",
36746.83 
],
[
 "Liechtenstein",
0.762,
0.889,
"Europe",
87085.09 
],
[
 "Israel",
0.854,
0.888,
"Middle East",
29966.2 
],
[
 "France",
0.816,
0.884,
"European Union",
36628.78 
],
[
 "Austria",
0.794,
0.881,
"European Union",
42929.64 
],
[
 "Belgium",
0.812,
0.881,
"European Union",
39470.9 
],
[
 "Luxembourg",
0.762,
0.881,
"European Union",
58694.72 
],
[
 "Finland",
0.815,
0.879,
"European Union",
37366.07 
],
[
 "Slovenia",
0.863,
0.874,
"European Union",
26808.6 
],
[
 "Italy",
0.79,
0.872,
"European Union",
32668.99 
],
[
 "Spain",
0.794,
0.869,
"European Union",
30561.47 
],
[
 "Czech Republic",
0.866,
0.861,
"European Union",
24534.55 
],
[
 "Greece",
0.797,
0.853,
"European Union",
24657.99 
],
[
 "Brunei Darussalam",
0.692,
0.852,
"Asia",
70883.48 
],
[
 "Qatar",
0.686,
0.851,
"Middle East",
119029.12 
],
[
 "Cyprus",
0.776,
0.845,
"European Union",
26770.73 
],
[
 "Estonia",
0.859,
0.84,
"European Union",
23387.24 
],
[
 "Saudi Arabia",
0.723,
0.836,
"Middle East",
52109.36 
],
[
 "Lithuania",
0.877,
0.834,
"European Union",
23740.31 
],
[
 "Poland",
0.825,
0.834,
"European Union",
21487.18 
],
[
 "Andorra",
0.67,
0.83,
"Europe",
40597.12 
],
[
 "Slovakia",
0.802,
0.83,
"European Union",
25336.07 
],
[
 "Malta",
0.733,
0.829,
"European Union",
27022.18 
],
[
 "United Arab Emirates",
0.673,
0.827,
"Middle East",
58068.22 
],
[
 "Chile",
0.746,
0.822,
"North America, Latin America, Caribbean",
20804.03 
],
[
 "Portugal",
0.728,
0.822,
"European Union",
24130.07 
],
[
 "Hungary",
0.805,
0.818,
"European Union",
21239.13 
],
[
 "Bahrain",
0.714,
0.815,
"Middle East",
32072.13 
],
[
 "Cuba",
0.743,
0.815,
"North America, Latin America, Caribbean",
19844.1 
],
[
 "Kuwait",
0.646,
0.814,
"Middle East",
85819.68 
],
[
 "Croatia",
0.77,
0.812,
"Europe",
19024.93 
],
[
 "Latvia",
0.813,
0.81,
"European Union",
22185.73 
],
[
 "Argentina",
0.783,
0.808,
"North America, Latin America, Caribbean",
17296.7 
],
[
 "Uruguay",
0.712,
0.79,
"North America, Latin America, Caribbean",
18108.11 
],
[
 "Bahamas",
0.714,
0.789,
"North America, Latin America, Caribbean",
21414.27 
],
[
 "Montenegro",
0.774,
0.789,
"Europe",
14710.23 
],
[
 "Belarus",
0.82,
0.786,
"Europe",
16403.22 
],
[
 "Romania",
0.689,
0.785,
"European Union",
17432.66 
],
[
 "Libya",
0.748,
0.784,
"Africa",
21665.64 
],
[
 "Oman",
0.698,
0.783,
"Middle East",
42191.36 
],
[
 "Russian Federation",
0.603,
0.778,
"Europe",
22616.58 
],
[
 "Bulgaria",
0.78,
0.777,
"European Union",
15401.58 
],
[
 "Barbados",
0.749,
0.776,
"North America, Latin America, Caribbean",
13603.98 
],
[
 "Palau",
0.74,
0.775,
"Oceania",
12822.58 
],
[
 "Antigua and Barbuda",
0.787,
0.774,
"North America, Latin America, Caribbean",
18800.32 
],
[
 "Malaysia",
0.681,
0.773,
"Asia",
21823.93 
],
[
 "Mauritius",
0.671,
0.771,
"Africa",
16776.9 
],
[
 "Trinidad and Tobago",
0.718,
0.766,
"North America, Latin America, Caribbean",
25325.06 
],
[
 "Lebanon",
0.7,
0.765,
"Middle East",
16263.34 
],
[
 "Panama",
0.631,
0.765,
"North America, Latin America, Caribbean",
16379 
],
[
 "Venezuela",
0.657,
0.764,
"North America, Latin America, Caribbean",
17066.62 
],
[
 "Costa Rica",
0.682,
0.763,
"North America, Latin America, Caribbean",
13011.71 
],
[
 "Turkey",
0.654,
0.759,
"Europe",
18391.4 
],
[
 "Kazakhstan",
0.652,
0.757,
"Asia",
19440.65 
],
[
 "Mexico",
0.762,
0.756,
"North America, Latin America, Caribbean",
15854.09 
],
[
 "Seychelles",
0.638,
0.756,
"Africa",
24631.83 
],
[
 "Saint Kitts and Nevis",
0.636,
0.75,
"North America, Latin America, Caribbean",
20150.05 
],
[
 "Sri Lanka",
0.638,
0.75,
"Asia",
9249.91 
],
[
 "Iran",
0.738,
0.749,
"Middle East",
13450.7 
],
[
 "Azerbaijan",
0.683,
0.747,
"Asia",
15725.27 
],
[
 "Jordan",
0.7,
0.745,
"Middle East",
11337.03 
],
[
 "Serbia",
0.7,
0.745,
"Europe",
11300.9 
],
[
 "Brazil",
0.695,
0.744,
"North America, Latin America, Caribbean",
14274.77 
],
[
 "Georgia",
0.661,
0.744,
"Asia",
6889.52 
],
[
 "Grenada",
0.77,
0.744,
"North America, Latin America, Caribbean",
10338.92 
],
[
 "Peru",
0.724,
0.737,
"North America, Latin America, Caribbean",
11279.88 
],
[
 "Ukraine",
0.664,
0.734,
"Europe",
8214.53 
],
[
 "Belize",
0.796,
0.732,
"North America, Latin America, Caribbean",
9363.83 
],
[
 "Macedonia",
0.642,
0.732,
"Europe",
11744.85 
],
[
 "Bosnia and Herzegovina",
0.655,
0.731,
"Europe",
9430.78 
],
[
 "Armenia",
0.701,
0.73,
"Asia",
7952.35 
],
[
 "Fiji",
0.767,
0.724,
"Oceania",
7213.85 
],
[
 "Thailand",
0.608,
0.722,
"Asia",
13364.3 
],
[
 "Tunisia",
0.621,
0.721,
"Africa",
10439.7 
],
[
 "China",
0.61,
0.719,
"Asia",
11477.15 
],
[
 "Saint Vincent and the Grenadines",
0.657,
0.719,
"North America, Latin America, Caribbean",
10339.02 
],
[
 "Algeria",
0.643,
0.717,
"Africa",
12554.57 
],
[
 "Dominica",
0.607,
0.717,
"North America, Latin America, Caribbean",
9234.74 
],
[
 "Albania",
0.609,
0.716,
"Europe",
9225.05 
],
[
 "Jamaica",
0.668,
0.715,
"North America, Latin America, Caribbean",
8170.21 
],
[
 "Saint Lucia",
0.631,
0.714,
"North America, Latin America, Caribbean",
9250.98 
],
[
 "Colombia",
0.602,
0.711,
"North America, Latin America, Caribbean",
11526.53 
],
[
 "Ecuador",
0.594,
0.711,
"North America, Latin America, Caribbean",
9997.96 
],
[
 "Suriname",
0.588,
0.705,
"North America, Latin America, Caribbean",
15112.77 
],
[
 "Tonga",
0.72,
0.705,
"Oceania",
5315.73 
],
[
 "Dominican Republic",
0.59,
0.7,
"North America, Latin America, Caribbean",
10844.19 
],
[
 "Maldives",
0.548,
0.698,
"Asia",
10073.97 
],
[
 "Mongolia",
0.694,
0.698,
"Asia",
8465.76 
],
[
 "Turkmenistan",
0.679,
0.698,
"Asia",
11533.11 
],
[
 "Samoa",
0.702,
0.694,
"Oceania",
4707.91 
],
[
 "State of Palestine",
0.662,
0.686,
"Middle East",
5167.85 
],
[
 "Indonesia",
0.603,
0.684,
"Asia",
8970.35 
],
[
 "Botswana",
0.619,
0.683,
"Africa",
14791.95 
],
[
 "Egypt",
0.573,
0.682,
"Africa",
10399.77 
],
[
 "Paraguay",
0.587,
0.676,
"North America, Latin America, Caribbean",
7579.65 
],
[
 "Gabon",
0.589,
0.674,
"Africa",
16976.54 
],
[
 "Bolivia",
0.674,
0.667,
"North America, Latin America, Caribbean",
5551.94 
],
[
 "Moldova",
0.653,
0.663,
"Europe",
5041.2 
],
[
 "El Salvador",
0.553,
0.662,
"North America, Latin America, Caribbean",
7240.34 
],
[
 "Uzbekistan",
0.651,
0.661,
"Asia",
5227.37 
],
[
 "Philippines",
0.61,
0.66,
"Asia",
6381.44 
],
[
 "South Africa",
0.695,
0.658,
"Africa",
11787.91 
],
[
 "Syrian Arab Republic",
0.553,
0.658,
"Middle East",
5771.23 
],
[
 "Iraq",
0.467,
0.642,
"Middle East",
14007.32 
],
[
 "Guyana",
0.582,
0.638,
"North America, Latin America, Caribbean",
6340.8 
],
[
 "Viet Nam",
0.513,
0.638,
"Asia",
4892.41 
],
[
 "Cape Verde",
0.483,
0.636,
"Africa",
6364.83 
],
[
 "Micronesia (Federated States of)",
0.611,
0.63,
"Oceania",
3662.01 
],
[
 "Guatemala",
0.484,
0.628,
"North America, Latin America, Caribbean",
6865.97 
],
[
 "Kyrgyzstan",
0.656,
0.628,
"Asia",
3021.47 
],
[
 "Namibia",
0.52,
0.624,
"Africa",
9185.47 
],
[
 "Timor-Leste",
0.472,
0.62,
"Asia",
9673.61 
],
[
 "Honduras",
0.505,
0.617,
"North America, Latin America, Caribbean",
4137.65 
],
[
 "Morocco",
0.468,
0.617,
"Africa",
6905.18 
],
[
 "Vanuatu",
0.596,
0.616,
"Oceania",
2652.4 
],
[
 "Nicaragua",
0.484,
0.614,
"North America, Latin America, Caribbean",
4266 
],
[
 "Kiribati",
0.602,
0.607,
"Oceania",
2644.66 
],
[
 "Tajikistan",
0.639,
0.607,
"Asia",
2424.39 
],
[
 "India",
0.473,
0.586,
"Asia",
5149.81 
],
[
 "Bhutan",
0.421,
0.584,
"Asia",
6774.89 
],
[
 "Cambodia",
0.495,
0.584,
"Asia",
2805.43 
],
[
 "Ghana",
0.553,
0.573,
"Africa",
3532.33 
],
[
 "Laos",
0.436,
0.569,
"Asia",
4351.27 
],
[
 "Congo, Republic of the",
0.511,
0.564,
"Africa",
4909.37 
],
[
 "Zambia",
0.591,
0.561,
"Africa",
2898.19 
],
[
 "Bangladesh",
0.447,
0.558,
"Asia",
2713.09 
],
[
 "Sao Tome and Principe",
0.469,
0.558,
"Africa",
3110.65 
],
[
 "Equatorial Guinea",
0.415,
0.556,
"Africa",
21972.27 
],
[
 "Nepal",
0.452,
0.54,
"Asia",
2193.98 
],
[
 "Pakistan",
0.372,
0.537,
"Asia",
4651.64 
],
[
 "Kenya",
0.515,
0.535,
"Africa",
2157.94 
],
[
 "Swaziland",
0.551,
0.53,
"Africa",
5536.44 
],
[
 "Angola",
0.474,
0.526,
"Africa",
6322.94 
],
[
 "Myanmar",
0.371,
0.524,
"Asia",
3998.06 
],
[
 "Rwanda",
0.478,
0.506,
"Africa",
1403.26 
],
[
 "Cameroon",
0.486,
0.504,
"Africa",
2556.7 
],
[
 "Nigeria",
0.425,
0.504,
"Africa",
5353.38 
],
[
 "Yemen",
0.339,
0.5,
"Middle East",
3945.18 
],
[
 "Madagascar",
0.458,
0.498,
"Africa",
1333.45 
],
[
 "Zimbabwe",
0.5,
0.492,
"Africa",
1307.41 
],
[
 "Papua New Guinea",
0.376,
0.491,
"Oceania",
2452.98 
],
[
 "Solomon Islands",
0.405,
0.491,
"Oceania",
1384.57 
],
[
 "Comoros",
0.45,
0.488,
"Africa",
1504.87 
],
[
 "Tanzania (United Republic of)",
0.426,
0.488,
"Africa",
1702.12 
],
[
 "Mauritania",
0.352,
0.487,
"Africa",
2988.15 
],
[
 "Lesotho",
0.504,
0.486,
"Africa",
2797.89 
],
[
 "Senegal",
0.368,
0.485,
"Africa",
2169.26 
],
[
 "Uganda",
0.479,
0.484,
"Africa",
1335.15 
],
[
 "Benin",
0.414,
0.476,
"Africa",
1725.83 
],
[
 "Sudan",
0.306,
0.473,
"Africa",
3428.12 
],
[
 "Togo",
0.514,
0.473,
"Africa",
1128.74 
],
[
 "Haiti",
0.374,
0.471,
"North America, Latin America, Caribbean",
1635.69 
],
[
 "Afghanistan",
0.365,
0.468,
"Asia",
1903.66 
],
[
 "Djibouti",
0.306,
0.467,
"Africa",
3108.91 
],
[
 "Cote d'Ivoire",
0.389,
0.452,
"Africa",
2774.27 
],
[
 "Gambia",
0.346,
0.441,
"Africa",
1557.31 
],
[
 "Ethiopia",
0.317,
0.435,
"Africa",
1302.64 
],
[
 "Malawi",
0.44,
0.414,
"Africa",
714.94 
],
[
 "Liberia",
0.367,
0.412,
"Africa",
752 
],
[
 "Mali",
0.305,
0.407,
"Africa",
1499.38 
],
[
 "Guinea-Bissau",
0.325,
0.396,
"Africa",
1090.15 
],
[
 "Mozambique",
0.372,
0.393,
"Africa",
1011.04 
],
[
 "Guinea",
0.294,
0.392,
"Africa",
1141.86 
],
[
 "Burundi",
0.37,
0.389,
"Africa",
749.11 
],
[
 "Burkina Faso",
0.25,
0.388,
"Africa",
1601.51 
],
[
 "Eritrea",
0.228,
0.381,
"Africa",
1146.89 
],
[
 "Sierra Leone",
0.305,
0.374,
"Africa",
1815.1 
],
[
 "Chad",
0.256,
0.372,
"Africa",
1621.77 
],
[
 "Central African Republic",
0.318,
0.341,
"Africa",
587.86 
],
[
 "Congo, Democratic Republic of the",
0.372,
0.338,
"Africa",
443.96 
],
[
 "Niger",
0.198,
0.337,
"Africa",
872.53 
] 
];
data.addColumn('string','Country');
data.addColumn('number','edu.index.2013');
data.addColumn('number','HDI.2013');
data.addColumn('string','PrimaryRegion');
data.addColumn('number','GNI.2013');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartBubbleChartID1a2439091bab() {
var data = gvisDataBubbleChartID1a2439091bab();
var options = {};
options["width"] =   1000;
options["height"] =    500;
options["chartArea"] = {top:50};
options["bubble"] = {textStyle:{color: 'none'},
                                        stroke:'none', opacity:0.6};
options["hAxis"] = {title:'Education Index'};
options["vAxis"] = {title:'Human Development Index', maxValue:1.2};
options["explorer"] = {};

    var chart = new google.visualization.BubbleChart(
    document.getElementById('BubbleChartID1a2439091bab')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "corechart";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartBubbleChartID1a2439091bab);
})();
function displayChartBubbleChartID1a2439091bab() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartBubbleChartID1a2439091bab"></script>
 
<!-- divChart -->
  
<div id="BubbleChartID1a2439091bab" 
  style="width: 1000; height: 500;">
</div>









