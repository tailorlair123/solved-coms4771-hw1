Download Link: https://assignmentchef.com/product/solved-coms4771-hw1
<br>
<ul>

 <li>[Statistical Estimators] Here we will study some statistical estimators.

  <ul>

   <li>Given <em>a,b </em>∈ R s.t. <em>a &lt; b</em>, consider the density .</li>

  </ul></li>

</ul>

Suppose that <em>n </em>samples <em>x</em><sub>1</sub><em>,…,x<sub>n </sub></em>are drawn i.i.d. from <em>p</em>(<em>x</em>|<em>θ</em>). What is the Maximum Likelihood Estimate (MLE) of <em>θ </em>given the samples?

<ul>

 <li>Show that for the MLE <em>θ</em><sub>ML </sub>of a parameter <em>θ </em>∈ R<em><sup>d </sup></em>and any known injective function <em>g </em>: R<em><sup>d </sup></em>→ R<em><sup>k</sup></em>, the MLE of <em>g</em>(<em>θ</em>) is <em>g</em>(<em>θ</em><sub>ML</sub>).</li>

 <li>For a 1-dimensional Gaussian distribution, give two examples for each of the following types of estimators for the mean parameter.

  <ul>

   <li>consistent and unbiased.</li>

   <li>consistent, but not unbiased.</li>

   <li>not consistent, but unbiased.</li>

   <li>neither consistent, nor unbiased.</li>

  </ul></li>

 <li>[Universality of Decision Trees]

  <ul>

   <li>Show that any binary classifier <em>g </em>: {0<em>,</em>1}<em><sup>D </sup></em>→ {0<em>,</em>1} can be implemented as a decision tree classifier. That is, for any classifier <em>g </em>there exists a decision tree classifier <em>T </em>with <em>k </em>nodes <em>n</em><sub>1</sub><em>,…,n<sub>k </sub></em>(each <em>n<sub>i </sub></em>with a corresponding threshhold <em>t<sub>i</sub></em>), such that <em>g</em>(<em>x</em>) = <em>T</em>(<em>x</em>) for all <em>x </em>∈ {0<em>,</em>1}<em><sup>D</sup></em>.</li>

   <li>What is the best possible bound one can give on the maximum height of such a decision tree <em>T </em>(from part (i))? For what function <em>g </em>is the bound tight?</li>

  </ul></li>

 <li>[Designing the optimal predictor for continuous output spaces] We studied in class that the “Bayes Classifier” <em>f </em>:= argmax is optimal in the sense that it minimizes generalization error over the underlying distribution, that is, it maximizes E<em>x,y</em>[<strong>1</strong>[<em>g</em>(<em>x</em>) = <em>y</em>]]. But what can we say when the output space Y is continuous?</li>

</ul>

Consider predictors of the kind <em>g </em>: X → R that predict a real-valued output for a given input <em>x </em>∈ X. One intuitive way to define the quality of of such a predictor <em>g </em>is as

<em>Q</em>(<em>g</em>) := E<em>x,y</em>[(<em>g</em>(<em>x</em>) − <em>y</em>)<sup>2</sup>]<em>.</em>

Observe that one would want a predictor <em>g </em>with the lowest <em>Q</em>(<em>g</em>).

<ul>

 <li>Show that if one defines the predictor as <em>f</em>(<em>x</em>) := E[<em>Y </em>|<em>X </em>= <em>x</em>], then <em>Q</em>(<em>f</em>) ≤ <em>Q</em>(<em>g</em>) for any <em>g</em>, thereby showing that <em>f </em>is the optimal predictor with respect to <em>Q </em>for continuous output spaces.</li>

 <li>If one instead defines quality as, which <em>f </em>is the optimal predictor? Justify your reasoning.</li>

 <li>[Finding (local) minima of generic functions] Finding extreme values of functions in a closed form is often not possible. Here we will develop a generic algorithm to find the extremal values of a function. Consider a smooth function <em>f </em>: R →

  <ul>

   <li>Recall that Taylor’s Remainder Theorem states:</li>

  </ul></li>

</ul>

For any <em>a,b </em>∈ R, exists <em>z </em>∈ [<em>a,b</em>], such that.

Assuming that there exists <em>L </em>≥ 0 such that for all <em>a,b </em>∈ R, |<em>f</em><sup>0</sup>(<em>a</em>) − <em>f</em><sup>0</sup>(<em>b</em>)| ≤ <em>L</em>|<em>a </em>− <em>b</em>|, prove the following statement:

