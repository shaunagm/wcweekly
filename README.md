Contents:
- About the project
- How to contribute
- About Woodhull and Claflin's Weekly
- Miscellaneous

#### About the Project

This project is an attempt to make a digital archive of a radical feminist newspaper published in the 1870s.  There are other archives out there (namely [this one](http://www.victoria-woodhull.com/wcwarchive.htm)) but none which are complete, unchanged from the original, and well-indexed.

Original, non-digital material (right now, only pdfs of scans of microforms) can be found in the directory "originals".  Within that directory, scans are broken down by year, then issue.  There is also a folder marked "excerpts" which contains better scans of individual articles within issues.

Transcribed, digitized material can be found in the directory "transcriptions".  These two are broken down by year, then issues, with another folder called "excerpts".

An index of the journal's issues and their status can be found in [index.csv](https://github.com/shaunagm/wcweekly/blob/master/index.csv).  Excerpts are listed in [excerpts.csv](https://github.com/shaunagm/wcweekly/blob/master/excerpts.csv).  [sources.csv](https://github.com/shaunagm/wcweekly/blob/master/sources.csv) contains information on where scans (or in some cases, pre-transcribed articles) come from.  You can find a further description of these files and their fields under the heading "Miscellaneous", sub-heading "Reading the csvs".

Eventually, the images will be viewable online.  The mechanism will be in the directory "viewer", which is currently empty.  If you are interested in building this interface, see [this thread](https://github.com/shaunagm/wcweekly/issues/16) in the issue tracker.

#### How to contribute

##### Transcribe

The main way to contribute is by transcribing scans.  To do this, go to the file [index.csv](https://github.com/shaunagm/wcweekly/blob/master/index.csv) or [excerpt.csv](https://github.com/shaunagm/wcweekly/blob/master/excerpts.csv) and locate a scan marked "not started" or "incomplete" and not claimed.  Edit index.csv and write your github username in the claimed column.  Once you've done that, you'll to fork and clone the repository.  (If you're not familiar with those terms, you'll probably want to read [Git basics](https://openhatch.org/wiki/Git_Basics).)  Once you've got a local copy of the repository, you can open up the pdf files for your claimed issue/excerpt in the folder "originals".  In the folder "transcriptions", go to the corresponding issue/excerpt folder and create a markdown document for transcription.  You may need to create the folders for years or months if scans are new.  You may not need to create the markdown document for transcription if someone has partially transcribed a scan.

Markdown transcription documents should follow these naming conventions:

Issue transcriptions are named by date, with the format __YYYY-MM-DD.md__.  For example, the transcription for the January 14th, 1874 issue of the weekly would be in a document titled __1874_01_14.md__.

Excerpt transcriptions are named by title, all lower-case, punctuation stripped, with hyphens between all words.  For example, the transcription of the excerpt titled "The Anti-fashion convention" would be in a document titled __the-anti-fashion-convention.md__.

A few rules for transcription:

+ Transcript should include the fields show in the [template document](https://github.com/shaunagm/wcweekly/blob/master/template.md).
+ You can use the [markdown conventions](http://daringfireball.net/projects/markdown/syntax) of using a single underscore on either side of a piece of text for \_italics\_ and a double underscore for \_\_bold\_\_.
+ Many articles have multiple headlines of different sizes.  Use markdown conventions of hashmarks (\#) to display headlines, with the biggest headlines being proceeded by one \# and the smallest being proceeded by six \#\#\#\#\#\#.  It's not important that headlines have consistent sizes across articles, however within each article you transcribe headlines should be correctly sized relative to each other. So if an article has one big headline and a smaller sub-headline, make sure that your transcription does the same.
+ If you are unsure of a letter, word, or segment of text, you can use a double %% to replace it.  Within the percent signs, in parentheses and separated by commas, list guesses, if any, as to the contents, for example: %(t,i,l)% or %(the,then) (she,shes,she'd)%
+ If you need to skip a large chunk of the scan, write that you did so at the bottom of the file in a new paragraph, between two @ signs, for example: @(skipped two paragraphs on p. 13 because they were too blurry)@

##### Scan

A large number of issues still need to be scanned.  If you would like to help, I suggest looking in libraries you have access to.  The most likely resource will be microformed copies of journals, as the original journals are likely in too fragile a condition to be scanned.  There are also some books which contain excerpts, which you may be able to scan (see [this thread](https://github.com/shaunagm/wcweekly/issues/15) in the issue tracker for discussion of potential intellectual property issues).

##### Edit

A number of transcriptions could use a once-over, both to have an extra set of eyes deciphering blurry scans and to make sure the transcriptions follow the format described above.  The process for editing is currently informal - find documents labeled "needs editing" in issues.csv or excerpts.csv, and submit any changes you think appropriate via pull request.

##### Work on the display

These scans and their transcriptions will eventually be displayed via a website.  If you are interested in building this interface, see [this thread](https://github.com/shaunagm/wcweekly/issues/16) in the issue tracker.

#### About Woodhull and Claflin's Weekly

Victoria Woodhull and her sister Tennessee were pioneering feminists in the latter half of the 19th century.

Using money earned as the United States' first female stockbrokers, they began publishing 'Woodhull and Claflin's Weekly', a weekly newspaper advocating women's suffrage, redistribution of wealth, and free love, among other radical ideas.

During the Weekly's run, Woodhull ran for the US Presidency, but was jailed on charges of obscenity during the election.

You can read more about her here: <http://en.wikipedia.org/wiki/Victoria_Woodhull>

#### Miscellaneous

##### Reading the csvs

index.csv has the following fields, which should be used thusly:

+ __ISSUE YEAR__ : The year the issue came out, written with four digits (YYYY), for example: 1874
+ __ISSUE MONTH__: The month the issue came out, written with two digits (MM), for example February would be: 02 
+ __ISSUE DAY__:  The day of the month the issue came out, written with two digits (DD), for example the third would be: 03
+ __STATUS__:  There are five possible statuses: _needs scans_ if there are no scans available for the text or if the current scans are simply unusable, _not started_ if a scan exists but no transcription has been started, _incomplete_ if transcription has been started but not finished (if you see this status, check the CLAIMED field), _needs editing_ if transcription has been completed but no one has reviewed it or if there remain questions about content marked by %%, and _completed_ if the scan is completely transcribed.
+ __CLAIMED__:  Issues and excerpts can be claimed by individuals to work on.  A person can only claim one thing at a time, for a period of up to one week.  The maintainer (Shauna) will periodically remove claims where no updates have been made for at least a week.  Individuals can also check the commit history and remove claims where no updates have been made for at least a week.
+ __EXCERPTS__:  A list of excerpts, separated by semi-colons, that can be found in this issue.
+ __SOURCES__:  A list of sources for the transcriptions, referencing names from sources.csv

excerpts.csv has the following fields, which should be used thusly:

+ __FILE NAME__:  The file name of the excerpt.  (From above: Excerpt transcriptions are named by title, all lower-case, with hyphens between all words.  For example, the transcription of the excerpt titled "The Anti-fashion convention" would be in a document titled __the-anti-fashion-convention.md__.)
+ __ISSUE__:  The issue the excerpt can be found in, formatted YYYY-MM-DD.
+ __STATUS__:  There are five possible statuses: _needs scans_ if there are no scans available for the text or if the current scans are simply unusable, _not started_ if a scan exists but no transcription has been started, _incomplete_ if transcription has been started but not finished (if you see this status, check the CLAIMED field), _needs editing_ if transcription has been completed but there remain questions about content marked by %%, and _completed_ if the scan is completely transcribed.
+ __CLAIMED__:  Issues and excerpts can be claimed by individuals to work on.  A person can only claim one thing at a time, for a period of up to one week.  The maintainer (Shauna) will periodically remove claims where no updates have been made for at least a week.  Individuals can also check the commit history and remove claims where no updates have been made for at least a week.
+ __SOURCES__:  A list of sources for the transcriptions, referencing names from sources.csv

sources.csv has the following fields, which should be used thusly:
NAME-REFERENCE, URL (if applicable), NOTES
+ __NAME-REFERENCE__:  A short name to use when referencing the source in index.csv, excerpts.csv
+ __URL__:  If the source is a website, include a URL
+ __NOTES__:  Any notes about the source that might be useful, including who is responsible for any scans
