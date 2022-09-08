---
title: Darbo sandėlyje atšaukimas dėl išimčių tvarkymo
description: Šiame straipsnyje aprašomos darbo atšaukimo funkcijos, kurias leidžia sandėlio prižiūrėtojai tvarkyti užblokuotą darbą.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404431"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Darbo sandėlyje atšaukimas dėl išimčių tvarkymo

[!include [banner](../includes/banner.md)]

"Microsoft Dynamics 365 Supply Chain Management " darbo atšaukimo funkcija leidžia administratoriui atšaukti konkretų sandėlio darbą, kuris šiuo metu vyksta, bet kurį blokuoja sistema arba kurį galima atlikti dėl išskirtinių aplinkybių. Ši funkcija yra patraukli ir saugi alternatyva SQL koreguojamiems scenarijams, kurie nustato prieštaringus duomenis. Tačiau, kadangi šių scenarijų paprastai reikalauja IT specialistai, atšauktų darbų funkciją gali naudoti įmonės vartotojai, kurie turi administratoriaus teises.

Galite pasiekti atšauktų darbo funkcijų sandėlio valdymo **periodines** \> **užduotis Valyti** \> **\> darbą.** Dialogo lange **Atšaukti darbą** nurodykite darbo, kurį norite atšaukti, ID ir pasirinkite **Gerai**.

## <a name="warehouse-work-that-can-be-canceled"></a>Sandėlio darbas, kurį galima atšaukti

Atliekant sandėlio paėmimo veiksmus, darbuotojas gali susidurti su situacijomis, kuriose jis užregistravo kiekius, paimtus iš saugojimo vietos į vartotojo vietą, tačiau negali užregistruoti padėjimo veiksmo. Nesuderinami sandėlio duomenys dažnai, bet ne visada yra priežastis, kodėl darbas blokuojamas.

Skirtingai nei įprasto **atšaukimo** funkcijos, kurias galima pasiekti naudojant mygtuką Atšaukti darbo antraštėje, **naudojant darbo atšaukimo darbo funkcijas nebūtina, kad paskutinė užbaigto darbo eilutė būtų padėjus tipo darbo** eilutė. Kitaip tariant, norint atšaukti darbo funkciją, atšaukimo logiką galima vykdyti net jei prekės kiekis darbo eilutėje yra vartotojo vietoje.

> [!NOTE]
> Dėl veikimo priežasčių reikia atšaukti darbą, sandėlio vartotojai turi ir toliau naudoti įprastas atšaukimo funkcijas darbo puslapyje.

Tik pardavimo, perkėlimo **išdavimo** **·**, **žaliavų** **paėmimo** arba papildymo tipo darbą galima atšaukti naudojant darbo atšaukimo funkciją. Atšaukimo logika nebus vykdoma sušaldytų žaliavų paėmimo darbu arba darbu, kurį galima atšaukti naudojant reguliarią atšaukimo funkciją (žr. ankstesnę pastabą).

Norint atblokuoti darbą, sistema atšaukia likusias darbo eilutes ir nustato sandėlio duomenis, susietus su vartotojo nurodytu darbo ID. Tada galės būti tęsiami bet kokie įprasti sandėlio tvarkymo veiksmai, susiję su paveiktu prekių kiekiu.

Norėdamas perkelti paveiktą prekę į konkrečią vietą po to, kai buvo atšauktas darbas, vartotojas turi atlikti atsargų perkėlimą arba kiekio koregavimą mobiliajame įrenginyje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]