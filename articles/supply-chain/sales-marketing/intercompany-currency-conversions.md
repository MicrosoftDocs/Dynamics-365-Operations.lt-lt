---
title: Vidinės įmonės valiutos konvertavimas
description: Šioje temoje paaiškinamas vidinės įmonės operacijų valiutos konvertavimas
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671904"
---
# <a name="intercompany-currency-conversions"></a>Vidinės įmonės valiutos konvertavimas

[!include [banner](../../includes/banner.md)]

Kai skiriasi pradinio pardavimo užsakymo ir vidinės įmonės pirkimo užsakymo valiutos kodas, toliau pateikti laukai konvertuojami valiuta, jei įgalintas sinchronizavimas:

- **Vnt. kaina**
- **Pirkimo pardavimo** arba **išlaidos už pirkimus**
- **Nuolaida**
- **Kelių eilučių nuolaida**

Šie laukai yra sinchronizuoti pagal pradinio vidinės įmonės pardavimo užsakymo eilutes.

Tačiau kadangi vidinės įmonės pirkimo užsakymo ir vidinės įmonės pardavimo užsakymo valiuta yra visada sinchronizuojama, šie laukai sinchronizuojami be valiutos konversijos:

- **Vnt. kaina**
- **Pirkimo pardavimo** arba **išlaidos už pirkimus**
- **Nuolaida**
- **Nuolaidos procentas**
- **Kelių eilučių nuolaida**
- **Kelių eilučių nuolaidos procentas**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
