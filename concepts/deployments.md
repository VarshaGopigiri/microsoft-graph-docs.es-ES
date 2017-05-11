# <a name="sovereign-cloud-deployments"></a>Implementaciones de nube soberana


Este artículo proporciona información sobre las diferentes instancias de nube soberana de Microsoft Graph y las funcionalidades que están disponibles para los desarrolladores. 


## <a name="microsoft-graph-operated-by-21vianet-in-china"></a>Microsoft Graph operado por 21Vianet en China

En este artículo se proporciona información sobre Microsoft Graph ofrecido por 21Vianet y las funcionalidades que están disponibles para los desarrolladores. 

### <a name="microsoft-graph-service-root-endpoints"></a>Extremos de raíz del servicio de Microsoft Graph
| Microsoft Graph operado por 21Vianet | Microsoft Graph|
|---------------------------|----------------|
| https://microsoftgraph.chinacloudapi.cn | https://graph.microsoft.com|

### <a name="microsoft-graph-explorer"></a>Probador de Microsoft Graph
| Probador de Microsoft Graph en China | Probador de Microsoft Graph|
|---------------------------|----------------|
|https://developer.microsoft.com/zh-cn/graph/graph-explorer-china| https://developer.microsoft.com/graph/graph-explorer|

### <a name="azure-openid-connect-and-oauth20"></a>OpenID Connect y OAuth 2.0 de Azure
Los extremos que se utilizan para adquirir tokens de inicio de sesión o para llamar a Microsoft Graph ofrecido por 21Vianet difieren de las de otras ofertas. 

| Microsoft Graph operado por 21Vianet | Microsoft Graph|
|---------------------------|----------------|
| https://login.chinacloudapi.cn | https://login.microsoftonline.com|
 
Use https://login.chinacloudapi.cn/common/oauth2/authorize para autenticar el usuario y https://login.chinacloudapi.cn/common/oauth2/token para adquirir un token para su aplicación para llamar a Microsoft Graph operado por 21Vianet.

> **Nota:** Los [puntos de conexión de tokens y de autorización de v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-appmodel-v2-overview/) más recientes NO están disponibles para su uso con Microsoft Graph operado por 21Vianet. 

>Las aplicaciones solo pueden acceder a datos de la organización y no a datos de clientes a través del punto de conexión **https://microsoftgraph.chinacloudapi.cn**. Las aplicaciones deben usar el punto de conexión **https://graph.microsoft.com** para acceder a los datos de clientes.

### <a name="service-capabilities-offered-by-microsoft-graph-operated-by-21vianet"></a>Funcionalidades del servicio ofrecidas por Microsoft Graph operado por 21Vianet
Las siguientes características de Microsoft Graph están generalmente disponibles (en el punto de conexión de `/v1.0`):

* Usuarios
* Groups
* Files
* Correo
* Calendario
* Contactos personales 
* Crear, leer, actualizar y eliminar (CRUD) operaciones 
* Compatibilidad para compartir recursos de origen cruzado (CORS).

Las siguientes características de Microsoft Graph también están disponibles en versión preliminar (en el punto de conexión de `/beta`):

* Contactos de la organización
* Aplicaciones
* Entidades de servicio
* Extensiones de esquema de directorio
* Webhooks
