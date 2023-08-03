# Retail Analytics
This project focuses on enhancing customer experience by providing customers relevant recommendations on grocery store items that are most commonly bought based on either their purchase history, items in cart, or other associations, through a machine learning model that uses Association Rule Mining (an a priori algorithm)

# The Context
The goal of our analysis and report is to build personalized grocery baskets and an intelligent product recommendation system to improve the customer online experience which will help the "company" keep their existing customers but also conquer those who are still hesitating to join. In order to achieve that, our team would provide TNG Strategic Solutions and recommendations to help them optimize the sales of their grocery baskets, so client do not spend too much time online looking for specific items.

Our company is obsessed about providing their customers best experience possible and has asked us to improve the shopping experience of the customer by providing them with pre- grocery baskets for weekly groceries. Our target audience is the end customer of the website. With the dataset supplied, we can recommend them product(s) that the customer will most likely buy and add it to the basket. Basket will be customizable, allowing the customer to add/ edit/ delete the items. Initially, the baskets will be created with available purchase history and with time TNG will be able to accurately predict the weekly groceries by further capturing the purchase data of the customers.


<p>5.4 Assessing and Developing our Association Rules</p>
</blockquote>
<p>Now we can finally apply our rule association algorithm to our
transaction data that we have just formatted. To get an initial sense of
what we will be looking for, we will first run our algorithm on the
order data with the default parameters.</p>
<div class="sourceCode" id="cb7"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb7-1"><a href="#cb7-1" tabindex="-1"></a>default_rules <span class="ot">&lt;-</span> <span class="fu">apriori</span>(order_transactions, <span class="at">parameter =</span> <span class="fu">list</span>(<span class="at">supp=</span><span class="fl">0.001</span>), <span class="at">control =</span> <span class="fu">list</span>(<span class="at">memopt =</span> <span class="cn">TRUE</span>))</span></code></pre></div>
<pre><code>## Apriori
## 
## Parameter specification:
##  confidence minval smax arem  aval originalSupport maxtime support minlen
##         0.8    0.1    1 none FALSE            TRUE       5   0.001      1
##  maxlen target  ext
##      10  rules TRUE
## 
## Algorithmic control:
##  filter tree heap memopt load sort verbose
##     0.1 TRUE TRUE   TRUE TRUE    2    TRUE
## 
## Absolute minimum support count: 3421 
