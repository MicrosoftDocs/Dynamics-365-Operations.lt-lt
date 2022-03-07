---
title: Vidinės įmonės valiutos konvertavimas
description: Šioje temoje paaiškinamas vidinės įmonės operacijų valiutos konvertavimas
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548433"
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
