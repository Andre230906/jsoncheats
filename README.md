
![image](https://github.com/Andre230906/jsoncheats/assets/156432253/f29758ef-d1cf-49d8-857c-4326c5a03ec5)



| title                                  | description                                                                                                    |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Python Json Module - Python Cheatsheet | Python tiene incorporado el módulo json, que nos permite trabajar con datos JSON (JavaScript Object Notation). |

Módulo Json de Python
JSON significa JavaScript Object Notation y es un formato ligero para almacenar y transportar datos. JSON se utiliza a menudo cuando los datos se envían desde un servidor a una página web.

Python tiene incorporado el módulo json, que nos permite trabajar con datos JSON.


```import json```

Un objeto JSON es similar a un diccionario Python, pero tiene las siguientes diferencias:

Las claves JSON son siempre cadenas.
Las cadenas siempre van entre comillas dobles.
Un booleano JSON empieza con minúsculas.
null es el equivalente JSON de None en Python.

Los tipos de datos que soporta JSON son:
String
Number
boolean
null
Object
Array

example
```
{
  "name": "Charles",
  "age": 33,
  "has_hair": false,
  "hobbies": ["photography", "running"],
  "appearance": {
    "eyes": "brown",
    "hair_color": null
  }
}
```
Significa las siguientes operaciones:

C- CREAR
R- LEER
U- UPDATE
D- ELIMINAR
Ahora, tomando el JSON significa JavaScript Object Notation que es un formato ligero de intercambio de datos utilizado para enviar datos entre ordenadores y es independiente del lenguaje.

Está escrito en formato de directorio.

#Ejemplo de JSON
```
{
 "name"  :"Sam",
 "age"   :30,
 "gender":male
}
```
Python tiene un paquete incorporado llamado json, que se puede utilizar para trabajar con datos JSON.
A continuación, vamos a tomar un programa de ejemplo para realizar una operación crud, En primer lugar, vamos a crear un archivo json y luego almacenar los datos en ese archivo.
```
FILEPATH = 'city.json'
def get_json_data():
  with open(FILEPATH) as json_file:
       data = json.load(json_file)
return data
```
para el almacenamiento :
```
def store_json_data(data):
    with open(FILEPATH, 'w') as outfile:
         json.dump(data, outfile)
```
Ahora tengamos la función principal para pasar los datos a otras funciones, para la función principal la nombraremos como """startpy()""" En ella, primero declararemos los datos y pasamos a crear una función   
```
from pprint import pprint
def startpy():
   print("CRUD started!")
   # CRUD: Add City
   city    = "Madurai"
   state   = "Tamilnadu"
  add_city(city, state)
  # # CRUD: READ all
  cities = get_all_cities()
  pprint(cities)
  ```
![image](https://github.com/Andre230906/jsoncheats/assets/156432253/2322cbea-3bac-4b9c-8eb0-0083fe7fea48)

#JSON loads() method
With the json.loads method, you can parse a JSON object and transform it to a Python dictionary:
```
>>> import json

>>> json_person = '{"name": "Charles", "age": 33, "has_hair": false, "hobbies": ["photography", "running"]}'
>>> python_person = json.loads(json_person)
>>> python_person
# {'name': 'Charles', 'age': 33, 'has_hair': False, 'hobbies': ['photography', 'running']}

>>> type(python_person)
# <class 'dict'>

>>> python_person.get("name")
# 'Charles'
```
#JSON dumps() method
The other way around. The dumps() method transforms a Python object to a JSON string:
```
>>> import json

>>> python_person = {'name': 'Charles', 'age': 33, 'has_hair': False, 'hobbies': ['photography', 'running']}
>>> json_person = json.dumps(python_person)

>>> json_person
# '{"name": "Charles", "age": 33, "has_hair": false, "hobbies": ["photography", "running"]}'

>>> type(json_person)
# <class 'str'>
```
Reading and writing Json Files
Reading a Json File
```
>>> import json
>>> with open("filename.json", "r") as f:
...     json_content = json.loads(f.read())
...
>>> json.loads(json_content)
# {'name': 'Charles', 'age': 33, 'has_hair': False}
```
Writing a Json File
```
>>> import json

>>> person = {'name': 'Charles', 'age': 33}

>>> with open("filename.json", "w") as f:
...     f.write(json.dumps(person))
```
