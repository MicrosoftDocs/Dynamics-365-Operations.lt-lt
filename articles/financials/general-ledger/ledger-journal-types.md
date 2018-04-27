---
title: "DK žurnalo tipai"
description: "Šiame straipsnyje aprašyti žurnalų tipai, kuriuos galite nustatyti finansiniams žurnalams. Naudokite puslapį **Žurnalo pavadinimai** norėdami nustatyti žurnalus, kuriuos galite naudoti visoje „Microsoft Dynamics 365 for Finance and Operations“."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9f8fc40f199b83a9e0cb36ce905163c3ed547057
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="ledger-journal-types"></a>DK žurnalų tipai

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje aprašyti žurnalų tipai, kuriuos galite nustatyti finansiniams žurnalams. Naudokite puslapį **Žurnalo pavadinimai** norėdami nustatyti žurnalus, kuriuos galite naudoti visoje „Microsoft Dynamics 365 for Finance and Operations“.

| Žurnalo tipas                      | Paskirtis                       | Operacijų įvedimas šiame puslapyje                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Paskirstymas                        | Kurkite paskirstymo operacijas paskirstymo žurnale. Kurti paskirstymo žurnalą galėsite tik sukūrę paskirstymo taisyklę puslapyje **Didžiosios knygos paskirstymo taisyklė**.      | Apdoroti paskirstymo užklausą             |
| Patvirtinimas                          | Registruoti į tinkamas DK sąskaitas patvirtintas tiekėjo SF.  | SF patvirtinimo žurnalas                                       |
| Banko čekio atšaukimas               | Anuliuoti registruotą čekį. Norėdami naudoti šį žurnalo tipą, puslapyje **Grynųjų pinigų ir banko valdymo parametrai** pasirinkite parinktį **Naudoti mokėjimų atšaukimų peržiūros procesą**.   | Čekių atšaukimai, mokėjimo atšaukimas                   |
| Banko depozito kvito atšaukimas    | Atšaukti mokėjimo kvitą. Norėdami naudoti šį žurnalo tipą, puslapyje **Grynųjų pinigų ir banko valdymo parametrai** pasirinkite parinktį **Naudoti mokėjimų mokėjimo kvitais atšaukimų peržiūros procesą**.   | Depozito kvito mokėjimų atšaukimai            |
| Biudžetas                            | Apdoroti biudžeto asignavimus. Norėdami naudoti šį žurnalo tipą, puslapyje **Didžiosios knygos parametrai** pasirinkite parinktį **Įgalinti biudžeto asignavimą**. Biudžeto žurnalo įrašuose bus pateikta informacija, pagrįsta DK sąskaitomis, nurodytomis puslapyje **Registravimo aprašas**.                                                        |                                                                |
| Klientas priėmė įsakomąjį vekselį  | Kurkite kliento priėmimo operacijas įsakomiesiems vekseliams.             | Išduotų įsakomųjų vekselių žurnalas, pakartotinai išduotų įsakomųjų vekselių žurnalas. |
| Kliento banko pavedimas          | Kurkite įsakomojo vekselio pavedimo failą, kurį bus galima siųsti į jūsų organizacijos banką. Norėdami naudoti šį žurnalo tipą, puslapyje **Sąskaitų** **gautinų sumų parametrai** išvalykite parinktį **Automatinis sudengimas**.            | Pavedimas                                                     |
| Kliento išduotas įsakomasis vekselis    | Kurkite kliento išduoto įsakomojo vekselio operacijas. Norėdami naudoti šį žurnalo tipą, puslapyje **Mokėjimo metodai – klientai** išvalykite parinktį **Kurti ir registruoti išdavimų žurnalą automatiškai registruojant sąskaitas faktūras**.   | Išduoti įsakomųjų vekselių žurnalą                                  |
| Kliento mokėjimas                  | Kurkite kliento mokėjimo operacijas.                             | Mokėjimų žurnalas             |
| Kliento užprotestuotas įsakomasis vekselis | Kurkite kliento užprotestuoto įsakomojo vekselio operacijas.                    | Užprotestuoti įsakomųjų vekselių žurnalą                               |
| Kliento perrašytas įsakomasis vekselis  | Kurkite kliento perrašyto įsakomojo vekselio operacijas.                     | Iš naujo išrašyti įsakomųjų vekselių žurnalą                                |
| Kliento sudengtas įsakomasis vekselis  | Kurkite kliento sudengto įsakomojo vekselio operacijas.                       | Sudengti įsakomųjų vekselių žurnalą                                |
| Kasdien                             | Kurkite pagrindinį žurnalą kasdienėms operacijoms.                          | Pagrindinis žurnalas                                                |
| Pašalinimas                       | Kurkite pašalinimo operacijas pašalinimų žurnale. Norėdami naudoti šį žurnalo tipą, puslapyje **Juridiniai subjektai** pasirinkite parinktis **Naudoti finansinio pašalinimo procese** ir **Naudoti finansinio konsolidavimo procese**. Šį žurnalo tipą galėsite naudoti tik sukūrę didžiosios knygos pašalinimo taisyklę puslapyje **Didžiosios knygos pašalinimo taisyklė**. | Pašalinimas                                                    |
| Ilgalaikio turto biudžetas                | Kurkite ilgalaikio turto biudžeto registro įrašus.                                                                                                                                                                                                                                                                                                                 | Ilgalaikio turto biudžetas                                             |
| SF registras                  | Registruokite pagrindinę tiekėjo SF informaciją.                                                                                                                                                                                                                                                                                                           | SF registras                                               |
| Atlyginimo išmokėjimas              | Išmokėkite pagal atlyginimų mokėjimo pažymas. Negalite rankiniu būdu įvesti operacijų šiame žurnale. Turite generuoti mokėjimo išrašus ir tada pateikti tuos išrašus mokėjimui.                                                                                                                                                              |                                                                |
| Laikotarpio                          | Kurkite periodines periodinio žurnalo operacijas.                                                                                                                                                                                                                                                                                                      | Periodiniai žurnalai                                              |
| Registruoti ilgalaikį turtą                 | Registruokite ilgalaikio turto operacijas.                                                                                                                                                                                                                                                                                                                              | Ilgalaikis turtas                                                   |
| Projektas – Išlaidos                | Kurkite projekto išlaidų operacijas.                                                                                                                                                                                                                                                                                                                        | Išlaidos                                                        |
| Statistikos operacijos            | Kurkite statistines operacijas.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Tiekėjo banko pavedimas            | Kurkite paprastojo vekselio pavedimo failą, kurį bus galima siųsti į jūsų organizacijos banką.                                                                                                                                                                                                                                                                      | Pavedimų žurnalas                                             |
| Išmoka tiekėjui               | Kurkite išmokų tiekėjui operacijas.                                                                                                                                                                                                                                                                                                                    | Mokėjimų žurnalas                                                |
| Tiekėjo išduoti paprastieji vekseliai       | Sudarykite tiekėjo paprastuosius vekselius kaip mokėjimo metodą. Norėdami naudoti šį žurnalo tipą, puslapyje **Mokėjimo metodai – tiekėjai** išvalykite parinktį **Kurti ir registruoti išdavimų žurnalą automatiškai registruojant sąskaitas faktūras**.                                                                                                                                          | Išduoti paprastųjų vekselių žurnalą                                   |
| Tiekėjų SF telkinys be registravimo | Sukurkite tiekėjo SF operacijas, kurios dar neužregistruotos laikino gavimo sąskaitoje.                                                                                                                                                                                                                                                             | Tiekėjo SF telkinys be registravimo informacijos                  |
| Tiekėjo SF telkinys               | Kurkite tiekėjų SF telkinių operacijas.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Tiekėjo SF registravimas          | Registruokite žurnale esančius tiekėjo SF.                                                                                                                                                                                                                                                                                                                 | SF žurnalas                                                |
| Iš naujo tiekėjo išduotas paprastasis vekselis     | Pakartotinai išduokite paprastąjį vekselį, kurį prieš tai apmokėjo jūsų organizacijos bankas.                                                                                                                                                                                                                                                                      | Iš naujo išrašyti paprastųjų vekselių žurnalą                                 |
| Tiekėjo sudengtas paprastasis vekselis     | Kurkite tiekėjo sudengtų paprastųjų vekselių operacijas.                                                                                                                                                                                                                                                                                                          | Sudengti paprastųjų vekselių žurnalą                                 |






