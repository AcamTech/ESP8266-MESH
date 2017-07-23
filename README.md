EspMesh

Implementaci�n de la librer�a serial de software Arduino para el ESP8266
mas detalles en https://github.com/uagaviria/EspSoftwareSerial

Documentaci�n t�cnica de EspMesh

EspMesh crea una red de auto-organizaci�n, donde todos los nodos est�n conectados. Todos los nodos en la malla son iguales. La red utiliza una topolog�a en estrella, evitando rutas circulares. Los mensajes entre los diferentes nodos se env�an en formato JSON, haci�ndolos f�ciles de entender y producir.

![Screenshot](espmesh.png)


Informaci�n de enrutamiento

La informaci�n de enrutamiento se comparte en forma de mensajes de sincronizaci�n de nodos. Cada nodo informa a sus vecinos acerca de todos los otros nodos a los que est� conectado directamente ya todas sus respectivas subconnexiones. De esta manera, cada nodo tiene una imagen en tiempo real de toda la malla y sabe qu� nodos est�n conectados a la malla. Esta informaci�n se actualiza  cada 3 segundos aproximadamente.

Casos en los que se realiza una nueva sincronizaci�n de nodo

-La petici�n de sub-conexiones se realiza peri�dicamente
-Cuando se detecta cualquier actualizaci�n en la red, es decir,  cualquier subconecci�n de un nodo ha cambiado
-Cuando un nuevo nodo se conecta a un nuevo AP



