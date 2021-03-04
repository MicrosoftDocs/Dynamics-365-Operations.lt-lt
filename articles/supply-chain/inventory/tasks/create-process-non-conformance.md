---
title: Atitikimo kūrimas ir apdorojimas
description: Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433857"
---
# <a name="create-and-process-a-conformance"></a>Atitikimo kūrimas ir apdorojimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu. Galite paleisti šį įrašą naudodami USMF demonstracinę įmonę ir galite naudoti siūlomas vertes. Paprastai šią procedūrą atlieka kokybės klerkas.  Reikia įvesti būtinus duomenis, todėl užpildykite instrukcijas, esančias [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). Norint apdoroti neatitikties patvirtinimą, užduoties įrašą paleidusiam vartotojui vartotojo puslapyje turi būti priskirta vertė „Pavadinimas“. Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.


## <a name="select-a-quality-order"></a>Pasirinkti kokybės užsakymą
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Periodinės užduotys > Kokybės valdymas > Kokybės užsakymai**.
2. Sąraše pasirinkite kokybės užsakymą, kuris buvo sukurtas [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Neatitikties kūrimas
1. Veiksmų srityje pažymėkite **Užklausos**.
2. Pasirinkite **Neatitikimai**.
3. Pasirinkite **Naujas**.
4. Lauko **Problemos tipas** išskleidžiamajame meniu pažymėkite problemą, kuri buvo aptikta patikrinimo metu.  
5. Pasirinkite **Gerai**.

## <a name="approvereject-a-nonconformance"></a>Neatitikties tvirtinimas / atmetimas
1. Pasirinkite **Funkcijos**.
2. Pažymėkite **Patvirtinti neatitikimą**. Šiuo atveju patvirtinkite neatitiktį. Patvirtintus neatitikimus galima susieti su susijusiomis operacijomis, siekiant įrašyti darbą, kuris atliktas kaip neatitikimo tvarkymo dalis, ir, kaip šioje temoje, taisomojo tvarkymo apdorojimas.  
3. Pasirinkite **Taip**.

## <a name="create-a-correction-action"></a>Koregavimo veiksmo kūrimas
1. Pažymėkite **Taisymai**.
2. Pasirinkite **Naujas**.
3. Naujos eilutės lauke **Darbuotojų skaičius** išplečiamajame meniu pažymėkite pageidaujamą įrašą.
4. Spustelėkite **Pažymėti**.
5. Pažymėkite **Pridėti**. Sukurkite pastabą apie koregavimą. Šiuo atveju veiksmas yra susisiekti su tiekėju ir aptarti neatitikties atvejį.  
6. Pasirinkite **Naujas**.
7. Pažymėkite **Pastaba**. Atsižvelgiant į ataskaitos sąranką, galima atspausdinti skirtingus ataskaitų, kurios susijusios su neatitikimų valdymu, dokumentų tipus.  
8. Lauke **Aprašo laukas** surinkite reikšmę.
9. Uždarykite puslapį.

## <a name="maintain-a-correction"></a>Koregavimo tvarkymas
1. Pažymėkite **Žymėti kaip užbaigtą**.
2. Pasirinkite **Gerai**.
3. Uždarykite puslapį.

## <a name="close-a-nonconformance"></a>Neatitikties uždarymas
1. Pažymėkite **Funkcijos**.
2. Pažymėkite **Uždaryti neatitikimą**.
3. Pasirinkite **Taip**.
4. Uždarykite puslapius.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]