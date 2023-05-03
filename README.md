Download Link: https://assignmentchef.com/product/solved-cpts-570-machine-learning-homework-2
<br>






NOTE 1: Please use a word processing software (e.g., Microsoft word or Latex) to write your answers. The rationale is that it is sometimes hard to read and understand the hand-written answers. Thanks for your understanding.

NOTE 2: Please ensure that all the graphs are appropriately labeled (x-axis, y-axis, and each curve). The caption or heading of each graph should be informative and self-contained.

<h1>1           Analytical Part (3 percent grade)</h1>

This part will be graded as a PASS or FAIL.

<ol>

 <li>Suppose we have <em>n</em><sub>+ </sub>positive training examples and <em>n</em><sub>− </sub>negative training examples. Let <em>C</em><sub>+ </sub>be the center of the positive examples and <em>C</em><sub>− </sub>be the center of the negative examples, i.e., and. Consider a simple classifier called CLOSE</li>

</ol>

that classifies a test example <em>x </em>by assigning it to the class whose center is closest.

<ul>

 <li>Show that the decision boundary of the CLOSE classifier is a linear hyperplane of the form <em>sign</em>(<em>w </em> <em>x </em>+ <em>b</em>). Compute the values of <em>w </em>and <em>b </em>in terms of <em>C</em><sub>+ </sub>and <em>C</em><sub>−</sub>.</li>

 <li>Recall that the weight vector can be written as a linear combination of all the training examples: . Compute the dual weights (<em>α</em>’s). How many of the training examples are support vectors?</li>

</ul>

<ol start="2">

 <li>Suppose we use the following radial basis function (RBF) kernel:), which has some implicit unknown mapping <em>φ</em>(<em>x</em>).

  <ul>

   <li>Prove that the mapping <em>φ</em>(<em>x</em>) corresponding to RBF kernel has infinite dimensions.</li>

   <li>Prove that for any two input examples <em>x<sub>i </sub></em>and <em>x<sub>j</sub></em>, the squared Euclidean distance of their corresponding points in the higher-dimensional space defined by <em>φ </em>is less than 2, i.e., k<em>φ</em>(<em>x<sub>i</sub></em>) − <em>φ</em>(<em>x<sub>j</sub></em>)k<sup>2 </sup>≤ 2.</li>

  </ul></li>

 <li>The decision boundary of a SVM with a kernel function (via implicit feature mapping <em>φ</em>(<em>.</em>)) is defined as follows:</li>

</ol>

<em>w </em>· <em>φ</em>(<em>x</em>) + <em>b </em>= <sup>P</sup><em><sub>i</sub></em>∈<em><sub>SV </sub>y<sub>i</sub>α<sub>i</sub>K</em>(<em>x<sub>i</sub>,x</em>) + <em>b </em>= <em>f</em>(<em>x</em>;<em>α,b</em>)

, where <em>w </em>and <em>b </em>are parameters of the decision boundary in the feature space <em>phi </em>defined by the kernel function <em>K</em>, SV is the set of support vectors, and <em>α<sub>i </sub></em>is the dual weight of the <em>i<sup>th </sup></em>support vector.

Let us assume that we use the radial basis function (RBF) kernel); also assume that the training examples are linearly separable in the feature space <em>φ </em>and SVM finds a decision boundary that perfectly separates the training examples.

If we choose a testing example <em>x<sub>far </sub></em>that is far away from any training instance <em>x<sub>i </sub></em>(distance here is measured in the original feature space &lt;<em><sup>d</sup></em>). Prove that <em>f</em>(<em>x<sub>far</sub></em>;<em>α,b</em>) ≈ <em>b.</em>

<ol start="4">

 <li>The function <em>K</em>(<em>x<sub>i</sub>,x<sub>j</sub></em>) = −h<em>x<sub>i</sub>,x<sub>j</sub></em>i is a valid kernel. Prove or Disprove it.</li>

 <li>You are provided with <em>n </em>training examples: (<em>x</em><sub>1</sub><em>,y</em><sub>1</sub>)<em>,</em>(<em>x</em><sub>2</sub><em>,y</em><sub>2</sub>)<em>,</em>··<em>,</em>(<em>x<sub>n</sub>,y<sub>n</sub>,</em>), where <em>x<sub>i </sub></em>is the input example, <em>y<sub>i </sub></em>is the class label (+1 or -1). The teacher gave you some additional information by specifying the costs for different mistakes <em>C</em><sub>+ </sub>and <em>C</em><sub>−</sub>, where <em>C</em><sub>+ </sub>and <em>C</em><sub>− </sub>stand for the cost of misclassifying a positive and negative example respectively.</li>

 <li>How will you modify the Soft-margin SVM formulation to be able to leverage this extra information? Please justify your answer.</li>

 <li>You are provided with a set of n training examples: (<em>x</em><sub>1</sub><em>,y</em><sub>1</sub>)<em>,</em>(<em>x</em><sub>2</sub><em>,y</em><sub>2</sub>)<em>,</em>··<em>,</em>(<em>x<sub>n</sub>,y<sub>n</sub>,</em>), where <em>x<sub>i </sub></em>is the input example, <em>y<sub>i </sub></em>is the class label (+1 or -1). Suppose <em>n </em>is very large (say in the order of millions). In this case, standard SVM training algorithms will not scale due to large training set.</li>

