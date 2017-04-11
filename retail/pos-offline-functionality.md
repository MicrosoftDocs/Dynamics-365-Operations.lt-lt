---
title: "POS autonominės funkcijos"
description: "Šiame straipsnyje pateikiama informacija apie „Retail Modern POS“ autonominį režimą, kai EKA įrenginiai automatiškai perjungiami iš kanalo duomenų bazės į autonominę duomenų bazę, jei mažmeninės prekybos serveris nepasiekiamas. Šiame straipsnyje taip pat pateikiama bendroji autonominio režimo nustatymo informacija ir paaiškinta apie duomenų sinchronizavimą tarp autonominės duomenų bazės ir kanalo duomenų bazės."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS autonominės funkcijos

Šiame straipsnyje pateikiama informacija apie „Retail Modern POS“ autonominį režimą, kai EKA įrenginiai automatiškai perjungiami iš kanalo duomenų bazės į autonominę duomenų bazę, jei mažmeninės prekybos serveris nepasiekiamas. Šiame straipsnyje taip pat pateikiama bendroji autonominio režimo nustatymo informacija ir paaiškinta apie duomenų sinchronizavimą tarp autonominės duomenų bazės ir kanalo duomenų bazės.

<a name="overview"></a>Apžvalga
--------

Mažmeninės prekybos Šiuolaikinės pos, dėl pardavimo (PV) prietaisas patenka į atjungties režimu kai mažmeninės prekybos serveris neprieinamas. Todėl, jei prarandamas ryšys su serveriu, mažmeninė, mažmeninės prekybos šiuolaikinės EKA automatiškai persijungia su autonomine duomenų baze. Jei, vykdant pardavimo operaciją, duomenų užklausa nėra sėkminga per skirtojo laiko intervalą, kuris sukonfigūruotas autonominiame profilyje, „Retail Modern POS‟ automatiškai persijungia į autonominę duomenų bazę ir tęsia pardavimo operaciją. Kai POS įrenginys veikia autonominiu režimu, po pakartotinio bandymo prisijungti intervalo, kuris sukonfigūruotas autonominiame profilyje, „Retail Modern POS‟ mėgina prisijungti prie mažmeninės prekybos serverio. Pakartotinai prisijungti bandoma tik operacijos pradžioje.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>„Retail Modern POS‟ ryšio režimo nustatymas

„Retail Modern POS‟ antraštės būsena nurodo dabartinę ryšio būseną, o **Ryšio būsenos** lange rodoma paskutinio bandymo sinchronizuoti su autonomine duomenų baze būsena. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Rankinio perjungimo tarp internetinio ir autonominio režimų mygtuko kūrimas

Į „Retail Modern POS‟ galite pridėti mygtuką, skirtą rankiniu būdu perjungti tarp internetinio ir autonominio režimų. Sukurkite POS naudojimo mygtuką **917 – duomenų bazės ryšio būsena**. Kai „Retail Modern POS‟ prisijungęs prie mažmeninės prekybos serverio, šio mygtuko pavadinimas yra **Atsijungti**, o, kai modulis atsijungęs, mygtukas vadinasi **Prisijungti**. Šį mygtuką galite naudoti peržiūrėti ryšiui ir atsijungti nuo mažmeninės prekybos serverio arba prie jo prisijungti. [![Atsijungti mygtuką mažmeninės prekybos Šiuolaikinės pos](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Sąranka
Būtų įgalinta autonominių POS įrenginį (registras), nustatyti į **remti neprisijungęs** į **taip** ant į **registruotis** puslapis. Naujas kanalo duomenų bazės objekto yra sukurta ir įtrauktas į parduotuvės kanalo duomenų grupės. Tada, vykdydami visus reikiamus paskirstymo grafikus, generuokite autonominių duomenų bazių duomenų paketus. Be to, įdiegti NEINTERNETINĖ versija mažmeninės prekybos šiuolaikinės EKA. Diegimo procesas sukuria atjungta duomenų bazė. Be to, įdiegti Microsoft SQL Server 2014 m. Express jei to reikia. Autonominis duomenų sinchronizavimas prasideda pirmą kartą prisijungus prie „Retail Modern POS‟.

## <a name="data-synchronization"></a>Duomenų sinchronizavimas
Duomenų apsikeitimo valdymas naudojamas bendriesiems duomenims siųsti į autonominę duomenų bazę. Pagal numatytąsias nuostatas, vykdant paskirstymo grafiką, duomenų pakeitimai siunčiami tiek į kanalo duomenų bazę, tiek į autonominę duomenų bazę. „Retail Modern POS‟ modulyje yra „async sync‟ biblioteka, kuri atsisiunčia visus galimus duomenų paketus ir juos įterpia į autonominę duomenų bazę. Jei kokios nors operacijos sukuriamos autonomiškai, „Retail Modern POS‟ jas įkelia į mažmeninės prekybos serverį, kad jas būtų galima įterpti į kanalo duomenų bazę. Autonominis duomenų sinchronizavimas gali vykti tik tada, jei veikia „Retail Modern POS‟. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


