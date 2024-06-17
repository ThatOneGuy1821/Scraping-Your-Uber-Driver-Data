This is the code I developed to scrape my Delivery History from Uber's website. I'm sure it can be iterated and improved upon. But this was my attempt to simplify & automate the process as much as possible, at my current skill level.

### Instructions:

Before we begin, you'll need to create a folder that will be used exclusively for this project. We will be referencing it throughout.

The example I give is a folder titled **uber_webscrape** which I stored at this path:
**‘/Users/yourname/uber_webscrape/’**

You will also need to install and have a cursory knowledge of:
- Python 3
- Selenium
- Chrome
- Beautiful Soup
- Pandas
- Jupyter Notebooks (or some other IDE)

An explanation for each is beyond the scope of this project.

## Step 1:

Now that we have our file set up, click the Folder titled **Step 1** and run the code titled **1_login**.

You will need to replace the snippet of text that says _Enter the Phone Number Associated with your Account Here_ with a valid phone number. Digits only, no dashes. Do not delete the quote marks ' '  (See Line 20)

Running this should prompt a verification process, which will need to be completed manually.

Your screen should now look something like this: 


<img width="797" alt="Screenshot 2024-05-25 at 12 37 26 PM" src="https://github.com/ThatOneGuy1821/Scraping-Your-Uber-Driver-Data/assets/142834049/d7fda5a2-b52c-41e3-964a-0e1e12e2616e">

### Initial Scrape:

Now that you're logged in, use the calendar widget to scroll back to your first delivery. The page should list your earnings activity for the entire week.

Scroll down to make sure all of the data is populated. If you see a "Load More" button at the bottom, click it and continue scrolling. Repeat as necessary until everything has been loaded on the page.

Now it's time to run the code titled **2_extract_overview_data**. Make sure to replace the text that says _Insert Your Folder Path and File Name Here_ on Line 33. An example has been provided on the line below.

You should now have a Data Frame that looks something like this: 


<img width="615" alt="Screenshot 2024-05-25 at 12 53 07 PM" src="https://github.com/ThatOneGuy1821/Scraping-Your-Uber-Driver-Data/assets/142834049/cff87b0c-2a7f-4b9c-94fd-69e9d5431837">


This Data Frame should also be saved to your computer as a file titled _week1.csv_, found in the folder you created earlier. Check to make sure it's there and that everything looks good.

Then, using the calendar widget referenced above, manually click to the next week and repeat the process above. 

IMPORTANT: For every page you want to capture, you'll need to adjust the name of the file on Line 33. Failure to do so will result in previous data being over-written. Using the example I provided of _week1_, simply iterate the file name so that **week1** becomes **week2**; **week2** becomes **week3**; etc. You'll also want to make sure that all of the data is populated on the page before you attempt scraping. Make sure to scroll down and click "Load More" if it exists.

Rinse and repeat until you have downloaded your entire Overview History. We will be using this data for the Primary Scrape, which will be fully automated.

### Combining your CSV Files:

Once you've completed this process, let's combine all of the data into a single CSV File. This can easily be accomplished by running the code titled **3_combine_overview_files**.

Make sure to edit the text on Lines 1 and 13, per examples provided.

This will give you a new file titled _combined_data.csv_ which will be used for the final scrape!

## Step 2:

Okay, now we can get to the real data!

The previous scrape was primarily to capture the URL associated with each of your orders. Now, we will use the _combined_data.csv_ file to create a bot that allows us to automate the primary scrape.

Before continuing, it's important to note that this process is _fully automated_, but may take a _significant amount of time_ depending on how many deliveries you performed.

To calculate the amount of time it will take, open the _combined_data.csv_ file and check to see how many rows of data you have. Multiply this number by 8, as it will take roughly 8 seconds per row. Divide that number by 60 and you should have the estimated amount of minutes expected to finish the final scrape.

If you're ready to continue, open the file titled **Step 2**.

If you closed the Chrome Browser at any point, or need to return to this later, simply rerun the login code titled **1_login** when you're ready to continue.

### Primary Scrape:

You can now run the final code titled **2_extract_complete_data**.

Make sure to edit the text in Lines 149 & 165, per example.

Once the process has begun, I recommend keeping an eye on it for the first several minutes to make sure there are no errors. After that, feel free to walk away and check in periodically, keeping in mind how long it should take to complete.

And Voila!
You should now have a final file titled **full_data.csv**!

Congratulations! 
Your entire delivery history should be compiled in a single, easy-to-reference CSV!

For more on me, check out: linkedin.com/in/cameronccraig
