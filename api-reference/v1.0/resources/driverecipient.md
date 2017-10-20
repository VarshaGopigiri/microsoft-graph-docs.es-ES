---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveRecipient
ms.openlocfilehash: 53f6a5559cb90142a88b839a996cb2eedfd1037a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="driverecipient-resource"></a><span data-ttu-id="db275-102">Recurso DriveRecipient</span><span class="sxs-lookup"><span data-stu-id="db275-102">DriveRecipient resource type</span></span>

<span data-ttu-id="db275-103">El recurso **DriveRecipient** representa una persona, grupo u otro destinatario con el que se va a compartir mediante el uso de la acción [invite](../api/driveitem_invite.md).</span><span class="sxs-lookup"><span data-stu-id="db275-103">The **DriveRecipient** resource represents a person, group, or other recipient to share with using the [invite](../api/driveitem_invite.md) action.</span></span>

## <a name="json-representation"></a><span data-ttu-id="db275-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="db275-104">JSON representation</span></span>

<!-- { 
  "blockType": "resource", 
  "@odata.type": "microsoft.graph.driveRecipient", 
  "optionalProperties": ["alias", "objectId", "email"] } -->
```json
{
  "email": "string",
  "alias": "string",
  "objectId": "string",
}
```

## <a name="properties"></a><span data-ttu-id="db275-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db275-105">Properties</span></span>
<span data-ttu-id="db275-106">El recurso recipients tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="db275-106">The recipients resource has these properties.</span></span>

| <span data-ttu-id="db275-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="db275-107">Property name</span></span> | <span data-ttu-id="db275-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="db275-108">Type</span></span>   | <span data-ttu-id="db275-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="db275-109">Description</span></span>                                                                                             |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db275-110">email</span><span class="sxs-lookup"><span data-stu-id="db275-110">email</span></span>         | <span data-ttu-id="db275-111">String</span><span class="sxs-lookup"><span data-stu-id="db275-111">String</span></span> | <span data-ttu-id="db275-112">Dirección de correo del destinatario, si este tiene una dirección de correo asociada.</span><span class="sxs-lookup"><span data-stu-id="db275-112">The email address for the recipient, if the recipient has an associated email address.</span></span>                  |
| <span data-ttu-id="db275-113">alias</span><span class="sxs-lookup"><span data-stu-id="db275-113">alias</span></span>         | <span data-ttu-id="db275-114">String</span><span class="sxs-lookup"><span data-stu-id="db275-114">String</span></span> | <span data-ttu-id="db275-115">Alias del objeto de dominio, para los casos en que una dirección de correo no está disponible (por ejemplo, los grupos de seguridad).</span><span class="sxs-lookup"><span data-stu-id="db275-115">The alias of the domain object, for cases where an email address is unavailable (e.g. security groups).</span></span> |
| <span data-ttu-id="db275-116">objectId</span><span class="sxs-lookup"><span data-stu-id="db275-116">objectId</span></span>      | <span data-ttu-id="db275-117">String</span><span class="sxs-lookup"><span data-stu-id="db275-117">String</span></span> | <span data-ttu-id="db275-118">Identificador único del destinatario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="db275-118">The unique identifier for the recipient in the directory.</span></span>                                               |

## <a name="remarks"></a><span data-ttu-id="db275-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db275-119">Remarks</span></span>

<span data-ttu-id="db275-120">Si se usa [invite](../api/driveitem_invite.md) para agregar permisos, el objeto DriveRecipient puede especificar **email**, **alias** u **objectId**.</span><span class="sxs-lookup"><span data-stu-id="db275-120">When using invite to add permissions, the DriveRecipient can specify email, alias, or objectId. Only one of these values is required.</span></span>
<span data-ttu-id="db275-121">Solo se requiere uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="db275-121">Only one of these values is required.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients"
} -->
