import os
import time
import re
import requests
import pandas as pd
from bs4 import BeautifulSoup

import selenium
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from selenium.common.exceptions import NoSuchElementException

browser = webdriver.Chrome()
browser.get('https://drivers.uber.com/earnings/activities')

time.sleep(3)

login_element = browser.find_element(By.ID, 'PHONE_NUMBER_or_EMAIL_ADDRESS')
login_element.send_keys('Enter the Phone Number Associated with your Account Here' + Keys.ENTER)
