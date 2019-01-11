---
title: Recursos compartidos en Intune de Microsoft
description: Estos extremos se usan en varias API de gráfico de Microsoft para los flujos de trabajo Intune.  La intención, el propósito y los permisos necesarios para usar un recurso determinado varía según el contexto de la llamada subyacente y el flujo de trabajo específico.  Además, determinados métodos, propiedades y acciones se admiten sólo para flujos de trabajo específicos.
localization_priority: Normal
ms.openlocfilehash: d0d615be8d185c5dfe24d58f6a2e371e6baf18c9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840071"
---
# <a name="shared-resources-in-microsoft-intune"></a><span data-ttu-id="54e11-105">Recursos compartidos en Intune de Microsoft</span><span class="sxs-lookup"><span data-stu-id="54e11-105">Shared resources in Microsoft Intune</span></span>

> <span data-ttu-id="54e11-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54e11-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="54e11-107">Estos extremos se usan en varias API de gráfico de Microsoft para los flujos de trabajo Intune.</span><span class="sxs-lookup"><span data-stu-id="54e11-107">These endpoints are used in multiple Microsoft Graph API for Intune workflows.</span></span>  <span data-ttu-id="54e11-108">La intención, el propósito y los permisos necesarios para usar un recurso determinado varía según el contexto de la llamada subyacente y el flujo de trabajo específico.</span><span class="sxs-lookup"><span data-stu-id="54e11-108">The intent, purpose, and permissions required to use a given resource varies according to the specific workflow and context of the underlying call.</span></span>  <span data-ttu-id="54e11-109">Además, determinados métodos, propiedades y acciones se admiten sólo para flujos de trabajo específicos.</span><span class="sxs-lookup"><span data-stu-id="54e11-109">In addition, certain methods, properties, and actions are supported only for specific workflows.</span></span>

<span data-ttu-id="54e11-110">Los siguientes recursos de gráfico se comparten entre los flujos de trabajo Intune:</span><span class="sxs-lookup"><span data-stu-id="54e11-110">The following Graph resources are shared between Intune workflows:</span></span>  

- [<span data-ttu-id="54e11-111">Destino de asignación de todos los dispositivos</span><span class="sxs-lookup"><span data-stu-id="54e11-111">All devices assignment target</span></span>](intune-shared-alldevicesassignmenttarget.md)
- [<span data-ttu-id="54e11-112">Destino de asignación de todos los usuarios con licencia</span><span class="sxs-lookup"><span data-stu-id="54e11-112">All licensed users assignment target</span></span>](intune-shared-alllicensedusersassignmenttarget.md)
- [<span data-ttu-id="54e11-113">Estado de cumplimiento de normas</span><span class="sxs-lookup"><span data-stu-id="54e11-113">Compliance status</span></span>](intune-shared-compliancestatus.md)
- [<span data-ttu-id="54e11-114">Destino de asignación de administración de dispositivos y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="54e11-114">Device and app management assignment target</span></span>](intune-shared-deviceandappmanagementassignmenttarget.md)
- [<span data-ttu-id="54e11-115">Administración de aplicaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54e11-115">Device app management</span></span>](intune-shared-deviceappmanagement.md)
- [<span data-ttu-id="54e11-116">Categoría de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54e11-116">Device category</span></span>](intune-shared-devicecategory.md)
- [<span data-ttu-id="54e11-117">Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="54e11-117">Device management</span></span>](intune-shared-devicemanagement.md)
- [<span data-ttu-id="54e11-118">Destino de asignación de grupo de exclusión</span><span class="sxs-lookup"><span data-stu-id="54e11-118">Exclusion group assignment target</span></span>](intune-shared-exclusiongroupassignmenttarget.md)
- [<span data-ttu-id="54e11-119">Destino de asignación de grupo</span><span class="sxs-lookup"><span data-stu-id="54e11-119">Group assignment target</span></span>](intune-shared-groupassignmenttarget.md)
- [<span data-ttu-id="54e11-120">Instalar la intención</span><span class="sxs-lookup"><span data-stu-id="54e11-120">Install intent</span></span>](intune-shared-installintent.md)
- [<span data-ttu-id="54e11-121">Contenido MIME</span><span class="sxs-lookup"><span data-stu-id="54e11-121">MIME content</span></span>](intune-shared-mimecontent.md)
- [<span data-ttu-id="54e11-122">Report</span><span class="sxs-lookup"><span data-stu-id="54e11-122">Report</span></span>](intune-shared-report.md)
- [<span data-ttu-id="54e11-123">Raíz de informes</span><span class="sxs-lookup"><span data-stu-id="54e11-123">Report root</span></span>](intune-shared-reportroot.md)
- [<span data-ttu-id="54e11-124">Guarda las opciones de generación de estado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="54e11-124">Saved UI state generation options</span></span>](intune-shared-saveduistategenerationoptions.md)
- [<span data-ttu-id="54e11-125">URI</span><span class="sxs-lookup"><span data-stu-id="54e11-125">URI</span></span>](intune-shared-uri.md)
- [<span data-ttu-id="54e11-126">Usuario</span><span class="sxs-lookup"><span data-stu-id="54e11-126">User</span></span>](intune-shared-user.md)
- [<span data-ttu-id="54e11-127">Tipo de símbolo (token) de cuenta VPP</span><span class="sxs-lookup"><span data-stu-id="54e11-127">VPP token account type</span></span>](intune-shared-vpptokenaccounttype.md)
