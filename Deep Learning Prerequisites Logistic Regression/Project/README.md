<h1>Course Project</h1>
<ul>
<li>We will do some practical data analysis throughout the course</li>
<li>So you know exactly how the techniques you learn are used in real-world scenario</li>
<li>Data could have been derived from <ul>
<li>Excel Spreadsheet</li>
<li>SQL Table</li>
<li>Log files̥</li>
</ul></li>
<li>Suppose you are a data scientist at an e-commerce store</li>
<li>Want to predict user actions on our site</li>
<li>Direct monetary impact
<ul>
<li>Predict bounce --> Prompt</li>
<li>Discover which area of the site are weak</li>
<li>Ex. Mobile, User-friendliness</li>
<li>Make data-driven decisions</li>
<li>Use science to improve user experience</li>
</ul>
</li>
<li>CSV(comma-separated values), i.e. a table</li>
<li>Headers:
<ul>
<li>Is_mobile (0/1)</li>
<li>N_products_viewed (int >= 0)</li>
<li>Visit_duration (real >= 0)</li>
<li>Is_returning_visitor (0/1)</li>
<li>Time_of_day (0/1/2/3 = 24h split into 4 categories, assumptions?)</li>
<li>User_action (bounce/ add_to_cart/ begin_checkout/ finish_checkout)</li>
</ul>
</li>
<li>User_action is what we'll predict</li>
<li>Logistic class: binary classification</li>
<li>Neural network class: multi-class classification</li>
</ul>

<h2>Data Pre-processing</h2>
<hr/>
<ul> 
<li>Logistic regression / neural network work on numerical vectors, not categories</li>
<li>One-hot encoding
<ul><li>Ex. Time of day = 0, 1, 2, 3 becomes:
<img src="..\img\timeDay.png" width="600px" height="200px"/>
</li>
</ul>
</ul>
<h2>Binary categories</h2>
<hr>

<p>Aren't is_mobile and is_returning_visitor also categories?
<br>Yes but we don't need 2 columns "off" and "on". <br> Just absorb the "off" into the bias term</p>
<h2>Numerical columns</h2>
<hr/>
<p>These are n_products_viewed and visitors_duration<br/> Int = category or ordinal? Can we just treat it as real? Is 1.5 "in between" 1 and 2?
<br/> Ex. if user who view 3 or fewer products don't convert, and users who view 4+ products do convert, then what does 0.1 mean? 0.5? 2.5?
<br/>We expect those to behave the same as "3 or fewer".<br/>Simple way of treating numbers: normalization (0 mean, 1 standard deviation)<br/>sigmoid(10) ~= sigmoid(11) ~= sigmoid(12) ~= 0.999...
<br/><b>Ζ=(X- μ)/σ</b>
</p>
<h2>Integration with the course</h2>
<hr/>
<ul>
<li>Each supervised machine learning model typically has 2 tasks:<ul>
<li>1) Prediction - input --> predict output</li>
<li>2) Training - how to make output accurate?</li>
</ul></li>
<li>Each task has a corresponding section in this course</li>
<li>After each section, which will teach you both theory and how to implement it in code, we will come back to this example.</li>
<li>1) How will we make predictions on our e-commerce data?</li>
<li>2) How will we train our model on the e-commerce data?</li>
</ul>