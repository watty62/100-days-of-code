# 100 Days Of Code - Log

## Contents
* [Rules](rules.md)
* [Log - click here to see my progress](log.md)
* [FAQ](FAQ.md)
* [Resources](resources.md)

### Day 29: 2017-Jan-31
**Today's Progress** Got the new bot working just to watch it crash again and again. Some of that is from stripping specifics out of the example code I have to base my bot on. Struggling with Object Orientation and inheritance in Python. I may just revert to a non- OO version and buid on what I did last week. 

**Thoughts** Another brick wall! 

### Day 28: 2017-Jan-30
**Today's Progress** VirtualEnv now all working. Installed my friend Andrew Sage's [Slackbot module](https://github.com/andrewsage/slackbot) which is packaged to install via pip. Created a new bot from it, using his Eventbrite example. Couldn't get it running. Spent an hour debugging to no avail.

**Thoughts** Sleep on it - again!

### Day 27: 2017-Jan-29
**Today's Progress** Fixed my VirtualEnv setup (I think) then spent a very long time trying to get a Python library work so that I could use it in my project in VirtualEnv. 

**Thoughts** Going to bed with no clear sense of what the problem is.

### Day 26: 2017-Jan-28
**Today's Progress** Had a great start today. Cleaned up the album listing script and got that fully working. Wrote the new script to take the output of that and write it to a SQLite database. There were issues with extended character sets which I overcame, logging the problem ones then fixing them at source. The day ended less well while trying to sort out VirtualEnv - which I have intended to use for a while. Something is screwed up since I installed it months ago. Spent 2 hours trying to fix it that I was going to use to work on my jazz bot. 

**Thoughts** Ho hum.

### Day 25: 2017-Jan-27
**Today's Progress** Having missed my first day yesteday I could have done with more time today. As we prepare for [Code The City](http://codethecity.org)'s Chatbot and AI weekend I returned for an hour of working on a SlackBot as a demo for the weekend. I decided to use my MP3 album collection as a basis. So I am putting the albums in a SQLite database (almost done), then I am going to use the Bot to query it. For example, which albums do I have by Sonny Rollins? Do I have an album called "Stardust" etc. This builds on teh album lister, below. 

**Thoughts** Soon I will be able to stand in a record shop and ask a bot if I have a certain album. 

### Day 24: 2017-Jan-25
**Today's Progress** New file - album_lister.py now working. Has test and non-test modes. It will run through fie structure, identify folders, pull out the artist and album name, apply Title Case, create a list of Tuples , order that and write that out to a TSV file. Rough round the edges with redundant code. Runs slowly. But works.  

**Thoughts** A work in progress.

### Day 23: 2017-Jan-24 
**Today's Progress** Decided to go back to scratch on the MP3 logger. I need to separate out various separate tasks. 1. Create an artist / album index which I can access from afar (when checking if I have *that* album or not). 2. Check for missing folder.jpg's in every album folder. 3. Check the ID3 tags in every music file - are they complete and are they correct. (And establish a way as automatedly as possible to fix 2 & 3). Started to recode (1) - almost finished. 

**Thoughts** More organised now.

### Day 22: 2017-Jan-23 
**Today's Progress** I was able to spend a few hours working on various Python projects today. I started with my very old [Twitter Followers](https://github.com/watty62/Count_twitter_followers) scraper, hosted on Github and running on [morph.io](https://morph.io/watty62/Count_twitter_followers). This had been erroring for a long time and I hadn't got around to fixing it. Now done. Then after a few other small things I came back to the MP3 listing project. I tried creating a stripped down version and running that on my whole collection. It ran but didn't give the expected result. It is not traversing the whole tree. More work tomorrow.

**Thoughts** Perplexed

### Day 21: 2017-Jan-22 
**Today's Progress** Added a test flag to handle correct paths. Started to rewrite the main routine to use a dictionary. Rolled back. Needs more thought. Committed v1.3. 

**Thoughts** I need to sketch his out better before jumping into more code. I might make more than one script - one to check files and log anomalies. One to read that and act to fix the anomalies. One to create an index of all music whcih I will publish to Github so I can check it from afar before buying an album.

### Day 20: 2017-Jan-21

**Today's Progress** Amended the function which was comparing data derived from the file path with the ID3 tags to just return the tag values. Moved the comparison to later in the programme. Created an output file. Writes data to that with highlighted anomalies. 

**Thoughts** Needs more checking, and tidying then (later) write updates to the ID3 tags.

### Day 19: 2017-Jan-20

**Today's Progress** Back to the MP3 checker. Now doing a comparison on the Artist, Album, and Title fom the file path with those from the ID3 tags. Highlighting mis-matches. Still some issues with the more weirdly named files with miscellaneous putuation in the filename.

**Thoughts** Next step to log the data, then (later) write updates to the ID3 tags.

### Day 18: 2017-Jan-19

**Today's Progress** Jumped to creating a Slack Chat bot using this [easy formula](https://www.fullstackpython.com/blog/build-first-slack-bot-python.html) Got it working and responding to others' input. Not much polish or finesse - but the bones are there (after only a short time). This might play a part in our [Chatbots and AI weekend](http://codethecity.org/2016/10/chatbots-and-ai-ctc8/)

**Thoughts** I accept - I am easily distracted!

### Day 17: 2017-Jan-18

**Today's Progress** Changed some of my code to use RegEx to grab text from file names. Works in (almost) every case. Tested Mutagen library for reading ID3 tags. Too awkward. Settled on eyed3 library. Populated the function for checking ID3 tags. At the moment I am just printing everything but the bones are now there. Created a github repo [mp3_checker](https://github.com/watty62/mp3_checker). Pushed v1.2 as work working demo.

**Thoughts** Been listening to loads of [TalkPythonToMe](https://talkpython.fm) as I walk to and from work.Highly recommended.

### Day 16: 2017-Jan-17

**Today's Progress** Created a much deeper structure of test files. Got os.walk now traversing the files. Grabbing genre, artist and album from that structure. The routine still chokes on inconsistent file naming. Created a blank fucction for checking ID3 tags and grabbing content - or identifying gaps. 

**Thoughts** Unexpected progress.

### Day 15: 2017-Jan-16

**Today's Progress** After sruggling yesterday, I found this [script on Stackoverflow](http://stackoverflow.com/questions/7201203/python-current-directory-in-an-os-walk) It looks like I can modify this to identify the current directory and grab that as I descend though the tree structure. This will be quicker than writing this from scratch. Started amending it. 

**Thoughts** Hopefully more time tomorrow to come up with something that I can publish to GitHub.

### Day 14: 2017-Jan-15

**Today's Progress** Spent a lot of time tinkering with routines using OS Walk to traverse a file structure. Looking to be able to work out how many levels deep I am at any time, and how the folder name maps onto a genre, artist, or album name. Quite a few blind alleys. Also blogged about my railway scraper [here](http://10ml.com/2017/01/scraping-goes-off-the-rails/)

**Thoughts** I need a few hours straight at this one!

### Day 13: 2017-Jan-14

**Today's Progress** Published this repo on [Github Pages](http://apperdeen.org/100-days-of-code/) to make it a little more readable. 

Started to think about my next project and sketch that out. Going to create a crawler and logger for my music collection. I want it to spider a structured file store, which is in the format: 

* Genre  
|--Artist  
   |--Album  
      |--Track  

 Lots of the MP3s are well tagged but not all Some are wrong. Many folders have folder.jpg but most don't. 

 I want to walk the file structure, derive genre, artist, album name from the structure and then compare those with the ID3 tags. Look for untagged files, and missing folder,jpg files, and report on that. 

 I might look at fixing tags automatically.

 So far I have created a file-walker, set up a simplified test file structure, and got it reporting on missing folder.jpgs.

**Thoughts** This is going to be a bigger project.  

### Day 12: 2017-Jan-13

**Today's Progress** Back to the main project. Noticed that the rail company had published new performance reports; this one for period 10 of 2016-17. I ran the scraper - and it crashed. After some investigation I spotted that they had changed the file naming convention to now use underscores instead of dashes. Created the logic to deal with that - now [scraper_v1.4.py](https://github.com/watty62/SRPPM/) That change followed last month's change to the PDF to introduce a blank column in the middle of the table of data for individual stations. I guess this shows how scraping is always a game of catch-up

**Thoughts** Good to have three complete (4-week) periods of data built up now. 

### Day 11: 2017-Jan-12

**Today's Progress** Struck by the difference in tone of the speeches of presidents Obama and Trump as reported on last night's news I decided to do a very quick bit of frequency analysis tonight. You can find the code in this new [repo](https://github.com/watty62/pres_speeches)

**Thoughts** A fun side project.

### Day 10: 2017-Jan-11

**Today's Progress** Great progress. Fixed the database write issue. Created code to test for an extra column to the right of station names in output CSV file. Pushed v1.3 of the scraper to [the repo](https://github.com/watty62/SRPPM). 

**Thoughts** A much more positive night!

### Day 9: 2017-Jan-10

**Today's Progress** Back on my main project tonight. Struggled to debug a script in Python to write to the database. Two out of three table writes are ok but the main table one is causing problems. Need to find a couple of hours back to back to sort it out tomorow.

**Thoughts** Going in circles tonight.

### Day 8: 2017-Jan-09

**Today's Progress** Was bad today. Instead of fixing my scraper to cope with malformed / inconsistently formed PDFs which break it when I try to process one, I jumped to another scraping programme for a bit of a change.

**Thoughts** I must come back to the first project tomorrow. No excuses.

### Day 7: 2017-Jan-08

**Today's Progress** Moved the code to drop and create SQL tables to a function, and commented out the call to it to stop existing data being lost. Started to create a routine to convert old performance reports. I have one downloaded. I have been promised others.

**Thoughts** I need to test the code on the new report which will be released w/c 2017-Jan-09. Then it will be essentially complete. Need to decide on my next project - probably a Twitter one.

### Day 6: 2017-Jan-07

**Today's Progress** Created second and third DB tables, and linked these through foreign keys. Wrote code to extract the overall monthly performance percentages. Stored these in the Percentages table. Amended the main table so that it stores fewer fields but a pointer to the Periods table in which I store the definition of years, periods and dates covered by each report.

**Thoughts** A couple of hours well spent.

### Day 5: 2017-Jan-06 

**Today's Progress** Added and tested code to create a SQLite database and populate the main table of monthly data per station. Still to create a linked table to store both the period definition (e.g. 9 = 13 Nov to 10 Dec) and the overall network performance

**Thoughts** Managed over an hour again but too tired tonight to do more.

### Day 4: 2017-Jan-05 

**Today's Progress**: Tidied a litte code. Worked on getting the Git files sorted and pushing those to the repo below. Also forked and published this repo.

**Thoughts** Unsettled by being thrown into VI editor for the first time since about 1998! Pleased that I've created a first public version. 

**Link(s) to work**
You can find the project on my [Github Repo](https://github.com/watty62/SRPPM)

### Day 3: 2017-Jan-04 

**Today's Progress**: Worked on my railways data scraper in Python.  Strung all test progs together into one combined programme. Archived the test scripts. the combined programme worked straight off. Will push v1 to github tomorrow, I promise.

**Thoughts** Pleased that the parts of the programme came together without issue.

### Day 2: 2017-Jan-03

**Today's Progress**: I signed up for the PDFTables API (see Day 1). I got the PDF to CSV conversion via API working. Now it retrieves a CSV file and saves that. I created an initial data extraction from CSV but it is still quite rough.

**Thoughts**: I chose CSV as, having tested the alternative file formats that the API returns, it seems easier to work with than XSLX or XML in this case due to the weird format of the original PDF. 

### Day 1: 2017-Jan-02

**Today's Progress**: Started my first #100DaysOfCode project today. Its purpose is to make railway performance data available as open data and over time. To do that, I need to scrape PDFs, extract data via [PDFTables](http://twitter.com/@pdftables) and put that into #SQLITE database, and finally visualise it. I might try to create an API too. I got the first part started. Found the target link on the page, followed it, grabbed the name of the PDF, stored that, and downloaded the PDF itself.

**Thoughts:** Having been doing no coding for what feels like years (but is more like months) it feels good to be back working on a project. This builds on the [four Coursera python courses](https://www.coursera.org/specializations/python) I studied over xmas and New Year. 

