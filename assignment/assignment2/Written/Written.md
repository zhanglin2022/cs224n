## Written: Understanding word2vec (26 points)
(a) (3 points) Show that the naive-softmax loss given in Equation (2) is the same as the cross-entropy loss between $y$ and $\hat{y}$; i.e., show that<br>
$$
-\sum_{w\in \mathrm{Vocab}}{y_w}\log \left( \hat{y}_w \right) =-\log \left( \hat{y}_o \right) \ \tag{3}
$$
Your answer should be one line.  

$$
-\sum_{w\in Vocab}{y_w}\log \left( \hat{y}_w \right) =-\left(\sum_{\begin{array}{c} w\in Vocab\\ w\ne o\\ \end{array}}^{}{y_w}\log \left( \begin{array}{c} \hat{y}_w\\\end{array} \right) +\mathrm{y}_o\log \left( \hat{y}_o \right) \right) =-\log \left( \hat{y}_o \right) 
$$


(b) (5 points) Compute the partial derivative of $ J_{\text {naive-softmax }}\left(v_{c}, o, U\right) $ with respect to $V_c$.Please write your answer in terms of $y$, $\hat{y}$ and $U$. Note that in this course, we expect your final answers to follow the shape convention. This means that the partial derivative of any function f(x) with respect to x should have the same shape as x. For this subpart, please present your answer in vectorized form. In particular, you may not refer to specific elements of $y$, $\hat{y}$ and $U$ in your final answer (such as $y_1$, $y_2$, ...).


(c) (5 points) Compute the partial derivatives of $ J_{\text {naive-softmax }}\left(v_{c}, o, U\right) $ with respect to each of the ‘outside’ word vectors $u_w$'s. There will be two cases: when w = o, the true ‘outside’ word vector, and w $\neq$ o, for all other words. Please write your answer in terms of $y$, $\hat{y}$ and $v_c$. . In this subpart, you may use specific elements within these terms as well, such as ( $y_1$, $y_2$, ...).


