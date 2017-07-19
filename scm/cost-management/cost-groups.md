---
title: "Išlaidų grupės"
description: "Išlaidų grupės suteikia pagamintų prekių apskaičiuotų išlaidų, pvz., medžiagų, darbo ir pridėtinių išlaidų įnašų, segmentavimo ir analizavimo pagrindą. Išlaidų grupių segmentavimas turi keletą sinonimų gamybos aplinkoje, pvz., išlaidų paskirstymas, išlaidų skaidymas ar išlaidų klasifikacija."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fb335a521a1a79ea7d978171d233364c58765a0b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="cost-groups"></a>Išlaidų grupės

[!include[banner](../includes/banner.md)]


Išlaidų grupės suteikia pagamintų prekių apskaičiuotų išlaidų, pvz., medžiagų, darbo ir pridėtinių išlaidų įnašų, segmentavimo ir analizavimo pagrindą. Išlaidų grupių segmentavimas turi keletą sinonimų gamybos aplinkoje, pvz., išlaidų paskirstymas, išlaidų skaidymas ar išlaidų klasifikacija. 

Išlaidų grupių segmentavimas turi keletą sinonimų gamybos aplinkoje, pvz., išlaidų paskirstymas, išlaidų skaidymas ar išlaidų klasifikacija. Išlaidų grupių segmentavimas yra naudojamas įvairiais tikslais. Štai keletas pavyzdžių:

-   Galima segmentuoti išlaidas už skirtingų tipų medžiagas, pvz. ingredientus ir konservuotų produktų pakavimo medžiagas, remiantis išlaidų grupėmis, priskirtomis prekėms.
-   Galima segmentuoti skirtingų tipų operacijų išteklių išlaidas, pvz., skirtingų tipų darbą ar mašinas, remiantis išlaidų grupėmis, priskirtomis išlaidų kategorijoms, susijusioms su operacijų ištekliais ir maršruto planavimo operacijomis.
-   Galima segmentuoti išlaidas už maršruto planavimo operacijų nustatymo ir apdorojimo laiką, remiantis išlaidų grupėmis, priskirtomis išlaidų kategorijoms, susijusioms su tomis maršruto planavimo operacijomis.
-   Galima segmentuoti skirtingų tipų pridėtines išlaidas, pvz., su darbu ar mašinomis susijusias pridėtines išlaidas, remiantis išlaidų grupėmis, priskirtomis netiesioginėms išlaidoms nustatant įkainojimo lapą.
-   Segmentavimu galima remtis apskaičiuojant įvairių tipų gamybos pridėtines išlaidas, kai nustatomas įkainojimo lapas. Pridėtinės išlaidos gali apimti skirtingus pridėtinių išlaidų tipus, susijusius su maršruto planavimo informacija apie operacijų išteklius ar nustatymo ir apdorojimo laiko informacija. Pridėtinės gamybos išlaidos taip pat gali būti susijusios su komponentų medžiagų išlaidų įnašais ir atspindėti efektyvesnės gamybos filosofiją, dėl kurios maršruto planavimo informacija nebėra reikalinga.

Išlaidų grupių segmentavimas taikomas apskaičiuotoms pagamintos prekės išlaidoms, nepaisant, ar jos buvo pagrįstos standartinėmis išlaidomis ar suplanuotomis išlaidomis. Puslapyje **Suvestinė** šis segmentavimas rodomas pagal išlaidų grupę, pagal lygį arba pagal išlaidų grupę ir lygį. 

Galimybė išlaikyti išlaidų grupės segmentavimą keliuose produkto struktūros lygmenyse vadinama *skaidymu*. Skaidymas taikomas tik pagamintoms prekėms, kurioms naudojamas standartinis išlaidų atsargų modelis. Jei skaidymas netaikomas, pagaminto komponento išlaidos vertinamos kaip medžiagų išlaidų įnašai. Išlaidų paskirstymo pagal papildomą knygą atsargų parametras nurodo, kad išlaidų grupės segmentavimas liks kelių lygių standartiniuose išlaidų skaičiavimuose. Jei taikoma neskirstymo į lygius strategija, išlaidų grupės segmentavimas taikomas tik vieno lygio skaičiavimui. Pvz., puslapyje **Išlaidų sumavimas pagal išlaidų grupę** rodomas standartinių išlaidų prekių išlaidų grupės segmentavimas keliuose lygiuose. 

Išlaidų grupių segmentavimas taip pat gali būti taikomas standartinių išlaidų elementų nuokrypiams. Antrasis atsargų parametras apibrėžia, ar nuokrypiai yra nustatyti pagal išlaidų grupę ar tik susumuoti. 

Išlaidų grupei gali būti priskirtas išlaidų grupės tipas ir papildomo segmentavimo veikimo būdas.

-   **Išlaidų grupės tipas** − kiekvienai išlaidų grupei turi būti priskirtas išlaidų grupės tipas, kuris nurodo, kad išlaidų grupė susijusi su tiesiogine medžiaga, tiesiogine gamyba ar tiesioginėmis užsakomosiomis paslaugomis arba nurodo ją kaip netiesioginę ar neapibrėžtą. Išlaidų grupė, nurodyta kaip tiesioginė medžiaga, gali būti priskirta prekėms. Tiesioginės gamybos išlaidų grupė gali būti priskirta išlaidų kategorijoms. Tiesioginių užsakomųjų paslaugų išlaidų grupę galima priskirti paslaugos produkto tipui, kuris leidžia klasifikuoti išlaidas, susijusias su paslaugų pirkimo subrangos veikla. Netiesioginių išlaidų grupė gali būti priskirta netiesioginėms išlaidoms, apmokant papildomus mokesčius ar tarifus. Išlaidų grupė, nurodyta kaip neapibrėžta, gali būti priskirta prekėms, išlaidų kategorijoms ar netiesioginėms išlaidoms. Išlaidų grupės tipo priskyrimas turi kelias paskirtis. Pirma, teikiama galimybė priskirti išlaidų grupę ir peržiūrėti taikomų išlaidų grupių sąrašą. Antra, suteikiamas papildomas segmentavimas ataskaitų kūrimui. Trečia, jis gali būti naudojamas priskirti DK sąskaitas nuokrypiams.
-   **Veikimo būdas** − kiekvienai išlaidų grupei gali būti pasirinktinai priskirtas veikimo būdas, kuris nurodo, kad išlaidų grupė susijusi su fiksuotomis išlaidomis ar kintamomis išlaidomis. Išlaidų grupė, kurios veikimo būdas pateiktas kaip nulinis, yra laikoma kintamomis išlaidomis. Veikimo būdo priskyrimas atlieka tik ataskaitų kūrimo funkciją. Pavyzdžiui, išlaidos gali būti rodomos su fiksuotų ir kintamų išlaidų segmentavimu įkainojimo lape bei puslapyje**Išlaidų sumavimas pagal išlaidų grupę**. Priskyrus pelno parametrų procentines vertes kiekvienai išlaidų grupei, skaičiuojant komplektavimo specifikacijas (KS), nurodomos siūlomos pardavimo kainos, pagrįstos požiūriu „išlaidos plius antkainis“.





