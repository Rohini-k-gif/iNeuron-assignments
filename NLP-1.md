##### NLP Text Processing assignment

------

1. A python program to find out the words after '@' from the below sentences with the use of regex.

"xyz@gmail.com","abc@yahoo.com","xyz@hotmail.com","abc@ineuron.ai","xyz@outlook.com"

```python
import re
l1=["xyz@gmail.com","abc@yahoo.com","xyz@hotmail.com","abc@ineuron.ai",
"xyz@outlook.com"]


for i in l1:
    text=re.split(r'[@.]',i)
    print(text[1]+'.'+text[2])
    
    
    
```

2. Write a python program with the use of regex to take out the word "New" from the following sentence.

   ["New Delhi is the capital of India"]

```python
t="New Delhi is the capital of India"
x=re.findall("New",t)
print(x)
```

3. Create one python program in which you have to lowercase the sentence first and than delete digits from the following sentence.

   "In India, 184 people got affected with Corona virus and 4 are died."

   ```python
   def edit_text(text):
       edited_text=text.lower()
       edited_text=re.sub(r'\d+', '', edited_text)
       print(edited_text)
       
       
   text="In India, 184 people got affected with Corona virus and 4 are died."    
   edit_text(text)
   ```

   4. Do stemming, lemmatization and tokenization from the following sentence.

      "I hope that, when I have built up my savings, I will be able to travel to Hawai."

      ```python
      from nltk.stem.porter import PorterStemmer 
      from nltk.tokenize import word_tokenize 
from nltk.stem import wordnet 
      
      
      nltk.download('wordnet')
      lemma = wordnet.WordNetLemmatizer()
      stem1 = PorterStemmer() 
        
       
      def edit_text(text): 
          word_tokens = word_tokenize(text) 
          stems = [stem1.stem(word) for word in word_tokens]
          lemmas = [lemma.lemmatize(word, pos ='v') for word in word_tokens]
          print("Stems from given string : \n",stems)
          print("Lemmas from given string : \n",lemmas)
          print("Tokens from given string : \n ",word_tokens)
        
      text = 'I hope that, when I have built up my savings, I will be able to travel to Hawai.'
      edit_text(text)
      ```
      
      
      
      5. Create one python program from the following sentence.
      
      "I love NLP, not you"
      
      output : ['I', 'l', 'N', 'n', 'y']

```python
t="I love NLP, not you"
x=re.split('\s',t)
print(x)
nl=[]
for i in x:
    nl.append(i[0])
print(nl)
```

