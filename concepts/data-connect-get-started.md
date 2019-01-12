---
title: Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)
description: 'Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM). '
author: ajacks-msft
localization_priority: Priority
ms.prod: data-connect
ms.openlocfilehash: f7426147908a2ded298bee065c05afffc182cd4b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914447"
---
# <a name="get-started-with-microsoft-graph-data-connect-preview"></a><span data-ttu-id="79286-103">Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="79286-103">Get started with Microsoft Graph data connect (preview)</span></span>

<span data-ttu-id="79286-104">Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM).</span><span class="sxs-lookup"><span data-stu-id="79286-104">Before you can use Microsoft Graph data connect, an Office 365 administrator must take two actions, both of which enable the ability for the admin to control data movement through Privileged Access Management (PAM).</span></span> 

1. <span data-ttu-id="79286-105">Conceder permisos para participar en la conexión a los datos de Microsoft Graph a través del Portal de administración de Microsoft 365, en la página**Servicios y complementos**.</span><span class="sxs-lookup"><span data-stu-id="79286-105">Give consent to opt in to Microsoft Graph data connect through the Microsoft 365 Admin Portal, on the **Services & add-ins** page.</span></span> <span data-ttu-id="79286-106">Esto permitirá las solicitudes de movimiento de datos a Microsoft Azure (esto es, mantener pleno control sobre los datos, pero permitir que los recursos de Azure accedan a ellos).</span><span class="sxs-lookup"><span data-stu-id="79286-106">This will allow data movement requests to Microsoft Azure (that is, keep full control over the data, but allow Azure resources to access it).</span></span> <span data-ttu-id="79286-107">No se transferirán datos a menos que se conceda la aprobación de una canalización específica más adelante.</span><span class="sxs-lookup"><span data-stu-id="79286-107">No data is transferred unless approval for a specific pipeline is provided later.</span></span>
2. <span data-ttu-id="79286-108">Establecer un grupo aprobador dentro de la suscripción de Office 365.</span><span class="sxs-lookup"><span data-stu-id="79286-108">Set an approver group within the Office 365 subscription.</span></span> <span data-ttu-id="79286-109">Asegúrese de que el grupo aprobador no esté vacío.</span><span class="sxs-lookup"><span data-stu-id="79286-109">Make sure that the approver group is not empty.</span></span> <span data-ttu-id="79286-110">Solo los usuarios del grupo pueden aprobar solicitudes de movimiento de datos.</span><span class="sxs-lookup"><span data-stu-id="79286-110">Only the users in the group can approve data movement requests.</span></span>

<span data-ttu-id="79286-111">Para obtener instrucciones detalladas, consulte el [módulo de formación de conexión a los datos de Microsoft Graph](https://github.com/microsoftgraph/msgraph-training-dataconnect/blob/master/Lab.md).</span><span class="sxs-lookup"><span data-stu-id="79286-111">For detailed step-by-step instructions, see the [Microsoft Graph data connect training module](https://github.com/microsoftgraph/msgraph-training-dataconnect/blob/master/Lab.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="79286-112">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="79286-112">Next steps</span></span>

<span data-ttu-id="79286-113">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="79286-113">Congratulations!</span></span> <span data-ttu-id="79286-114">Ya puede empezar a crear aplicaciones inteligentes con herramientas de Azure.</span><span class="sxs-lookup"><span data-stu-id="79286-114">You're now ready to start building intelligent applications with Azure tooling.</span></span> <span data-ttu-id="79286-115">Para una aplicación de ejemplo y documentación adicional, consulte el [repositorio de GitHub de conexión a los datos de Microsoft Graph](https://github.com/OfficeDev/MS-Graph-Data-Connect/wiki).</span><span class="sxs-lookup"><span data-stu-id="79286-115">For a sample application and additional documentation, see the [Microsoft Graph data connect GitHub repo](https://github.com/OfficeDev/MS-Graph-Data-Connect/wiki).</span></span> 
