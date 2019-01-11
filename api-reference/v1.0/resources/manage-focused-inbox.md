---
title: Administrar Bandeja de entrada Prioritarios
description: 'Foco de la Bandeja de entrada le permite ver los mensajes importantes en la `Focused` ficha de la Bandeja de entrada y el resto de los mensajes de la Bandeja de entrada en el `Other` ficha. El sistema de clasificación '
localization_priority: Normal
ms.openlocfilehash: b4c6ceca3248a03f814e42298c9892a1447dd2a2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826729"
---
# <a name="manage-focused-inbox"></a>Administrar Bandeja de entrada Prioritarios

La Bandeja de entrada Prioritarios permite ver mensajes importantes en la pestaña `Focused` de la Bandeja de entrada y el resto de los mensajes en la pestaña `Other`. El sistema de clasificación organiza inicialmente los mensajes de la Bandeja de entrada de manera predeterminada. Puede corregir y entrenar el sistema con el tiempo a través de la interfaz de usuario o mediante programación. Cuanto más se use, el sistema podrá deducir mejor qué mensaje entrante es importante.

A nivel de programación, la API de REST de la Bandeja de entrada Prioritarios funciona en los mensajes del usuario especificado y admite una propiedad **inferenceClassification** para cada mensaje. Los valores posibles son `Focused` y `Other`, que indican si el usuario considera ese mensaje más importante o menos importante, respectivamente. Para corregir el sistema de clasificación de un mensaje, [actualice la propiedad inferenceClassification del mensaje](../api/message-update.md). Con el tiempo, estas correcciones también entrenan al sistema de clasificación de mensajes.

La API de REST de la Bandeja de entrada Prioritarios también permite crear invalidaciones. Cada invalidación, representada por una instancia de [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md), es una instrucción para que el sistema de clasificación designe siempre los mensajes de un remitente específico de forma coherente (es decir, siempre como "Prioritarios" o siempre como "Otros"), independientemente de los enfoques aprendidos anteriormente. Puede [crear](../api/inferenceclassification-post-overrides.md), [enumerar](../api/inferenceclassification-list-overrides.md), [actualizar](../api/inferenceclassificationoverride-update.md) y [eliminar](../api/inferenceclassificationoverride-delete.md) invalidaciones para el usuario especificado. Las invalidaciones de ese usuario, si las hay, están disponibles en una propiedad de navegación **inferenceClassification**, que es una colección de instancias **inferenceClassificationOverride**. Las invalidaciones permiten al usuario tener más control sobre la clasificación de los mensajes entrantes y confiar más en el sistema de clasificación.

Tenga en cuenta que el sistema de clasificación solo aprende y aplica clasificaciones en los mensajes entrantes de la Bandeja de entrada. De manera predeterminada, los mensajes de otras carpetas son "Prioritarios". La configuración de una invalidación afecta a los futuros mensajes que lleguen a la Bandeja de entrada. La invalidación no modifica la propiedad **inferenceClassification** de los mensajes existentes en cualquier carpeta, incluida la Bandeja de entrada.

## <a name="focused-inbox-api"></a>API de la Bandeja de entrada Prioritarios

**Entrenar el sistema de clasificación de mensajes**

[Actualizar la propiedad inferenceClassification de un mensaje](../api/message-update.md)


**Uso de invalidaciones para clasificar de forma coherente según el remitente**

[Crear una invalidación para un remitente](../api/inferenceclassification-post-overrides.md) | [Enumerar todas las invalidaciones de usuario](../api/inferenceclassification-list-overrides.md) |

[Actualizar una invalidación para un remitente](../api/inferenceclassificationoverride-update.md) | [Eliminar una invalidación de remitente](../api/inferenceclassificationoverride-delete.md) 
