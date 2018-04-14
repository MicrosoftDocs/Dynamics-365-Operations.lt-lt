---
title: "Medžiagų išimčių matomumas"
description: "Šioje temoje aprašoma, kaip galima padidinti gamybos užsakymų ir paketinių užsakymų žaliavų išimčių matomumą."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: eca3141fc48aea24411524e5fc84686d9e4bfaa7
ms.contentlocale: lt-lt
ms.lasthandoff: 03/08/2018

---
# <a name="visibility-into-material-exceptions"></a>Medžiagų išimčių matomumas

[!INCLUDE [banner](../includes/banner.md)]

Darbo srities **Gamybos vietos valdymas** trys plytelės suteikia galimybę geriau matyti gamybos užsakymų ir paketinių užsakymų žaliavų išimtis.

- Neišleistos medžiagų eilutės, į kurias reikia atkreipti dėmesį
- Neapdorotos bangos, į kurias reikia atkreipti dėmesį
- Atidarytas sandėlio darbas, į kurį reikia atkreipti dėmesį

Visose trijose plytelėse komplektavimo specifikacijos (KS) eilučių ir formulės eilučių žaliavų data lyginama su darbo srities data, taip pat su parinkčių **Gamybos vienetas**, **Išteklių grupė** ir **Išteklius** filtrais, kurie nustatyti meniu **Mano darbo vietos konfigūravimas**. Pagal numatytuosius parametrus darbo srities data yra nustatyta į dabartinę datą, bet ją galite koreguoti.

Neišleistai KS eilutei arba formulės eilutei reikia skirti dėmesio, jei eilutės žaliavų data yra tokia pati arba ankstesnė nei darbo srities data, taip pat jei ji atitinka kriterijus, kurie nustatyti darbo srityje naudojant filtrus.

Tolesniame paveikslėlyje mėlyna juosta vaizduoja suplanuotą ištekliaus gamybos užduotį. Užduotis planuojama pradėti 2017 m. gegužės 1 d. (2017-05-01). Ši data yra žaliavų data. Kitaip tariant, medžiagos, priskirtos užduočiai KS ir formulės eilutėse, šią dieną turi būti paruoštos. Kita paveikslėlyje nurodyta data, 2017 m. gegužės 6 d. (2017-05–06), nurodo darbo srities datą. Šiame pavyzdyje žaliavų data yra ankstesnė už darbo srities datą. Todėl diena, kurią žaliavų suvartojimas turėjo prasidėti, jau praėjo ir KS bei formulės eilutės atitinka dėmesio skyrimo kriterijus.

![Gamybos užduoties pavyzdys, kuriame žaliavų data yra ankstesnė už darbo srities datą](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Neišleistos medžiagų eilutės, į kurias reikia atkreipti dėmesį

KS arba formulės eilutę galima išleisti į sandėlį trimis būdais.

- Išleidžiant gamybos užsakymą arba paketinį užsakymą
- Išleidžiant neautomatiškai
- Išleidžiant automatiškai, naudojant paketinę užduotį

Daugiau informacijos žr. [KS ir formulės eilučių išleidimas į sandėlį](releasing-bom-and-formula-lines-to-warehouse.md). 

Jei KS arba formulės eilutė neišleista arba išleista tik iš dalies, o darbo srities datos ir filtrų kriterijai tenkinami, eilutė įtraukiama skaičiuojant skaičių, rodomą plytelėje **Neišleistos medžiagų eilutės, į kurias reikia atkreipti dėmesį**.

Kai pasirenkate plytelę, atidaromas puslapis **Išleisti į sandėlį**. Šiame puslapyje rodomas neišleistų KS ir formulės eilučių skaičius, kurį nurodo plytelėje pateikiamas skaičius. Neišleistos eilutės rodomos viršutiniame tinklelyje. Šiame tinklelyje rodomas pradinis apskaičiuotas eilutės kiekis, kiekis, kuris jau išleistas, ir likęs kiekis, kurį vis dar reikia išleisti. Eilutes iš viršutinio tinklelio galite įtraukti į apatinį tinklelį. Tada iš apatinio tinklelio pasirinktas eilutes galite išleisti į sandėlį. Apatiniame tinklelyje taip pat galite koreguoti išleistiną kiekį, kad būtų išleistas tik dalinis kiekis.

## <a name="unprocessed-waves-needing-attention"></a>Neapdorotos bangos, į kurias reikia atkreipti dėmesį

Išleidus KS arba formulės eilutę, ji įtraukiama į naują gamybos bangą arba esamą atvirą bangą, priklausomai nuo gamybos bangos šablono konfigūracijos. Naudodami bangos šablono konfigūraciją taip pat galite nustatyti bangą, kad ji būtų automatiškai apdorojama išleidus KS arba formulės eilutę. Apdorojus bangą, sugeneruojamas žaliavų paėmimo sandėlio darbas. Jei bangos šablonas sukonfigūruotas taip, kad bangos nebūtų apdorojamos išleidimo metu, banga išlieka neapdorotos būsenos. Plytelėje **Neapdorotos bangos, į kurias reikia atkreipti dėmesį** rodomas KS ir formulės eilučių, kurios išleistos į sandėlį neapdorotomis bangomis ir kurių žaliavų data yra ankstesnė arba tokia pati kaip darbo srities data, skaičius. Eilutes taip pat turi suvartoti operacijos išteklius, taikomas darbo srities filtrui.

Pasirinkus plytelę, atidaromas puslapis **Visos gamybos bangos**. Šis puslapis filtruojamas pagal atidarytų bangų, kuriose yra išleistų KS ir formulės eilučių bangų eilučių, atitinkančių plytelės kriterijus, skaičių. Puslapyje **Visos gamybos bangos** galite neautomatiškai apdoroti bangą.

## <a name="open-warehouse-work-needing-attention"></a>Atidarytas sandėlio darbas, į kurį reikia atkreipti dėmesį

Plytelėje **Atidarytas sandėlio darbas, į kurį reikia atkreipti dėmesį** rodomas KS ir formulės eilučių, kurios išleistos į sandėlį, turi neapdoroto darbo ir kurių žaliavų data yra ankstesnė arba tokia pati kaip darbo srities data, skaičius. Eilutes taip pat turi suvartoti operacijos išteklius, taikomas darbo srities filtrui.

Pasirinkus plytelę, atidaromas puslapis **Visas darbas**. Šis puslapis filtruojamas pagal atidarytų darbo antraščių, kuriose yra išleistų KS ir formulės eilučių darbo eilučių, atitinkančių plytelės kriterijus, skaičių. Puslapyje **Visas darbas** galite neautomatiškai apdoroti darbą.

