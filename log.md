# 100 Days Of Code - Log

I've reversed sorted by date order the log below. I've also adopted ISO8601 date formats for consistency. 

### Day 13: 2017-Jan-14

**Today's Progress** Published this repo on [Github Pages](http://apperdeen.org/100-days-of-code/) to make it a little more readable. 

Started to think about my next project and sketch that out. Going to create a crawler and logger for my music collection. I want it to spider a structured file store, which is in the format: 
1. Genre
 - Artist
 -- Album
 --- Track

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

