---
title: tipo de recurso iosWebContentFilterSpecificWebsitesAccess
description: Representa un tipo de configuración de filtro de contenido Web, que instala marcadores de dirección URL en el explorador integrado de iOS iOS. Un escenario de ejemplo se encuentra en el aula donde los profesores gustaría a los alumnos para navegar por los sitios Web a través de marcadores de explorador configurados en sus dispositivos iOS y no hay acceso a otros sitios.
ms.openlocfilehash: c5e23905ab9e5b692500544161fc052dd606da5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087439"
---
# <a name="ioswebcontentfilterspecificwebsitesaccess-resource-type"></a><span data-ttu-id="e8deb-104">tipo de recurso iosWebContentFilterSpecificWebsitesAccess</span><span class="sxs-lookup"><span data-stu-id="e8deb-104">iosWebContentFilterSpecificWebsitesAccess resource type</span></span>

> <span data-ttu-id="e8deb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8deb-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8deb-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8deb-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e8deb-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8deb-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8deb-108">Representa un tipo de configuración de filtro de contenido Web, que instala marcadores de dirección URL en el explorador integrado de iOS iOS.</span><span class="sxs-lookup"><span data-stu-id="e8deb-108">Represents an iOS Web Content Filter setting type, which installs URL bookmarks into iOS built-in browser.</span></span> <span data-ttu-id="e8deb-109">Un escenario de ejemplo se encuentra en el aula donde los profesores gustaría a los alumnos para navegar por los sitios Web a través de marcadores de explorador configurados en sus dispositivos iOS y no hay acceso a otros sitios.</span><span class="sxs-lookup"><span data-stu-id="e8deb-109">An example scenario is in the classroom where teachers would like the students to navigate websites through browser bookmarks configured on their iOS devices, and no access to other sites.</span></span>

<span data-ttu-id="e8deb-110">Hereda de [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span><span class="sxs-lookup"><span data-stu-id="e8deb-110">Inherits from [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e8deb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8deb-111">Properties</span></span>
|<span data-ttu-id="e8deb-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8deb-112">Property</span></span>|<span data-ttu-id="e8deb-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8deb-113">Type</span></span>|<span data-ttu-id="e8deb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8deb-114">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e8deb-115">specificWebsitesOnly</span><span class="sxs-lookup"><span data-stu-id="e8deb-115">specificWebsitesOnly</span></span>|<span data-ttu-id="e8deb-116">colección de [iosBookmark](../resources/intune-deviceconfig-iosbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="e8deb-116">[iosBookmark](../resources/intune-deviceconfig-iosbookmark.md) collection</span></span>|<span data-ttu-id="e8deb-117">Marcadores de dirección URL que se va a instalar en el explorador integrado y el usuario sólo se permite tener acceso a sitios Web a través de marcadores.</span><span class="sxs-lookup"><span data-stu-id="e8deb-117">URL bookmarks which will be installed into built-in browser and user is only allowed to access websites through bookmarks.</span></span> <span data-ttu-id="e8deb-118">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="e8deb-118">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="e8deb-119">websiteList</span><span class="sxs-lookup"><span data-stu-id="e8deb-119">websiteList</span></span>|<span data-ttu-id="e8deb-120">colección de [iosBookmark](../resources/intune-deviceconfig-iosbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="e8deb-120">[iosBookmark](../resources/intune-deviceconfig-iosbookmark.md) collection</span></span>|<span data-ttu-id="e8deb-121">Marcadores de dirección URL que se va a instalar en el explorador integrado y el usuario sólo se permite tener acceso a sitios Web a través de marcadores.</span><span class="sxs-lookup"><span data-stu-id="e8deb-121">URL bookmarks which will be installed into built-in browser and user is only allowed to access websites through bookmarks.</span></span> <span data-ttu-id="e8deb-122">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="e8deb-122">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e8deb-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e8deb-123">Relationships</span></span>
<span data-ttu-id="e8deb-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e8deb-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e8deb-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e8deb-125">JSON Representation</span></span>
<span data-ttu-id="e8deb-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e8deb-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
  "specificWebsitesOnly": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ],
  "websiteList": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ]
}
```





