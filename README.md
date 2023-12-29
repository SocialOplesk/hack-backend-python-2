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
| H-1      | CLOUD - CRUD basic with QUERY and BODY |
| H-2      | LOCAL ( UX/UI ) - CU simple Upload image | 
| H-3      | CLOUD ( UX/UI ) - CUD basic with BODY more upload image in (Module) |
| H-4      | LOCAL - CR basic JSONWEBTOKEN |
| H-5      | CLOUD / TEAM - CRUD upload image more jsonwebtoken with (Module)|

<br/> 

## 🏆 H-1 

```sh
CREAR UN CRUD QUE RESPONDA A LAS SIGUIENTES ACCIONES Y EMPLEO DE TECNOLOGÍAS
ABAJO TIENES EL MOCK DE DATOS & DEBE ESTAR DENTRO DE UN ARCHIVO mock.json:


users = [
    {"email": "foo@example.com", "name": "foo", "age": 30, "role": "admin"},
    {"email": "bar@example.com", "name": "bar", "age": 25, "role": "editor"},
    {"email": "baz@example.com", "name": "baz", "age": 28, "role": "viewer"},
    {"email": "echo@example.com", "name": "echo", "age": 35, "role": "admin"},
    {"email": "qux@example.com", "name": "qux", "age": 29, "role": "viewer"},
    {"email": "delta@example.com", "name": "delta", "age": 47, "role": "viewer"},
    {"email": "zi@example.com", "name": "zi", "age": 20, "role": "viewer"},
    {"email": "charlie@example.com", "name": "charlie", "age": 31, "role": "viewer"}
]


---------------------------------------------------

✔ POST / BODY    -  Permitir crear usuario
✔ PUT / BODY     -  Actualizar los datos filtrado por email
✔ GET / QUERY    -  Buscar usuario por el derivado del email
✔ GET            -  Listar todos los usuarios ordenados por edad de menor a mayor
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
CREAR UNA INTERFAZ GRÁFICA CON HTML & CSS3, SI ES POSIBLE UTILIZAR FLEXBOX, PARA QUE EL FORMULARIO
ESTE 100% CENTRADO VERTICAL & HORIZONTAL A LA VISTA MOBILE & DESKTOP (RESPONSIVE)
LA VISTA TIENE LA FUNCIÓN DE SUBIR UNA IMAGEN

---------------------------------------------------

✔ POST / BODY    -  Subir imagen 

---------------------------------------------------

📊 Requiere el desarrollo de interfaz gráfica, "no requiere" deploy en nube
📦 No requiere, almacenar las imágenes en el store de S3 en AWS, sino en local
💻 No requiere, hospedar el backend en una VM del servicio EC2, sino en local

---------------------------------------------------

```
<br/>

## 🏆 H-3
```sh
CREAR UN CUD QUE RESPONDA A LAS SIGUIENTES ACCIONES Y EMPLEO DE TECNOLOGÍAS,
ADICIONAL EL CÓDIGO DEBE SER MODULAR,
ABAJO TIENES EL MOCK DE DATOS & DEBE ESTAR DENTRO DE UN ARCHIVO mock.json:


users = [
    {"email": "foo@example.com", "name": "foo", "age": 30, "role": "admin", "image": ""},
    {"email": "bar@example.com", "name": "bar", "age": 25, "role": "editor", "image": ""},
    {"email": "baz@example.com", "name": "baz", "age": 28, "role": "viewer", "image": ""},
    {"email": "echo@example.com", "name": "echo", "age": 35, "role": "admin", "image": ""},
    {"email": "qux@example.com", "name": "qux", "age": 29, "role": "viewer", "image": ""},
    {"email": "delta@example.com", "name": "delta", "age": 47, "role": "viewer", "image": ""},
    {"email": "zi@example.com", "name": "zi", "age": 20, "role": "viewer", "image": ""},
    {"email": "charlie@example.com", "name": "charlie", "age": 31, "role": "viewer", "image": ""}
]

---------------------------------------------------

✔ POST / BODY    -  Permitir crear usuario con su imagen 
✔ PUT / BODY     -  Actualizar los datos filtrado por email
✔ DELETE / BODY -   Eliminar usuario por email

---------------------------------------------------

🏹 Emplear el uso del rate-limit en los endpoints
🧪 utilizar el uso del checking de datos si es de tipo email, name, age
🧩 Aplicar una nomenclatura de endpoints bajo versiones, colección ó estandares 
   - ejemplo: /v1/user ||  /c1/user  ||  /std1/user

---------------------------------------------------

📊 Requiere el desarrollo de interfaz gráfica, como host Vercel
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

## 🏆 H-4
```sh
CREAR UN CR QUE RESPONDA A 2 ACCIONES EN LA ELABORACION
DE 1 TOKEN BAJO EL ESTANDAR JSONWEBTOKEN

ESTRUCTURA DEL TOKEN
{"sub": "foo@example.com", "name": "foo", "role": "admin", "exp":time}


---------------------------------------------------

✔ POST / BODY    -  Crear jsonwebtoken
✔ GET / BODY    -   Verificar jsonwebtoken 

---------------------------------------------------

⏳ Establecer un tiempo de caducidad de 1 minuto 

---------------------------------------------------

📊 No requiere el desarrollo de interfaz gráfica
💻 No requiere, hospedar el backend en una VM del servicio EC2, sino en local

---------------------------------------------------

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

