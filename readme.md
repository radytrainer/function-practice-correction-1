## Exercise correction note

### Exercise #1
<img src="ex1.PNG">

#### Step 1: Remove the "-" sign from string
```python
text = "H-e-l-l-o" 
result = ""
for i in range(len(text)):
    if text[i] != '-':
        result += text[i]
print(result) # result: Hello
```

#### Step 2: Convert that code to functions
```python
def removeMinuses(word):
    result = ""
    for i in range(len(word)):
        if word[i]!= '-':
            result += word[i]
    return result
print(removeMinuses("H-e-l-l-o")) # result: Hello
```
#### Step 3: Enter many time until you enter "N" to stop and "Y" to continue
```python
isContinue = True
while isContinue:
    stop = input("Do you want to continue (y/n): ")
    if stop.upper() != "Y":
        isContinue = False
```
#### Step 4: Combine all of them together (Final code)
```python
def removeMinuses(word):
    result = ""
    for i in range(len(word)):
        if word[i]!= '-':
            result += word[i]
    return result

isContinue = True
while isContinue:
    text = input("Enter word: ")
    print("Word without minus: " + removeMinuses(text))
    stop = input("Do you want to continue (y/n): ")
    if stop.upper() != "Y":
        isContinue = False
```