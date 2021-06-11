---
title: Grynųjų pinigų padėtis (peržiūros versija)
description: Šioje temoje aprašoma, kaip funkcija Grynųjų pinigų srautų prognozavimas prognozoja organizacijos grynųjų pinigų padėtį tam tikru laiku. Joje taip pat aprašomos galimos parinktys, naudojamos norint rodyti skirtingų laikotarpių prognozes.
author: ShivamPandey-msft
ms.date: 05/26/2020
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
ms.openlocfilehash: cf9d3fd905a90a2937bfac97c8e44ea13be4f42e
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123395"
---
# <a name="cash-position-preview"></a>Grynųjų pinigų padėtis (peržiūros versija)

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

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
