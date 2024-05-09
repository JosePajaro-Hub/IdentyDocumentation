
.. autosummary::
   :toctree: generated

1.	Objetivo
--------------------------

Describir de manera técnica y detallada el consumo de los servicios de IDENTY. 

2.	Usuario y contraseña
--------------------------

 Para poder consumir los servicios y generar un token es necesario solicitar un usuario y una contraseña. 
 
3.Endpoint Login
--------------------------

Todas las operaciones POST deben consumir un token el cual será generado a través del servicio login (ingresando usuario y contraseña previamente solicitados) y este debe ser ingresado al momento de consumir cada servicio.

AMBIENTE: Producción  
--------------------------
URL Servicio: https://cotejoselfie-core.gse.com.co/BackLogin/users/login
--------------------------

3.1.     Parámetros de entrada
--------------------------

Objeto JSON que debe cumplir con los siguientes atributos:
+-----------+----------+---------+----------------+--------------------------------------------------+
|Nombre     | Tipo     | Tamaño  |  Obligatorio   |  Descripcion                                     |
+===========+==========+=========+================+==================================================+
| email     |  string  |    30   |    si          |Usuario para el acceso a Identy entregado por GSE |
+-----------+----------+---------+----------------+--------------------------------------------------+
| password  |  string  |    30   |      si        |Clave del usuario para el acceso a GSE            |
+-----------+----------+---------+----------------++-------------------------------------------------+
   
3.2     Ejemplo JSON de entrada
--------------------------
.. image:: docs/img/Captura.png
   :width: 400px
   :height: 300px
   :alt: Ejemplo JSON de entrada