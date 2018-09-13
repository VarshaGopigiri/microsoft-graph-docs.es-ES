# <a name="usersecuritystate-resource-type"></a>Tipo de recurso userSecurityState

Contiene información de estado acerca de la cuenta de usuario.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|aadUserId|Cadena|Identificador de objeto de usuario (GUID) de AAD: representa la entidad de usuario física/multicuenta.|
|accountName|Cadena|Nombre de cuenta de la cuenta de usuario (sin dominio de Active Directory o dominio DNS) - (también denominada `mailNickName`).|
|domainName|Cadena|Dominio de NetBIOS o Active Directory de la cuenta de usuario (es decir, el formato dominio\cuenta).|
|emailRole|emailRole|Para las alertas relacionadas con el correo electrónico: correo electrónico de una cuenta de usuario 'rol'. Los valores posibles son: `unknown`, `sender` y `recipient`.|
|isVpn|Booleano|Indica si el usuario se ha conectado mediante una red privada virtual (VPN).|
|logonDateTime|DateTimeOffset|Hora del inicio de sesión. El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|logonId|Cadena|Id. de usuario de inicio de sesión.|
|logonIp|Cadena|Dirección IP desde la que se ha originado la solicitud.|
|logonLocation|Cadena|Ubicación (mediante asignación de dirección IP) asociada a un evento de inicio de sesión de usuario por parte de este usuario.|
|logonType|logonType|Método de inicio de sesión de usuario. Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch` y `service`.|
|onPremisesSecurityIdentifier|Cadena|Identificador de seguridad (SID) de Active Directory (local) del usuario.|
|riskScore|Cadena|Puntuación de riesgo calculado/generado por el proveedor de la cuenta de usuario. Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.|
|userAccountType|userAccountSecurityType|Tipo de cuenta de usuario (pertenencia a grupo), por definición de Windows. Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.|
|userPrincipalName|Cadena|Nombre de inicio de sesión de usuario - formato de internet: (nombre de cuenta de usuario) @(nombre de dominio DNS de cuenta de usuario).|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
{
  "aadUserId": "String",
  "accountName": "String",
  "domainName": "String",
  "emailRole": "@odata.type: microsoft.graph.emailRole",
  "isVpn": true,
  "logonDateTime": "String (timestamp)",
  "logonId": "String",
  "logonIp": "String",
  "logonLocation": "String",
  "logonType": "@odata.type: microsoft.graph.logonType",
  "onPremisesSecurityIdentifier": "String",
  "riskScore": "String",
  "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
