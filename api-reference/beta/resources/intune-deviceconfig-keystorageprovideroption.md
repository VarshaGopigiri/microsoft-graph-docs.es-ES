---
title: tipo de enumeración keyStorageProviderOption
description: Opciones de importación de almacenamiento de claves (KSP) del proveedor.
author: tfitzmac
ms.openlocfilehash: 7923dd5c4b8a09d834d29b65928430828f3dafac
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342220"
---
# <a name="keystorageprovideroption-enum-type"></a><span data-ttu-id="35965-103">tipo de enumeración keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="35965-103">keyStorageProviderOption enum type</span></span>

> <span data-ttu-id="35965-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35965-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35965-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35965-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="35965-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35965-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35965-107">Opciones de importación de almacenamiento de claves (KSP) del proveedor.</span><span class="sxs-lookup"><span data-stu-id="35965-107">Key Storage Provider (KSP) Import Options.</span></span>
## <a name="members"></a><span data-ttu-id="35965-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="35965-108">Members</span></span>
|<span data-ttu-id="35965-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="35965-109">Member</span></span>|<span data-ttu-id="35965-110">Valor</span><span class="sxs-lookup"><span data-stu-id="35965-110">Value</span></span>|<span data-ttu-id="35965-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="35965-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35965-112">useTpmKspOtherwiseUseSoftwareKsp</span><span class="sxs-lookup"><span data-stu-id="35965-112">useTpmKspOtherwiseUseSoftwareKsp</span></span>|<span data-ttu-id="35965-113">0</span><span class="sxs-lookup"><span data-stu-id="35965-113">0</span></span>|<span data-ttu-id="35965-114">Importar a Trusted Platform Module (TPM) KSP si está presente, en caso contrario, importar a Software KSP.</span><span class="sxs-lookup"><span data-stu-id="35965-114">Import to Trusted Platform Module (TPM) KSP if present, otherwise import to Software KSP.</span></span>|
|<span data-ttu-id="35965-115">useTpmKspOtherwiseFail</span><span class="sxs-lookup"><span data-stu-id="35965-115">useTpmKspOtherwiseFail</span></span>|<span data-ttu-id="35965-116">1</span><span class="sxs-lookup"><span data-stu-id="35965-116">1</span></span>|<span data-ttu-id="35965-117">En caso contrario, producirá un error en la importación a Trusted Platform Module (TPM) KSP si está presente.</span><span class="sxs-lookup"><span data-stu-id="35965-117">Import to Trusted Platform Module (TPM) KSP if present, otherwise fail.</span></span>|
|<span data-ttu-id="35965-118">usePassportForWorkKspOtherwiseFail</span><span class="sxs-lookup"><span data-stu-id="35965-118">usePassportForWorkKspOtherwiseFail</span></span>|<span data-ttu-id="35965-119">2</span><span class="sxs-lookup"><span data-stu-id="35965-119">2</span></span>|<span data-ttu-id="35965-120">Importar a la cuenta de Passport para el trabajo KSP si está disponible, en caso contrario, producirá un error.</span><span class="sxs-lookup"><span data-stu-id="35965-120">Import to Passport for work KSP if available, otherwise fail.</span></span>|
|<span data-ttu-id="35965-121">useSoftwareKsp</span><span class="sxs-lookup"><span data-stu-id="35965-121">useSoftwareKsp</span></span>|<span data-ttu-id="35965-122">3</span><span class="sxs-lookup"><span data-stu-id="35965-122">3</span></span>|<span data-ttu-id="35965-123">Importación a Software KSP.</span><span class="sxs-lookup"><span data-stu-id="35965-123">Import to Software KSP.</span></span>|





