This is the code that I developed to scrape my Delivery History from Uber's website. I have no doubt that it can be iterated and improved upon. This was my attempt to simplify the process and automate as much as I could with my current skills.

### Instructions:

Before we begin, you'll need to create a folder that will be used exclusively for this project. We will be referencing it throughout.

The example I give is a folder titled **uber_webscape** which can be found at this path:
**‘/Users/yourname/uber_webscrape/’**

## Step 1:

Now that we have our file set up, click the Folder titled **Step 1** and run the code **1_login**

You will need to replace the snippet of text that says _Enter the Phone Number Associated with your Account Here_ with a valid phone number. Digits only, no dashes. Do not delete the quote marks ' '  (See Line 20)

Running this should prompt a verification process, which will need to be completed manually.

Your screen should now look something like this: <img width="797" alt="Screenshot 2024-05-25 at 12 37 26 PM" src="https://github.com/ThatOneGuy1821/Scraping-Your-Uber-Driver-Data/assets/142834049/d7fda5a2-b52c-41e3-964a-0e1e12e2616e">

### Initial Scrape:

Now that you're logged in, use the calendar widget to scroll back to your first delivery. The page should list your earnings activity for the entire week.

Scroll down to make sure all of the data is populated. If you see a "Load More" button at the bottom, click it and continue scrolling. Repeat as necessary until all of everything has been loaded on the page.

Now it's time to run **2_extract_overview_data** code. Make sure to replace the text that says _Insert Your Folder Path and File Name Here_ on Line 33. An example has been provided.

You should now have a Data Frame that looks something like this: <img width="615" alt="Screenshot 2024-05-25 at 12 53 07 PM" src="https://github.com/ThatOneGuy1821/Scraping-Your-Uber-Driver-Data/assets/142834049/cff87b0c-2a7f-4b9c-94fd-69e9d5431837">

This Data Frame should also be saved to your computer as a CSV File, found in the folder you created earlier. Check to make sure everything looks good.

Then, using the calendar widget referenced above, manually click to the next week and repeat the process above. Remember to make sure all of the data is populated.

IMPORTANT: Before running your code again, make sure to iterate the file name so that **week1** becomes **week2**; **week2** becomes **week3**; etc. (See Line 33 and the example directly beneath it)

Rinse and repeat until you have downloaded your entire Overview History.

### Combining your CSV Files:

Once you've completed this process, let's combine all of the data into one CSV File. This can easily be accomplished by running the code found here: **3_combine_overview_files** 

Make sure to edit the text on Lines 1 and 13, per examples provided.

Once this is complete, you should have a new file titled _combined_data.csv_. It is now time to perform your final scrape.

## Step 2:

At this point, if you have not exited Python, you should be ready to run the final 











1_login
Rename login to 1_login
yesterday

2_extract_overview_data
Update 2_extract_overview_data
15 minutes ago

3_combine_overview_files
