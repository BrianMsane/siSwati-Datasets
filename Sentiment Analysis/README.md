The data was collected from the YouTube platform as comments from videos where people express themselves in the siSwati language. To curate a representative dataset, we collected data from entertainment and comedy, news, cultural, sports, gospel, and other channels which served to be a source. 

In this platform, the users mix siSwati with other languages like English and Zulu and this called for direct translation to siSwati language as we try to maintain the initial expresssion of the user. Further, the pre-processing steps that were applied on the data include removing HTML tags, links, Unicode characters, and emoticons and emojis. These have no value in the actual text and had to be removed. This was made possible by our proposed siSwati text cleaner, sswcleaner (https://github.com/BrianMsane/sswcleaner).

There were some language specific cleaning methods that we used which include resolving borrowed words to their siSwati version, resolving some common typos that are used by people on social media, and resolving some slang words that are common in our vocabulary. It is worth mentioning that some words could not be directly resolved to siSwati because the language has not yet come up with so they were treated as an adjective of place or left on their foreign versions.

In the siSwati vocabulary, it is not allowed to have two vowels following each other and when we have such a case we implement morphophonological processes like deleting a vowel, adding a consonant, vowel gliding and more. That was decided by the situation at hand and what we assumed was the user's intent or message. Also, siSwati language does not allow for words that do not end with a vowel so the letter i was added to such because our observations from the dataset stressed that many users do not include the vowel i when it is appearing at the end of a word.

The data was annotated by two siSwati native speakers. We accounted for negative, positive and neutral sentiments. To make the actual annotation we represented negative, positive, and neutral comments which negative one, positive one, and zero, respectively.

``` latex
\begin{table}
  \caption{Dataset statistics table}
  \label{STATS}
  \centering
  \begin{tabular}{ll}
    \toprule
    \multicolumn{1}{c}{Description} & \multicolumn{1}{c}{Value} \\
    \cmidrule(r){1-2}  \\
        Total number of words & 11837 \\
        Total unique words & 5972 \\
        Number of sentences & 1895 \\
        Average Comment Length & 6 \\
        Positive Sentiments & 774 \\
        Negative Sentiments & 495 \\
        Neutral sentiments & 626 \\
    \bottomrule
  \end{tabular}
\end{table}
```

The table above defines the statistics of the dataset.