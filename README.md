# Ziphs-Law
This includes the Python code for Ziph's Law and how we can find Lambda, and k from any Book. 

• We first choose our favourite book, I downloaded the copies (book1.txt and book2.txt) from Project Gutenberg (https://www.gutenberg.org/). 

• Then we format all the words in the book, like removing special characters (* / - _ ; : '), making all the words in lower-case (so, The == the), etc. 

• Then we used potters stemmer - it groups words in form of its different tenses (realize, realizes, realized are grouped together as realize). 

• Then we count the word frequency. This gives us a term count pair {Ti, Ci}. 

• Using this we create a lineplot which is sorted based on Rank (Rank means the ascending order of word count, i.e., a word with maximum frequency is ranked 1). This gives us a curve (I have used to logarithmic value of the frequency count to make the graph easily readable). 

• Then we make a scatter plot, find the line of best fit, and then plot them both.

• Then we can easily get the slope and intercept of the straight line. Why do we need this?
    f(r) = c*r^(-alpha)
    Taking log on both sides,
    ln(f) = ln(c) - (alpha)(ln(r))
    ln(f) = -(alpha)*ln(r) + k
    this is similar to y = m*x + c, where f(r) -> frequency of word, r is the rank, c is the corpus constant, alpha is the corpus exponenet, and ln is natural logarithm.

• Hence we get the corpus constanmt and exponent.

• Then we make a word cloud which shows the most frequent word as the word with maximum size. We use NLTK to filter out stopwords, and only view the top 100 most frequent non-stopwords.  
