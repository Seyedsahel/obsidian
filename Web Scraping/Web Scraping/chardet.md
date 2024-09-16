
```python
import chardet
 encoding = chardet.detect(page.content)["encoding"]

 html = page.content.decode(encoding)

 soup = BeautifulSoup(html, "html.parser")
```