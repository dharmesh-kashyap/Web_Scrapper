# Web Scrapper

Web Scrapper brushes the valuable data from the websites into useful .csv files

## How to use this Jupyter Notebook ?

Change the link in the URL section to your desired webpage 
```bash
URL = 'Your link here'

```
Use the Link [headers](http://httpbin.org/get) to get the header of your computer.

```bash
http://httpbin.org/get
```

![Screenshot (36)](https://user-images.githubusercontent.com/70679348/190306821-0524ff9b-3586-46b8-8270-b4d228d44057.png)

Page jsut like above picture will appear. Paste the highlited text in the header section 
```bash
headers = {"User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/105.0.0.0 Safari/537.36 Edg/105.0.1343.3

```


Look out for the data you want to get and copy the Span id, the span class or the div class into title and price section 

```bash
title = soup2.find('span',{'class':"B_NuCI"}).get_text()

price = soup2.find('div',{'class':'_30jeq3 _16Jk6d'}).get_text()

```

![Screenshot (37)](https://user-images.githubusercontent.com/70679348/190308235-fa3690dd-a848-4534-8781-c63ee5186d2a.png)

Now for creating the .CSV file. Run below code and replace the file name as per your preferrence.
```python
import csv 

header = ['Title', 'Price', 'Date']
data = [title, price, today]


with open('NothingPhone1Datascrapper.csv', 'w', newline='', encoding='UTF8') as f:
    writer = csv.writer(f)
    writer.writerow(header)
    writer.writerow(data)
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
