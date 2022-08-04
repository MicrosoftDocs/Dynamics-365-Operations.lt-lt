---
title: Centralizuotų mokėjimų nustatymas
description: Atlikite šiuos veiksmus, norėdami pasiruošti apdoroti mokėjimus viename juridiniame subjekte kitų jūsų organizacijos juridinių subjektų vardu.
author: angelad116
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5474f7a698f5c055717e6c5d23b95fe0ecce8961
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151677"
---
# <a name="set-up-centralized-payments"></a>Centralizuotų mokėjimų nustatymas

[!include [banner](../includes/banner.md)]

Atlikite šiuos veiksmus, norėdami pasiruošti apdoroti mokėjimus viename juridiniame subjekte kitų jūsų organizacijos juridinių subjektų vardu. Prieš pradėdami turite įvykdyti šias nustatymo procedūras:

-   Sukurkite juridinius subjektus.
-   Nustatykite DK parametrus ir sąskaitų planus.
-   Nustatykite mokėtinų sumų parametrus ir gautinų sumų parametrus (priklausomai nuo to, kokie moduliai naudoja centralizuotus mokėjimus).
-   Sukurkite vidinę įmonės apskaitą.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Centralizuotų mokėjimų organizacijos hierarchijos nustatymas
Turite nustatyti centralizuotų mokėjimų organizacijos hierarchiją. Ta pati organizacijos hierarchija naudojama apdorojant centralizuotus tiekėjų mokėjimus ir centralizuotus klientų mokėjimus. **Pastaba:** Centralizuotų mokėjimų hierarchijos struktūra nėra svarbi. Bet koks hierarchijoje esantis juridinis subjektas galės apdoroti mokėjimus bet kokio kito hierarchijoje esančio juridinio subjekto vardu. Puslapyje **Organizacijos hierarchijos** galite sukurti naują organizacijos hierarchiją. Lauke **Tikslas** turite pasirinkti reikšmę **Centralizuoti mokėjimai**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Centralizuotiems mokėjimams skirtos vidinės įmonės sąskaitos kūrimas
Kai dabartinio juridinio subjekto mokėjimo operacijos sudengiamos pagal kitų juridinių subjektų SF, kiekvienam juridiniam subjektui sukuriamos atitinkamos mokėjimo ir mokėjimo priėmimo operacijos. Reikia nurodyti juridinį subjektą, kuriame užregistruotos visos taikomos mokėjimo nuolaidos ir realizuoto pelno arba patirto nuostolio sumos. Prieš pradėdami nuspręskite, kurį juridinį subjektą naudosite tiekėjo ir kliento mokėjimams apdoroti. Jei vienas juridinis subjektas apdoroja tiekėjo mokėjimus, o kitas juridinis subjektas apdoroja kliento mokėjimus, turite pereiti į kiekvieną juridinį subjektą. Puslapyje **Vidinių įmonių apskaita** galite pasirinkti juridinio subjekto, kurio vardu apdorosite mokėjimus, vidinės įmonės ryšių įrašą. 

Skirtuke **Centralizuoti mokėjimai** galite pasirinkti, ar mokėjimo nuolaidų registravimą taikyti su mokėjimu (arba kita operacija, kuri sumažina tiekėjo sąskaitos likutį) susijusiam juridiniam subjektui, ar su SF (arba kita operacija, kuri padidina tiekėjo sąskaitos likutį) susijusiam juridiniam subjektui. Šis pasirinkimas veikia kartu su puslapių **Mokėtinų sumų parametrai** ir **Gautinų sumų parametrai** lauku **Mokėjimo nuolaidos administravimas**. Leistiniems permokėjimų ir centų skirtumo nuokrypiams naudojamas su mokėjimu susijusio juridinio subjekto parametras. Leistiniems neprimokėjimų ir centų skirtumo nuokrypiams naudojamas SF juridinio subjekto parametras.

## <a name="map-vendor-accounts-across-legal-entities"></a>Juridinių subjektų tiekėjų sąskaitų susiejimas
Jei mokate tiekėjui iš vieno juridinio subjekto ir norite pasirinkti to tiekėjo SF kituose juridiniuose subjektuose, turite būti tikri, kad visos atitinkamos tiekėjo sąskaitos kiekviename juridiniame subjekte naudoja tą patį adresų knygelės ID. Jei gaunate mokėjimą iš kliento, kuris moka SF daugiau negu viename juridiniame subjekte, turite užtikrinti, kad kiekviename juridiniame subjekte visos atitinkamo kliento sąskaitos naudos tokį patį adresų knygelės ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Nustatykite centralizuotų mokėjimų registravimo šablonus
Kai sukuriate mokėjimą viename juridiniame subjekte, kuris sudengia SF kituose juridiniuose subjektuose, abiejų juridinių subjektų registravimo šablonų ID turi būti tokie patys. Siekdami užtikrinti, kad mokėjimai būtų sukurti tinkamai, kiekviename SF juridiniame subjekte nustatykite registravimo profilį, kuris atitinka mokėjimo juridiniame subjekte naudojamus registravimo profilius. Pereikite į pirmą sąskaitos faktūros juridinį subjektą, tada puslapyje **Tiekėjų registravimo šablonai** galite sukurti naują registravimo šabloną arba redaguoti esamą registravimo šabloną. Jūsų atliekami SF juridinio subjekto registravimo šablono pasirinkimai neturi atitikti to, kaip registravimo šablonas nustatomas su mokėjimu susijusiame juridiniame subjekte.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Nustatykite centralizuotų mokėjimų mokėjimo metodus
Kai sukuriate mokėjimą viename juridiniame subjekte, kuris sudengia SF kituose juridiniuose subjektuose, abiejų juridinių subjektų mokėjimo būdų ID turi būti tokie patys. Siekdami užtikrinti, kad mokėjimai būtų sukurti tinkamai, nustatykite kiekvieno SF juridinio subjekto mokėjimo būdą, kuris atitiktų mokėjimo juridiniame subjekte naudojamus mokėjimo būdus. Pereikite į pirmą SF juridinį subjektą, tada puslapyje **Mokėjimo būdai** galite sukurti naują mokėjimo būdą arba redaguoti esamą mokėjimo būdą. Jūsų atliekami SF juridinio subjekto mokėjimo būdo pasirinkimai neturi atitikti mokėjimo juridinio subjekto mokėjimo būdo nustatymų.

## <a name="set-up-default-descriptions"></a>Numatytųjų aprašų nustatymas
Galite nustatyti numatytuosius vidinės įmonės sudengimo kvitų aprašus. Numatytasis aprašas įtraukiamas į operacijas, mokėtinas iki ir nuo tam tikros datos, visos įmonės sudengimo proceso metu. Puslapyje **Numatytieji aprašymai** pasirinkdami kalbą ir įvesdami tekstą galite sukurti naujus aprašymus, tinkamus, kai atliekamas **Vidinės įmonės klientų sudengimas** ir **Vidinės įmonės tiekėjų sudengimas**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
