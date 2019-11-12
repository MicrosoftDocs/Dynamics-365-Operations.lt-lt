---
title: Darbo sandėlyje atšaukimas dėl išimčių tvarkymo
description: Šioje temoje aprašomas darbo funkcijų atšaukimas, kuris leidžia sandėlio prižiūrėtojams tvarkyti užblokuotą darbą.
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625875"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Darbo sandėlyje atšaukimas dėl išimčių tvarkymo

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ darbo atšaukimo funkcija leidžia administratoriui atšaukti konkretų vykdomą sandėlio darbą, kuris yra blokuojamas sistemos arba kurio negalima baigti dėl išimtinių aplinkybių. Ši funkcija yra patraukli ir saugi alternatyva SQL koreguojamiems scenarijams, kurie nustato prieštaringus duomenis. Tačiau, kadangi šie scenarijai įprastai yra reikalaujami iš IT profesionalų, darbo atšaukimo funkciją gali naudoti įmonės vartotojai, turintys administratoriaus teises.

Darbo atšaukimo funkciją galite pasiekti **Sandėlio valdymas** \> **Periodinės užduotys** \> **Valyti \> Atšaukti darbą**. Dialogo lange **Atšaukti darbą** nurodykite darbo, kurį norite atšaukti, ID ir pasirinkite **Gerai**.

## <a name="warehouse-work-that-can-be-canceled"></a>Sandėlio darbas, kurį galima atšaukti

Atliekant sandėlio paėmimo veiksmus, darbuotojas gali susidurti su situacijomis, kuriose jis užregistravo kiekius, paimtus iš saugojimo vietos į vartotojo vietą, tačiau negali užregistruoti padėjimo veiksmo. Nesuderinami sandėlio duomenys dažnai, bet ne visada yra priežastis, kodėl darbas blokuojamas.

Skirtingai nuo įprastos atšaukimo funkcijos, kurią galima pasiekti naudojant darbo antraštėje esantį mygtuką **Atšaukti**, darbo atšaukimo funkcija nereikalauja, kad paskutinio užbaigto darbo eilutė būtų **padėjimo** tipo darbo eilutė. Kitaip tariant, dirbant su darbo atšaukimo funkcija, atšaukimo logika gali būti vykdoma, net jei darbo eilutėje nurodytas prekių kiekis yra vartotojo vietoje.

> [!NOTE]
> Esant darbui, kurį reikia atšaukti dėl darbinių priežasčių, sandėlio vartotojai turi toliau naudoti įprastinę atšaukimo funkciją darbo puslapyje.

Naudojant darbo atšaukimo funkciją galima atšaukti tik darbus, kurių tipas yra **Pardavimas**, **Perkėlimo išdavimas**, **Žaliavų paėmimas** arba **Papildymas**. Atšaukimo logika nebus vykdoma sušaldytos žaliavos paėmimo darbui arba darbui, kurį galima atšaukti naudojant įprastą atšaukimo funkciją (žr. ankstesnę pastabą).

Norint atblokuoti darbą, sistema atšaukia likusias darbo eilutes ir nustato sandėlio duomenis, susietus su vartotojo nurodytu darbo ID. Tada galės būti tęsiami bet kokie įprasti sandėlio tvarkymo veiksmai, susiję su paveiktu prekių kiekiu.

Norėdamas perkelti paveiktą prekę į konkrečią vietą po to, kai buvo atšauktas darbas, vartotojas turi atlikti atsargų perkėlią arba kiekio koregavimą mobiliajame įrenginyje.