</ol>

Tom wants to devise a solution based on “Coarse-to-Fine” framework of problem solving. The basic idea is to cluster the training data; train a SVM classifier based on the clusters (coarse problem); refine the clusters as needed (fine problem); perform training on the finer problem; and repeat until convergence. Suppose we start with <em>k</em><sub>+ </sub>positive clusters and <em>k</em><sub>− </sub>negative clusters to begin with (a cluster is defined as a set of examples). Please specify the <em>mathematical formulation </em>(define all the variables used in your formulation) and concrete algorithm for each of the following steps to instantiate this idea:

<ol>

 <li>How to define the SVM training formulation for a given level of coarseness: a set of <em>k</em><sub>+ </sub>positive clusters and a set of <em>k</em><sub>− </sub>negative clusters?</li>

 <li>How to refine the clusters based on the resulting SVM classifier?</li>

 <li>What is the stopping criteria?</li>

</ol>

Optional question: For what kind of problems will this solution fail?

<ol start="7">

 <li>You are provided with a set of <em>n </em>training examples: (<em>x</em><sub>1</sub><em>,y</em><sub>1</sub>)<em>,</em>(<em>x</em><sub>2</sub><em>,y</em><sub>2</sub>)<em>,</em>··<em>,</em>(<em>x<sub>n</sub>,y<sub>n</sub>,</em>), where <em>x<sub>i </sub></em>is the input example, <em>y<sub>i </sub></em>is the class label (+1 or -1). Suppose <em>n </em>is very large (say in the order of millions). In this case, online kernelized Perceptron algorithms will not scale if the number of allowed support vectors are <em>unbounded</em>.

  <ol>

   <li>Suppose you have trained using kernelized Perceptron algorithm (without any bounds onsupport vectors) and got a set of support vectors <em>SV </em>. Tom wants to use this classifier for real-time prediction and cannot afford more than <em>B </em>kernel evaluations for each classification decision. Please give an algorithm to select <em>B </em>support vectors from <em>SV </em>. You need to motivate your design choices in order to convince Tom to use your solution.</li>

   <li>Tom wants to train using kernelized Perceptron algorithm, but wants to use at most <em>B </em>support vectors during the training process. Please modify the standard kernelized Perceptron training algorithm (from class slides) for this new setting. You need to motivate your design choices in order to convince Tom to use your solution.</li>

  </ol></li>

</ol>

<h1>2           Programming and Empirical Analysis Part (5 percent grade)</h1>

