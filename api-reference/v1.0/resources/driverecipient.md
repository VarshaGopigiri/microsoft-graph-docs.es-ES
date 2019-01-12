---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveRecipient
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: bd1b4466a361af031b9c8e11be63acb46044351a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983383"
---
# <a name="driverecipient-resource"></a><span data-ttu-id="0c6d1-102">Recurso DriveRecipient</span><span class="sxs-lookup"><span data-stu-id="0c6d1-102">DriveRecipient resource</span></span>

<span data-ttu-id="0c6d1-103">El recurso **DriveRecipient** representa una persona, grupo u otro destinatario con el que se va a compartir mediante el uso de la acción [invite](../api/driveitem-invite.md).</span><span class="sxs-lookup"><span data-stu-id="0c6d1-103">The **DriveRecipient** resource represents a person, group, or other recipient to share with using the [invite](../api/driveitem-invite.md) action.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0c6d1-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c6d1-104">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="0c6d1-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c6d1-105">Properties</span></span>
<span data-ttu-id="0c6d1-106">El recurso recipients tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c6d1-106">The recipients resource has these properties.</span></span>

| <span data-ttu-id="0c6d1-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="0c6d1-107">Property name</span></span> | <span data-ttu-id="0c6d1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c6d1-108">Type</span></span>   | <span data-ttu-id="0c6d1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c6d1-109">Description</span></span>                                                                                             |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6d1-110">email</span><span class="sxs-lookup"><span data-stu-id="0c6d1-110">email</span></span>         | <span data-ttu-id="0c6d1-111">String</span><span class="sxs-lookup"><span data-stu-id="0c6d1-111">String</span></span> | <span data-ttu-id="0c6d1-112">Dirección de correo del destinatario, si este tiene una dirección de correo asociada.</span><span class="sxs-lookup"><span data-stu-id="0c6d1-112">The email address for the recipient, if the recipient has an associated email address.</span></span>                  |
| <span data-ttu-id="0c6d1-113">alias</span><span class="sxs-lookup"><span data-stu-id="0c6d1-113">alias</span></span>         | <span data-ttu-id="0c6d1-114">String</span><span class="sxs-lookup"><span data-stu-id="0c6d1-114">String</span></span> | <span data-ttu-id="0c6d1-115">Alias del objeto de dominio, para los casos en que una dirección de correo no está disponible (por ejemplo, los grupos de seguridad).</span><span class="sxs-lookup"><span data-stu-id="0c6d1-115">The alias of the domain object, for cases where an email address is unavailable (e.g. security groups).</span></span> |
| <span data-ttu-id="0c6d1-116">objectId</span><span class="sxs-lookup"><span data-stu-id="0c6d1-116">objectId</span></span>      | <span data-ttu-id="0c6d1-117">String</span><span class="sxs-lookup"><span data-stu-id="0c6d1-117">String</span></span> | <span data-ttu-id="0c6d1-118">Identificador único del destinatario en el directorio.</span><span class="sxs-lookup"><span data-stu-id="0c6d1-118">The unique identifier for the recipient in the directory.</span></span>                                               |

## <a name="remarks"></a><span data-ttu-id="0c6d1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c6d1-119">Remarks</span></span>

<span data-ttu-id="0c6d1-p101">Si se usa [invite](../api/driveitem-invite.md) para agregar permisos, el objeto DriveRecipient puede especificar **email**, **alias** u **objectId**. Solo se requiere uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0c6d1-p101">When using [invite](../api/driveitem-invite.md) to add permissions, the DriveRecipient can specify **email**, **alias**, or **objectId**. Only one of these values is required.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients"
} -->
