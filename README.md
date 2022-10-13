# Beautifulsoup: How to get class name


```python

# ********** 👇 Beautifulsoup Get Class Name 👇 ********** #



from bs4 import BeautifulSoup # 👉️ Import BeautifulSoup module



# -- 👇 Beautifulsoup Get Class Name of a tag  👇 -- #


# 👇 HTML Source
html = '''

<div class="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find("div") # 👉️ Find <div>

div_class = el['class'] # 👉️ Get div class name

print(div_class) # 👉️ Print Result

# 👆 Output: ['node']


if div_class: # 👉️ Check if <div> has a class
    print(div_class[0]) # 👉️ Print Class name

# 👆 Output: node






# -- 👇 Beautifulsoup Get Class Name of a tag 👇 -- #


# 👇 HTML Source
html = '''

<div class="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find("div", class_=True) # 👉️ Find <div> and with class name attr

div_class = el['class'] # 👉️ Get <div> class name

print(div_class[0]) # 👉️ Print Class name

# 👆 Output: node






# -- 👇 Beautifulsoup Get multi-class names of an element 👇 -- #


# 👇 HTML Source
html = '''

<div class="node text fav">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find("div") # 👉️ Find <div>

div_class = el['class'] # 👉️ Get <div> class name

print(div_class) # 👉️ Print Result

# 👆 Output: ['node', 'text', 'fav']


# 👇 Print each class name
for _class in div_class:
    print(_class)

# 👇 Output: node
""" 
node
text
fav 
"""






# -- 👇 Get the class name of multi-elements 👇 -- #


# 👇 HTML Source
html = '''

<div class="node">
<p>Hello Beautifulsoup</p>
</div>

<div class="node_1">
<p>Hello Beautifulsoup</p>
</div>


<div class="node_2">
<p>Hello Beautifulsoup</p>
</div>


<div>
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

els = soup.find_all("div", class_=True) # 👉️ Find all <div> tags and with class name attr

for el in els: # 👉️ Loop over els
    print(el['class']) # 👉️ Print Class name

# 👇 Output
"""
['node']
['node_1']
['node_2']
"""
```




For the tutorial of the examples, vists (beautifulsoup-get-class-name - PyTutorial)[https://pytutorial.com/beautifulsoup-get-class-name]
