---
title: „Power BI“ turinys Sandėlio našumas
description: Šiame straipsnyje aprašoma, kas įtraukta į sandėlio našumo Power BI turinį.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.form: WHSWarehousePerformancePowerBI
ms.openlocfilehash: 82f43f45b43df864cbda8ba372dbed46d8f4c7e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289853"
---
# <a name="warehouse-performance-power-bi-content"></a>„Power BI“ turinys Sandėlio našumas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kas įtraukta į sandėlio **našumo** Microsoft Power BI turinį. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Sandėlio našumas** sukurtas tam, kad sandėlio ir operacijų vadovai galėtų stebėti svarbias gavimo, siuntimo ir atsargų metrikas. Jame naudojami sandėlio valdymo, produktų ir kiti operacijų duomenys iš jūsų sistemos bei pateikiamas tiek sujungtas sandėlio efektyvumo rodinys, tiek rodinys, skirtas tiekėjams, produktų grupėms bei produktams ir teritorijai bei sandėliams.

„Power BI“ turinį **Sandėlio našumas** sandėlio vadovai gali naudoti toliau nurodytoms sritims nustatyti.

- **Gavimo efektyvumas** – nustatykite tiekėjo efektyvumą pagal kliento reikalavimus (kitaip sakant, nustatykite pristatymo efektyvumą) ir nustatykite padėjimo efektyvumą, kad galėtumėte identifikuoti problemas, tam tikru laikotarpiu susijusias su darbininkais arba prekėmis. Svarbu žinoti, ar tiekėjai pristato laiku, anksti, ar pavėluotai, kad galėtumėte nustatyti, kaip tiekėjų efektyvumas veikia visą padėjimo efektyvumą. Tiekėjas, kuris prekes pristato ne sutartomis dienomis, gali padidinti sandėlio apkrovą dėl nenumatyto darbo ir pailginti vidutinį padėjimo laiką.
- **Siuntimo efektyvumas** – nustatykite, ar jūsų sandėlis klientams viską išsiunčia laiku (kitaip sakant, nustatykite siuntimo ir pristatymo efektyvumą), kad galėtumėte identifikuoti problemas, susijusias su produktais, teritorijomis, sandėliais arba paskirtais klientais. Jei pastebėsite, kad į konkrečius regionus arba miestus siunčiate pavėluotai, galbūt turėsite daugiau dėmesio skirti transportavimui arba sąskaitai valdyti.
- **Vietos atsargų tikslumas** – atsargų tikslumas yra svarbi vidaus sandėlio verslo įžvalga (BI). Labai svarbu nustatyti, kaip tiksliai vykdomi bendrieji skaičiavimai. Tačiau taip pat svarbu nustatyti, kaip tiksliai saugomos prekės tinkamose vietose, ir pažymėti nesutampančius duomenis, kad galėtumėte prekėms rasti geresnę vietą arba inicijuoti tam tikrų prekių viso kiekio skaičiavimą. (Šiuo metu nauja preke pagrįsto skaičiavimo funkcija teikiama kaip karštoji pataisa.) Jei naudojate šį „Power BI“ turinį norėdami nustatyti turimų atsargų duomenų teisingumą pagal vietą, taip pat galite identifikuoti vagystes savo parduotuvėse. Taip pat galite nustatyti, ar yra vietų, kurių turimų atsargų kiekiai skiriasi nuo įmonės išteklių planavimo (ERP) duomenų. Šios vietos gali būti per didelės arba gali būti neįmanoma jų suskaičiuoti. Be to, faktinis išdėstymas gali būti netikslus, todėl sunku vieno tipo prekę sinchronizuoti su turimais duomenimis.

