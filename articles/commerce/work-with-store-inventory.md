---
title: Parduotuvės atsargų valdymas
description: Šioje temoje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 293040ccbe99c07b15373b92d64d086227de9d3f09c8feba700648b320cd8c74
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762553"
---
# <a name="commerce-inventory-management"></a>„Commerce“ inventoriaus valdymas

[!include [banner](includes/banner.md)]

Jums dirbant su inventoriumi „Microsoft Dynamics 365 Commerce“ ir naudojant bet kurią iš „Commerce“ programų sujungtų su „Commerce Scale Unit“ (CSU), svarbu žinoti, kad užsakymo apdorojimo logika CSU suteikia apribotą palaikymą kai kurioms inventoriaus dimensijoms ir kai kuriems inventoriaus prekės tipams. „Commerce“ programos nepalaiko viso intervalo prekių konfigūravimo galimybių, kurios yra prieinamos per prekės konfigūravimo parinktis „Dynamics 365 Supply Chain Management“.

„Commerce“ programos veikiančios CSU nepalaiko tolesnių produkto dimensijų ir prekės konfigūravimų:

- Produkto dimensijos ir KS prekių (išskyrus mažmeninės prekybos rinkinio produktus, kurie naudoja kai kuriuos KS sistemos komponentus) konfigūracija
- Esamo svorio prekės
- Versijos produkto dimensijos kontroliuojamos prekės

„Commerce“ programos veikiančios CSU nepalaiko tolesnių palaikymo sekimo dimensijų:
- Savininko dimensija

- Prekybos vietos (POS) programa gali pasiūlyti ribotą palaikymą tolesnėms dimensijoms. POS gali automatiškai įvesti kai kurias dimensijas į inventoriaus transakcijas pagal sandėlio ar parduotuvės nustatymų konfigūravimus. POS visiškai nepalaikys dimensijų taip, kad jos būtų palaikomos, jei prekybos transakcija rankiniu būdu įvedama į „Commerce“ būstinę. 

- **Sandėlio vieta** – kai vartotojai naudoja naujas [gavimo operacijos](./pos-inbound-inventory-operation.md) ir [siuntimo operacijos](./pos-outbound-inventory-operation.md) EKA operacijas, jie gali pasirinkti sandėlio atsargų vietą, į kurią būtų galima gauti prekes arba iš kurios būtų galima siųsti siunčiamo perkėlimo užsakymo prekes. Jei jie naudoja seną operaciją **Paėmimas ir gavimas**, gavimo ir siuntimo perkėlimo užsakymams galimas ribotas vietos valdymo palaikymas. Palaikymas galimas tik tada, jei buvo įjungta prekės ir parduotuvės sandėlio parinktis **Naudoti sandėlio valdymo procesą**. Šiuo metu atsargų vietos negalima naudoti su operacija **Inventorizacija** arba operacija **Atsargų peržvalga**.

- **Numerio lentelė** – numerio lentelės taikomos tik tada, kai įjungta prekės ir parduotuvės sandėlio parinktis **Naudoti sandėlio valdymo procesą**. EKA atveju, jei atsargos gaunamos į parduotuvės sandėlį, naudojant operaciją **Gavimo operacija** arba operaciją **Paėmimas ir gavimas**, kai sandėlio valdymo procesas įjungtas, ir jei vieta, į kurią buvo pasirinkta gauti prekę, yra susiejama su vietos profiliu, kuriam reikalinga numerio lentelės kontrolė, EKA programa sistemiškai taikys numerio lentelę gavimo eilutei. EKA vartotojai negali keisti arba tvarkyti šių numerio lentelės duomenų. Jei būtinas visapusiškas numerio lentelės valdymas, rekomenduojame parduotuvei naudoti [sandėliavimo programą](../supply-chain/warehousing/install-configure-warehousing-app.md) arba biuro klientą šių prekių priėmimui valdyti.

- **Serijos numeris** – EKA programa reikia ribotą palaikymą vienam serijos numeriui registruoti pardavimo operacijos eilutėje tuose užsakymuose, kurie yra sukurti EKA ir turi serijos prekių. Šis serijos numeris nėra patikrintas pagal užregistruotus atsargose jau esančius serijos numerius. Jei pardavimo užsakymas sukurtas skambučių centro kanale arba įvykdytas per įmonės išteklių planavimo (ERP) modulį, ir keli serijos numeriai užregistruojami vienoje pardavimo eilutėje ERP vykdymo proceso metu, tie serijos numeriai negali būti taikomi arba tikrinami, jei apdorojamas EKA užsakymo grąžinimas. Kai atsargos gaunamos naudojant operaciją **Gavimo operacija**, vartotojai gali [užregistruoti arba patvirtinti gautus serijos numerius](./pos-serialized-items.md).

- **Paketo ID** - POS programa suteikia ribotą paramą pareiškimo publikavimo metu, jei paketo kontroliuojama prekė yra parduodama, bet POS vartotojai negali nustatyti paketo ID, kuris buvo parduotas ar paimtas naudojant POS programą.

