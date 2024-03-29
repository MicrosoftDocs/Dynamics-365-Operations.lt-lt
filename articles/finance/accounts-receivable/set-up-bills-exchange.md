---
title: Įsakomųjų vekselių nustatymas
description: Šiame straipsnyje aprašomi įsakomųjų vekselių nustatymo veiksmai.
author: ShivamPandey-msft
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: kfend
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91821b10afe7cdbabd0a58b61219ce29d686c5c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874731"
---
# <a name="set-up-bills-of-exchange"></a>Įsakomųjų vekselių nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi įsakomųjų vekselių nustatymo veiksmai.

Parašomas įsakomasis vekselis arba elektroninis kliento užsakymas, kuris nurodo, kad trečioji šalis, paprastai bankas, sumokėtų įmonei nurodytą sumą. Kai naudojate įsakomąjį vekselį kaip mokėjimą už pardavimo užsakymo SF arba laisvos formos SF, kredituojate kliento sąskaitą. Kreditas saugomas įsakomojo vekselio kol klientas apmoka įsakomąjį vekselį bankui. Paprastai sudengsite sąskaitą faktūrą įsakomuoju vekseliu atėjus terminui. Kai iš banko gausite pranešimą, kad įsakomasis vekselis apmokėtas, galite jį uždaryti. Įsakomąjį vekselį galite išduoti per savo banką bet kuriuo metu iš pateiktų:

-   Atėjus terminui. Šis būdas žinomas kaip perdavimas inkasacijai.
-   Prieš terminą, paprastai esant nuolaidos datai, kuri nurodyta mokėjimo sąlygose, kurios nustatomos kliento. Registruojant operaciją, nuolaidos suma užregistruojama išlaidų sąskaitoje. Likusi suma yra įsipareigojimas jums, kol bankas gauna mokėjimą iš kliento. Šis būdas žinomas kaip pavertimas į nuolaidą.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Įsakomųjų vekselių šablonų registravimo nustatymas

Naudokite puslapį **Kliento registravimo šablonai** norėdami nustatyti registravimo šablonus, kuriuos galite naudoti su įsakomaisiais vekseliais, užprotestuoti įsakomąjį vekselį, perdavimams inkasacijai ir pavertimams į nuolaidą. Lauke **Suminė sąskaita** pasirinkite suminę sąskaitą, kuriai bus registruojamos įsakomojo vekselio sumos. Ši sąskaita debetuojama arba kredituojama atsižvelgiant į įsakomojo vekselio operacijos tipą.
-   Įsakomiesiems vekseliams ši sąskaita debetuojama kai įsakomasis vekselis yra užregistruojamas ir kredituojamas tada, kai užregistruojamas nuolaidos pavedimas arba perdavimas inkasacijai.
-   Užprotestuotiems įsakomiesiems vekseliams ši sąskaita debetuojama kai užregistruojamas užprotestuotas įsakomasis vekselis.
-   Perdavimams inkasacijai ši sąskaita debetuojama kai užregistruojamas perdavimas inkasacijai.
-   Nuolaidos pavedimams ši sąskaita debetuojama kai užregistruojamas nuolaidos pavedimas.

Lauke **Sudengimo sąskaita** pasirinkite kasos kodą, kuriai bus registruojamos įsakomojo vekselio sumos. Ši sąskaita debetuojama kai sudengiamas įsakomasis vekselis. Lauke **PVM išankstinai apmokėjimai** pasirinkite suminę sąskaitą, kurioje norite registruoti PVM sumą, kai įsakomieji vekseliai naudojami išankstiniam apmokėjimui. Lauke **Nuolaidų sąskaitos skolos** pasirinkite sąskaitą, kurioje norite registruoti nuolaidos sumą, taikomą nuolaidos pavedimams. Sąskaita kredituojama kai užregistruojamas pavedimas nuolaidai.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Nustatykite Gautinų sumų parametrus, skirtus įsakomiesiems vekseliams.

Puslapyje **Gautinų sumų parametrai** numatytieji registravimo šablonai, skirti įsakomiesiems vekseliams, įvedami skirtuke **DK ir PVM**. Numeracijos nustatomos skirtuke **Numeracijos**.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Nustatykite įsakomųjų vekselių žurnalų pavadinimus


