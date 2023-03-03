# AutomationBITM10

## LINK
- https://pypi.org/project/selenium/
- https://pypi.org/project/webdriver-manager/
- https://chromedriver.chromium.org/downloads
- https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
- https://github.com/mozilla/geckodriver/releases

## 1_Browser_configure:
### Manual:
- 1st: from selenium import webdriver
- 2nd: driver = webdriver.Firefox(executable_path="E:\\...\\...\\...\\geckodriver.exe")
### Automatic:
- https://pypi.org/project/webdriver-manager/
- 1st: import this => 
(1) from selenium import webdriver
(2) from selenium.webdriver.chrome.service import Service as ChromeService
(3) from webdriver_manager.chrome import ChromeDriverManager
- 2nd: For Chrome => driver = webdriver.Chrome(service=ChromeService(ChromeDriverManager().install()))
- or For Edge => driver = webdriver.Edge(service=EdgeService(EdgeChromiumDriverManager().install()))
- or For Firefox => driver = webdriver.Firefox(service=FirefoxService(GeckoDriverManager().install()))

## 2_Open_Website:
### Online_website
- driver.get("https://www.google.com")
### Offline_Website
- driver.get("file:///E:/SoftwareTestingAndQualityAssurance/PythonProjects/AutomationBatch10/offlineWebpage/YourStore.html")
### Localhost
- driver.get("http://localhost:8000/")

## 3_Browser_Command
### Driver commands
- driver.get("<Webpage_url>")
- driver.close() - To Close the current browser page
- driver.quit() - close the browser
- driver.maximize_window()
- driver.set_window_size(768, 1024)
- driver.back()
- driver.forward()
- driver.refresh()
### To View URL
- url = driver.current_url
- print(url)
### To View Title
- title = driver.title
- print(title)
### Time
- import time
- time.sleep(3) - hold 3 sec
