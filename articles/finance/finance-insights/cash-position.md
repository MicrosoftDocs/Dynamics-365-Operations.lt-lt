---
title: Grynųjų pinigų pozicija
description: Šioje temoje aprašoma, kaip funkcija Grynųjų pinigų srautų prognozavimas prognozoja organizacijos grynųjų pinigų padėtį tam tikru laiku. Joje taip pat aprašomos galimos parinktys, naudojamos norint rodyti skirtingų laikotarpių prognozes.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 6bb99084a2ffef067dd0d7158ecb5e57d6d97d75
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945806"
---
# <a name="cash-position"></a>Grynųjų pinigų pozicija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Grynųjų pinigų padėtis yra grynųjų pinigų prognozė artimiausiam laikotarpiui. Ji paremta grynųjų pinigų gavimo iš klientų, kurie moka neapmokėtas SF ir užsakymus, prognoze bei numatomu grynųjų pinigų išmokėjimu, vykdomu tiekėjams už pirkimo SF ir užsakymus.

Kai sistema prognozuoja kliento mokėjimus, ji naudoja mokėjimo prognozes iš kliento mokėjimo prognozavimo funkcijos. Be mokėjimo prognozių, mokėjimo datai apskaičiuoti naudojamas vidutinis laikas, kurio reikia norint konvertuoti kliento SF į kiekvieno kliento mokėjimą. Atidarytų kliento užsakymų atveju sistema SF datą apskaičiuoja naudodama vidutinį užsakymo eilučių skaičių, pateiktą kiekvienam klientui, kuriam bus išrašyta SF. Tada SF data naudojama kaip mokėjimo prognozavimo funkcijos įvestis. Kliento mokėjimo prognozavimo funkcija apskaičiuoja kiekvienos užsakymo eilutės apmokėjimo datą. 

Neapmokėtų sąskaitų faktūrų mokėjimo data yra numatoma pagal mokėjimo prognozes pasirenkant datą, atitinkančią penkiasdešimtąją kaupiamojo paskirstymo funkcijos procentilį, gaunamą iš prognozuojamų talpyklų tikimybių.

Panašus metodas naudojamas prognozuojant mokėjimus tiekėjams. Kiekvienam tiekėjui sistema apskaičiuoja vidutinį laiką, kurio reikia norint konvertuoti tiekėjo SF į mokėjimą. Tas dienų skaičius tada naudojamas skaičiuojant mokėjimo datą. Atidarytų tiekėjo užsakymų atveju sistema SF datą apskaičiuoja atsižvelgdama į vidutinį dienų skaičių, kurio reikia norint konvertuoti užsakymo eilutes į kiekvieno tiekėjo SF. Sistema tada mokėjimo datą apskaičiuoja nauodama vidutinį laiką, kurio reikia norint konvertuoti tiekėjo SF į kiekvieno tiekėjo mokėjimą.

Viršutinėje skirtuko **Grynųjų pinigų padėtis** dalyje yra grynųjų pinigų padėties diagrama. Šioje diagramoje rodomos grynųjų pinigų įplaukos ir išmokos bei jų poveikis bendrajam likvidumo balansui. Grynųjų pinigų padėties diagramos informaciją galima peržiūrėti dienos, savaitės, mėnesio arba ketvirčio laikotarpiais. Pasirinkę **Dienos**, galite peržiūrėti artimiausios 21 dienos prognozes. Pasirinkę **Savaitės**, galite peržiūrėti artimiausių 20 sav. prognozes. Pasirinkę **Mėnesio**, galite peržiūrėti artimiausių 12 mėn. prognozes. Pasirinkę **Ketvirčio**, galite peržiūrėti artimiausių 12 ketvirčių prognozes. Galite paslėpti diagramą, jei reikia papildomos vietos ekrane, kad galėtumėte peržiūrėti turinį skirtuke **Grynųjų pinigų padėtis**.

