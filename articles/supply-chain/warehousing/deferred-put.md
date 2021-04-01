---
title: Atidėtas sandėlio darbo apdorojimas
description: Šioje temoje aprašomos funkcijos, dėl kurių „Dynamics 365 Supply Chain Management” galima naudoti sandėlio darbo atidėjimo operacijų apdorojimą.
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2f670a3b4b75434853ddcd3d790ad2c55971d72a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243924"
---
# <a name="deferred-processing-of-warehouse-work"></a>Atidėtas sandėlio darbo apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, dėl kurių Dynamics 365 Supply Chain Management galima naudoti sandėlio darbo atidėjimo operacijų apdorojimą.

Atidėta apdorojimo funkcija leidžia sandėlio darbuotojams atlikti kitus darbus, o padėjimo operacija apdorojama fone. Atidėtas apdorojimas naudingas, kai reikia apdoroti daug darbo eilučių ir darbuotojas gali leisti, kad darbas būtų apdorojamas asinchroniškai. Jis taip pat naudingas, kai serveris gali turėti „ad-hoc“ arba neplanuotą apdorojimo laiko padidėjimą, o didesnis apdorojimo laikas gali turėti įtakos vartotojo produktyvumui.

Fono apdorojimas pasiekiamas naudojant „SysOperation“ sistemą. Daugiau informacijos žr. [„SysOperation“ sistemos apžvalga](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Darbo apdorojimo strategijų konfigūravimas

Norėdami naudoti atidėtą apdorojimą, turite sukonfigūruoti ir naudoti darbo apdorojimo strategiją.

Strategijos konfigūruojamos puslapyje **Darbo apdorojimo strategijos**. Toliau pateiktoje lentelėje aprašomi to puslapio laukai.

| Laukas                           | Aprašymas |
|---------------------------------|-------------|
| Darbo apdorojimo strategijos pavadinimas     | Darbo apdorojimo strategijos pavadinimas. |
| Darbo užsakymo tipas                 | Darbo užsakymo tipas, kuriam taikoma strategija. |
| Operacija                       | Operacija, kuri apdorojama naudojant strategiją. |
| Darbo apdorojimo metodas          | Metodas, naudojamas darbo eilutei apdoroti. Jei metodas nustatytas į **Nedelsiant**, elgesys primena elgesį, kai eilučių apdorojimui nėra naudojamos jokios darbo apdorojimo strategijos. Jei metodas nustatytas į **Atidėtas**, naudojamas atidėtas apdorojimas, kuris naudoja paketinę sistemą. |
| Atidėto apdorojimo riba   | Vertė **0** (nulis) nurodo, kad nėra ribinės reikšmės. Tokiu atveju naudojamas aidėtas apdorojimas, jei jis gali būti naudojamas. Jei konkrečios ribinės reikšmės skaičiavimas yra žemesnis už ribinę reikšmę, naudojamas metodas Nedelsiant. Priešingu atveju naudojamas atidėtasis metodas, jei jį galima naudoti. Su pardavimu ir perkėlimu susijusiam darbui, ribinė reikšmė apskaičiuojama kaip susieto šaltinio įkėlimo eilučių, kurios apdorojamos darbui, skaičius. Papildymo darbams ribinė reikšmė apskaičiuojama kaip darbo eilučių, kurias papildo darbas, skaičius. Nustatydami ribinę reikšmę, pvz., **5**, pardavimams, mažesniems darbams, kuriuose yra mažiau nei penkios pradinio šaltinio įkėlimo eilutės, nebus naudojamas atidėtas apdorojimas, tačiau jį naudos didesni darbai. Ribinė reikšmė taikoma tik tada, kai darbo apdorojimo metodas nustatytas į **Atidėtas**. |
| Atidėto apdorojimo paketų grupė |Paketų grupė, naudojama apdorojimui. |

Atidėtam padėjimo apdorojimui palaikomi šie darbo užsakymo tipai: pardavimo užsakymas, perkėlimo užsakymo išdavimas ir papildymas.

## <a name="assigning-the-work-creation-policy"></a>Darbo kūrimo strategijos priskyrimas

Darbo kūrimo strategiją galima priskirti sandėlio valdymo parametruose. Ją taip pat galima priskirti atskirų sandėlių lygyje. Jei strategija priskirta sandėliui, ji taikoma tik tam sandėliui kuriamam darbui. Jei sandėlio lygiu nepriskirta jokia strategija, taikoma strategija iš sandėlio valdymo parametrų.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Atidėto padėjimo apdorojimo užduočių peržiūra

Puslapyje **Atidėto padėjimo apdorojimo užduotys** galite peržiūrėti atidėtas apdorojimo užduotis.

Pagal numatytuosius nustatymus rodomos **Atliktos** užduotys.

| Laukas            | Aprašymas |
|------------------|-------------|
| Būsena           | Užduoties būsena. |
| Paketinės užduoties būsena | Susijusios paketinės užduoties būsena. Jei paketinė užduotis apdorota, paketinėje retrospektyvoje yra žurnalas ir paketinės užduoties informacija. |

Toliau pateiktas galimų būsenų paaiškinimas:

- **Laukiama** – susijusi paketinė užduotis laukia apdorojimo paketų serveryje.
- **Nepavyko** – apdorojimas nepavyko. Užduotis gali būti apdorota naudojant veiksmą **Apdoroti atidėtą padėjimą** arba ji gali būti atšaukta naudojant veiksmą **Atšaukti atidėtą padėjimą**.
- **Baigta** – užduotis baigta.

## <a name="impact-on-closed-work-dates"></a>Poveikis uždaryto darbo datoms

Kai naudojamas atidėto padėjimo apdorojimas, uždaryto darbo data nustatoma kaip atidėtų padėjimo apdorojimo užduočių data / laikas. Naudojama uždaryto darbo data, nes tai yra geriausias įvertinimas, kada buvo baigta padėjimo operacija.

## <a name="reprocessing-a-failed-task"></a>Nepavykusios užduoties pakartotinis apdorojimas

Nepavykusią užduotį galima pakartotinai apdoroti pasirinkus ją puslapyje, tada pasirinkus **Apdoroti atidėtą padėjimą**. Pakartotinis apdorojimas taikomas situacijai, kai vartotojas iš mobiliojo įrenginio užpildo padėjimus tarsi jie būtų nustatyti neatidėliotinam apdorojimui.

## <a name="canceling-failed-tasks"></a>Nepavykusių užduočių atšaukimas

Atšaukti galima tik nepavykusias užduotis. Atšaukiant užduotį galima priskirti ją naujam vartotojui. Be to, užduotis gali likti priskirta vartotojui, kuris apdorojo darbą. Atšaukimas taikomas situacijoje, kai darbas grąžinamas į mobilųjį įrenginį, tarsi ką tik būtų baigtas paskutinis paėmimo etapas ir yra būtina padėti darbą. Tačiau vartotojas galės nustatyti, kad darbas yra „skirtingas“, nes jis turės tik padėjimo etapą, o vieta atitiks vietą, kurią pirmasis vartotojas naudojo kaip galutinio padėjimo vietą.

Kai užduotis atšaukiama, darbo neblokuoja atidėto padėjimo apdorojimo blokavimo priežastis. Jį galima pakartotinai apdoroti naudojant mobilųjį įrenginį.

Užduoties įrašas panaikinamas, kai užduotis atšaukiama.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiliojo įrenginio meniu konfigūravimas, kad būtų nepaisoma atidėto apdorojimo strategijos

Galima sukonfigūruoti mobiliojo įrenginio meniu elementą taip, kad nebūtų naudojama atidėto apdorojimo strategija. Darbas apdorojamas toks, koks yra, jeigu nėra naudojama atidėto apdorojimo strategija. Ši funkcija leidžia prižiūrėtojui naudoti konkretų meniu elementą, kuriame atidėtas padėjimas nėra naudojamas. Norėdami jį sukonfigūruoti, lauką **Atidėto padėjimo apdorojimo strategija** nustatykite į **Perrašyti nustatymus ir apdoroti padėjimą sinchroniškai**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Apribojimai, kai netaikomas atidėto padėjimo apdorojimas

Yra keli scenarijai, kai atidėto padėjimo apdorojimas nėra taikomas, net jei strategija yra sukonfigūruota. Štai keletas pavyzdžių:

- Naudojamas rankinis darbo užbaigimas.
- Darbas užbaigtas naudojant automatinį užbaigimą.
- Naudojami audito šablonai.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Atidėtų apdorojimo užduočių stebėjimas iš darbo siuntimo stebėjimo darbo srities

**Siunčiamo darbo stebėjimo** darbo srityje yra dvi plytelės, kurios padeda stebėti atidėto padėjimo apdorojimo užduotis:

- **Nepavykusios atidėtos apdorojimo užduotys** – šioje plytelėje rodomas nepavykusių užduočių skaičius. Jei yra nepavykusių užduočių, sandėlio vadovas turi arba pakartotinai apdoroti arba atšaukti, nes jos nebus automatiškai pakartotinai apdorojamos.
- **Laukiama atidėto padėjimo apdorojimo užduočių** – šioje plytelėje rodoma užduočių, kurios yra būsenos **Laukia** daugiau nei 10 minučių, skaičius. Jei plytelėje rodomas skaičius, jis gali nurodyti, kad paketinio apdorojimo metu kilo problemų. **Laukiančias** užduotis galima apdoroti neautomatiniu būdu. Jei užduoties paketinė užduotis apdorojama vėliau, ji tiesiog nepavyks, nes ji jau buvo apdorota. Nebus jokio poveikio.

## <a name="deleting-completed-tasks"></a>Baigtų užduočių naikinimas

Galima panaikinti atidėto padėjimo apdorojimo užduotis, kurios buvo baigtos jas pasirenkant ir panaikinant puslapyje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]