## <a name="accessing-the-power-bi-content-pack"></a>Prieiga prie „Power BI“ turinio paketo
„Power BI“ turinys **Sandėlio našumas** rodomas puslapyje **Sandėlio našumas** (**Sandėlio valdymas** \> **Užklausos ir ataskaitos** \> **Sandėlio našumo analizė** \> **Sandėlio našumas**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
Į „Power BI“turinį **Sandėlio našumas** įtraukta ataskaita. Šią ataskaitą sudaro metrikų, pavaizduotų diagramomis, plytelėmis ir lentelėmis, rinkinys. Toliau pateiktoje lentelėje pateikiama „Power BI“ turinio **Sandėlio našumas** vizualizacijų apžvalga.

| Ataskaitų puslapis                 | Diagramos                                   | aprašymas |
|-----------------------------|------------------------------------------|-------------|
| Gavimo efektyvumas         | Iš viso atidėta                          | Atidėjimo darbo eilučių, apdorojamų per tam tikrą laiką, skaičius. |
| Gavimo efektyvumas         | Atidėjimo vidutinis laikas                    | Visų apdorojamų pirkimo užsakymų atidėjimo eilučių vidutinis laikas (valandomis) nuo prekių registravimo iki tol, kol apdorojamas paskutinis padėjimas. |
| Gavimo efektyvumas         | Gauta anksti                           | Anksčiau gautų pirkimo užsakymo eilučių skaičius. |
| Gavimo efektyvumas         | Gauta laiku                         | Laiku gautų pirkimo užsakymo eilučių skaičius. |
| Gavimo efektyvumas         | Gauta pavėluotai                            | Pavėluotai gautų pirkimo užsakymo eilučių skaičius. |
| Gavimo efektyvumas         | Laiku pagal tiekėją                        | Pirkimo užsakymo eilučių, kurios gautos iš tiekėjo arba tiekėjų grupės anksčiau, laiku ir pavėluotai, procento rodinys. |
| Gavimo efektyvumas         | Iš rampos į atsargas atidėjimo vidutinis laikas (valandomis) | Iš rampos į atsargas atidėjimo vidutinis laikas valandomis per tam tikrą laiką. |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal darbininką               | Vidutinis laikas (valandomis), per kurį darbininkas apdorojo pirkimo užsakymo eilučių atidėjimą. |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal tiekėją (valandomis)          | Vidutinis atidėjimo laikas (valandomis) pagal tiekėją arba tiekėjų grupę. |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal produktą         | Vidutinis atidėjimo laikas (valandomis) pagal prekę arba prekių grupę. |
| Vietos atsargų tikslumas | Bendroji suma                              | Skaičiavimo darbo eilučių, apdorojamų per tam tikrą laikotarpį, skaičius. |
| Vietos atsargų tikslumas | Neatitikimo koeficientas                         | Visų neatitikimų koeficientas kaip visų per tam tikrą laikotarpį suskaičiuotų eilučių procentas. |
| Vietos atsargų tikslumas | Skaičius be neatitikimų                | Skaičiavimo darbo eilučių, kurios apdorotos be neatitikimų, bendra suma. |
| Vietos atsargų tikslumas | Prekės, suskaičiuotos per tam tikrą laiką                  | Per tam tikrą laiką suskaičiuotų prekių su ir be neatitikimų procentas. |
| Vietos atsargų tikslumas | Prekės kiekio neatitikimas didesnis nei % | Skaičiavimo eilučių su neatitikimais, viršijančiais nurodytą procentą, lentelės rodinys. Lentelėje pateikiama informacija apie vietas, prekes, vidutinį neatitikimą, bendrą skaičiavimo darbo skaičiuojamų eilučių skaičių, skaičiavimo eilučių su vietos neatitikimais skaičių, vidutinį suskaičiuotą kiekį, numatomą bendrą kiekį, kuris bus skaičiuojamas, ir faktinį prekių kiekį, kuris yra skaičiuojamas. |
| Vietos atsargų tikslumas | Prekių skaičius pagal darbininką                     | Darbuotojų skaičiavimo efektyvumas. Efektyvumas yra išreikštas kaip skaičiavimo eilučių, kurios turi ir neturi nesutapimų, procentas. |
| Vietos atsargų tikslumas | Prekių skaičius pagal teritoriją / sandėlį           | Skaičiavimo efektyvumas pagal apdorotų skaičiavimo darbo eilučių atsižvelgiant į teritoriją arba sandėlį, turinčių ir neturinčių nesutapimų, skaičius. |
| Vietos atsargų tikslumas | Neatitikimo koeficientas pagal produktą              | Skaičiavimo efektyvumo neatitikimo procentas. Koeficientas yra išreikštas kaip apdorotų skaičiavimo darbo eilučių skaičius pagal prekę arba prekių grupę. |
| Siuntimo efektyvumas        | Išsiųstos eilutės                            | Visų siuntimo eilučių, išsiųstų per tam tikrą laikotarpį, skaičius. |
| Siuntimo efektyvumas        | Anksčiau                                    | Siuntimo eilučių, išsiųstų anksčiau, procentas. |
| Siuntimo efektyvumas        | Laiku                                  | Siuntimo eilučių, išsiųstų laiku, procentas. |
| Siuntimo efektyvumas        | Vėliau                                     | Siuntimo eilučių, išsiųstų pavėluotai, procentas. |
| Siuntimo efektyvumas        | Siuntos per tam tikrą laikotarpį                      | Siuntimo eilučių, per tam tikrą laikotarpį išsiųstų anksčiau, laiku arba pavėluotai, procentas. Tendencijų eilutė rodo laiku išsiųstų eilučių tendenciją. |
| Siuntimo efektyvumas        | Išsiųsta pavėluotai pagal miestą                     | Miestų ir vietovių, kurias paveikė pavėluotos siuntos, vaizdinė schema. |
| Siuntimo efektyvumas        | Išsiųsta pagal produktą                       | Anksčiau, laiku arba pavėluotai išsiųstų prekių procentas pagal prekę arba prekių grupę. |
| Siuntimo efektyvumas        | Išsiųsta pagal klientą                      | Anksčiau, laiku arba pavėluotai išsiųstų prekių procentas pagal klientą arba klientų grupę. |
| Siuntimo efektyvumas        | Išsiųsta pagal teritoriją / sandėlį              | Anksčiau, laiku arba pavėluotai išsiųstų prekių procentas pagal teritoriją arba sandėlį. |

## <a name="understanding-the-data-model-and-calculations"></a>Duomenų modelio ir skaičiavimų supratimas
Tolesniais duomenimis pildomi „Power BI“ turinio **Sandėlio našumas** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Šie pagrindiniai sujungti matavimo vienetai naudojami kaip turinio pagrindas.

| Ataskaitų puslapis                 | Diagramos                                   | Lentelės                                | Skaičiavimo aprašai |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Gavimo efektyvumas         | Iš viso atidėta                          | WHSWorkLine                           | Darbo eilučių, kurių darbo tipas yra **padėjimas**, skaičius. |
| Gavimo efektyvumas         | Atidėjimo vidutinis laikas                    | WHSWorkLine                           | Maksimalaus darbo eilučių laiko suma, padalyta iš maksimalaus darbo eilučių laiko skaičiaus, kai darbo eilučių maksimalus laikas yra maksimalus laiko skirtumas tarp darbo pradžios ir uždarymo datų. |
| Gavimo efektyvumas         | Gauta anksti                           | WHSWorkLine                           | Darbo eilučių, kuriose darbo sukūrimo data yra ankstesnė nei naudojama pristatymo data, skaičius. Jei patvirtinta pristatymo data nėra nustatyta, naudojama numatytoji pristatymo data. |
| Gavimo efektyvumas         | Gauta laiku                         | WHSWorkLine                           | Darbo eilučių, kuriose darbo sukūrimo data atitinka naudojamą pristatymo datą, skaičius. Jei patvirtinta pristatymo data nėra nustatyta, naudojama numatytoji pristatymo data. |
| Gavimo efektyvumas         | Gauta pavėluotai                            | WHSWorkLine                           | Darbo eilučių, kuriose darbo sukūrimo data yra vėlesnė nei naudojama pristatymo data, skaičius. Jei patvirtinta pristatymo data nėra nustatyta, naudojama numatytoji pristatymo data. |
| Gavimo efektyvumas         | Laiku pagal tiekėją                        | WHSWorkLine                           | Gauta anksti, Gauta laiku ir Gauta pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Gavimo efektyvumas         | Iš rampos į atsargas atidėjimo vidutinis laikas (valandomis)   | WHSWorkLine                           | Vidutinis atidėjimo laikas (žr. anksčiau šioje lentelėje pateiktą aprašymą). |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal darbininką               | WHSWorkLine                           | Vidutinis atidėjimo laikas (žr. anksčiau šioje lentelėje pateiktą aprašymą). |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal tiekėją (valandomis)          | WHSWorkLine                           | Vidutinis atidėjimo laikas (žr. anksčiau šioje lentelėje pateiktą aprašymą). |
| Gavimo efektyvumas         | Vidutinis atidėjimas pagal produktą         | WHSWorkLine                           | Vidutinis atidėjimo laikas (žr. anksčiau šioje lentelėje pateiktą aprašymą). |
| Vietos atsargų tikslumas | Bendroji suma                              | WHSWorkLineCycleCount                 | Ciklų skaičiavimai, kuriuose absoliutus neatitikimų kiekis yra lygus arba didesnis už 0 (nulis). |
| Vietos atsargų tikslumas | Neatitikimo koeficientas                         | WHSWorkLineCycleCount                 | Ciklo skaičiavimai su neatitikimais, padalyti iš bendros sumos. Laikoma, kad yra ciklo skaičiavimo neatitikimų, jei absoliutus neatitikimų kiekis yra didesnis už 0 (nulis). |
| Vietos atsargų tikslumas | Skaičius be neatitikimų                | WHSWorkLineCycleCount                 | Ciklų skaičiavimai, kuriuose absoliutus neatitikimų kiekis yra didesnis už 0 (nulis). |
| Vietos atsargų tikslumas | Skaičius su neatitikimais                   | WHSWorkLineCycleCount                 | Ciklų skaičiavimai, kuriuose absoliutus neatitikimų kiekis yra lygus 0 (nulis). |
| Vietos atsargų tikslumas | Prekės, suskaičiuotos per tam tikrą laiką                  | WHSWorkLineCycleCount                 | Skaičiavimai be neatitikimų ir Skaičiavimai su neatitikimais (žr. anksčiau šioje lentelėje pateiktus aprašymus.) |
| Vietos atsargų tikslumas | Prekės kiekio neatitikimas didesnis nei % | WHSWorkLineCycleCount                 | Vidutinis neatitikimas yra absoliutus neatitikimų kiekis, padalytas iš numatomo kiekio, kai absoliutus neatitikimų kiekis yra didesnis už 0 (nulis). Vidutinis neatitikimo kiekis yra vidutinis absoliutus neatitikimų kiekis, kai absoliutus neatitikimų kiekis yra didesnis už 0 (nulis). Skaičiavimai su neatitikimais, Bendra suma, Numatomas kiekis ir Suskaičiuotas kiekis, kai visas kiekis sugrupuojamas pagal prekę ir vietą (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Vietos atsargų tikslumas | Prekių skaičius pagal darbininką                     | WHSWorkLineCycleCount                 | Skaičiavimai be neatitikimų ir Skaičiavimai su neatitikimais (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Vietos atsargų tikslumas | Prekių skaičius pagal teritoriją / sandėlį           | WHSWorkLineCycleCount                 | Skaičiavimai be neatitikimų ir Skaičiavimai su neatitikimais (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Vietos atsargų tikslumas | Neatitikimo koeficientas pagal produktą              | WHSWorkLineCycleCount                 | Neatitikimų koeficientas (žr. anksčiau šioje lentelėje pateiktą aprašymą). |
| Siuntimo efektyvumas        | Išsiųstos eilutės                            | SalesLine               | Išsiųstų pardavimo eilučių skaičius. |
| Siuntimo efektyvumas        | Anksčiau                                    | CustPackingSlipOnTimeStatus           | Pardavimo eilutės, kurių siuntimo datos būsena yra **1 (anksti)**. Anksti reiškia, kad važtaraščio siuntimo data yra ankstesnė nei pardavimo eilutės patvirtinta siuntimo data. Jei patvirtinta siuntimo data nenustatyta, naudojama pageidaujama siuntimo data. |
| Siuntimo efektyvumas        | Laiku                                  | CustPackingSlipOnTimeStatus           | Pardavimo eilutės, kurių siuntimo datos būsena yra **2 (laiku)**. Laiku reiškia, kad važtaraščio siuntimo data atitinka pardavimo eilutės patvirtintą siuntimo datą. Jei patvirtinta siuntimo data nenustatyta, naudojama pageidaujama siuntimo data. |
| Siuntimo efektyvumas        | Vėliau                                     | CustPackingSlipOnTimeStatus           | Pardavimo eilutės, kurių siuntimo datos būsena yra **3 (pavėluotai)**. Pavėluotai reiškia, kad važtaraščio siuntimo data yra vėlesnė nei pardavimo eilutės patvirtinta siuntimo data. Jei patvirtinta siuntimo data nenustatyta, naudojama pageidaujama siuntimo data. |
| Siuntimo efektyvumas        | Siuntos per tam tikrą laikotarpį                      | SalesLine CustPackingSlipOnTimeStatus | Visiškai išsiųsti užsakymai, kai išsiųstas visas pardavimo eilutės kiekis, ir būsenos Anksti, Laiku bei Pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Siuntimo efektyvumas        | Išsiųsta pavėluotai pagal miestą                     | CustPackingSlipOnTimeStatus           | Pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Siuntimo efektyvumas        | Išsiųsta pagal produktą                       | CustPackingSlipOnTimeStatus           | Anksti, Laiku ir Pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Siuntimo efektyvumas        | Išsiųsta pagal klientą                      | CustPackingSlipOnTimeStatus           | Anksti, Laiku ir Pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |
| Siuntimo efektyvumas        | Išsiųsta pagal teritoriją / sandėlį              | CustPackingSlipOnTimeStatus           | Anksti, Laiku ir Pavėluotai (žr. anksčiau šioje lentelėje pateiktus aprašymus). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