<ol>

 <li>Empirical analysis question. You can use a publicly available SVM classifier implementation(e.g., scikit-learn) for SVM related experiments. scikit-learn (<a href="http://scikit-learn.org/stable/modules/svm.html">http://scikit-learn.org/ </a><a href="http://scikit-learn.org/stable/modules/svm.html">stable/modules/svm.html</a><a href="http://scikit-learn.org/stable/modules/svm.html">)</a>.</li>

</ol>

You will use the Fashion MNIST data (<a href="https://github.com/zalandoresearch/fashion-mnist">https://github.com/zalandoresearch/fashion-mnist</a><a href="https://github.com/zalandoresearch/fashion-mnist">)</a>. There is a fixed training and testing set. From training data, use first 80 percent for “training” and last 20 percent as “validation data”.

Each example is a 28×28 grayscale image, associated with a label from 10 classes: 0 Tshirt/top, 1 Trouser, 2 Pullover, 3 Dress, 4 Coat, 5 Sandal, 6 Shirt, 7 Sneaker, 8 Bag, 9 Ankle boot.

You will use ONLY training data for training and testing data for evaluation.

<ul>

 <li>Using a linear kernel, train the SVM on the training data for different values of <em>C </em>parameter: 10<sup>−4</sup><em>,</em>10<sup>−3</sup><em>,</em>10<sup>−2</sup><em>,</em>10<sup>−1</sup><em>,</em>10<sup>0</sup><em>,</em>10<sup>1</sup><em>,</em>10<sup>2</sup><em>,</em>10<sup>3</sup><em>,</em>10<sup>4</sup>. Compute the training accuracy, validation accuracy, and testing accuracy for the SVM obtained with different values of the C parameter. Plot the training accuracy, validation accuracy, and testing accuracy as a function of <em>C </em>(<em>C </em>value on x-axis and Accuracy on y-axis) – one curve each for training, validation, and testing data. Also, plot the number of support vectors (if applicable for the SVM toolkit you are using) as a function of <em>C</em>. List your observations.</li>

 <li>Select the best value of hyper-parameter <em>C </em>based on the accuracy on validation set and train a linear SVM on the <em>combined </em>set of training and validation examples. Compute the testing accuracy and the corresponding confusion matrix: a 10 × 10 matrix.</li>

 <li>Repeat the experiment (a) with the best <em>C </em>value from (a) with polynomial kernel of degree 2, 3, and 4. Compare the training, validation, testing accuracies, and the number of support vectors for differnt kernels (linear, polynomial kernel of degree 2, polynomial kernel of degree 3, and polynomial kernel of degree 4). List your observations.</li>

</ul>

<ol start="2">

 <li>Programming question. You will implement the kernelized Perceptron training algorithm (discussed in the class) for <em>multi-class </em>

  <ul>

   <li>You will use the Fashion MNIST data. Train the kernelized Perceptron classifier for 5 iterations with polynomial kernel (pick the best degree out of 2, 3, and 4 from the above experiment). Plot the number of mistakes as a function of training iterations. Compute the training, validation, and testing accuracy at the end of 5 iterations.</li>

  </ul></li>

 <li>Programming question. “Breast Cancer” Classifier using Decision Trees. You will use thefollowing dataset for this question: <a href="https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29">https://archive.ics.uci.edu/ml/datasets/Breast+ </a><a href="https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29">Cancer+Wisconsin+%28Diagnostic%29</a><a href="https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29">.</a> You will use the first 70 percent examples for training, next 10 percent examples for validation, and last 20 percent examples for testing.

  <ul>

   <li>Implement the ID3 decision tree learning algorithm that we discussed in the class. Thekey step in the decision tree learning is choosing the next feature to split on. Implement the information gain heuristic for selecting the next feature. Please see lecture notes or <a href="https://en.wikipedia.org/wiki/ID3_algorithm">https://en.wikipedia.org/wiki/ID3_algorithm</a> for more details. Do the following to select candidate thresholds for continuous features: Sort all candidate values for feature <em>f </em>from training data. Suppose <em>f</em><sub>1</sub><em>,f</em><sub>2</sub><em>,</em>··<em>,f<sub>n </sub></em>is the sorted list. The candidate thresholds are chosen as <em>f<sub>i </sub></em>+ (<em>f<sub>i</sub></em><sub>+1 </sub>− <em>f<sub>i</sub></em>)<em>/</em>2 for <em>i</em>=1 to <em>n</em>.</li>

   <li>Run the decision tree construction algorithm on the training examples. Compute theaccuracy on validation examples and testing examples.</li>

   <li>Implement the decision tree pruning algorithm discussed in the class (via validation data).</li>

   <li>Run the pruning algorithm on the decision tree constructed using training examples.Compute the accuracy on validation examples and testing examples. List your observations by comparing the performance of decision tree with and without pruning.</li>

  </ul></li>

</ol>

To debug and test your implementation, you can employ scikit-learn (<a href="http://scikit-learn.org/stable/modules/tree.html">http://scikit-learn. </a><a href="http://scikit-learn.org/stable/modules/tree.html">org/stable/modules/tree.html</a><a href="http://scikit-learn.org/stable/modules/tree.html">)</a>.

<h1>3           Instructions for Submission</h1>

Please follow the below instructions. If you do not follow them, your homework will not be graded. We will provide a dropbox folder link for the homework submission.

<strong>PDF submission. </strong>One PDF file with both answers for analytical part (Part I) and empirical analysis questions with results/analysis (Part-II). Please label x-axis, y-axis, and name of the graphs appropriately. Please name this file as WWSUID-LASTNAME.pdf (e.g., 111222-Fern.pdf).

<strong>Code submission. </strong>You will submit one zip file for your code as per the instructions below. If your script and/or code does not execute, we will try to give some partial credit by looking at the overall code contents.

<ul>

 <li>Mention the programming language and version (e.g., Python 2.5) that you used.</li>

 <li>Submit one folder with name WSUID-LASTNAME.zip (e.g., 111222-Fern.zip) and include a README file.</li>

 <li>Include a script to run the code and it should be referred in the README file. Please make sure that your script runs on a standard linux machine.</li>

 <li>Don’t submit the data folder. Assume there is a folder “data” with all the files.</li>

 <li>Output of your programs should be well-formatted in order to answer the empirical analysis questions.</li>

 <li>Structure your code meaningfully and add comments to make it readable.</li>

</ul>

If you have collaborated or discussed the homework with some student, please provide this information with all the relevant details. If we find that the code of two different students has traces of plagiarism, both students will be penalized and we will report the academic dishonesty case to graduate school (see https://communitystandards.wsu.edu/policies-and-reporting/academic-integritypolicy/). The bottom line is please DO NOT even think of going this route. It is very unpleasant to deal with these things for both faculty, TA, and students involved.


