## Shakespeare Sentiment Analysis and Categorisation: an NLP project

Shakespeare's 37 plays are categorised according to their main theme; Comedy, History, Tragedy. In this project I will be analysing each play to discern whether these categories are accurate for each play using sentiment analysis. This is just for fun and to practise my coding skills. I am starting this from a point of having no idea how I am going to do it or what exactly I am trying to achieve with it, but language and literature both interest me so I'm interested to see what will come out of this, beyond just learning some cool stuff (hopefully).

I have started by downloading text files of all 37 plays, listed and enumerated below for ease.

#### COMEDIES
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

#### HISTORIES
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

#### TRAGEDIES
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

### Stage One: Text Pre-Processing
Before I do anything I will need to pre-process the text so it's ready for analysis.
First off I will remove legal notices, introductions, prelims and end matter, leaving just the text of the play. Need also to remove weird punctuation and line numbers. Will also need to delete footnotes. ARGH. Wonder how regex-able that all is.

(To experiment with later - remove stage directions leaving only dialogue and see if that changes sentiment ratings, for now leave them in)

Then I will go through the NLP pipeline using SpaCy, listed below (but I will look into NLTK and any others to see if they give different results)

#### NLP Pipeline:
1. Sentence Fragmentation: split plays into lists of individual sentences.
2. Tokenisation: split sentences into individual words (tokens)
3. Lemmatisation: remove inflectional morphemes (need to look into the influence of modern lemmatisation on shakespearean language as there may be different morphemes that should be removed)
4. Removal of Stopwords: remove unimportant words such as prepositions, determiners (articles), pronouns, etc. (need to include shakespearean stop words - see other people's projects for what they used and research best practise)
5. PoS Tagging: Parts of Speech tagging, e.g. noun/verb/adjective (research how this can be done with Shakespeare as some of the language has changed in usage/semantics - also will be important for the sentiment analysis)
6. Named Entity Recognition: remove names, entities, etc. (will need to specify character names as well as archaic references, need to research if this has been done or if I need to compile a list from scratch - need to keep words such as "king"/"queen"/"lord" except where used as name.)

Then I will do some basic analysis, again for funnsies:
- Analyse unique word choices, similarities between plays, frequency of words, etc.
- Perform basic SpaCy sentiment analysis to see what that shows
- Figure out if there are any Custom Components to add to the NLP pipeline for what I want to do/further analysis I want to perform, etc.

Then I will need to figure out how to do the more advanced analysis and categorisation model to give plays a score of how comedic/tragic/historic they are. 

- train model on several of each type of play to analyse word frequency differences, sentiment differences, etc.


### Dev log
22/11/24 - Turns out doing a part time degree with a full time job (plus a million hobbies) is a bit time consuming. But I am finally getting around to actually sorting the regex for the preprocessing, meanwhile I have also been learning more about implimenting language models and I have started working on a simplistic ML model for the shakespeare plays. A friend on my compling course suggested using individual word predictions to see if certain words appear more in certain plays and I like the idea because I can gradually make it more complicated by adding more words, like an n-gram model, to see if the sentences as a whole are more likely in given contexts. Though it is unlikely a specific line appears more than once in all of shakespeare (barr, like, omg) but I'm thinking of more stacked predictions. I will figure that out more when it isn't midnight on a Friday after a full day of set theory and regression classifiers. 

In other news, I may have figured out a dissertation topic which will inevitably also get logged and uploaded here. Move over, shakespeare, I've got speech patterns to classify.

