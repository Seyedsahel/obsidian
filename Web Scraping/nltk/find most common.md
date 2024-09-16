

1. ` این خط متن ورودی را به توکن‌ها (کلمات) تقسیم می‌کند.`
```python
tokens = word_tokenize(text)
```

2. `این خط مجموعه‌ای از کلمات توقف (stop words) را که در زبان انگلیسی رایج هستند و معمولاً در تحلیل متن نادیده گرفته می‌شوند، بارگذاری می‌کند.`
```python
stop_words = set(stopwords.words('english'))
```
3. `این خط توکن‌ها را فیلتر می‌کند و فقط کلماتی را نگه می‌دارد که در مجموعه کلمات توقف نیستند.`
```python
filtered_tokens = [word for word in tokens if word.lower() not in stop_words]
```

4. `این خط توزیع فراوانی کلمات فیلتر شده را محاسبه می‌کند.`
```python
fdist = FreqDist(filtered_tokens)
```
5. `این خط ۱۲ کلمه‌ای که بیشترین فراوانی را دارند، استخراج می‌کند.`
```python
keywords = fdist.most_common(12)
```



```python
from nltk.probability import FreqDist
from nltk.tokenize import word_tokenize
```
