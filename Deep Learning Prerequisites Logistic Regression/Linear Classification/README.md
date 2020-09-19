<h1>Linear Classification</h1>
<h2>2-dimensional classification</h2>
<hr/>
<div style="display:flex;">
<p style="margin-right:20px" >y = mx + b<br/> or<br/> 0 = ax + by + c<br/>a=1, b=-1, c=0
</p>
<img  src="..\img\2-dClassification.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
<div style="display:flex;">
<p style="margin-right:20px;">0 = x - y is the line<br/>
I have a new point at (2,1).<br/>
Should it be classified as an 'x' or 'o'?
<br/>
h(x,y) = x - y<br/>
h(2,1) = 1> 0 --> 'o'</p>
<img src="..\img\2d2.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
<div style="display:flex;">
<p style="margin-right:20px;">0 = x - y is the line<br/>
I have a new point at (1,2).<br/>
Should it be classified as an 'x' or 'o'?
<br/>
h(x,y) = x - y<br/>
h(2,1) = -1< 0 --> 'x'</p>
<img src="..\img\2d3.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
<h2>Machine learning lingo</h2>
<hr/>
<p>
We call (x,y) --> (x<sub>1</sub>, x<sub>2</sub>) = <b>x</b>
<br/>
We rename the constants to w<sub>1</sub>
<br/>We call the bias term / intercept w<sub>0</sub><br/>
h(x) = w<sub>0</sub> + w<sub>1</sub>x<sub>1</sub> + w<sub>2</sub>x<sub>2</sub><br/>
We say h() is a <b>linear combination</b> of the components of <b>x</b>
<br/>In vector form: h(<b>x</b>) = <b>w</b><sup>T</sup><b>x</b>
<br/>In 3-dimensions: line --> plane, In > 3 dimensions: hyperplane
</p>