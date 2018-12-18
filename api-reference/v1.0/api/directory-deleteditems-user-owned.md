---
title: Permisos
description: 'Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.  '
author: lleonard-msft
ms.openlocfilehash: 9ce487d957f4bdaa2684d00865aeac7ea293ad67
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351173"
---
# <a name="list-deleted-items-owned-by-a-user"></a>**Lista de los elementos eliminados que pertenecen a un usuario**

Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.  

Actualmente, la funcionalidad de elementos de lista eliminada sólo se admite para [agrupar](../resources/group.md) los recursos que pertenecen al usuario.

Se trata de una acción de servicio, lo que significa que no admite la paginación.  La API devuelve objetos eliminados hasta 1.000 que pertenecen al usuario, ordenado por identificador.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).

| Tipo de permiso | Permisos (de menos a más privilegiados) |
| --- | --- |
| Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) |  No admitida. |
| Aplicación | Group.Read.All, Group.ReadWrite.All  |

## <a name="http-request"></a>Solicitud HTTP

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción               |
| ------------- | ------------------------- |
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

```json
{
  "userId":"{id}",
  "type":"Group"
}
```

El cuerpo de solicitud requiere los siguientes parámetros:

| Parámetro    | Type |Descripción|
|:---------------|:--------|:----------|
|userId|String|Identificador del propietario.|
|type|String|Tipo de objetos que posea para devolver; `Group` actualmente es el único valor admitido.|


## <a name="response"></a>Respuesta

Solicitudes correctas devuelven `200 OK` los códigos de respuesta; el objeto de respuesta incluye las propiedades del [directorio (elementos eliminados)](../resources/directory.md) .

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

``` http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/getUserOwnedObjects
Content-type: application/json
```

``` json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"group"
}
```

###### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Este objeto de respuesta es posible que esté truncada por razones de brevedad. Se devuelven todas las propiedades admitidas de llamadas reales.

``` http
HTTP/1.1 200
Content-type: application/json
Content-length: 1249

{
"value": [
          {
              "@odata.type": "#microsoft.graph.group",
              "id": "bfa7033a-7367-4644-85f5-95aaf385cbd7",
              "deletedDateTime": 2018-04-01T12:39:16Z,
              "classification": null,
              "createdDateTime": "2017-03-22T12:39:16Z",
              "description": null,
              "displayName": "Test",
              "groupTypes": [
                  "Unified"
              ],
              "mail": "Test@contoso.com",
              "mailEnabled": true,
              "mailNickname": "Test",
              "membershipRule": null,
              "membershipRuleProcessingState": null,
              "preferredDataLocation": null,
              "preferredLanguage": null,
              "proxyAddresses": [
                  "SMTP:Test@contoso.com"
              ],
              "renewedDateTime": "2017-09-22T22:30:39Z",
              "securityEnabled": false,
              "theme": null,
              "visibility": "Public"
          } 
        ]
 }
```


