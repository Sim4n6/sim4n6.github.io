---
title: Geo-Location of Defibrillators at Toulouse city
updated: 2019-07-28
---


```python 
import csv
import folium

m = folium.Map(location=[43.6047, 1.442], zoom_start=12)
```

```python

popup_html = """
    <h4>{}</h4>
    <p>{}<br>{}, {}</p>
    <p>{} {} {}.</p>
"""
```

```python
with open('defibrillateurs-toulouse.csv', newline='', encoding='utf-8') as csv_file:
        csv_reader = csv.DictReader(csv_file, delimiter=';')
        next(csv_reader)
        for row in csv_reader:
            geoloc = row['Geo Point'].split(',')
            folium.Marker(location=[float(geoloc[0]), float(geoloc[1])], 
                          popup=popup_html.format(row['nom_site'], row['implantation'], row['adresse'], row['commune'], row['type_structure'], row['accessibilite'], row['pb_disponibilite_temporaire'] ), 
                          icon=folium.Icon(color='red', icon='info-sign')).add_to(m)

```

```python
m
```

<img src="/assets/defib.png" />

<a href="https://github.com/Sim4n6/defib-geolocation" target="_blank">defib-geolocation repository</a>