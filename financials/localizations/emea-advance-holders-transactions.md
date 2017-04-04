---
title: "Išankstinio savininko operacijos"
description: "Sužinokite, kaip dirbti su išankstinio turėtojo sandorių Microsoft Dynamics 365 operacijoms."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262554
ms.assetid: 84ff97bb-ae21-4d6d-8160-9325f64134ce
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: c819fbbb4a68dd5b8b192416fedb34827bbf3823
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holder-transactions"></a>Išankstinio savininko operacijos

Sužinokite, kaip dirbti su išankstinio turėtojo sandorių Microsoft Dynamics 365 operacijoms.

Šiems darbuotojams, kurie yra iš anksto turėtojai gali būti registruojamos naudojant išankstinio turėtojo sąskaitų operacijas. Darbuotojo ID, kuris nurodytas kiekvienos išankstinio leidimo galima stebėti visus išankstinio turėtojo operacijas. Šis numeris perrašomas kaip sąskaitos numeris, skirtas iš anksto turėtojo sandorių, **bendrųjų žurnalų** ir **iš anksto savininko sandoriai** puslapius.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Kurti ir registruoti pirkimo užsakymas, informacija apie iš anksto
Daugiau bendros informacijos apie pirkimo užsakymus, rasite [pirkimo užsakymų apžvalga](/manufacturing/procurement/purchase-order-overview). Jei tiekėjo SF yra sukurtas ir paskelbtas su informacija apie iš anksto, išankstinis savininkas likučiai registruojama į darbuotojo balans vietoj tiekėjo balansas. Norėdami pridėti iš anksto informacija apie pirkimo užsakymą, atlikite šiuos veiksmus:

-   – Į **mokėjimo sąlygos** lauke, **kaina ir nuolaida**, skyriuje mokėjimo terminas. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).-->Pasirinkite mokėjimo terminas, kuris yra į **iš anksto turėtojo** pasirinktas variantas su **mokėjimo sąlygos** puslapis. Daugiau informacijos apie mokėjimo išankstinių savininkų sąlygos nustatymą, peržiūrėkite [iš anksto turėtojams](emea-advance-holders.md).
-   – Į **išankstinis savininkas** lauko, **kaina ir nuolaida** FastTab, pasirinkite išankstinio turėtojo pirkimo užsakyme.

Pirkimo užsakymo registravimo procesas sukuria du tiekėjo operacijų su priešinga sumas ir viena iš anksto turėtojas operacija. Be išankstinio savininko duomenis, tik vieno tiekėjo operacijos sukuriamos.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Išankstinis savininkas balansus, per banką
Kai jūs balansus iš anksto turėtojas per banką, išankstinio turėtojo likučių uždarymo žurnalo įrašus sukuriami bendrajame žurnale. Jūs galite nustatyti žurnalo ir banko kodas į **iš anksto laikikliai** skirsnis, **sudaro mokėtinų sumų parametrai** puslapis. Daugiau informacijos rasite [iš anksto turėtojams](emea-advance-holders.md). Norėdami uždaryti išankstinio turėtojo balansas per banką, atidaryti **mokėtinos sumos**&gt;**iš anksto turėtojams**&gt;**iš anksto laikikliai**. Spustelėkite į **balansas** Naujintiveiksmų srityje, o tada – **arti per banko**. Įveskite šią informaciją į **arti per banką** puslapis.

| Laukas                    | aprašymas |
|------------------------------|-------------------|
| **Date of payment**          | Įveskite datą, kuri turėtų būti registruojamos mokėjimo.|
| **Pervedamą sumą** | Įveskite likučio suma, o pabaigos. Suma, kuri yra nurodyta ir **suma** lauko į **balansas** forma rodoma pagal numatytuosius nustatymus. |
| **Automatic**                | Pasirinkite į **Automatinis** žymės langelį kurti ir registruoti žurnalą, yra iš anksto nustatytu ir **sąskaitos mokėtinų sumų parametrai** puslapis.|

## <a name="settle-advance-holder-balances-via-cash"></a>Per grynųjų pinigų avanso turėtojas balansus
Kai jūs balansus iš anksto turėtojas per grynųjų pinigų, išankstinio turėtojo likučių uždarymo žurnalo įrašus sukuriami slydimo žurnale. Galite nustatyti kodą ir grynus pinigus į **iš anksto turėtojams** spustelėkite į **sudaro mokėtinų sumų parametrai** puslapis. Daugiau informacijos rasite [iš anksto turėtojams](emea-advance-holders.md). Norėdami uždaryti išankstinio turėtojo per grynųjų pinigų balansas, atidarykite **mokėtinos sumos**&gt;**iš anksto laikikliai**&gt;**iš anksto laikikliai**. Spustelėkite į **balansas** Naujintiveiksmų srityje, o tada – **arti per grynųjų pinigų**. Įveskite šią informaciją į **arti per grynųjų pinigų** puslapis.

| Laukas                    | aprašymas
|------------------------------|-----------------|
| **Date of payment**          | Įveskite datą, kuri turėtų būti registruojamos mokėjimo.|
| **Pervedamą sumą** | Įveskite likučio suma, o pabaigos. Suma, kuri yra nurodyta ir **suma** lauko į **balansas** forma rodoma pagal numatytuosius nustatymus. |
| **Automatic**                | Pasirinkite į **Automatinis** žymės langelį, jei norite sukurti ir automatiškai registruoti žurnalą, yra iš anksto nustatytu ir **sąskaitos mokėtinų sumų parametrai** puslapis.     |

Po slydimo leidinyje bus apdorotas, jei suma, **pervedamą sumą** srityje buvo neigiamas, išmokėjimo kvito susidaro išankstinio leidimo, kai likučiai uždaromi. Jei suma, **pervedamą sumą** srityje buvo teigiamas, susidaro kompensacijų kvitų.


