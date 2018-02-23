# <a name="windowsinformationprotectionpolicy-resource-type"></a>Tipo de recurso windowsInformationProtectionPolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva para Windows Information Protection sin MDM

Hereda de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionPolicies](../api/intune_mam_windowsinformationprotectionpolicy_list.md)|Colección [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).|
|[Obtener windowsInformationProtectionPolicy](../api/intune_mam_windowsinformationprotectionpolicy_get.md)|[windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).|
|[Crear windowsInformationProtectionPolicy](../api/intune_mam_windowsinformationprotectionpolicy_create.md)|[windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Cree un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).|
|[Eliminar windowsInformationProtectionPolicy](../api/intune_mam_windowsinformationprotectionpolicy_delete.md)|Ninguno|Elimina un [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).|
|[Actualizar windowsInformationProtectionPolicy](../api/intune_mam_windowsinformationprotectionpolicy_update.md)|[windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Actualice las propiedades de un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|description|Cadena|La descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|versión|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|enforcementLevel|Cadena|Nivel de obligatoriedad del trabajo en curso. Consulte la definición de enumeración para los valores compatibles. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md). Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.|
|enterpriseDomain|Cadena|Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseProtectedDomainNames|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|protectionUnderLockConfigRequired|Booleano|Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|dataRecoveryCertificate|[windowsInformationProtectionDataRecoveryCertificate](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados. Esto es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|revokeOnUnenrollDisabled|Booleano|Esta directiva controla si quiere revocar las claves de trabajo en curso cuando un dispositivo anule la inscripción del servicio de administración. Si se establece en 1 (No revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción. Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|rightsManagementServicesTemplateId|Guid|GUID de TemplateID que se va a usar para el cifrado RMS. La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo tienen acceso. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|azureRightsManagementServicesAllowed|Booleano|Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|iconsVisible|Booleano|Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio. A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|protectedApps|Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|exemptApps|Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos. Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseNetworkDomainNames|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Esta es la lista de dominios que forman parte de los límites de la empresa. Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseProxiedDomains|Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)|Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección. Las conexiones a estos recursos se consideran datos empresariales. Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80). Un servidor proxy que se use para este propósito también debe configurarse mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseIPRanges|Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)|Establece los intervalos IP empresariales que definen los equipos de la red empresarial. Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos. Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseIPRangesAreAuthoritative|Booleano|Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes. El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseProxyServers|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Esta es una lista de servidores proxy. Cualquier servidor que no esté en esta lista se considera que no es de empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseInternalProxyServers|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Esta es la lista de valores separados por comas de servidores proxy internos. Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59". El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet. Se consideran ubicaciones de red empresarial. Los servidores proxy solo se usan para configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|enterpriseProxyServersAreAuthoritative|Booleano|Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo. El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|neutralDomainResources|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|indexingEncryptedStoresOrItemsBlocked|Booleano|Esta opción es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|smbAutoEncryptedFileExtensions|Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)|Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|isAssigned|Booleano|Indica si la directiva se implementará en los grupos de inclusión o no. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|revokeOnMdmHandoffDisabled|Booleano|Nueva propiedad en RS2, pendiente de documentación|
|mdmEnrollmentUrl|Cadena|Dirección URL de la inscripción para MDM|
|windowsHelloForBusinessBlocked|Booleano|Valor booleano que establece Windows Hello para empresas como un método para iniciar sesión en Windows.|
|pinMinimumLength|Int32|Valor entero que establece el número mínimo de caracteres necesarios para el PIN. El valor predeterminado es 4. El número más bajo que se puede configurar para esta configuración de directiva es 4. El número más alto que se puede configurar debe ser menor que el número establecido en la configuración de directiva de longitud máxima del PIN o el número 127, lo que sea más bajo.|
|pinUppercaseLetters|Cadena|Valor entero que configura el uso de mayúsculas en el PIN de Windows Hello para empresas. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.|
|pinLowercaseLetters|Cadena|Valor entero que configura el uso de minúsculas en el PIN de Windows Hello para empresas. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.|
|pinSpecialCharacters|Cadena|Valor entero que configura el uso de caracteres especiales en el PIN de Windows Hello para empresas. Los caracteres especiales válidos para el PIN de Windows Hello para empresas incluyen: ! " # $ % & ' ( ) * + , - . / : ; < = > ? @ \[ \ \] ^ _ ` { | } ~. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.|
|pinExpirationDays|Int32|El valor entero especifica el período de tiempo (en días) que se puede usar un PIN antes de que el sistema solicite que el usuario lo cambie. El número más alto que puede configurar para esta configuración de directiva es 730. El número más bajo que puede configurar para esta configuración de directiva es 0. Si esta directiva se establece en 0, el PIN del usuario nunca expirará. Este nodo se agregó en Windows 10, versión 1511. El valor predeterminado es 0.|
|numberOfPastPinsRemembered|Int32|Valor entero que especifica el número de PIN anteriores que se pueden asociar a una cuenta de usuario que no se pueden volver a usar. El número más alto que puede configurar para esta configuración de directiva es 50. El número más bajo que puede configurar para esta configuración de directiva es 0. Si esta directiva se establece en 0, no es necesario almacenar los PIN antiguos. Este nodo se agregó en Windows 10, versión 1511. El valor predeterminado es 0.|
|passwordMaximumAttemptCount|Int32|El número de errores de autenticación permitidos antes de que se borre el dispositivo. Un valor de 0 deshabilita la funcionalidad de borrado del dispositivo. El intervalo es un entero X donde 4 < = X < = 16 para equipos de escritorio y 0 < = X < = 999 para dispositivos móviles.|
|minutesOfInactivityBeforeDeviceLock|Int32|Especifica la cantidad máxima de tiempo (en minutos) permitida después de que el dispositivo esté inactivo que hará que el dispositivo esté bloqueado con PIN o contraseña.   El intervalo es un entero X, donde 0 < = X < = 999.|
|daysWithoutContactBeforeUnenroll|Int32|Intervalo sin conexión antes de que se borren los datos de la aplicación (días) |

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|protectedAppLockerFiles|Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Otra forma de introducir aplicaciones protegidas por archivos XML. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|exemptAppLockerFiles|Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Otra forma de excluir aplicaciones protegidas por archivos XML. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|
|asignaciones|Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)|Propiedad de navegación a la lista de grupos de seguridad destinados a la directiva. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "enforcementLevel": "String",
  "enterpriseDomain": "String",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "String",
    "description": "String",
    "expirationDateTime": "String (timestamp)",
    "certificate": "binary"
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "String",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "String",
          "proxy": "String"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "String",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "String",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 1024,
  "pinUppercaseLetters": "String",
  "pinLowercaseLetters": "String",
  "pinSpecialCharacters": "String",
  "pinExpirationDays": 1024,
  "numberOfPastPinsRemembered": 1024,
  "passwordMaximumAttemptCount": 1024,
  "minutesOfInactivityBeforeDeviceLock": 1024,
  "daysWithoutContactBeforeUnenroll": 1024
}
```



