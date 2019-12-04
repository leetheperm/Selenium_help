# Ultimate Py-Selenium snippets

## Chrome options
```
from selenium.webdriver.chrome.options import Options
options = Options()
options.add_argument('--headless')
options.add_argument('--no-sandbox')
options.add_argument('--disable-gpu')
```
## Firefox options
```
from selenium.webdriver.firefox.options import Options
options = Options()
options.headless = True
options.set_preference("dom.popup_maximum", 150)
```

## Init default
```
self.driver = webdriver.Firefox(options = options, executable_path='/Users/yourname/yourpath')
self.driver = webdriver.Chrome(options = options, executable_path='/Users/yourname/yourpath')
```
## print all links
```
links = browser.find_elements_by_css_selector("a")
for link in links:
  try:
    r = requests.head(link.get_attribute('href'))
    print(link.get_attribute('href'))
  except:
    continue
```
## Print all alt text for images
```
images = browser.find_elements_by_tag_name("img")
for image in images:
  print(image.get_attribute("alt"))	
```
## Get screenshot of file
```
driver.get_screenshot_as_file("filename.png")
```

## Scroll to the bottom of the page
```
driver.execute_script("window.scrollTo(0, document.body.scrollHeight);")
```
## Open new tab
```
browser.execute_script("window.open('new window')")
```
## manage newly opened tabs
```
browser.switch_to.window(browser.window_handles[1])
```
## Open new tabs and manage them 
```
tabNum = 0
browser.execute_script("window.open('new window')")
browser.switch_to.window(browser.window_handles[tabNum])
```      

## Xpath cheatsheet
```
search = driver.find_element_by_xpath('//*[@title="Search"]') # This works
search = driver.find_element_by_xpath('//*[@name="q"]') # This works
```
source: https://devhints.io/xpath

## Twitter SEO
```
twitter_site = browser.find_element_by_css_selector("meta[name='twitter\\:site']")
print('twitter site: ', end ='')
print(twitter_site.get_attribute('content'))

twitter_creator = browser.find_element_by_css_selector("meta[name='twitter\\:creator']")
print('twitter creator: ', end ='')
print(twitter_creator.get_attribute('content'))

url_twitter = browser.find_element_by_css_selector("meta[name='twitter\\:url']")
print('twitter url: ', end ='')
print(url_twitter.get_attribute('content'))	

twitter_title = browser.find_element_by_css_selector("meta[name='twitter\\:title']")
print('twitter title: ', end ='')
print(twitter_title.get_attribute('content'))

twitter_description = browser.find_element_by_css_selector("meta[name='twitter\\:description']")
print('twitter dexcription: ', end ='')
print(twitter_description.get_attribute('content'))		
```
## Facebook SEO
```
facebook_site = browser.find_element_by_css_selector("meta[property='og:site_name']")
print('Facebook site: ', end ='')
print(facebook_site.get_attribute('content'))

url_facebook = browser.find_element_by_css_selector("meta[property='og\\:locale']")
print('facebook language: ', end ='')
print(url_facebook.get_attribute('content'))	

facebook_title = browser.find_element_by_css_selector("meta[property='og\\:title']")
print('facebook title: ', end ='')
print(facebook_title.get_attribute('content'))

facebook_description = browser.find_element_by_css_selector("meta[property='og\\:description']")
print('facebook description: ', end ='')
print(facebook_description.get_attribute('content'))
```
## Other SEO data
```
item_prop = browser.find_element_by_css_selector("meta[property='og\\:country-name']")
print('country name: ', end ='')
print(item_prop.get_attribute('content'))	

item_prop = browser.find_element_by_css_selector("meta[itemprop='name']")
print('item prop name: ', end ='')
print(item_prop.get_attribute('content'))		

canonical_link = browser.find_element_by_css_selector('link[rel="canonical"')
print('canonical link: ', end ='')
print(canonical_link.get_attribute('href'))	

item_prop = browser.find_element_by_css_selector("meta[itemprop='keywords']")
print('Keywords: ', end ='')
print(item_prop.get_attribute('content'))	

site_code = browser.find_element_by_css_selector("meta[name='sitecode']")
print('Site code: ', end ='')
print(site_code.get_attribute('content'))				

page_title = browser.find_element_by_css_selector('meta[name="title"]')
print('Page title: ', end ='')
print(page_title.get_attribute('content'))
```
