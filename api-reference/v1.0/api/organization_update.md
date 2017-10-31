# <a name="update-organization"></a>Actualizar organización

Actualice las propiedades de la organización autenticada actualmente.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | No admitida.    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization

```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedPlans|AssignedPlan|La colección de planes de servicio asociados con el inquilino. **Notas**: no admite valores NULL.            |
|city|String|            |
|companyLastDirSyncTime|DateTimeOffset|Fecha y hora en las que el inquilino se ha sincronizado por última vez con el directorio local.|
|country|String|            |
|countryLetterCode|String|            |
|deletionTimestamp|DateTimeOffset||
|dirSyncEnabled|Boolean|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).|
|displayName|String|El nombre para mostrar del inquilino.|
|marketingNotificationEmails|String|                                        **Notas**: no admite valores NULL.            |
|objectType|String|Cadena que identifica el tipo de objeto. Para los inquilinos, el valor es siempre "Company". Heredado de [directoryObject](../resources/directoryobject.md).|
|postalCode|String|            |
|preferredLanguage|String|            |
|provisionedPlans|ProvisionedPlan|                                        **Notas**: no admite valores NULL.            |
|provisioningErrors|ProvisioningError|                                        **Notas**: no admite valores NULL.            |
|securityComplianceNotificationMails|String||
|securityComplianceNotificationPhones|String||
|state|String|            |
|street|String|            |
|technicalNotificationMails|String|                                        **Notas**: no admite valores NULL.            |
|telephoneNumber|String|            |
|verifiedDomains|VerifiedDomain|La colección de dominios asociados a este inquilino. **Notas**: no admite valores NULL.            |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/organization
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

<br/>

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. **Nota**: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

<br/>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
