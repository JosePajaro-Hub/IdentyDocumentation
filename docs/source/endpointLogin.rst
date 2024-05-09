
.. autosummary::
   :toctree: generated

1.	Objetivo
^^^^^^^^^^^^^^^^^^^^^^^^

Describir de manera técnica y detallada el consumo de los servicios de IDENTY. 

2.	Usuario y contraseña
^^^^^^^^^^^^^^^^^^^^^^^^

 Para poder consumir los servicios y generar un token es necesario solicitar un usuario y una contraseña. 
 
3.Endpoint Login
^^^^^^^^^^^^^^^^^^^^^^^^

Todas las operaciones POST deben consumir un token el cual será generado a través del servicio login (ingresando usuario y contraseña previamente solicitados) y este debe ser ingresado al momento de consumir cada servicio.

AMBIENTE: Producción  

URL Servicio: https://cotejoselfie-core.gse.com.co/BackLogin/users/login


3.1.     Parámetros de entrada

Objeto JSON que debe cumplir con los siguientes atributos:

+------------+--------+--------+-------------+---------------------------------------------------+
| Nombre     | Tipo   | Tamaño | Obligatorio | Descripción                                       |
+============+========+========+=============+===================================================+
| email      | string | 30     | si          | Usuario para el acceso a Identy entregado por GSE |
+------------+--------+--------+-------------+---------------------------------------------------+
| password   | string | 30     | si          | Clave del usuario para el acceso a GSE            |
+------------+--------+--------+-------------+---------------------------------------------------+
   

3.2     Ejemplo JSON de entrada

.. image:: https://thinkdigitalco-my.sharepoint.com/:i:/g/personal/luna_herrera_gse_com_co/ETCU_nfitjtFmC3RwC6SavYBtyrWYTU5SV6W5L_MPOQ6aA?e=eZAweo
   :width: 400
   :alt: Ejemplo JSON de entrada


.. raw:: html

   <iframe src="https://thinkdigitalco-my.sharepoint.com/personal/luna_herrera_gse_com_co/_layouts/15/embed.aspx?UniqueId=77fe9430-b6e2-453b-982d-d1c02e926af6" width="640" height="360" frameborder="0" scrolling="no" allowfullscreen title="Captura.PNG"></iframe>

3.3      Respuesta 

Como respuesta de la operación se va a devolver un (Código 200 - Inicio de Sesión Exitoso) un JSON con la siguiente estructura:

+---------------+--------+---------+---------------------------------+
| Nombre        | Tipo   | Tamaño  | Descripción                     |
+===============+========+=========+=================================+
| accessToken   | string |         | Cadena con el token de tipo JWT |
+---------------+--------+---------+---------------------------------+


3.4.      Ejemplo JSON de respuesta 

El siguiente es un ejemplo JSON con el formato token de un response: 

   .. image:: img/Captura.png
      :width: 400
      :height: 300
      :alt: Ejemplo JSON de entrada
