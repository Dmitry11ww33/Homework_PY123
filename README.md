PY123

Ex.1
---------------------------------------------
Воспроизвести пользовательские действия на
тестируемом сайте.
---------------------------------------------
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://www.python.org/")
elem = driver.find_element(By.NAME,"q")
elem.click()
elem.send_keys("print")
elem.send_keys(Keys.ENTER)

elem = driver.find_element(By.NAME,"q")
elem.clear()
elem.send_keys("def")
elem.send_keys(Keys.ENTER)
time.sleep(2)
