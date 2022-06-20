---
title: Vidinės įmonės valiutos konvertavimas
description: Šiame straipsnyje paaiškinamas vidinės įmonės operacijų valiutos konvertavimas
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851484"
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
