---
title: Kliento mokėjimo prognozių įjungimas
description: Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio „Finance Insights” funkciją Kliento mokėjimo prognozės.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a52d38e8fb842c7fbc8adf60a6daaef6cdc9d5ec
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713366"
---
# <a name="enable-customer-payment-predictions"></a>Kliento mokėjimo prognozių įjungimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio „Finance Insights” funkciją Kliento mokėjimo prognozės. Įjunkite priemonių valdymo darbo srities funkciją **ir** įveskite konfigūracijos parametrus finansų žinių **konfigūracijos** puslapyje. Šioje temoje taip pat pateikiama informacija, kuri gali padėti veiksmingai naudoti funkciją.

> [!NOTE]
> Prieš atlikdami šiuos veiksmus, būtinai atlikite būtinuosius veiksmus, aprašytus temoje [Konfigūravimas moduliui „Finance Insights”](configure-for-fin-insites.md).

1. Įjungti kliento mokėjimo numatymų funkciją:

    1. Atidarykite parinkties **Funkcijos valdymas** darbo sritį.
    2. Pasirinkite **Tikrinti, ar yra naujinimų**.
    3. Skirtuke **Visi** ieškokite kliento **mokėjimo numatyių**. Jei tos priemonės nerandate, ieškokite **(Peržiūrėti) kliento mokėjimo numatymams**. 
    4. Įjungti funkciją.

    Kliento mokėjimo numatyma dabar įjungta ir parengta konfigūruoti.

2. Funkcijos Kliento mokėjimo įžvalgos konfigūravimas

    1. Eikite **į Kreditas ir rinkiniai \> Nustatymo \> finansai žinių \> kliento mokėjimų numatyme**.
    2. Finansų žinių **konfigūracijos puslapio skirtuke Kliento mokėjimo numatymas pasirinkite Peržiūrėti duomenų laukus,** **naudojamus** **·** **numatymo modelyje, kad atidarytumėte duomenų laukus numatymo modelio puslapiui.** Čia galite peržiūrėti numatytąjį laukų, kurie naudojami kuriant kliento mokėjimo prognozių dirbtinio intelekto (DI) prognozavimo modelį, sąrašą.

        Norėdami naudoti numatytąjį laukų sąrašą numatymo modeliui sukurti, **uždarykite duomenų laukus numatymo modelio puslapiui,** **tada, finansų žinių konfigūracijos puslapyje, nustatykite pasirinktį** **Įgalinti priemonę kaip** Taip **.**
        
   > [!NOTE]
   > Kliento **mokėjimų numatymo funkcija reikalauja daugiau** nei 100 operacijų per praėjusius šešis iki devynių mėnesių. Operacijos gali būti laisvos formos SF, pardavimo užsakymai ir kliento mokėjimai. Šie duomenys turi būti paskirstyti pagal **laikus**, pavėluotus **ir** labai vėluoja **parametrus**.    
     

    3. Nurodykite „labai pavėluotą“ operacijos laikotarpį, kad nustatytumėte, ką jūsų įmonei reiškia prognozavimo talpykla **Labai vėluoja**.

        Kiekvienoje atidarytoje SF sistema prognozuoja mokėjimo tikimybę pagal tris talpyklas: **Laiku**, **Vėluoja** ir **Labai vėluoja**.

        - **Laiku** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti operacijos termino dieną arba anksčiau.
        - **Vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti po operacijos termino dienos, bet prieš „labai vėluojančio“ operacijos laikotarpio pradžią.
        - **Labai vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti prasidėjus „labai vėluojančiam“ operacijos laikotarpiui.

        > [!NOTE]
        > Pakeitus „labai vėluojantį“ operacijos laikotarpį ir pasirinkus **Pakeisti vėlavimo ribinę reikšmę** po to, kai buvo sukurtas kliento mokėjimų DI prognozavimo modelis, esamas prognozavimo modelis panaikinamas ir sukuriamas naujas modelis. Naujas prognozavimo modelis perkels operacijas į „labai vėluojantį“ laikotarpį, atsižvelgdamas į parametrus, įvestus jam nustatyti.

    4. Kai baigsite apibrėžti „labai vėluojantį“ operacijos laikotarpį, pasirinkite **Kurti prognozavimo modelį**, kad sukurtumėte prognozavimo modelį. Finansų **žinių žinių** konfigūracijos puslapyje esantis **Numatymo modelio** skyrius rodo numatymo modelio būseną.

        > [!NOTE]
        > Bet kuriuo metu kurdami prognozavimo modelį, galite pasirinkti **Iš naujo nustatyti modelio kūrimą**, kad procesas būtų paleistas iš naujo.

    Funkcija jau sukonfigūruota ir yra parengta naudoti.

Kai priemonė įjungta ir sukonfigūruota, o sukurtas **ir veikia numatymo modelis,** **finansų** žinių parametrų puslapio skyriuje Numatymo modelis rodomas modelio tikslumas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