Apatinėje skirtuko **Grynųjų pinigų vieta** dalyje pateikiama išsami informacija apie padėtį, grynųjų pinigų srautą, numatomus mokėjimus ir banko sąskaitą.

- Informacija tinklelyje **Padėties informacija** pateikiama trijuose skyriuose: likvidumo sąskaitų sąrašas, dokumentų, kurie sudaro grynųjų pinigų įplaukas, sąrašas ir dokumentų, kurie sudaro grynųjų pinigų išmokas, sąrašas. Tinklelyje taip pat rodomi grynųjų pinigų padėties balansai. Pirmo peržiūrimo laikotarpio atveju likvidumo sąskaitų balansas yra pradinis balansas. Vėlesnių laikotarpių atveju likvidumo sąskaitų balansai apskaičiuojami atsižvelgiant į grynųjų pinigų įplaukų pridėjimą ir grynųjų pinigų išmokų atėmimą iš ankstesnių laikotarpių. Norėdami peržiūrėti informaciją apie operacijas, kurios sudaro balansą, pasirinkite saitą **Balansas**.
- Tinklelyje **Grynųjų pinigų srautas** rodomos grynųjų pinigų įplaukos, grynųjų pinigų išmokos, sutelktos per laikotarpį, ir jų įtaka likvidumo sąskaitų balansams. Pirmo laikotarpio atveju likvidumo sąskaitų balansas yra pradinis balansas. Vėlesnių laikotarpių atveju likvidumo sąskaitų balansai apskaičiuojami atsižvelgiant į grynųjų pinigų įplaukų pridėjimą ir grynųjų pinigų išmokų atėmimą iš ankstesnių laikotarpių.
- Tinklelyje **Numatomas banko balansas** rodomos numatomos grynųjų pinigų išmokos ir jų įtaka likvidumo sąskaitoms.
- Tinklelyje **Banko sąskaita** rodoma numatomų grynųjų pinigų įplaukų ir išmokų įtaka banko balansui.

Norėdami įrašyti ir redaguoti grynųjų pinigų padėtį, sukurkite momentinę kopiją. Daugiau informacijos apie tai, kaip dirbti su momentinėmis kopijomis, žr. [Momentinių kopijų apžvalga](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Išsami informacija apie grynųjų pinigų padėties galimybę 

Grynųjų pinigų pozicijas sudaro toliau nurodytos funkcijos. 

- Grynųjų pinigų pareigų funkcija rodo grynųjų pinigų srautus, remiantis sistemoje esamais dokumentais, bei iš išorinių sistemų importuotas grynųjų pinigų įplaukas ir nutekėjimo eilutes.
- Leidžia lengvai integruoti grynųjų pinigų srautų duomenis iš išorinių sistemų į „Dynamics 365 Finance“. Grynųjų pinigų pozicijai taip pat galima naudoti duomenų importavimo - eksportavimo sistemą. Ši sistema leidžia lengvai integruoti su „Excel“ „OData“. Taip pat galite sujungti duomenis iš kelių šaltinių, kad sukurtumėte išsamų grynųjų pinigų pareigų sprendimą.
- Įdiegiama sumanios grynųjų pinigų padėties funkcija. Grynųjų pinigų pozicija sukuriama atsižvelgiant į kliento mokėjimo būdą numatyma, kada įmonė gali tikėtis, kad grynieji pinigai bus pristatyti į savo sąskaitas.
- Kliento užsakymuose ir SF kliento mokėjimo numatymo AI funkcija naudojama norint nustatyti retrospektyvią kliento mokėjimo elgseną, kai už užsakymą arba SF bus mokama.
- Tiekėjo užsakymams ir SF mes naudojame vidutinį laiką tarp siuntimo ir SF apmokėjimo vienam tiekėjui, kad nustatytumėte, kada tiekėjo užsakymui arba SF bus sumokėta, kad grynųjų pinigų išlaidos būtų tikslesnės.

Taip sukuriamas tikslesnis pinigų srautų rodinys pagal retrospektyvinio iždininko mokėjimo būdą. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
