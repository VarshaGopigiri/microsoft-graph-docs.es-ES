---
title: tipo de recurso registryKeyState
description: Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.
localization_priority: Normal
ms.openlocfilehash: 688c690083e24dc6c8ee7229498910befd0fdf3e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804679"
---
# <a name="registrykeystate-resource-type"></a><span data-ttu-id="6fb7f-103">tipo de recurso registryKeyState</span><span class="sxs-lookup"><span data-stu-id="6fb7f-103">registryKeyState resource type</span></span>

<span data-ttu-id="6fb7f-104">Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-104">Contains information about registry key changes related to the alert, and the process that changed the registry keys.</span></span>

## <a name="properties"></a><span data-ttu-id="6fb7f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fb7f-105">Properties</span></span>

| <span data-ttu-id="6fb7f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fb7f-106">Property</span></span>     | <span data-ttu-id="6fb7f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fb7f-107">Type</span></span>        | <span data-ttu-id="6fb7f-108">Description</span><span class="sxs-lookup"><span data-stu-id="6fb7f-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6fb7f-109">subárbol</span><span class="sxs-lookup"><span data-stu-id="6fb7f-109">hive</span></span>|<span data-ttu-id="6fb7f-110">registryHive</span><span class="sxs-lookup"><span data-stu-id="6fb7f-110">registryHive</span></span>|<span data-ttu-id="6fb7f-111">Un [subárbol del registro de Windows](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives) :</span><span class="sxs-lookup"><span data-stu-id="6fb7f-111">A [Windows registry hive](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives) :</span></span> <ul><li><span data-ttu-id="6fb7f-112">HKEY_CURRENT_CONFIG</span><span class="sxs-lookup"><span data-stu-id="6fb7f-112">HKEY_CURRENT_CONFIG</span></span></li> <li><span data-ttu-id="6fb7f-113">HKEY_CURRENT_USER</span><span class="sxs-lookup"><span data-stu-id="6fb7f-113">HKEY_CURRENT_USER</span></span></li> <li><span data-ttu-id="6fb7f-114">HKEY_LOCAL_MACHINE\SAM</span><span class="sxs-lookup"><span data-stu-id="6fb7f-114">HKEY_LOCAL_MACHINE\SAM</span></span></li> <li><span data-ttu-id="6fb7f-115">HKEY_LOCAL_MACHINE\Security</span><span class="sxs-lookup"><span data-stu-id="6fb7f-115">HKEY_LOCAL_MACHINE\Security</span></span></li> <li><span data-ttu-id="6fb7f-116">HKEY_LOCAL_MACHINE\Software</span><span class="sxs-lookup"><span data-stu-id="6fb7f-116">HKEY_LOCAL_MACHINE\Software</span></span></li> <li><span data-ttu-id="6fb7f-117">HKEY_LOCAL_MACHINE\System</span><span class="sxs-lookup"><span data-stu-id="6fb7f-117">HKEY_LOCAL_MACHINE\System</span></span></li> <li><span data-ttu-id="6fb7f-118">HKEY_USERS\\. De forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-118">HKEY_USERS\\.Default.</span></span></li></ul> <span data-ttu-id="6fb7f-119">Los valores posibles son: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem` y `usersDefault`.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-119">Possible values are: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem`, `usersDefault`.</span></span>|
|<span data-ttu-id="6fb7f-120">Key</span><span class="sxs-lookup"><span data-stu-id="6fb7f-120">key</span></span>|<span data-ttu-id="6fb7f-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-121">String</span></span>|<span data-ttu-id="6fb7f-122">Clave del registro (es decir, modificado) actual (que no sean SUBÁRBOL).</span><span class="sxs-lookup"><span data-stu-id="6fb7f-122">Current (i.e. changed) registry key (excludes HIVE).</span></span>|
|<span data-ttu-id="6fb7f-123">oldKey</span><span class="sxs-lookup"><span data-stu-id="6fb7f-123">oldKey</span></span>|<span data-ttu-id="6fb7f-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-124">String</span></span>|<span data-ttu-id="6fb7f-125">Anterior (es decir, antes de cambiar) clave del registro (excluye SUBÁRBOL).</span><span class="sxs-lookup"><span data-stu-id="6fb7f-125">Previous (i.e. before changed) registry key (excludes HIVE).</span></span>|
|<span data-ttu-id="6fb7f-126">oldValueData</span><span class="sxs-lookup"><span data-stu-id="6fb7f-126">oldValueData</span></span>|<span data-ttu-id="6fb7f-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-127">String</span></span>|<span data-ttu-id="6fb7f-128">Anterior (es decir, antes de cambiar) los datos de valor de la clave del registro (contenido).</span><span class="sxs-lookup"><span data-stu-id="6fb7f-128">Previous (i.e. before changed) registry key value data (contents).</span></span>|
|<span data-ttu-id="6fb7f-129">oldValueName</span><span class="sxs-lookup"><span data-stu-id="6fb7f-129">oldValueName</span></span>|<span data-ttu-id="6fb7f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-130">String</span></span>|<span data-ttu-id="6fb7f-131">Anterior (es decir, antes de cambiar) nombre del valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-131">Previous (i.e. before changed) registry key value name.</span></span>|
|<span data-ttu-id="6fb7f-132">operación</span><span class="sxs-lookup"><span data-stu-id="6fb7f-132">operation</span></span>|<span data-ttu-id="6fb7f-133">registryOperation</span><span class="sxs-lookup"><span data-stu-id="6fb7f-133">registryOperation</span></span>|<span data-ttu-id="6fb7f-134">Operación que ha cambiado el nombre de la clave del registro o valor.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-134">Operation that changed the registry key name and/or value.</span></span> <span data-ttu-id="6fb7f-135">Los valores posibles son: `unknown`, `create`, `modify` y `delete`.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-135">Possible values are: `unknown`, `create`, `modify`, `delete`.</span></span>|
|<span data-ttu-id="6fb7f-136">processId</span><span class="sxs-lookup"><span data-stu-id="6fb7f-136">processId</span></span>|<span data-ttu-id="6fb7f-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6fb7f-137">Int32</span></span>|<span data-ttu-id="6fb7f-138">Proceso de identificador (PID) del proceso que modifica la clave del registro (proceso detalles aparecerán en la colección de procesos de alerta' ').</span><span class="sxs-lookup"><span data-stu-id="6fb7f-138">Process ID (PID) of the process that modified the registry key (process details will appear in the alert 'processes' collection).</span></span>|
|<span data-ttu-id="6fb7f-139">datosDeValor</span><span class="sxs-lookup"><span data-stu-id="6fb7f-139">valueData</span></span>|<span data-ttu-id="6fb7f-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-140">String</span></span>|<span data-ttu-id="6fb7f-141">Datos de valor de la clave de actuales del registro (es decir, modificado) (contenido).</span><span class="sxs-lookup"><span data-stu-id="6fb7f-141">Current (i.e. changed) registry key value data (contents).</span></span>|
|<span data-ttu-id="6fb7f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb7f-142">valueName</span></span>|<span data-ttu-id="6fb7f-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fb7f-143">String</span></span>|<span data-ttu-id="6fb7f-144">Nombre del valor de la clave del registro (es decir, modificado) actual</span><span class="sxs-lookup"><span data-stu-id="6fb7f-144">Current (i.e. changed) registry key value name</span></span>|
|<span data-ttu-id="6fb7f-145">tipo de valor</span><span class="sxs-lookup"><span data-stu-id="6fb7f-145">valueType</span></span>|<span data-ttu-id="6fb7f-146">registryValueType</span><span class="sxs-lookup"><span data-stu-id="6fb7f-146">registryValueType</span></span>|[<span data-ttu-id="6fb7f-147">Tipo de valor de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="6fb7f-147">Registry key value type</span></span>](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-value-types) <ul><li><span data-ttu-id="6fb7f-148">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6fb7f-148">REG_BINARY</span></span></li> <li><span data-ttu-id="6fb7f-149">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="6fb7f-149">REG_DWORD</span></span></li> <li><span data-ttu-id="6fb7f-150">REG_DWORD_LITTLE_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6fb7f-150">REG_DWORD_LITTLE_ENDIAN</span></span></li> <li><span data-ttu-id="6fb7f-151">REG_DWORD_BIG_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6fb7f-151">REG_DWORD_BIG_ENDIAN</span></span></li><li><span data-ttu-id="6fb7f-152">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="6fb7f-152">REG_EXPAND_SZ</span></span></li> <li><span data-ttu-id="6fb7f-153">REG_LINK</span><span class="sxs-lookup"><span data-stu-id="6fb7f-153">REG_LINK</span></span></li> <li><span data-ttu-id="6fb7f-154">REG_MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="6fb7f-154">REG_MULTI_SZ</span></span></li> <li><span data-ttu-id="6fb7f-155">REG_NONE</span><span class="sxs-lookup"><span data-stu-id="6fb7f-155">REG_NONE</span></span></li> <li><span data-ttu-id="6fb7f-156">REG_QWORD</span><span class="sxs-lookup"><span data-stu-id="6fb7f-156">REG_QWORD</span></span></li> <li><span data-ttu-id="6fb7f-157">REG_QWORD_LITTLE_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6fb7f-157">REG_QWORD_LITTLE_ENDIAN</span></span></li> <li><span data-ttu-id="6fb7f-158">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6fb7f-158">REG_SZ</span></span></li></ul> <span data-ttu-id="6fb7f-159">Los valores posibles son: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian` y `sz`.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-159">Possible values are: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian`, `sz`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6fb7f-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6fb7f-160">JSON representation</span></span>

<span data-ttu-id="6fb7f-161">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6fb7f-161">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.registryKeyState"
}-->

```json
{
  "hive": "@odata.type: microsoft.graph.registryHive",
  "key": "String",
  "oldKey": "String",
  "oldValueData": "String",
  "oldValueName": "String",
  "operation": "@odata.type: microsoft.graph.registryOperation",
  "processId": 1024,
  "valueData": "String",
  "valueName": "String",
  "valueType": "@odata.type: microsoft.graph.registryValueType"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "registryKeyState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
