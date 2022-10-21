---
title: Atšaukimo registravimas žurnale
description: Šiame straipsnyje aprašomi pajėgumai, kurie leidžia atšaukti kvitus iš kvitų operacijų sąrašo arba iš finansinių žurnalų.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 8912409ec0d2016ea4af12843319febda98663c5
ms.sourcegitcommit: e700528679a821237e644b3e21058c36ae1323c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2022
ms.locfileid: "9680390"
---
# <a name="reverse-journal-posting"></a>Atšaukimo registravimas žurnale

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi Microsoft Dynamics "365" finansai, suteikia galimybę atšaukti visą žurnalą arba atšaukti vieną ar daugiau kvitų operacijų sąrašo, neatsižvelgiant į jų kilmę. 

Kad būtų galima naudoti vieną iš šiame straipsnyje aprašytų funkcijų, ją reikia įjungti jūsų sistemoje. Administratoriai gali naudoti **Funkcijos valdymas** darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:
 - Modulis: Didžioji knyga
 - Priemonės pavadinimas: **kelių dokumentų masinis atšaukimas**

## <a name="reversing-journals"></a>Žurnalų atšaukimas

Galite atšaukti atskiras žurnalo eilutes. Registruodami atšaukimą žurnale, taip pat galite atšaukti visą finansinį žurnalą. Atšaukite žurnalą, atlikę toliau pateikiamus veiksmus. 

- Filtruoti užregistruotus žurnalus ir **atidaryti** žurnalo eilučių rodinį.
- Puslapio viršuje **pasirinkite viso** žurnalo meniu Atšaukti.
- Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių kiekį.
- Pasirinkite **Taip**, jei norite, kad būtų naudojamos esamos operacijų datos, arba **Ne**, kad įvestumėte naują. Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs turite įvesti naują atšaukimo operacijos datą.
- Jei pasirinksite **Ne**, įveskite atšaukimo operacijos datą. 
- Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją.
- Paspauskite mygtuką **Atšaukti**.

Operacijos bus atšauktos. 

Jei kvito eilučių skaičius viršija 100, atšaukimo procesas bus vykdomas naudojant paketinį procesą. Rezultatus galite peržiūrėti peržiūrėdami paketinės užduoties komentarus. Visos operacijos, kurių negalima atšaukti, bus įtrauktos į paketinės užduoties retrospektyvą.

Jei kvito eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant. Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, kartu su priežastimis, dėl kurių nepavyko atšaukti. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Kvitų atšaukimas kvitų operacijų sąraše. 

Kvitus taip pat galite atšaukti **Kvitų operacijų sąraše** visose papildomose knygose. Be to, vienu metu galite atšaukti keletą kvitų. 

Norėdami atšaukti vieną ar daugiau kvitų, atlikite toliau pateikiamus veiksmus. 

- Pasirinkite puslapio viršuje esantį meniu **Grąžinti visą žurnalą žemyn**.
- Matysite bendrą kvitų ir kvitų eilučių skaičių rodomas bendrai, taip pat bendrą atšaukiamų eilučių kiekį.
- Pasirinkite **Taip**, jei norite, kad būtų naudojamos esamos operacijų datos, arba **Ne**, kad įvestumėte naują. Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs turite įvesti naują operacijos datą, kad ją atšauktumėte.
- Jei pasirinksite **Ne**, įveskite atšaukimo operacijos datą. 
- Įveskite komentarą, kad aprašytumėte atšaukimo operaciją.
- Paspauskite mygtuką **Atšaukti**.

Operacijos bus atšauktos. 

Jei kvito eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą. Rezultatus galite peržiūrėti peržiūrėdami paketinės užduoties komentarus. Visos operacijos, kurių negalima atšaukti, bus įtrauktos į paketinės užduoties retrospektyvą.

Jei kvito eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant. Rezultatai bus rodomi dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, kartu su priežastimis. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

Operacijas galima atšaukti tik tuo atveju, jei jos atitinka atšaukimui taikomas verslo taisykles. Tiekėjo mokėjimų negalima atšaukti naudojant šiame straipsnyje aprašytą galimybę. Tiekėjo mokėjimai turi būti atšaukiami atliekant veiksmus, aprašytus [Tiekėjo mokėjimo atšaukimas](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
