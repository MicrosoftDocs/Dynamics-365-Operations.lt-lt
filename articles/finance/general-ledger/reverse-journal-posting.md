---
title: Atšaukimo registravimas žurnale
description: Šioje temoje aprašomos galimybės, leidžiančios atšaukti kvitus iš kvitų operacijų sąrašo arba iš finansinių žurnalų.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5d1c58463c24dc6a40b036f0bb803316bbb65c2
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091904"
---
# <a name="reverse-journal-posting"></a>Atšaukimo registravimas žurnale

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos „Microsoft Dynamics 365 Finance“ galimybės, leidžiančios atšaukti visą žurnalą arba atšaukti vieną ar keletą kvitų iš kvitų operacijų sąrašo, neatsižvelgiant į jų kilmę. 

## <a name="reversing-journals"></a>Žurnalų atšaukimas

Galite atšaukti atskiras žurnalo eilutes. Registruodami atšaukimą žurnale, taip pat galite atšaukti visą finansinį žurnalą. Atšaukite žurnalą, atlikę toliau pateikiamus veiksmus. 

- Atidarykite finansinį žurnalą ir filtruokite paskelbtus žurnalus.
- Pasirinkite puslapio viršuje esantį meniu **Atšaukti**.
- Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą
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

- Pasirinkite puslapio viršuje esantį meniu **Atšaukti**
- Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių kiekį.
- Pasirinkite **Taip**, jei norite, kad būtų naudojamos esamos operacijų datos, arba **Ne**, kad įvestumėte naują. Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs turite įvesti naują operacijos datą, kad ją atšauktumėte.
- Jei pasirinksite **Ne**, įveskite atšaukimo operacijos datą. 
- Įveskite komentarą, kad aprašytumėte atšaukimo operaciją.
- Paspauskite mygtuką **Atšaukti**.

Operacijos bus atšauktos. 

Jei kvito eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą. Rezultatus galite peržiūrėti peržiūrėdami paketinės užduoties komentarus. Visos operacijos, kurių negalima atšaukti, bus įtrauktos į paketinės užduoties retrospektyvą.

Jei kvito eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant. Rezultatai bus rodomi dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, kartu su priežastimis. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

Operacijas galima atšaukti tik tuo atveju, jei jos atitinka atšaukimui taikomas verslo taisykles. Tiekėjo mokėjimų negalima atšaukti naudojant šioje temoje aprašytą funkciją. Tiekėjo mokėjimai turi būti atšaukiami atliekant veiksmus, aprašytus [Tiekėjo mokėjimo atšaukimas](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).

