# RESEARCH

## What do Researchers do?
Researchers inspect the "uncrawlable" list to confirm that seeders' assessments were correct (that is, that the URL/dataset is indeed uncrawlable), and investigate how the dataset could be best harvested.

## Getting set up as a Researcher
 - Apply to become a Researcher 
    - By asking your DataRescue guide or by filling out [this form](https://goo.gl/forms/sRRJois9NAC1AduP2) 
    - Skills recommended: in general, Researchers need to have a good understanding of harvesting goals and have some familiarity with datasets. Ideally they would understand how federal data is organized (e.g. where the "master" datasets are vs. the derived partial views of those datasets.
    - Note that an email address is required to apply.
  - Link to sign into app, slack invite, and other details will be provided once your application is approved.
  - Verify that you have write access to the Researchers/Harvesters tab in the Uncrawlable spreadsheet
  - If you need any assistance:
    - Talk to your DataRescue Guide if you are at an in-person event
    - Or post questions on Slack in the #researchers or #harvesters channels
    
## Researchers and Harvesters
- Researchers and Harvesters should work very closely together as their work will feed from each other and much communication is needed between the two roles.
- For instance they could work in pairs or in small groups. 
  - In some cases, a single person might be both a Researcher and a Harvester.
- Note that in the Uncrawlable Action spreadsheet, Researchers and Harvesters share the same tab.
- As a Researcher, make sure to check out the [Harvesters documentation](harvesting-toolkit) to familiarize yourself with their role.

## Claiming a dataset to harvest

- Researchers work on datasets that were listed as uncrawlable by Seeders.
- Go to the app, click the Research item in the menu, and look for a dataset to research
  - Available datasets are the ones who don't have a user listed in the right-most column (indicating that set is Checked Out)
  - Click on the URL to see the dataset you'd like to research to open it in a new tab
  - Click on the UUID of the set you've chosen in the app
  - Click the CheckOut button to denote that you'll be researching this set
 
## Evaluating the data
Go to the URL, and start inspecting the content.

## Is the data actually crawlable?
Again, see [here](https://docs.google.com/document/d/1PeWefW2toThs-Pbw0CMv2us7wxQI0gRrP1LGuwMp_UQ/edit)
and [here](https://docs.google.com/document/d/1qpuNCmBmu4KcsS_hE2srewcCiP4f9P5cCyDfHmsSAVU/edit)
for a mostly non-technical introduction to the crawler. Some additional
technical notes for answering this:
- There is no specific file size cutoff on what is crawlable, but large files
  should be manually captured anyway.
- Files types like ZIP, PDF, Excel, etc. are crawlable if they are linked.
- The crawler can only follow HTTP links that appear directly in the DOM at load
  time. (That is, they should appear as `<a href ...>` tags in the page source.)
  If links are added by Javascript or require submitting a form, they are
  not crawlable.
- The crawler does not tolerate web frames (but it straightforward to inspect
  a page to obtain the content in the frame directly, and then nominate *that*).
- The crawler recently added the ability to crawl FTP, but we will not rely on
  this; we will treat resources served over FTP as uncrawlable.

What to do in each case:

- **YES**: If the URL is crawlable or you locate a crawlable URL that accesses the
  underlying dataset:
  - Nominate it: use our
    [Chrome extension](https://chrome.google.com/webstore/detail/nominationtool/abjpihafglmijnkkoppbookfkkanklok),
    and if that doesn't work then use the
    [bookmarklet](http://digital2.library.unt.edu/nomination/eth2016/about/)
  - Check the Do Not Harvest check box if all data is small, unstructured, and on a page crawlable by the Internet Archive
  - Fill out cell "Seeded?" = "yes" and tell what URL you seeded. 
 - **NO**: If it is confirmed not crawlable:
   - Continue to fill out the form
  - Search agency websites and data.gov for dataset entry points for your dataset collection   
      - Tips: Try to understand what data sets are underlying the web pages. Look for related entries in the spreadsheet, and ensure that you aren't harvesting a subdirectory if you can harvest the entire directory. Often, data underlying dozens of pages or multiple "access portal" apps is also available as one structured data file.
  - Add your suggested url for harvesting the data to the app in the Recommended Approach for Harvesting Data field
  -  Also add other information in the app that could help the Harvester, such as information about format (SQL, FTP, ZIP, PDF Collections, etc.), size, details about what you found, recommended approach, etc. 
  - Add related URLS to the Link URL field 
- **YES AND NO**: for example, FTP address, mixed content, big data sets:
   - Fill out the fields for the dataset. 
  - *While we understand that this may result in some dataset duplication, that is not a concern. We are ensuring that the data is fully preserved and accessible.*


## Finishing up
    - Check the checkbox at the top of the form to mark the Research process complete
    - Check the dataset back in by clicking the CheckIn button (formerly the CheckOut button)
    - If ever a day or more passed since you originally claimed the item, update the date to today's date. 
    - Note that if more than 2 days have passed since you claimed the dataset and it is still not closed, the **Date field will turn red**, signaling that someone else can claim it in your place and start working on it
      - This will avoid datasets being stuck in the middle of the workflow and not being finalized.
      
- You're done! Move on to the next URL!
