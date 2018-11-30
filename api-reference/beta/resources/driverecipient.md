---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveRecipient
ms.openlocfilehash: c658b45ad2e99fc447459e80bfca12c29029f5b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087574"
---
# <a name="driverecipient-resource"></a><span data-ttu-id="2497b-102">Recurso DriveRecipient</span><span class="sxs-lookup"><span data-stu-id="2497b-102">DriveRecipient resource</span></span>

> <span data-ttu-id="2497b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2497b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2497b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2497b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2497b-105">El recurso **DriveRecipient** representa una persona, grupo u otro destinatario con el que se va a compartir mediante el uso de la acción [invite](../api/driveitem-invite.md).</span><span class="sxs-lookup"><span data-stu-id="2497b-105">The **DriveRecipient** resource represents a person, group, or other recipient to share with using the [invite](../api/driveitem-invite.md) action.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2497b-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2497b-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="2497b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2497b-107">Properties</span></span>
<span data-ttu-id="2497b-108">El recurso recipients tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2497b-108">The recipients resource has these properties.</span></span>

| <span data-ttu-id="2497b-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="2497b-109">Property name</span></span> | <span data-ttu-id="2497b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2497b-110">Type</span></span>   | <span data-ttu-id="2497b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2497b-111">Description</span></span>                                                                                             |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2497b-112">email</span><span class="sxs-lookup"><span data-stu-id="2497b-112">email</span></span>         | <span data-ttu-id="2497b-113">String</span><span class="sxs-lookup"><span data-stu-id="2497b-113">String</span></span> | <span data-ttu-id="2497b-114">Dirección de correo del destinatario, si este tiene una dirección de correo asociada.</span><span class="sxs-lookup"><span data-stu-id="2497b-114">The email address for the recipient, if the recipient has an associated email address.</span></span>                  |
| <span data-ttu-id="2497b-115">alias</span><span class="sxs-lookup"><span data-stu-id="2497b-115">alias</span></span>         | <span data-ttu-id="2497b-116">String</span><span class="sxs-lookup"><span data-stu-id="2497b-116">String</span></span> | <span data-ttu-id="2497b-117">Alias del objeto de dominio, para los casos en que una dirección de correo no está disponible (por ejemplo, los grupos de seguridad).</span><span class="sxs-lookup"><span data-stu-id="2497b-117">The alias of the domain object, for cases where an email address is unavailable (e.g. security groups).</span></span> |
| <span data-ttu-id="2497b-118">objectId</span><span class="sxs-lookup"><span data-stu-id="2497b-118">objectId</span></span>      | <span data-ttu-id="2497b-119">String</span><span class="sxs-lookup"><span data-stu-id="2497b-119">String</span></span> | <span data-ttu-id="2497b-120">Identificador único del destinatario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="2497b-120">The unique identifier for the recipient in the directory.</span></span>                                               |

## <a name="remarks"></a><span data-ttu-id="2497b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2497b-121">Remarks</span></span>

<span data-ttu-id="2497b-p102">Si se usa [invite](../api/driveitem-invite.md) para agregar permisos, el objeto DriveRecipient puede especificar **email**, **alias** u **objectId**. Solo se requiere uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2497b-p102">When using [invite](../api/driveitem-invite.md) to add permissions, the DriveRecipient can specify **email**, **alias**, or **objectId**. Only one of these values is required.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients"
} -->