Puslapyje **Žurnalų pavadinimai** sukurkite mažiausiai penkis žurnalų pavadinimus, kurie bus naudojami su įsakomaisiais vekseliais. Toliau nurodyti žurnalų tipai:
-   **Kliento išduotas įsakomasis vekselis** – sukurkite Įsakomųjų vekselių išdavimo žurnalo pavadinimą.
-   **Kliento užprotestuotas įsakomasis vekselis** – sukurkite Užprotestuotų vekselių išdavimo žurnalo pavadinimą.
-   **Kliento perrašytas įsakomasis vekselis** – sukurkite Įsakomųjų vekselių pakartotinio išdavimo žurnalo pavadinimą.
-   **Kliento banko pavedimas** – sukurkite Pavedimų žurnalo pavadinimą.
-   **Kliento sudengtas įsakomasis vekselis** – sukurkite Įsakomųjų vekselių sudengimo žurnalo pavadinimą.

Žurnalo kvito puslapyje kiekvienam įsakomojo vekselio žurnalui įveskite informaciją apie įsakomąjį vekselį skirtuke **Įsakomasis vekselis**. Užregistravę įsakomojo vekselio žurnalo eilutes, jas galite peržiūrėti puslapyje **Įsakomųjų vekselių žurnalo užklausa** ir puslapyje **Įsakomųjų vekselių statistika**.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Nustatykite įsakomųjų vekselių mokėjimo metodą

Puslapyje **Mokėjimo būdai** nustatykite bent vieną mokėjimo už įsakomuosius vekselius būdą. Jei bendradarbiaujate daugiau nei su vienu banku, nustatykite mokėjimo metodą, kuris atitinka perdavimo formatą, kurio įsakomiesiems vekseliams reikalauja kiekvienas bankas.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Nustatykite įsakomųjų vekselių mokėjimo mokesčius

Mokėjimo mokestis – tai mokestis, susietas su mokėjimų iš klientų surinkimo procesu. Su kiekvienu mokėjimo mokesčiu galima susieti kelias mokėjimo mokesčių nustatymo eilutes. Galite naudoti nustatymo eilutes, kad galėtumėte valdyti numatytųjų sumų, skirtų mokėjimo mokesčiams, skaičiavimą. Pvz., galite sukurti nustatymo eilutes, taikomas mokėjimo būdams, mokėjimo specifikacijoms, valiutoms ir laikotarpiams. Taip pat galite sukurti nustatymo eilutes, taikomas procentiniam dydžiui arba sumai pagal dienos intervalus. Pvz., galite nustatyti palūkanų procentinį dydį pagal laiko trukmę praėjus mokėjimo terminui. Jei bankas ima skirtingus mokesčius už skirtingus pavedimo tipus, pvz., **Rinkimas** arba **Nuolaida**, nustatykite atskirą mokėjimo mokesčio eilutę kiekvienam pervedimo tipui.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Banko pavedimų failų pavedimo mokesčių nustatymas

Puslapyje **Banko sąskaitos** galite nustatyti kiekvieno sugeneruoto pervedimo failo pervedimo tipus, už kuriuos bankas ima mokestį. Pavedimo mokesčiai registruojami, kai pavedimas patvirtinamas ir žinomos realizuotų mokesčių sumos. Pervedimo mokesčiai skiriasi nuo mokėjimo mokesčių, kurie renkami iš klientų ir pridedami žurnalo eilutėse.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Nustatykite įsakomųjų vekselių dokumentų maketus

Puslapyje **Banko sąskaitos** spustelėkite **Nustatyti** ir nurodykite dokumento maketą, kuris reikalingas kiekvienai banko sąskaitai, kuriai generuosite spausdintus įsakomųjų vekselių dokumentus.

## <a name="set-up-customers-for-bills-of-exchange"></a>Nustatykite įsakomųjų vekselių klientus

Puslapyje **Klientai** kiekvienam klientui, kuris sutiko mokėti naudojantis įsakomuoju vekseliu, galite nustatyti numatytąjį mokėjimo metodą, skirtą įsakomajam vekseliui skirtuke **Mokėjimo numatytieji nustatymai**.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
