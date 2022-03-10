---
title: 'Vadovas: Poreikio prognozės modifikavimas rankiniu būdu'
description: Šioje temoje aprašoma, kaip modifikuoti prekės prognozę
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f48e1689d21fd0085ec38aab8f5171997fbf432
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567204"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Vadovas: Poreikio prognozės modifikavimas rankiniu būdu

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip modifikuoti prekės prognozę. Ši procedūra yra skirta gamybos planuotojui.

## <a name="modify-the-forecast-for-a-selected-item"></a>Pasirinktos prekės prognozės modifikavimas

Norėdami modifikuoti pasirinktos prekės prognozę:

1. Eikite į **Moduliai \> Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Sąraše raskite ir pasirinkite norimą įrašą. Pasirinkite prekę, kurios prognozę norite modifikuoti.
1. Veiksmų srityje atidarykite skirtuką **Planuoti** ir pasirinkite **Poreikio prognozė**.
1. Iš sąrašo pasirinkite eilutę. Jei nėra prognozės eilučių, sukurkite naują eilutę veiksmų srityje pasirinkę **Nauja**.  
1. Lauke **Pardavimo kiekis** įveskite teigiamą skaičių. Šis skaičius reprezentuoja prognozuojamą prekės kiekį. Jeigu įvesite neigiamą skaičių, bus rodoma klaida.
1. Užpildykite kitus laukus taip, kaip reikia.
1. Pasirinkite **Įrašyti** veiksmų srityje.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Redaguokite prognozę vienai ar kelioms prekėms su „Microsoft Excel”

Norėdami redaguoti prognozę vienai ar kelioms prekėms su „Microsoft Excel”:

1. Atlikite vieną iš toliau nurodytų veiksmų.
    - Atidarykite puslapį **Poreikio prognozė** bet kuriai prekei (nesvarbu kuriai), kaip aprašyta ankstesniame skyriuje.
    - Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Poreikio prognozės eilutės**.
1. Veiksmų srityje pasirinkite **Atidaryti „Microsoft Office” platformoje \> Poreikio prognozės įrašai**.
1. Pasirinkite atsisiuntimo vietą, įrašykite ir atidarykite atsisiųstą failą „Excel” programoje.
1. Jeigu matote įspėjimą, pasirinkite **Įgalinti redagavimą**.
1. „Excel” programoje prisijunkite prie „Supply Chain Management” naudodami „Microsoft Dynamics” užduočių sritį. Turite prisijungti su įgalinta parinktimi **Palikti mane prisijungusį** ir turite pasitikėti duomenų ryšio programa.
1. Dabar „Excel” skaičiuoklėje rodomos visos dabartinės jūsų įmonės poreikio prognozės eilutės.  Pridėkite, naikinkite ir redaguoti poreikio prognozės eilutes taip, kaip reikia.
1. „Microsoft Dynamics” užduočių srityje pasirinkite **Publikuoti**, kad savo keitimus vėl įkeltumėte į „Supply Chain Management”.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
