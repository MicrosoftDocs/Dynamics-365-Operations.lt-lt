---
title: Finansinių ataskaitų dizaino įrankio ataskaitų aprašai
description: Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 073df430892e01d4842b2af147b0ae2765b1c66a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570347"
---
# <a name="report-definitions-in-financial-report-designer"></a>Finansinių ataskaitų dizaino įrankio ataskaitų aprašai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus. Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą. 

Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaitos apibrėžtis taip pat teikia papildomų parinkčių ir nuostatų, kuriuos naudodami galite tinkinti ataskaitą. Apibrėžę eilučių aprašus ir stulpelių aprašus, turite juos sujungti į ataskaitos aprašą. Šiuo metu taip pat nustatomi kiti aprašų aspektai, pavyzdžiui, išsamumo lygis ir ataskaitos data. Tada galite įrašyti ir generuoti ataskaitą. Finansinės ataskaitos siūlo tokius išsamumo lygius.

- Finansinis
- Finansinis ir Sąskaitos
- Finansinis, Sąskaitos ir Operacijos

Tačiau atsižvelgiant į tai, kaip duomenys saugomi sistemoje „Microsoft Dynamics ERP“, ataskaitose gali nebūti operacijos informacijos.

## <a name="create-a-report-definition"></a>Ataskaitos aprašo kūrimas
1. Ataskaitų konstruktoriuje, meniu **Failas**, spustelėkite **Naujas**, ir tada pasirinkite **Ataskaitos aprašas**.
2. Nurodyti atitinkamą informaciją skirtukuose **Ataskaita**, **Išeiga ir paskirstymas**, **Antraštės ir poraštės** ir **Parametrai**.

## <a name="contents-of-a-report-definition"></a>Ataskaitos aprašo turinys
Toliau pateikiamoje lentelėje aprašomi ataskaitos aprašo skirtukai ir kaip naudojama informacija.

<table>
<thead>
<tr>
<th>Tabuliavimo ženklas</th>
<th>Aprašas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ataskaita</td>
<td>Ataskaitos kūrimas, konfigūravimas arba esamos ataskaitos modifikavimas.</td>
</tr>
<tr>
<td>Išeiga ir paskirstymas</td>
<td>Pakeiskite ataskaitos išeigos tipą ir paskirties vietą.</td>
</tr>
<tr>
<td>Antraštės ir poraštės</td>
<td>Apibrėžkite ir suformatuokite ataskaitos antraštes ir poraštes. Pavyzdžiui, galite pridėti prie antraštės arba poraštės teksto arba vaizdų. Finansinės ataskaitos palaiko .bmp, .jpg ir .png vaizdų failus. Taip pat galite pridėti automatinio teksto kodų kitai informacijai įterpti pavyzdžiui, įmonės pavadinimą, ataskaitos pavadinimą arba puslapio numerį.</td>
</tr>
<tr>
<td>Parametrai</td>
<td>Nurodykite ataskaitos aprašo parametrus, pavyzdžiui, šiuos parametrus.
<ul>
<li>Formatavimas ir sumos apvalinimas</li>
<li>Informacijos ataskaitų formatas</li>
<li>Ataskaitų medžių formatas</li>
<li>Išimčių ataskaitos generavimas</li>
<li>Valiutos konvertavimo nurodymas</li>
<li>Tarpinė suma ir sąskaitos informacijos filtravimas</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]