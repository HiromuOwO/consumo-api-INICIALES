# Practica: Consumiendo APIs de terceros

En esta practica se mostrara como consumir APIs externos, usando Angular version 18.2, en esta version no tenemos creado `app.module.ts` por lo que antes de continuar sera necesario crear un nuevo proyecto en formato no standalone

## 1. Creacion del proyecto

Colocar el comando `ng new consumo-api-INICIALES --no-standalone`
![image](https://github.com/user-attachments/assets/1c7437fe-f845-49d5-b5cb-50033eb5d904)
Y elegir las siguientes opciones como mas se prefiera y se creara el Proyecto
![image](https://github.com/user-attachments/assets/32ee24ad-4c2a-4db4-9925-abb2327a604e)

Y ahora debes estar colocado dentro del proyecto para hacer cualquier modificacion, para ellos se usa el comando `cd consumo-api-INICIALES`
![image](https://github.com/user-attachments/assets/5da4ddb3-2f2c-422a-acf9-c090312b8103)

## 2. Creacion del servicio 
Debe crearse un Servicio con el fin de poder consumir APIs, para ello se utiliza `ng generate service services/user`
![image](https://github.com/user-attachments/assets/3181f3de-7b67-4920-b6e4-74d470d96d66)

Lo cuanl nos creara la carpeta servicios y dos archivos mas
![image](https://github.com/user-attachments/assets/a76b55d1-cb12-428f-8f3e-2b6615bef3af)

Dentro del archivo `user.service.ts` debemos colocar el siguiente codigo
![image](https://github.com/user-attachments/assets/51163005-463d-444e-b53d-b5fa0d80b228)


## 3. Hacer petciones 

Para poder hacer peticiones HTTP debemos modificar el archivo `app.module.ts` de la siguiente manera: 
![image](https://github.com/user-attachments/assets/2f523c11-bd82-44e3-a44e-72d0ad3f011e)


## 4. Creacion del componente USER-LIST
Se crea un nueco componente con el comando `ng generate component components/user-list`
Se debe actualizar el componente para que pueda obtener los datos de usuario usando el servicio. 
En el archivo .ts del componente debe estar el codigo 
![image](https://github.com/user-attachments/assets/161a208d-f1b7-4d12-9709-16ccbe59e1e9)


## 5. Vista para mostrar la tabla
En el .html del componente se coloco la estructura basica de una tabla que se llena usando los datos de la API
![image](https://github.com/user-attachments/assets/5cf8e41c-4c94-41c5-989b-17551f82bb89)


## 6. Prueba de la aplicacion
El compoente debo colocarse en el .html de la plicacion, es decir en  `app.component.html` colocamos `<app-user-list></app-user-list>`
Y levantamos servidor con `ng serve`
![image](https://github.com/user-attachments/assets/58593e78-aed5-41c9-854a-ead39bd5a071)
Las APIs suelen cambiar, por lo que en ocasiones podemos ver mas o menos informacion 

## 7. Diseño de la tabla
Modificando el .css de nuestro componente podemos darle mas diseño a nuestro componente, colocaremos diferentes colores y tamaños de letra 
![image](https://github.com/user-attachments/assets/6beb2504-6a4e-4032-9e5b-7251609d6319)

## 8. Crear paginacion
En casos donde las APIs tiene muchos gatos podriamos usar paginacion para ver la informacion por bloques 
Descargamos la libreria `ngx-pagination` con el siguiente comando
![image](https://github.com/user-attachments/assets/76533d67-8d67-4342-8d3c-1e9a384358df)

Finalmente modificar 