For any <em>x </em>∈ R, there exists some <em>η &gt; </em>0, such that if <em>x</em>¯ := <em>x</em>−<em>ηf</em><sup>0</sup>(<em>x</em>), then <em>f</em>(¯<em>x</em>) ≤ <em>f</em>(<em>x</em>), with equality if and only if <em>f</em><sup>0</sup>(<em>x</em>) = 0.

(Hint: first show that the assumption implies that <em>f </em>has bounded second derivative, i.e., <em>f</em><sup>00</sup>(<em>z</em>) ≤ <em>L </em>(for all <em>z</em>); then apply the remainder theorem and analyze the difference <em>f</em>(<em>x</em>) − <em>f</em>(¯<em>x</em>)).

<ul>

 <li>Part (i) gives us a generic recipe to find a new value <em>x</em>¯ from an old value <em>x </em>such that <em>f</em>(¯<em>x</em>) ≤ <em>f</em>(<em>x</em>). Using this result, develop an iterative algorithm to find a local minimum starting from an initial value <em>x</em><sub>0</sub>.</li>

 <li>Use your algorithm to find the minimum of the function <em>f</em>(<em>x</em>) := (<em>x </em>− 4)<sup>2 </sup>+ 2<em>e<sup>x</sup></em>. You should code your algorithm in a scientific programming language like Matlab to find the solution.</li>

</ul>

<ul>

 <li>[Email spam classification case study] Download the datafile hw1data.tar.gz. This datafile contains email data of around 5,000 emails divided in two folders ‘ham’ and ‘spam’ (there are about 3,500 emails in the ‘ham’ folder, and 1,500 emails in the ‘spam’ folder). Each email is a separate text file in these folders. These emails have been slightly preprocessed to remove meta-data information.

  <ul>

   <li>(Embedding text data in Euclidean space) The first challenge you face is how to systematically embed text data in a Euclidean space. It turns out that one successful way</li>

  </ul></li>

</ul>

of transforming text data into vectors is via “Bag-of-words” model. Basically, given a dictionary of all possible words in some order, each text document can be represented as a word count vector of how often each word from the dictionary occurs in that document.

Example: suppose our dictionary <em>D </em>with vocabulary size 10 (|<em>D</em>| = 10). The words (ordered in say alphabetical order) are:

1: also

2: football

3: games

4: john

5: likes

6: Mary

7: movies

8: to

9: too

10: watch

Then any text document created using this vocabulary can be embedded in R<sup>|</sup><em>D</em>| by counting how often each word appears in the text document.

Say, an example text document <em>t </em>is:

John likes to watch football. Mary likes movies.

Then the corresponding word count vector in |<em>D</em>| = 10 dimensions is:

[ 0 1 0 1 2 1 1 1 0 1]

(because the word “also” occurs 0 times, “football” occurs 1 time, etc. in the document.)

While such an embedding is extremely useful, a severe drawback of such an embedding is that it treats similar meaning words (e.g. watch, watches, watched, watching, etc.) independently as separate coordinates. To overcome this issue one should preprocess the entire corpus to remove the common trailing forms (such as “ing”, “ed”, “es”, etc.) and get only the root word. This is called word-stemming.

Your first task is to embed the given email data in a Euclidean space by: first performing word stemming, and then applying the bag-of-words model.

Some useful references:

<ul>

 <li>Bag-of-words: <a href="https://en.wikipedia.org/wiki/Bag-of-words_model">http://en.wikipedia.org/wiki/Bag-of-words</a> <a href="https://en.wikipedia.org/wiki/Bag-of-words_model">model</a></li>

 <li>Word stemming: <a href="https://en.wikipedia.org/wiki/Stemming">http://en.wikipedia.org/wiki/Stemming</a></li>

 <li>Once you have a nice Euclidean representation of the email data. Your next task is to develop a spam classifier to classify new emails as spam or not-spam. You should compare performance of naive-bayes, nearest neighbor (with <em>L</em><sub>1</sub>, <em>L</em><sub>2 </sub>and <em>L</em><sub>∞ </sub>metric) and decision tree classifiers.</li>

</ul>

(you may use builtin functions for performing basic linear algebra and probability calculations but you should write the classifiers from scratch.) You must submit your code to Courseworks to receive full credit.

<ul>

 <li>Which classifier (discussed in part (ii)) is better for the email spam classification dataset? You must justify your answer with appropriate performance graphs demonstrating the superiority of one classifier over the other. Example things to consider: you should evaluate how the classifier behaves on a holdout ‘test’ sample for various splits of the data; how does the training sample size affects the classification performance.</li>

</ul>