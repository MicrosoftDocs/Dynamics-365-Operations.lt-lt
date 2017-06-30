---
title: Tiesioginiai pristatymai
description: "Šiame straipsnyje pateikiama informacija apie tiesioginius pristatymus. Tiesioginiai pristatymai yra pristatymai, kurie siunčiami tiesiogiai jūsų klientui iš tiekėjo."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fd1e98f677835f2ef3449adbb452d536441b0a65
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="direct-deliveries"></a>Tiesioginiai pristatymai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie tiesioginius pristatymus. Tiesioginiai pristatymai yra pristatymai, kurie siunčiami tiesiogiai jūsų klientui iš tiekėjo.

Tiesioginiai pristatymai taupo pristatymo laiką ir mažina su atsargų laikymu susijusias išlaidas, nes jums nereikia laikyti produktų savo sandėlyje prieš juos išsiunčiant klientui.  

Puslapyje **Pardavimo užsakymas** galite kurti tiesioginius pristatymus. Pirma, sukurkite pardavimo užsakymą ir užsakymo eilutes. Tada veiksmų srityje, skirtuke **Pardavimo užsakymas**, pasirinkite **Tiesioginis pristatymas**. Galiausiai nurodykite eilutes, kurios turi būti tvarkomos kaip tiesioginis pristatymas. Sukuriamas saitas tarp tiesioginio pristatymo pardavimo užsakymo eilučių ir atitinkamų pirkimo užsakymo eilučių.  

**Pastaba:** Jei dalis užsakyto kiekio jau pristatyta, turite padalyti likusį kiekį. Sukurkite naują eilutę kiekiui, kuris turi būti tiesiogiai pristatytas, ir atimkite tą kiekį iš kiekio pradinėje eilutėje. Pvz., jei pradinis kiekis buvo 15 ir pristatyti penki vienetai, turite sukurti naują eilutę likusiems 10 vienetų, o tada sumažinti pradinį kiekį ta suma.  

Sukūrę tiesioginio pristatymo saitą tarp pardavimo užsakymo eilučių ir pirkimo užsakymo eilučių, galite atnaujinti pardavimo užsakymą naudodami važtaraštį. Paleiskite arba važtaraščio atnaujinimą, arba SF atnaujinimą iš pirkimo užsakymo. Turite atnaujinti pardavimo užsakymo sąskaitą faktūrą puslapyje **Pardavimo užsakymas**. Atnaujinus sąskaitą faktūrą, pardavimo užsakymo kiekis negali būti didesnis už kiekį, kuris buvo užregistruotas kaip gautas. Pvz., pardavimo užsakymo eilutėje yra 10 dalių, bet tik penkios dalys iš pardavimo užsakymo eilutės buvo atnaujintos naudojant važtaraštį. Jei atnaujindami pardavimo užsakymo sąskaitą faktūrą sąraše **Kiekis** pasirinksite **Visas**, atnaujinama bus tik tų prekių sąskaita faktūra, kurios buvo fiziškai gautos arba kurios buvo atnaujintos naudojant važtaraštį. Visa pardavimo užsakymo eilutė neatnaujinama.

## <a name="delivery-date"></a>Pristatymo data
Atnaujinant lauką **Pageidaujama gavimo data** pardavimo užsakymo eilutėje, taip pat atnaujinamas laukas **Pristatymo data** atitinkamoje pirkimo užsakymo eilutėje. Tokiu pat būdu, kai atnaujinate lauką **Patvirtinta** pirkimo užsakymo eilutėje, taip pat atnaujinami laukai **Patvirtinta gavimo data** ir **Patvirtinta siuntimo data** atitinkamose pardavimo užsakymo eilutėse.

## <a name="delivery-address"></a>Pristatymo adresas
Paprastai pirkimo užsakymo pristatymo adresas yra numatytasis įmonės adresas. Tačiau kai kuriate tiesioginį pristatymą, kaip pristatymo adresą įvedate kliento adresą. Jeigu pakeisite pristatymo adresą pirkimo užsakymo eilutėje, kurios pristatymo tipas yra **Tiesioginis pristatymas**, tada atitinkamos pardavimo užsakymo eilutės pristatymo adresas taip pat atnaujinamas. Panašiai, jeigu pakeisite pristatymo adresą pardavimo užsakymo eilutėje, pristatymo adresas pirkimo užsakymo eilutėje taip pat atnaujinamas.

## <a name="deleting-order-lines"></a>Užsakymo eilučių naikinimas
Jeigu bandysite panaikinti pardavimo užsakymo eilutę, kurios pristatymo tipas yra **Tiesioginis pristatymas**, pranešimo lauke bus nurodoma, kad prie eilučių pridėtos pirkimo užsakymo eilutės. Jeigu pardavimo užsakymo eilutė dalinai pristatyta, negalite panaikinti pardavimo užsakymo eilutės arba prie jos pridėtų pirkimo užsakymo eilučių.

## <a name="warehouse"></a>Sandėlis
Kai kuriate tiesioginį pristatymą, prekės, kurias parduodate, niekada fiziškai neatvežamos į jūsų sandėlį. Tačiau vis tiek turite nurodyti sandėlį pardavimo užsakymo eilutėje. Panašiai paėmimo reikalavimai gali būti nurodyti prekės modelių grupėje. Tačiau kadangi prekės niekada fiziškai neatvežamos į sandėlį, šių reikalavimų nepaisoma, kai pardavimo užsakymas yra tiesioginis pristatymas.




