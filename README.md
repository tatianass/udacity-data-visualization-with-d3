# udacity-data-visualization-with-d3
Repository with examples made from the Udacity course.

#notes from video:
- With d3 4, to load the function in the console, you must put the "!" at the beggining of the function and remove the comments;

D3 Building blocks
https://d17h27t6h515a5.cloudfront.net/topher/2016/July/57966c9c_data-vis-demo/data-vis-demo.zip
https://d3js.org/d3.v4.min.js

d3.select('.main').html(null);
var svg = d3.select('.main').append('svg');
svg.attr('width', 600).attr('height', 300); 
//var y = d3.scaleLinear().domain([15, 90]).range([250,0]);
var y = d3.scale.linear().domain([15, 90]).range([250,0]);
//var x = d3.scaleLog().domain([250,100000]).range([0, 600]);
var x = d3.scale.log().domain([250,100000]).range([0, 600]);
//var r = d3.scaleSqrt().domain([52070,1380000000]).range([10, 40]);
var r = d3.scale.sqrt().domain([52070,1380000000]).range([10, 40]);
svg.append('circle').attr('fill', 'red').attr('r',r(1380000000)).attr('cx', x(13330)).attr('cy', y(77));
