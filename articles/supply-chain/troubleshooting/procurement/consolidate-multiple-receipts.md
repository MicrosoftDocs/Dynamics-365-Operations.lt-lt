---
title: Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą
description: Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą, jei skirtingų gavimo dokumentų eilučių apskaitos datos skiriasi.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477061"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą

## <a name="symptoms"></a>Požymiai

Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą, jei skirtingų gavimo dokumentų eilučių apskaitos datos skiriasi.

## <a name="resolution"></a>Sprendimas

Šioje situacijoje, ankstesnėse „Dynamics 365 Supply Chain Management” versijose, konsolidavimas buvo leistinas. Tačiau ši praktika yra linkusi į klaidą. Sukuriamų pirkimo užsakymo eilučių apskaitos data neturėtų skirtis nuo gavimo dokumento eilučių, kur buvo sukurtos šios pirkimo užsakymo eilutės, apskaitos datos. (Pirkimo užsakymo eilučių apskaitos data sutampa su pirkimo užsakymo antraštės apskaitos data.) Todėl kelių gavimo dokumentų konsolidavimas į vieną pirkimo užsakymą nebeleidžiamas.

Apskaitos data naudojama, pvz., biudžeto lėšų rezervavimui ir biudžeto rezervavimui. Todėl ji turi būti laikoma perėjimo iš gavimo dokumento į pirkimo užsakymą metu.
