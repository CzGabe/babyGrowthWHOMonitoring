# babyGrowthWHOMonitoring
### Plotting Weight and Height (Length) data on WHO percentiles.

* Used environment: Anaconda, Jupyterlab, Python 3

*data in WHO folder is downloaded on 2020.05.14.*

# Functionalities
1. Creating plots:
  * Weight plot
  * Weight plots zoomed to latest measurements, highlighted by categories
  * Weight plot zoomed to latest measurements for one selected category (convenient for mail)
  * Height plot
  * Weight-Lenght/Height plots
  * (TBD: Head Circumference)


2. Creating table for Weight containing the 3 nearest percentile values from WHO (and their differences)

3. Sending mail with selected plots and table.

# Usage
1. Create own data by Modifying sample excel file (Wonko.xlsx):
  * Measure baby when desired and set date in "DT" column
  * Add weight in gramms to "W" column
  * Set mearure error in "Err" column if desired
  * Create categories in "Cat" column. E.g. roughly the time when baby is fed. If it feeds 8 times a day (like 2-5-8-11-14-17-20-23) it can be used as categories.
  * Measurements can be flagged as "official" in the last column with "y" if needed. This can be handy to keep tracked as doctors mostly relying on these values. These values are highlighter on the large plots.
  * Set Height similarly, give values in cm


2. Set up code - Baby-WHO_Charts__PROD.ipynb:
  * set directory to import labelLine.py
  * Personalize the parameters (baby name, BDay, data filename, file path, etc...)
  * Set up sender and reciever e-mail addresses
    * The sender address might need special permissions to log in from Python
    * please note the password in the code is not encrypted...
  * Set up e-mail (subject and body) and select the plots and table to attach
