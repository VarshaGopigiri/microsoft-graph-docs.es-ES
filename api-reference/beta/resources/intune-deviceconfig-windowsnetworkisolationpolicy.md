---
title: tipo de recurso windowsNetworkIsolationPolicy
description: Directiva de aislamiento de red de Windows
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 82026ba4d82b85a0275f83bb729b495e17ff5d5c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834618"
---
# <a name="windowsnetworkisolationpolicy-resource-type"></a>tipo de recurso windowsNetworkIsolationPolicy

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva de aislamiento de red de Windows
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|enterpriseNetworkDomainNames|Colección String|Esta es la lista de dominios que forman parte de los límites de la empresa. Datos de uno de estos dominios que se envía a un dispositivo que se consideran datos de la empresa y protegidas. Estas ubicaciones se considerarán un destino para los datos de la empresa para compartirse a seguros.|
|enterpriseCloudResources|Colección [proxiedDomain](../resources/intune-shared-proxieddomain.md)|Contiene una lista de dominios de recursos de empresa hospedadas en la nube que deben estar protegidos. Las conexiones a estos recursos se consideran datos empresariales. Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80). Un servidor proxy utilizado para este propósito también debe configurarse con la directiva de EnterpriseInternalProxyServers. Esta colección puede contener un máximo de 500 elementos.|
|enterpriseIPRanges|Colección [ipRange](../resources/intune-shared-iprange.md)|Establece los intervalos IP empresariales que definen los equipos de la red empresarial. Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos. Estas ubicaciones se considerarán un destino para los datos de la empresa para compartirse a seguros. Esta colección puede contener un máximo de 500 elementos.|
|enterpriseInternalProxyServers|Colección String|Se trata de la lista de valores separados por comas de servidores proxy internos. Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59". El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet. Se consideran ubicaciones de red empresarial. Los servidores proxy se aprovechan sólo en la configuración de la directiva EnterpriseCloudResources para forzar que el tráfico a los recursos de la nube coincidente a través de estos servidores proxy.|
|enterpriseIPRangesAreAuthoritative|Booleano|Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes. Valor predeterminado es false.|
|enterpriseProxyServers|Colección String|Esta es una lista de servidores proxy. Cualquier servidor no en esta lista se considera que no sea de empresa.|
|enterpriseProxyServersAreAuthoritative|Booleano|Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo. El valor predeterminado es False.|
|neutralDomainResources|Colección String|Lista de nombres de dominio que puede usar para el recurso de trabajo o personal.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsNetworkIsolationPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsNetworkIsolationPolicy",
  "enterpriseNetworkDomainNames": [
    "String"
  ],
  "enterpriseCloudResources": [
    {
      "@odata.type": "microsoft.graph.proxiedDomain",
      "ipAddressOrFQDN": "String",
      "proxy": "String"
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "enterpriseInternalProxyServers": [
    "String"
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    "String"
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    "String"
  ]
}
```





