---
title: Registravimasis paėmimo moduliui
description: Ši tema paaiškina prisiregistravimo paėmimui modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f6359f41f3b97325db4fda083dc32d39839811297a96a1f2d99a93990c00afae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747470"
---
# <a name="check-in-for-pickup-module"></a>Registravimasis paėmimo moduliui

[!include [banner](includes/banner.md)]

Ši tema paaiškina prisiregistravimo paėmimui modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

Įsiregistravimo paėmimo modulyje pateikiamas patvirtinimo puslapis klientams, kurie naudoja klientų įsiregistravimo galimybę „Dynamics 365 Commerce“ pranešti parduotuvei apie atvykimą. Įregistravimas paėmimo moduliui taip pat leidžia konfigūruoti formą, kuri renka papildomą klientų informaciją ir palengvina užsakymo pristatymą. Ši informacija apima kliento automobilio stovėjimo vietos numerį, jų transporto priemonės gamintojas ir modelis. 

## <a name="module-properties"></a>Modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Patvirtinimo tekstas | Teksto eilutė | Antraštės turinys, rodomas įregistravimo patvirtinimo puslapyje. |
| Rodyti QR kodą | **Teisinga** arba **Klaidinga** | Kai ši ypatybė nustatyta kaip **Teisinga**, įregistravimo patvirtinimo puslapyje rodomas QR kodas, nurodantis užsakymo patvirtinimo ID. |
| Papildomos informacijos antraštė | Teksto eilutė | Antraštės turinys, rodomas sukonfigūrus papildomos informacijos laukus. |
| Papildomos informacijos raktai | Išteklių ID / išteklių reikšmės pora | Kiekvienas raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją. |
| Papildomų informacijos raktų \> išteklių ID | Teksto eilutė | Kiekvienas informacijos raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją. Ši ypatybė nurodo papildomos informacijos raktą. Sukūrus užduotį kasos punkte (EKA), šios ypatybės vertė rodoma kaip etiketė instrukcijų lauke. |
| Papildomų informacijos raktų \> išteklių vertė | Teksto eilutė | EKA užduoties teksto lauko žymė. |
| Papildomų informacijos raktų \> būtini | **Teisinga** arba **Klaidinga** | Ši ypatybė nurodo, ar klientai turi užpildyti formos lauką, kad galėtų tęsti. Kai ši ypatybė nustatyta kaip Teisinga, žvaigždutė atvaizduota šalia formos žymos, o atliktas nulinis patikrinimas, siekiant neleisti klientams tęsti, jei neįvedami **jokia** vertė. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Įtraukti paėmimo modulio įregistravimą į puslapį

Paėmimo modulio registravimas turi būti pridėtas prie naujo puslapio, kurį sukuriate patvirtinti registravimas. Šis puslapis bus naudojamas kaip klientų, kurie pasirenka mano čia esantį saitą ar mygtuką savo el. **laiške**, įregistravimo patvirtinimo patirtis. 

## <a name="configure-the-additional-information-form"></a>Konfigūruoti papildomos informacijos formą

Pagal numatytuosius nustatymus, jei nėra sukonfigūruotų papildomų informacijos raktų, modulis rodo klientams įregistravimo patvirtinimo puslapį. Kai rodomas įregistravimo patvirtinimas, EKA sukuriama parduotuvės, kurioje išrinktas užsakymas, užduotis.

Sukonfigūrus vieną ar daugiau papildomų informacijos raktų, klientai pirmiausia paraginamas įvesti informaciją. Kai **pasirenkate** Pateikti, jiems rodomas įregistravimo patvirtinimas, o užduotis sukuriama EKA. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)](enable-customer-check-in.md)
