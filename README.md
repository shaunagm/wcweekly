Contents:
- About the project
- How to contribute
- About Woodhull and Claflin's Weekly

#### About the Project

This project is an attempt to make a digital archive of a radical feminist newspaper published in the 1870s.  There are other archives out there (namely [this one](http://www.victoria-woodhull.com/wcwarchive.htm)) but none which are complete, unchanged from the original, and well-indexed.

Original, non-digital material (right now, only pdfs of scans of microforms) can be found in the directory "originals".  Within that directory, scans are broken down by year, then issue.  There is also a folder marked "excerpts" which contains better scans of individual articles within issues.

Transcribed, digitized material can be found in the directory "transcriptions".  These two are broken down by year, then issues, with another folder called "excerpts".

An index of the journal's issues and their status can be found in [index.csv]().

Eventually, the images will be viewable online.  The mechanism will be in the directory "viewer", which is currently empty.  If you are interested in building this interface, see [this thread]() in the issue tracker.

#### How to contribute

##### Transcribe

The main way to contribute is by transcribing scans.  To do this, go to the file [index.csv]() and locate a scan marked "incomplete" and not claimed.  Edit index.csv and write your github username in the claimed column.  Once you've done that, you'll to fork and clone the repository.  (If you're not familiar with those terms, you'll probably want to read our [Git basics](https://openhatch.org/wiki/Git_Basics).)  Once you've got a local copy of the repository, you can open up the pdf files for your claimed issue/excerpt in the folder "originals".  In the folder "transcriptions", go to the corresponding issue/excerpt folder and create a markdown document with the following naming conventions (there may already be a document created if the issue or excerpt is partially transcribed):

Issue transcriptions are named by date, with the format __YYYY-MM-DD.md__.  For example, the transcription for the January 14th, 1874 issue of the weekly would be in a document titled __1874_01_14.md__.

Excerpt transcriptions are named by title, all lower-case, with hyphens between all words.  For example, the transcription of the excerpt titled "The Anti-fashion convention" would be in a document titled __the-anti-fashion-convention.md__.

A few rules for transcription:

+ You can use the [markdown conventions](http://daringfireball.net/projects/markdown/syntax) of using a single underscore on either side of a piece of text for \_italics\_ and a double underscore for \_\_bold\_\_.
+ Many articles have multiple headlines of different sizes.  Use markdown conventions of hashmarks (\#) to display headlines, with the biggest headlines being proceeded by one \# and the smallest being proceeded by six \#\#\#\#\#\#.  It's not important that headlines have consistent sizes across articles, however within each article you transcribe headlines should be correctly sized relative to each other. So if an article has one big headline and a smaller sub-headline, make sure that your transcription does the same.
+ If you are unsure of a letter, word, or segment of text, you can use a double %% to replace it.  Within the percent signs, in parentheses and separated by commas, list guesses, if any, as to the contents, for example: %(t,i,l)%
+ If you need to skip a large chunk of the scan, write that you did so at the bottom of the file in a new paragraph, between two @ signs, for example: @(skipped two paragraphs on p. 13 because they were too blurry)@

##### Scan

A large number of issues still need to be scanned.  If you would like to help, I suggest looking in libraries you have access to.  The most likely resource will be microformed copies of journals, as the original journals are likely in too fragile a condition to be scanned.  There are also some books which contain excerpts, which you may be able to scan (see [this thread]() in the issue tracker for discussion of potential intellectual property issues).

##### Edit

A number of transcriptions could use a once-over, both to have an extra set of eyes deciphering blurry scans and to make sure the transcriptions follow the format described above.  If you are interested in editing, see [this thread]() in the issue tracker.

##### Work on the display

These scans and their transcriptions will eventually be displayed via a website.  If you are interested in building this interface, see [this thread]() in the issue tracker.

#### About Woodhull and Claflin's Weekly

Victoria Woodhull and her sister Tennessee were pioneering feminists in the latter half of the 19th century.

Using money earned as the United States' first female stockbrokers, they began publishing 'Woodhull and Claflin's Weekly', a weekly newspaper advocating women's suffrage, redistribution of wealth, and free love, among other radical ideas.

During the Weekly's run, Woodhull ran for the US Presidency, but was jailed on charges of obscenity during the election.

You can read more about her here: <http://en.wikipedia.org/wiki/Victoria_Woodhull>

There is no complete text of Woodhull and Claflin's Weekly online.  The best way to view it is to find a library which holds the journal articles or, more commonly, the microform version of them.

This project is an effort to create scans of the microforms of all issues of the newspaper.  Due to the low quality of the scans, I am also attempting to manually transcribe the newspapers so the text is available in digital format.

To find a microform pdf to transcribe, visit the issue tracker of this repo.

If, in transcribing, you run across any words you're not sure of, please write them with *asterisks* around them to indicate uncertainty.  For instance, you might write:

"The quick brown *fox* jumped over the lazy *[]*."  (Where the last word you cannot even guess at.)


