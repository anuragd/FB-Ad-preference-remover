# FB-Ad-preference-remover
Script to remove all ad preferences on facebook

## How to run
1. Log into Facebook on Google Chrome on a desktop
2. Go to Settings - > Ads -> Ads Based on my preferences -> Manage preferences
3. On the preferences page, expand all the categories. I was unable to automate this.
4. Press F12 on a Windows or Cmd+Shift+I on a Mac
5. This opens the developer console. On the top, you'll find a console tab. Click that
6. You'll see a STOP warning from Facebook here. Ignore that, we are just automating what you'd otherwise have to do by clicking about 350 times (Check out `fbapr.js` for code comments and reading the code so that you understand the security of this script you'll be running.)
7. Copy paste the code from the `fbapr-min.js` file into the console tab.
8. Sit back and watch hundreds of ad categories being removed!

## What it does
1. Loads jQuery into the console
2. Finds all "Show more" buttons and clicks them
3. Waits a little while(15 secs) for all the categories to load
4. Clicks the "X" button next to all the preferences

## Script Modifications/Requirements
- Occasionally, FB will update their div/button classes, so you'll need to update the script variables to point at the correct class id's.  Screenshots below on what each variable represents.

![see_more_button_class](see_more_button_class.png?raw=true "see_more_button_class")
![ad_cats_class](ad_cats_class.png?raw=true "ad_cats_class")
![category_class](category_class.png?raw=true "category_class")
![remove_button_class](remove_button_class.png?raw=true "remove_button_class")