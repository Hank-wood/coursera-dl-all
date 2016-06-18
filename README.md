# coursera-dl-all
Extend the Coursera Downloader by downloading quizzes and assignments (and hopefully forum posts soon!). Uses coursera-dl in the process.

##Features
Download quizzes
Download important files on assignment pages
Download videos (credits to coursera-dl)
Download sidebar links (Errata, Resources, etc.)
Download text file of important links.
Ability to automatically sign up for a class / bypass the honor code stuff (so you don't need to sign up for a class manually to download it).
A list of all classes on the old platform for Coursera

##Todo:
Add support for forums
Add support for human graded assignments
Fix bugs for any courses
Suggestions?

##Dependencies:
-Coursera-Dl. This must be installed if you want to download videos. If you only need to download non video stuff, just don't use the -v tag.  
-dryscrape https://dryscrape.readthedocs.io/en/latest/installation.html#recommended-installing-dryscrape-from-pypi

##To run:

First populate the classes.csv with slugs or URLs of desired classes. Slugs would be things like pgm-003 while the URL would be https://class.coursera.org/pgm-003
k
Next, run the program with the following tags:
-u: for username/email  
-p: for password  
-q: (optional) to download quizzes  
-v: (optional) to download videos  
-a: (optional) to download assignments  

So classes.csv might look something like:

https://class.coursera.org/gametheory-005/
neuralnets-2012-001

while your command line prompt would be:

python dl_all -u horacehe2007@yahoo.com -p hunter2 -q -v

Note: A list of all classes is provided 

##Output
The output is sorted into categories. Assignments is always there, and the other categories are pulled from the site itself.

Each category (e.g. Quizzes, Assignments, Homework) is split into subfolders for each quiz/assignment. Each of these folders hold a screenshot of the page, all zip files on the page, a links.txt holding all links on the page (in case there's files that you need to download that aren't a zip file).

This would download all the quizzes and videos for the game theory and neural nets course.
