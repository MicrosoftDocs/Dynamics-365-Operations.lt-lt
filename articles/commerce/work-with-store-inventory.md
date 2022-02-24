---
title: Parduotuvės atsargų valdymas
description: Šioje temoje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414361"
---
# <a name="store-inventory-management"></a>Parduotuvės atsargų valdymas

[!include [banner](includes/banner.md)]

Kai dirbate su atsargomis programoje „Microsoft Dynamics 365 Commerce“ ir naudojate elektroninio kasos aparato (EKA) programą, svarbu žinoti, kad EKA teikia ribotą kai kurių atsargų dimensijų ir kai kurių atsargų elementų prekių tipų palaikymą. EKA programa nepalaiko visų prekių konfigūracijos galimybių, kurios pasiekiamos naudojant prekių konfigūravimo parinktis programoje „Dynamics 365 Supply Chain Management“.

Šiuo metu EKA sprendimas nepalaiko toliau nurodytų produktų dimensijų ir prekių konfigūracijų.

- Produkto dimensijos ir KS prekių (išskyrus mažmeninės prekybos rinkinio produktus, kurie naudoja kai kuriuos KS sistemos komponentus) konfigūracija
- Esamo svorio prekės
- Versijos produkto dimensijos kontroliuojamos prekės

Šiuo metu EKA programa nepalaiko toliau nurodytų dimensijų EKA.

- Paketo sekimo dimensija
- Savininko dimensija

EKA teikia ribotą toliau nurodytų dimensijų palaikymą. Kitaip tariant, EKA gali automatiškai įvesti kai kurias iš šių dimensijų į atsargų operacijas, atsižvelgiant į sandėlio / parduotuvės sąrankos konfigūraciją. EKA dimensijų išsamiai nepalaikys taip, kaip jos yra palaikomos, jei pardavimo operacija bus neautomatiniu būdu įvesta „Commerce“ pagrindiniame komponente. 

