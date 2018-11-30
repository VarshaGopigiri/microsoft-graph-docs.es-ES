---
title: Recursos compartidos en Intune de Microsoft
description: Estos extremos se usan en varias API de gráfico de Microsoft para los flujos de trabajo Intune.  La intención, el propósito y los permisos necesarios para usar un recurso determinado varía según el contexto de la llamada subyacente y el flujo de trabajo específico.  Además, determinados métodos, propiedades y acciones se admiten sólo para flujos de trabajo específicos.
ms.openlocfilehash: a0e896b2aed219679ec45804dc94b22b7cb9d727
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090567"
---
# <a name="shared-resources-in-microsoft-intune"></a><span data-ttu-id="d7b20-105">Recursos compartidos en Intune de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d7b20-105">Shared resources in Microsoft Intune</span></span>

> <span data-ttu-id="d7b20-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7b20-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7b20-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7b20-107">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d7b20-108">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d7b20-108">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="d7b20-109">Estos extremos se usan en varias API de gráfico de Microsoft para los flujos de trabajo Intune.</span><span class="sxs-lookup"><span data-stu-id="d7b20-109">These endpoints are used in multiple Microsoft Graph API for Intune workflows.</span></span>  <span data-ttu-id="d7b20-110">La intención, el propósito y los permisos necesarios para usar un recurso determinado varía según el contexto de la llamada subyacente y el flujo de trabajo específico.</span><span class="sxs-lookup"><span data-stu-id="d7b20-110">The intent, purpose, and permissions required to use a given resource varies according to the specific workflow and context of the underlying call.</span></span>  <span data-ttu-id="d7b20-111">Además, determinados métodos, propiedades y acciones se admiten sólo para flujos de trabajo específicos.</span><span class="sxs-lookup"><span data-stu-id="d7b20-111">In addition, certain methods, properties, and actions are supported only for specific workflows.</span></span>

<span data-ttu-id="d7b20-112">Los siguientes recursos de gráfico se comparten entre los flujos de trabajo Intune:</span><span class="sxs-lookup"><span data-stu-id="d7b20-112">The following Graph resources are shared between Intune workflows:</span></span>

