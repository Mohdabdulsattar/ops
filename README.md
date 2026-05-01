"# ops" 
name: Python Test

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.10"

      - name: Run test
        run: python main.py

        import selenium
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time
driver=webdriver.Edge()
driver.get("http://facebook.com")
time.sleep(2)
print("EDGE opened successfully")
driver.quit()


from selenium import webdriver
from selenium.webdriver.common.by import By

# Start Edge browser
driver = webdriver.Edge()

# Open Google
driver.get("https://www.google.com")

# Search box status
search = driver.find_element(By.NAME, "q")
print("Displayed:", search.is_displayed())
print("Enabled:", search.is_enabled())

# Count elements
print("Links:", len(driver.find_elements(By.TAG_NAME, "a")))
print("Inputs:", len(driver.find_elements(By.TAG_NAME, "input")))
print("Buttons:", len(driver.find_elements(By.TAG_NAME, "button")))

driver.quit()


def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5 

