<h1>Linear Classification</h1>
<h2>2-dimensional classification</h2>
<hr/>
<div style="display:flex;">
<p style="margin-right:20px" >y = mx + b<br/> or<br/> 0 = ax + by + c<br/>a=1, b=-1, c=0
</p>
<img  src="..\..\img\2-dClassification.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
<div style="display:flex;">
<p style="margin-right:20px;">0 = x - y is the line<br/>
I have a new point at (2,1).<br/>
Should it be classified as an 'x' or 'o'?
<br/>
h(x,y) = x - y<br/>
h(2,1) = 1> 0 --> 'o'</p>
<img src="..\..\img\2d2.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
<div style="display:flex;">
<p style="margin-right:20px;">0 = x - y is the line<br/>
I have a new point at (1,2).<br/>
Should it be classified as an 'x' or 'o'?
<br/>
h(x,y) = x - y<br/>
h(2,1) = -1< 0 --> 'x'</p>
<img src="..\..\img\2d3.png" width="200px" height="200px"/>
</div>
<p>&nbsp;</p>
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
<p>&nbsp;</p>
<h2>Neural Network history</h2>
<hr/>
<ul>
<li>Neural networks have a long history in the artificial intelligence field going back to the mid-1900s.
</li>
<li>The neuron is the basic building blick of the neural network / brain.
</ul>
<h2>The Neuron</h2>
<img src="..\..\img\neuron.png" width="300px" height="200px"/>
<p>&nbsp;</p>

<h2>Hodgkin-Huxley</h2>
<img src="..\..\img\hh.png" width="300px" height="200px"/>
<p>&nbsp;</p>

<h2>FitzHugh-Nagumo</h2>
<img src="..\..\img\fn.png" width="200px" height="100px">

<p>&nbsp;</p>
<h2>Neuron Analogies</h2>
<ol>
<li>Many inputs --> One output
</li>
<li>Spike or no spike --> 0 / 1 output</li>
<li>Synapse strengths --> linear weights</li>
</ol>
<img src="..\..\img\na.png" width="200px" height="200px">

<p>&nbsp;</p>
<p>&nbsp;</p>
<h2>What does the output of logistic regression mean?</h2>
<li>I don't want to get into this too much, since it will only really began to make sense when we go to the next section (training)</li>
<h3><b>output = σ(w<sup>T</sup>x) ∈ (0, 1)</b></h3>
<p>&nbsp;</p>

<h2>What's classification again?</h2>
<div style="display:flex">
<p style="padding:20px">Each dot is represented by a feature vector (x)
<br/>
Its color is represented by a label (y)
<br/>Convention: y = 0 or 1
<br/> E.g. blue = 1, red = 0
</p>
<img src="..\..\img\dc.png" width="200px" height="200px">
</div>

<p>&nbsp;</p>
<h2>Convention: y = 0 or 1</h2>
<ul>
<li>For binary classification, we use the 2 values 0 and 1 to represented each class</li>
<li>You probably expected this anyway!</li>
<li>You wouldn't pick any random number, e.g. 42 and 97.5</li>
</ul>
<p>&nbsp;</p>
<h2>The output of logistic regression</h2>
<ul>
<li>We can interpret the output of logistic regression as the probability that y belongs to class 1, given x</li>
<li>Since y can only have 2 values:<br/>p( y = 0 | x ) = 1 - p( y = 1 | x )</li>
<li>i.e. they must sum to 1<br/>    p( y = 0 | x ) + p( y = 1 | x ) = 1</li>
</ul>
<h3><b>p( y = 1 | x ) = σ(w<sup>T</sup>x) ∈ (0, 1)</b></h3><p>&nbsp;</p>

<ul>
<li> Handy way of making predictions</li>
</ul>
<code>
<pre>
if p(y=1 | x) > p(y=0 | x):
    Predict class 1
else:
    Predict class 0
</pre>
</code>
<p>&nbsp;</p>
<h2>Equivalent expression</h2>
<ul><li>if you can't see how this is right away, try to prove it as an exercise</li></ul>
<code>
<pre>
    if p(y=1 | x) > 0.5:
        Predict class 1
    else:
        Predict class 0
</pre>
</code>

<p>&nbsp;</p>
<h2>Using 0.5 as a threshold</h2>
<ul>
<li>it is also to see that we can write an equivalent expression by rounding</li>
<li>Rounding gives us either 0 or 1 - exactly what we want!
<ul><li>Now you can see why 0 / 1 is convenient</li></ul>
</li>
</ul>
<code>
<pre>
Predict round(p(y=1 | x))
</pre>
</code>
<ul>
<li>
Side-note: it's possible to use threshold other than 0.5 (but not common in deep learning)
</li>
</ul>
