# Configuración centralizada


Esta carpeta contiene datos de configuración, no una aplicación independiente.
Platform la monta como /config en solo lectura y la sirve con Config Server native.

| Archivo | Contenido |
|---|---|
| application-cloud.properties | Propiedades comunes de Eureka y diagnóstico |
| account-service-cloud.properties | Conexión MySQL por variables y puerto |
| bff-web-cloud.properties | Nombre lógico de Account, JWT, timeouts y resiliencia |

Se utiliza spring.application.name y el perfil cloud para seleccionar los archivos.
Los valores sensibles son referencias a variables del cliente; no guardar
contraseñas, certificados privados ni tokens aquí.
Después de cambiar archivos, reiniciar los clientes para volver a importarlos.
