# intro-python

Please copy and paste the following code in Data Science Experience's notebook.

```{python}
# Import libraries
import urllib2
import re

# Pull html
website = urllib2.urlopen("http://clasificados.eltiempo.com/avisos/vivienda?query=Apartamento")
html = website.read()


# Extract all the links
links = re.findall('href=.(/anuncio/aviso-vivienda.*?)"', html)
print links[1]

```
