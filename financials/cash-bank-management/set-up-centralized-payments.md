---
title: "Centralizuotų mokėjimų nustatymas"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Centralizuotų mokėjimų nustatymas



Atlikite šiuos veiksmus ir parengti mokėjimų vieno juridinio subjekto vardu kiti juridiniai asmenys, organizacijos. Prieš pradėdami, privalo pildyti tokį nustatymą:

-   Sukurkite juridinius subjektus.
-   Nustatykite DK parametrus ir sąskaitų planus.
-   Nustatykite mokėtinų sumų parametrus ir gautinų sumų parametrus (priklausomai nuo to, kokie moduliai naudoja centralizuotus mokėjimus).
-   Sukurkite vidinę įmonės apskaitą.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Centralizuotų mokėjimų organizacijos hierarchijos nustatymas
Turite nustatyti centralizuotų mokėjimų organizacijos hierarchiją. Ta pati organizacijos hierarchija naudojama apdorojant centralizuotus tiekėjų mokėjimus ir centralizuotus klientų mokėjimus. **Pastaba:** Centralizuotų mokėjimų hierarchijos struktūra nėra svarbi. Bet koks hierarchijoje esantis juridinis subjektas galės apdoroti mokėjimus bet kokio kito hierarchijoje esančio juridinio subjekto vardu. Puslapyje **Organizacijos hierarchijos** galite sukurti naują organizacijos hierarchiją.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Centralizuotiems mokėjimams skirtos vidinės įmonės sąskaitos kūrimas
Kai dabartinio juridinio subjekto mokėjimo operacijos sudengiamos pagal kitų juridinių subjektų SF, kiekvienam juridiniam subjektui sukuriamos atitinkamos mokėjimo ir mokėjimo priėmimo operacijos. Reikia nurodyti juridinį subjektą, kuriame užregistruotos visos taikomos mokėjimo nuolaidos ir realizuoto pelno arba patirto nuostolio sumos. Prieš pradėdami nuspręskite, kurį juridinį subjektą naudosite tiekėjo ir kliento mokėjimams apdoroti. Jei vienas juridinis subjektas apdoroja tiekėjo mokėjimus, o kitas juridinis subjektas apdoroja kliento mokėjimus, turite pereiti į kiekvieną juridinį subjektą. Dėl to **tvarkant vidinių įmonių apskaitą** puslapyje, galite pasirinkti įrašą vidinės įmonės santykiai juridinį asmenį, kuris jums bus apdoroti mokėjimus vardu. Dėl to **centralizuoti mokėjimai** skirtuką, galite pasirinkti, ar po grynųjų pinigų nuolaidas (arba kita operacija, kuri sumažina tiekėjo sąskaitos balansą) juridinio asmens ar juridinio asmens sąskaitą faktūrą (arba kita operacija, kuri padidina tiekėjo sąskaitos balansas). Šis pasirinkimas veikia kartu su puslapių **Mokėtinų sumų parametrai** ir **Gautinų sumų parametrai** lauku **Mokėjimo nuolaidos administravimas**. Leistiniems permokėjimų ir centų skirtumo nuokrypiams naudojamas su mokėjimu susijusio juridinio subjekto parametras. Leistiniems neprimokėjimų ir centų skirtumo nuokrypiams naudojamas SF juridinio subjekto parametras.

## <a name="map-vendor-accounts-across-legal-entities"></a>Juridinių subjektų tiekėjų sąskaitų susiejimas
Jei mokate tiekėjui iš vieno juridinio subjekto ir norite pasirinkti to tiekėjo SF kituose juridiniuose subjektuose, turite būti tikri, kad visos atitinkamos tiekėjo sąskaitos kiekviename juridiniame subjekte naudoja tą patį adresų knygelės ID. Jei gaunate mokėjimą iš kliento, kuris moka SF daugiau negu viename juridiniame subjekte, turite užtikrinti, kad kiekviename juridiniame subjekte visos atitinkamo kliento sąskaitos naudos tokį patį adresų knygelės ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Nustatykite centralizuotų mokėjimų registravimo šablonus
Kai sukuriate mokėjimą viename juridiniame subjekte, kuris sudengia SF kituose juridiniuose subjektuose, abiejų juridinių subjektų registravimo šablonų ID turi būti tokie patys. Siekdami užtikrinti, kad mokėjimai būtų sukurti tinkamai, kiekviename SF juridiniame subjekte nustatykite registravimo profilį, kuris atitinka mokėjimo juridiniame subjekte naudojamus registravimo profilius. Pereiti į pirmą juridinio asmens sąskaitos, o tada ant to **tiekėjo registravimo šablonus** puslapyje, galite kurti naują registravimo šabloną arba redaguoti esamą registravimo šablonas. Pasirinkimus, kad jūs padaryti sąskaitą-faktūrą juridinio asmens registravimo šabloną nereikia suderinti registravimo šabloną juridinio asmens mokėjimo nustatymą.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Nustatykite centralizuotų mokėjimų mokėjimo metodus
Kai sukuriate mokėjimą viename juridiniame subjekte, kuris sudengia SF kituose juridiniuose subjektuose, abiejų juridinių subjektų mokėjimo būdų ID turi būti tokie patys. Siekdami užtikrinti, kad mokėjimai būtų sukurti tinkamai, nustatykite kiekvieno SF juridinio subjekto mokėjimo būdą, kuris atitiktų mokėjimo juridiniame subjekte naudojamus mokėjimo būdus. Pereikite į pirmą SF juridinį subjektą, tada puslapyje **Mokėjimo būdai **galite sukurti naują mokėjimo būdą arba redaguoti esamą mokėjimo būdą. Jūsų atliekami SF juridinio subjekto mokėjimo būdo pasirinkimai neturi atitikti mokėjimo juridinio subjekto mokėjimo būdo nustatymų.

## <a name="set-up-default-descriptions"></a>Numatytųjų aprašų nustatymas
Galite nustatyti numatytuosius vidinės įmonės sudengimo kvitų aprašus. Numatytasis aprašas įtraukiamas į operacijas, mokėtinas iki ir nuo tam tikros datos, visos įmonės sudengimo proceso metu. Puslapyje **Numatytieji aprašymai** pasirinkdami kalbą ir įvesdami tekstą galite sukurti naujus aprašymus, tinkamus, kai atliekamas **Vidinės įmonės klientų sudengimas **ir **Vidinės įmonės tiekėjų sudengimas**.


