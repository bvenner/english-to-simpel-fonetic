# english-to-simpel-fonetik
Develop Simpel-Fonetik Version of Wiktionary 

It should be relatively straightforward to convert the English language version of Wiktionary into a Simpel-Fonetik version.  Ideally, the converters that I apply can be fully automatic, so that the two dictionaries can remain synchronized.  I see three stages to this project.

1)  Develop a conversion table using an English -> IPA -> Simpel-Fonetik converter.

One of the potential advantages of Simpel-Fonetik is that it is an alternate version of IPA.  This means that the existing phonetic spellings of English words that are already in the English Wiktionary can be used as a basis for their spelling in Simpel-Fonetik.  This conversion step should be relatively simple and easy to mechanize.  The output of the converter can then be checked against the Simpel-Fonetik dictionary.  If there is a relatively small amount of ambiguity, then a relatively complete dictionary can be created automatically.  If there is more ambiguity, then a more sophisticated converter might need to be developed using a seq2seq neural network.

2)  Develop a converter from WikiText english language entries to WikiText SF

Using the dictionary above, perform a word-to-word translation of text entries in the WikiTionary.  This will require parsing the WikiText entries and converting only the text within, so that the converted files can still be processed by existing parsers.

3)  Automate these converters

Once the basic converters are developed, the process should be automated to allow the Wiktionaries to stay in sync.  I would like to use Cromwell to specify the workflow, as the goal of this system is to allow for transportation of workflows across computer platforms.  This would let the project be run on larger hardware as it grew.  