- **Atsargų būsena** – prekėms, kurios naudoja sandėlio valdymo procesą ir kurioms reikalinga atsargų būsena, šis būsenos laukas negali būti nustatytas arba modifikuotas EKA programoje. Numatytoji atsargų būsena, kuri yra apibrėžta parduotuvės sandėlio konfigūracijoje, naudojama, kai prekės gaunamos į atsargas.

> [!NOTE]
> Visos organizacijos privalo bandyti prekės konfigūravimus per „Commerce“ programas kūrimo ar testavimo aplinkose prieš prekių konfigūravimų talpinimą į gamybos aplinkas. Testuokite savo prekes naudodami jas siekiant atlikti reguliarias grynųjų ir paėmimo prekybos transakcijas POS ir sukurti kliento užsakymus (jei taikoma) per POS, skambučių centrą ar el. komerciją siekiant patvirtinti, kad jos yra visiškai palaikomos. Taip pat prieš diegdami bet kokias naujas prekių konfigūracijas turite patikrinti EKA vykdymo ir atsargų procesus (pvz., atsargų gavimo ir užsakymų įvykdymo operacijas), kad įsitikintumėte, jog EKA programa gali juos palaikyti. Testavimas turi apimti viso pareiškimo/užsakymo publikavimo proceso vykdymą jūsų testavimo aplinkoje ir patvirtinti, kad nėra jokių problemų, kurios gali atsitikti, kai užsakymai šioms prekėms yra kuriami ir publikuojami „Commerce“ štabe.
>
> Jei prekės yra konfigūruojamas taip, kad nėra palaikomos „Commerce“ programose ir atitinkamas testavimas nėra atliekamas, duomenų klaidos nėra paprastai ištaisomos ir negali būti ištaisytos jokiais būdais.

## <a name="purchase-orders"></a>Pirkimo užsakymai

Pirkimo užsakymai kuriami „Commerce“ pagrindiniame komponente. Jei parduotuvės sandėlis įtrauktas į pirkimo užsakymo antraštę arba pirkimo užsakymo eilutes, eilutes parduotuvėje galima gauti naudojant EKA operaciją [Gavimo operacija](./pos-inbound-inventory-operation.md). 

## <a name="transfer-orders"></a>Perkėlimo užsakymai

Perkėlimo užsakymai gali būti kuriami „Commerce“ pagrindiniame komponente arba EKA operaciją [Gavimo operacija](./pos-inbound-inventory-operation.md) arba [Siuntimo operacija](./pos-outbound-inventory-operation.md). Norėdami kurti perkėlimo užsakymo užklausą, kad atsargos būtų siunčiamos į parduotuvę iš kitos sandėlio ar parduotuvės vietos, naudokite EKA operaciją **Gavimo operacija**. Norėdami kurti perkėlimo užsakymo užklausą, kad atsargos būtų siunčiamos iš parduotuvės į kitą sandėlio ar parduotuvės vietą, naudokite EKA operaciją **Siuntimo operacija**. Sukūrus parduotuvės perkėlimo užsakymą, ta parduotuvė gali valdyti perkėlimo užsakymo atsargų gavimą per EKA operaciją **Gavimo operacija**. Jei parduotuvė siunčia atsargas į kitą vietą, parduotuvės siuntimo procesui valdyti naudojama EKA operacija **Siuntimo operacija**.

## <a name="stock-counts"></a>Inventorizacijos

Inventorizacijos gali būti planinės arba neplaninės. Suplanuoti inventorizacijos kuriamos „Commerce“ pagrindiniame komponente sukuriant inventorizacijos žurnalo dokumentą, susietą su parduotuvės sandėliu. Šis žurnalas nurodo prekes, kurios turi būti inventorizuotos. Tada parduotuvė gali pasiekti šiuos iš anksto apibrėžtus inventorizacijos žurnalus ir veikti pagal juos naudodama EKA operaciją **Inventorizacija**. Kai parduotuvės vartotojai naudoja EKA operaciją **Inventorizacija**, jie inicijuoja nesuplanuotą inventorizaciją, nes ji yra reikalinga. Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo. EKA atlikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Tada pagrindiniame biure inventorizacija turi būti patikrinta ir užregistruota „Commerce“ pagrindiniame komponente kaip atskiras veiksmas.

## <a name="inventory-lookup"></a>Atsargų peržvalga

Dabar keliose parduotuvėse ir sandėliuose turimą produktų kiekį galima peržiūrėti puslapyje **Atsargų peržvalga**. Neskaitant dabartinio turimo kiekio, galima pamatyti kiekvienos parduotuvės būsimus prieinamų atsargų (ATP) kiekius. Pasirinkite parduotuvę, kurios ATP kiekius norite peržiūrėti, tada pasirinkite **Rodyti parduotuvės pasiekiamumą**. Informacijos apie galimas konfigūracijos parinktis žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](./calculated-inventory-retail-channels.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]