- [<span data-ttu-id="d7b20-113">Estado de acción</span><span class="sxs-lookup"><span data-stu-id="d7b20-113">Action state</span></span>](intune-shared-actionstate.md)
- [<span data-ttu-id="d7b20-114">Destino de asignación de todos los dispositivos</span><span class="sxs-lookup"><span data-stu-id="d7b20-114">All devices assignment target</span></span>](intune-shared-alldevicesassignmenttarget.md)
- [<span data-ttu-id="d7b20-115">Destino de asignación de todos los usuarios con licencia</span><span class="sxs-lookup"><span data-stu-id="d7b20-115">All licensed users assignment target</span></span>](intune-shared-alllicensedusersassignmenttarget.md)
- [<span data-ttu-id="d7b20-116">Estado de cumplimiento de normas</span><span class="sxs-lookup"><span data-stu-id="d7b20-116">Compliance status</span></span>](intune-shared-compliancestatus.md)
- [<span data-ttu-id="d7b20-117">Destino de asignación de administración de dispositivos y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d7b20-117">Device and app management assignment target</span></span>](intune-shared-deviceandappmanagementassignmenttarget.md)
- [<span data-ttu-id="d7b20-118">Administración de aplicaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7b20-118">Device app management</span></span>](intune-shared-deviceappmanagement.md)
- [<span data-ttu-id="d7b20-119">Categoría de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7b20-119">Device category</span></span>](intune-shared-devicecategory.md)
- [<span data-ttu-id="d7b20-120">Tipo de dispositivo de inscripción</span><span class="sxs-lookup"><span data-stu-id="d7b20-120">Device enrollment type</span></span>](intune-shared-deviceenrollmenttype.md)
- [<span data-ttu-id="d7b20-121">Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d7b20-121">Device management</span></span>](intune-shared-devicemanagement.md)
- [<span data-ttu-id="d7b20-122">Tipo de plataforma de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7b20-122">Device platform type</span></span>](intune-shared-deviceplatformtype.md)
- [<span data-ttu-id="d7b20-123">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7b20-123">Device type</span></span>](intune-shared-devicetype.md)
- [<span data-ttu-id="d7b20-124">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="d7b20-124">Enablement</span></span>](intune-shared-enablement.md)
- [<span data-ttu-id="d7b20-125">Destino de asignación de grupo de exclusión</span><span class="sxs-lookup"><span data-stu-id="d7b20-125">Exclusion group assignment target</span></span>](intune-shared-exclusiongroupassignmenttarget.md)
- [<span data-ttu-id="d7b20-126">Destino de asignación de grupo</span><span class="sxs-lookup"><span data-stu-id="d7b20-126">Group assignment target</span></span>](intune-shared-groupassignmenttarget.md)
- [<span data-ttu-id="d7b20-127">Instalar la intención</span><span class="sxs-lookup"><span data-stu-id="d7b20-127">Install intent</span></span>](intune-shared-installintent.md)
- [<span data-ttu-id="d7b20-128">Intervalo IP</span><span class="sxs-lookup"><span data-stu-id="d7b20-128">IP range</span></span>](intune-shared-iprange.md)
- [<span data-ttu-id="d7b20-129">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="d7b20-129">IPv4 range</span></span>](intune-shared-ipv4range.md)
- [<span data-ttu-id="d7b20-130">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="d7b20-130">IPv6 range</span></span>](intune-shared-ipv6range.md)
- [<span data-ttu-id="d7b20-131">Par clave-valor</span><span class="sxs-lookup"><span data-stu-id="d7b20-131">Key/value pair</span></span>](intune-shared-keyvaluepair.md)
- [<span data-ttu-id="d7b20-132">Contenido MIME</span><span class="sxs-lookup"><span data-stu-id="d7b20-132">MIME content</span></span>](intune-shared-mimecontent.md)
- [<span data-ttu-id="d7b20-133">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="d7b20-133">Proxied domain</span></span>](intune-shared-proxieddomain.md)
- [<span data-ttu-id="d7b20-134">Report</span><span class="sxs-lookup"><span data-stu-id="d7b20-134">Report</span></span>](intune-shared-report.md)
- [<span data-ttu-id="d7b20-135">Raíz de informes</span><span class="sxs-lookup"><span data-stu-id="d7b20-135">Report root</span></span>](intune-shared-reportroot.md)
- [<span data-ttu-id="d7b20-136">Estado de la aplicación resultante</span><span class="sxs-lookup"><span data-stu-id="d7b20-136">Resultant app state</span></span>](intune-shared-resultantappstate.md)
- [<span data-ttu-id="d7b20-137">Color RGB</span><span class="sxs-lookup"><span data-stu-id="d7b20-137">RGB color</span></span>](intune-shared-rgbcolor.md)
- [<span data-ttu-id="d7b20-138">Ejecutar como tipo de cuenta</span><span class="sxs-lookup"><span data-stu-id="d7b20-138">Run as account type</span></span>](intune-shared-runasaccounttype.md)
- [<span data-ttu-id="d7b20-139">Estado de ejecución</span><span class="sxs-lookup"><span data-stu-id="d7b20-139">Run state</span></span>](intune-shared-runstate.md)
- [<span data-ttu-id="d7b20-140">Guarda las opciones de generación de estado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="d7b20-140">Saved UI state generation options</span></span>](intune-shared-saveduistategenerationoptions.md)
- [<span data-ttu-id="d7b20-141">URI</span><span class="sxs-lookup"><span data-stu-id="d7b20-141">URI</span></span>](intune-shared-uri.md)
- [<span data-ttu-id="d7b20-142">User</span><span class="sxs-lookup"><span data-stu-id="d7b20-142">User</span></span>](intune-shared-user.md)
- [<span data-ttu-id="d7b20-143">Tipo de símbolo (token) de cuenta VPP</span><span class="sxs-lookup"><span data-stu-id="d7b20-143">VPP token account type</span></span>](intune-shared-vpptokenaccounttype.md)
- [<span data-ttu-id="d7b20-144">Motivo del error VPP acción símbolo (token)</span><span class="sxs-lookup"><span data-stu-id="d7b20-144">VPP token action failure reason</span></span>](intune-shared-vpptokenactionfailurereason.md)
- [<span data-ttu-id="d7b20-145">Configuración de combinación de dominio de Windows</span><span class="sxs-lookup"><span data-stu-id="d7b20-145">Windows domain join configuration</span></span>](intune-shared-windowsdomainjoinconfiguration.md)
