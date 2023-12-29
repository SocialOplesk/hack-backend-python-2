# SOCIAL OPLESK
### 🏴‍☠️ HACKS - BACKEND - 2

<br/>

📚 tutorial de flask - 1 [tutorial](https://towardsdatascience.com/creating-restful-apis-using-flask-and-python-655bad51b24)
<br/>
📚 tutorial de flask - 2 [tutorial](https://www.moesif.com/blog/technical/api-development/Building-RESTful-API-with-Flask/)
<br/>
📚 tutorial de flask - 3 [tutorial](https://www.digitalocean.com/community/tutorials/processing-incoming-request-data-in-flask)
---

```diff
- NOTA HACER LAS PRÁCTICAS MEDIANTE VISUAL STUDIO CODE  
```

```diff
* Instalar el framework:
  npm install flask

* Crear el archivo app.py en modo debug

* ejecutar el servidor en terminal: flask run --debug

```
<br/>

|Hacks | Details | 
|----------|---------|
| H-1      | CRUD simple with QUERY and BODY |
| H-2      | Upload image (UX/UI) | 
| H-3      | CRUD with QUERY and BODY more upload image in (Module & UX/UI) |
| H-4      | JSONWEBTOKEN |
| H-5      | CRUD upload image more jsonwebtoken with (Module) / GROUP |

<br/> 

## 🏆 H-1 

```sh
CREAR UN CRUD QUE RESPONDA A LAS SIGUIENTES ACCIONES Y EMPLEO DE TECNOLOGÍAS
ABAJO TIENES EL MOCK DE DATOS:


users = [
    {"email": "foo@example.com", "name": "foo", "age": 30, "role": "admin"},
    {"email": "bar@example.com", "name": "bar", "age": 25, "role": "editor"},
    {"email": "baz@example.com", "name": "baz", "age": 28, "role": "viewer"},
    {"email": "echo@example.com", "name": "echo", "age": 35, "role": "admin"},
    {"email": "qux@example.com", "name": "qux", "age": 29, "role": "viewer"}
    {"email": "delta@example.com", "name": "delta", "age": 47, "role": "viewer"}
]


---------------------------------------------------

✔ POST / BODY    -  Permitir crear usuario
✔ PUT / BODY     -  Actualizar los datos filtrado por email
✔ GET / QUERY    -  Buscar usuario por el derivado del email
✔ GET            -  Listar el total de usuarios
✔ GET / QUERY    -  Listar los usuarios en paginas de 2 usuarios por response si es mobile
✔ GET / QUERY    -  Listar los usuarios en paginas de 4 usuarios por response si es desktop
✔ DELETE / QUERY -  Eliminar usuario por email

---------------------------------------------------

🏹 Emplear el uso del rate-limit en los endpoints
🧪 utilizar el uso del checking de datos si es de tipo email, name, age
🧩 Aplicar una nomenclatura de endpoints bajo un estandar de versiones y  tipo de dispositivo
   - ejemplo: /v1/mobile/user || /v1/desktop/user || /v1/general/user
   - ejemplo: /v1/m/user      || /v1/d/user       || /v1/g/user

---------------------------------------------------

📊 No requiere el desarrollo de interfaz gráfica, es 100% backend
📦 Almacenar el archivo mock de la lista de usuarios, en el store de S3 en AWS
💻 Hospedar el backend en una VM del servicio EC2

---------------------------------------------------

📜 Ejemplo de estrucutra para el reponse

 => {
      "payload":data,
      "status":200,
       "error":{
                "active":None,
                "msg":None           
               }
   }

---------------------------------------------------

```
<br/>


## 🏆 H-2
```sh
CREAR UN CRUD QUE RESPONDA A LAS SIGUIENTES ACCIONES Y EMPLEO DE TECNOLOGÍAS
ABAJO TIENES EL MOCK DE DATOS:

```
<br/>

## 🏆 H-3
```sh
* ENDPOINT:(PATH: "/h3")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "PUT"

METHOD:   "PUT"
TYPE: JSON

output => {"payload":"put"}
```
<br/>

## 🏆 H-4
```sh
* ENDPOINT:(PATH: "/h4")

CREAR UN ENDOPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "DELETE"

ENDPOINT: /h4
METHOD:   "DELETE"
TYPE: JSON

output => {"payload":"delete"}

```
<br/>

## 🏆 H-5
```sh
* ENDPOINT:(PATH: "/h5")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "GET"
EN CASO CONTRARIO RESPONDER CON LA SALIDA DE UN OBJETO {} SIN PROPIEDADES

TRUE  - output => {"payload":"success", "error": False}
FALSE - output => {}
```
<br/>


## 🏆 H-6
```sh
* ENDPOINT:(PATH: "/h6")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD CORRESPONDE CON ALGÚN METODO HTTP: "GET" | "POST"| "DELETE"
- EN CASO CONTRARIO RESPONDER CON LA SALIDA DE UN OBJETO sin payload data {} 
- EN LA OPCIÓN type ANEXAR EL TIPO DE METODO HTTP
- LA PROPIEDAD content EN method ESPECIFICAR EL METODO HTTP

TRUE  - output => {"method":"type", "payload":"success", "error":False}
FALSE - output => {"method":"type", "payload":None, "error":False}
```
<br/>

## 🏆 H-7
```sh
* ENDPOINT:(PATH: "/h7?email="....."&name=".....")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "GET"
SE DEBE ENVIAR EL VALOR DEL email, name MEDIANTE QUERY STRING

output => {
            "payload":{"email":"foo@foo.com", "name":"fooziman"},
            "error":{"available":False,"err_msg":None},
            "status":200
          }

```
<br/>

## 🏆 H-8
```sh
* ENDPOINT:(PATH: "/h8")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "POST"
SE DEBE ENVIAR EL VALOR DEL email, name MEDIANTE BODY

- ENVIAR LOS DATOS EN UN JSON {"email","add an email", "alias":"add an alias"}


output => {
            "payload":{"email":"foo@foo.com", "name":"fooziman"},
            "error":{"available":False,"err_msg":None},
            "status":200
          }

```
<br/>


## 🏆 H-9
```sh
* ENDPOINT:(PATH: "/h9?alias="...")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "GET"
- SE DEBE ENVIAR EL VALOR DEL alias  MEDIANTE QUERY STRING
- BUSCAR UN VALOR VALIDO DENTRO DE LA LISTA DE ALIAS Y MOSTRAR SU SALIDA
- EN CASO DE NO ENCONTRAR EL alias EN LA LISTA DE ALIAS ENVIAR UN MENSAJE DE not found

const Lista = ["foo","bar","baz","qux","fred"]


TRUE - output => {
            "payload":"bar",
            "error":{"available":False,"err_msg":None},
            "status":200
          }


FALSE - output => {
            "payload":"not found",
            "error":{"available":False,"err_msg":None},
            "status":404
          }

```
<br/>


## 🏆 H-10 (PATH: "/h10")
```sh
* ENDPOINT:(PATH: "/h10")

CREAR UN ENDPOINT QUE RESPONDA SI LA SOLICITUD ES DE TIPO "POST"
- SE DEBE ENVIAR EL VALOR DEL alias  MEDIANTE BODY
- BUSCAR UN VALOR VALIDO DENTRO DE LA LISTA DE ALIAS Y MOSTRAR SU SALIDA
- EN CASO DE NO ENCONTRAR EL alias EN LA LISTA DE ALIAS ENVIAR UN MENSAJE DE not found

const Lista = ["foo","bar","baz","qux","fred"]

TRUE - output => {"payload":"bar"}
FALSE - output => {"payload":"not found"}
```
<br/>
