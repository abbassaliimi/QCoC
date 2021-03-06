# QCoC
<h1>Question Classification of CoQA (QCoC) dataset</h1>

Dataset (json file): https://www.kaggle.com/datasets/saliimiabbas/question-classification-of-coqa-qcoc
<br>Paper: https://ieeexplore.ieee.org/abstract/document/9536971

<b>Class categories and definition:</b>
<ol>
  <li><b>YES/NO :</b><br><ul>Per its name, this class is intended for question with ground truth <i>yes</i> or <i>no</i> answer. In CoQA, some yes/no answers are with additional text (e.g: "Yes, shampoo is on sale today"). This type of answer will also be categorized under this class as the ground truth is still yes or no (similar case is implied to answer with yes or no keyword appearing at the back of the sentence).</ul><br></li>
  <li><b>UNKNOWN :</b><br><ul>As part of CoQA answer’s features, some questions are unanswerable. Unanswerable is because there is simply no factual answer in the given context. Instead of making up answers, good QA system must know when not to answer the unanswerable question. Because if the fact is not there, making up answer is incorrect answer.</ul><br></li> 
  <li><b>PICKING :</b><br><ul>From multiple selections in extracted span of context text, one selection is to be picked as an answer. Picking is essentially Factual (the next class) but with more refined output (eliminating wrong selection). As such, a respective class for this category is needed.</ul><br></li>
  <li><b>FACTUAL :</b><br><ul>Factual is intended to be a class whereby direct span answer can be extracted directly from the context text. In essence, this class is not under abstractive answers type but because QCoC is constructed using CoQA, such class is needed in order to group all factual answers under one tag/label. Although the focus is abstractive answer’s feature, QCoC is also intended to be a dataset that can work well with standard QA dataset. The imagined scenario is a classifier trained using QCoC that can determine whether the input question needs further processes because its expecting abstractive answer, or can straightaway produce factual answer using its core language model.</ul><br></li>
  <li><b>COUNTING/FLUENCY :</b><br><ul>“Counting is answer that requires counting of entities/objects in the context passage” and “Fluency is answer that needs to be rephrased in order to be highly relevant”. Syntactically, Counting is also Fluency in the sense that counting item result is essentially a rephrase of text span from the context text. By this rational, Counting and Fluency are being grouped together as to minimize the potential of false positive result in classification process. As Counting is also Fluency, but Fluency does not necessarily is Counting, falsely classify Counting answer as Fluency answer is highly possible.</ul></li>
</ol>