- **Sandėlio vieta** – kai vartotojai naudoja naujas [gavimo operacijos](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ir [siuntimo operacijos](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) EKA operacijas, jie gali pasirinkti sandėlio atsargų vietą, į kurią būtų galima gauti prekes arba iš kurios būtų galima siųsti siunčiamo perkėlimo užsakymo prekes. Jei jie naudoja seną operaciją **Paėmimas ir gavimas**, gavimo ir siuntimo perkėlimo užsakymams galimas ribotas vietos valdymo palaikymas. Palaikymas galimas tik tada, jei buvo įjungta prekės ir parduotuvės sandėlio parinktis **Naudoti sandėlio valdymo procesą**. Šiuo metu atsargų vietos negalima naudoti su operacija **Inventorizacija** arba operacija **Atsargų peržvalga**.
- **Numerio lentelė** – numerio lentelės taikomos tik tada, kai įjungta prekės ir parduotuvės sandėlio parinktis **Naudoti sandėlio valdymo procesą**. EKA atveju, jei atsargos gaunamos į parduotuvės sandėlį, naudojant operaciją **Gavimo operacija** arba operaciją **Paėmimas ir gavimas**, kai sandėlio valdymo procesas įjungtas, ir jei vieta, į kurią buvo pasirinkta gauti prekę, yra susiejama su vietos profiliu, kuriam reikalinga numerio lentelės kontrolė, EKA programa sistemiškai taikys numerio lentelę gavimo eilutei. EKA vartotojai negali keisti arba tvarkyti šių numerio lentelės duomenų. Jei būtinas visapusiškas numerio lentelės valdymas, rekomenduojame parduotuvei naudoti [sandėliavimo programą](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) arba biuro klientą šių prekių priėmimui valdyti.
- **Serijos numeris** – EKA programa reikia ribotą palaikymą vienam serijos numeriui registruoti pardavimo operacijos eilutėje tuose užsakymuose, kurie yra sukurti EKA ir turi serijos prekių. Šis serijos numeris nėra patikrintas pagal užregistruotus atsargose jau esančius serijos numerius. Jei pardavimo užsakymas sukurtas skambučių centro kanale arba įvykdytas per įmonės išteklių planavimo (ERP) modulį, ir keli serijos numeriai užregistruojami vienoje pardavimo eilutėje ERP vykdymo proceso metu, tie serijos numeriai negali būti taikomi arba tikrinami, jei apdorojamas EKA užsakymo grąžinimas. Kai atsargos gaunamos naudojant operaciją **Gavimo operacija**, vartotojai gali [užregistruoti arba patvirtinti gautus serijos numerius](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Atsargų būsena** – prekėms, kurios naudoja sandėlio valdymo procesą ir kurioms reikalinga atsargų būsena, šis būsenos laukas negali būti nustatytas arba modifikuotas EKA programoje. Numatytoji atsargų būsena, kuri yra apibrėžta parduotuvės sandėlio konfigūracijoje, naudojama, kai prekės gaunamos į atsargas.

> [!NOTE]
> Visos organizacijos turi patikrinti prekių konfigūracijas naudodamos EKA programavimo ar tikrinimo aplinkoje prieš diegdamos jas gamybos aplinkose. Tikrinkite prekes panaudodami jas įprastoms grynųjų pinigų pardavimo operacijoms atlikti ir kurkite klientų užsakymus (jei taikoma) naudodami EKA. Taip pat prieš diegdami bet kokias naujas prekių konfigūracijas turite patikrinti EKA vykdymo ir atsargų procesus (pvz., atsargų gavimo ir užsakymų įvykdymo operacijas), kad įsitikintumėte, jog EKA programa gali juos palaikyti. Tikrinimo metu jūsų tikrinimo aplinkoje turi būti atliktas visas išrašų registravimo procesas ir turi būti patikrinta, ar kuriant ir „Commerce“ pagrindiniame komponente skelbiant šių prekių užsakymus nekyla problemų.
>
> Jei EKA programa nepalaiko prekių konfigūracijos ir atitinkami patikrinimai nėra atlikti, užsakymo kūrimo proceso metu gali kilti problemų dėl duomenų gedimų, kurie nėra lengvai ištaisomi arba kuriems netaikomas standartinis produkto palaikymas.

## <a name="purchase-orders"></a>Pirkimo užsakymai

Pirkimo užsakymai kuriami „Commerce“ pagrindiniame komponente. Jei parduotuvės sandėlis įtrauktas į pirkimo užsakymo antraštę arba pirkimo užsakymo eilutes, eilutes parduotuvėje galima gauti naudojant EKA operaciją [Gavimo operacija](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation). 

## <a name="transfer-orders"></a>Perkėlimo užsakymai

Perkėlimo užsakymai gali būti kuriami „Commerce“ pagrindiniame komponente arba EKA operaciją [Gavimo operacija](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) arba [Siuntimo operacija](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation). Norėdami kurti perkėlimo užsakymo užklausą, kad atsargos būtų siunčiamos į parduotuvę iš kitos sandėlio ar parduotuvės vietos, naudokite EKA operaciją **Gavimo operacija**. Norėdami kurti perkėlimo užsakymo užklausą, kad atsargos būtų siunčiamos iš parduotuvės į kitą sandėlio ar parduotuvės vietą, naudokite EKA operaciją **Siuntimo operacija**. Sukūrus parduotuvės perkėlimo užsakymą, ta parduotuvė gali valdyti perkėlimo užsakymo atsargų gavimą per EKA operaciją **Gavimo operacija**. Jei parduotuvė siunčia atsargas į kitą vietą, parduotuvės siuntimo procesui valdyti naudojama EKA operacija **Siuntimo operacija**.

## <a name="stock-counts"></a>Inventorizacijos

Inventorizacijos gali būti planinės arba neplaninės. Suplanuoti inventorizacijos kuriamos „Commerce“ pagrindiniame komponente sukuriant inventorizacijos žurnalo dokumentą, susietą su parduotuvės sandėliu. Šis žurnalas nurodo prekes, kurios turi būti inventorizuotos. Tada parduotuvė gali pasiekti šiuos iš anksto apibrėžtus inventorizacijos žurnalus ir veikti pagal juos naudodama EKA operaciją **Inventorizacija**. Kai parduotuvės vartotojai naudoja EKA operaciją **Inventorizacija**, jie inicijuoja nesuplanuotą inventorizaciją, nes ji yra reikalinga. Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo. EKA alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Tada pagrindiniame biure inventorizacija turi būti patikrinta ir užregistruota „Commerce“ pagrindiniame komponente kaip atskiras veiksmas.

## <a name="inventory-lookup"></a>Atsargų peržvalga

Dabar keliose parduotuvėse ir sandėliuose turimą produktų kiekį galima peržiūrėti puslapyje **Atsargų peržvalga**. Neskaitant dabartinio turimo kiekio, galima pamatyti kiekvienos parduotuvės būsimus prieinamų atsargų (ATP) kiekius. Pasirinkite parduotuvę, kurios ATP kiekius norite peržiūrėti, tada pasirinkite **Rodyti parduotuvės pasiekiamumą**. Informacijos apie galimas konfigūracijos parinktis žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
