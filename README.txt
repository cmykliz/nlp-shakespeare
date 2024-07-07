README - Shakespeare Sentiment Analysis and Categorisation: an NLP project

Shakespeare's 37 plays are categorised according to their main theme; Comedy, History, Tragedy. In this project I will be analysing each play to discern whether these categories are accurate for each play using sentiment analysis. This is just for fun and to practise my coding skills. I am starting this from a point of having no idea how I am going to do it or what exactly I am trying to achieve with it, but language and literature both interest me so I'm interested to see what will come out of this, beyond just learning some cool stuff (hopefully).

I have started by downloading text files of all 37 plays, listed and enumerated below for ease.

COMEDIES
1 - All's Well That Ends Well
2 - As You Like It
3 - Comedy of Errors
4 - Love's Labour's Lost
5 - Measure for Measure
6 - Merchant of Venice
7 - Merry Wives of Windsor
8 - Midsummer Night's Dream
9 - Much Ado about Nothing
10 - Taming of the Shrew
11 - Tempest
12 - Twelfth Night
13 - Two Gentlemen of Verona
14 - Winter's Tale

HISTORIES
15 - Henry IV, Part I
16 - Henry IV, Part II
17 - Henry V
18 - Henry VI, Part I
19 - Henry VI, Part II
20 - Henry VI, Part III
21 - Henry VIII
22 - King John
23 - Pericles
24 - Richard II
25 - Richard III

TRAGEDIES
26 - Antony and Cleopatra
27 - Coriolanus
28 - Cymbeline
29 - Hamlet
30 - Julius Caesar
31 - King Lear
32 - Macbeth
33 - Othello
34 - Romeo and Juliet
35 - Timon of Athens
36 - Titus Andronicus
37 - Troilus and Cressida

Stage One: Text Pre-Processing
Before I do anything I will need to pre-process the text so it's ready for analysis.
First off I will remove legal notices, introductions, prelims and end matter, leaving just the text of the play.

(To experiment with later - remove stage directions leaving only dialogue and see if that changes sentiment ratings)

Then I will go through the NLP pipeline using SpaCy, listed below (but I will look into NLTK and any others to see if they give different results)

NLP Pipeline:
1. Sentence Fragmentation: split plays into lists of individual sentences.
2. Tokenisation: split sentences into individual words (tokens)
3. Lemmatisation: remove inflectional morphemes (need to look into the influence of modern lemmatisation on shakespearean language as there may be different morphemes that should be removed)
4. Removal of Stopwords: remove unimportant words such as prepositions, determiners (articles), pronouns, etc. (need to include shakespearean stop words - see other people's projects for what they used and research best practise)
5. PoS Tagging: Parts of Speech tagging, e.g. noun/verb/adjective (research how this can be done with Shakespeare as some of the language has changed in usage/semantics - also will be important for the sentiment analysis)
6. Named Entity Recognition: remove names, entities, etc. (will need to specify character names as well as archaic references, need to research if this has been done or if I need to compile a list from scratch)

Then I will do some basic analysis, again for funnies:

- Analyse unique word choices, similarities between plays, frequency of words, etc.
- Perform basic SpaCy sentiment analysis to see what that shows
- Figure out if there are any Custom Components to add to the NLP pipeline for what I want to do/further analysis I want to perform, etc.


Then I will need to figure out how to do the more advanced analysis and categorisation model to give plays a score of how comedic/tragic/historic they are. 


