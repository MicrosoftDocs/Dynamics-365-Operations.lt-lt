---
title: Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes
description: Šiame straipsnyje aprašoma, kaip iš praeities duomenų, kurie naudojami poreikio prognozei apskaičiuoti, pašalinti pašalines reikšmes. Pašalinę pašalines reikšmes, galite padidinti prognozės tikslumą.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9004c8a001bcf70897d1e9ee9a7962743bc3affd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987334"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip iš praeities duomenų, kurie naudojami poreikio prognozei apskaičiuoti, pašalinti pašalines reikšmes. Pašalinę pašalines reikšmes, galite padidinti prognozės tikslumą.

Pašalinę pašalines reikšmes galite padidinti prognozės tikslumą. Ši užduotis nėra privaloma. Toliau pateikta proceso apžvalga.

1.  Norėdami atidaryti puslapį **Pašalinių reikšmių šalinimas**, kuriame, naudodami užklausą, galėtumėte pasirinkti šalintinas operacijas, spustelėkite **Bendrasis planavimas** &gt; **Sąranka** &gt; **Poreikio prognozė** &gt; **Pašalinių reikšmių šalinimas**.
2.  Pasirinkite įmonę, kuriai užklausa taikoma, tada įveskite pavadinimą ir aprašą. **Užklausos datos** laukas automatiškai nustatomas į dabartinę datą.
3.  Pažymėkite žymės langelį **Aktyv.**, kad iš praeities duomenų pašalintumėte operacijas, rastas naudojant užklausą. Šis parametras pradės veikti, kai kursite pagrindinę prognozę.
4.  Puslapyje **Pašalinių reikšmių šalinimo užklausa** galite pridėti, šalinti ir pasirinkti kriterijus, apibrėžiančius, kurios operacijos bus pašalintos skaičiuojant pagrindinę prognozę. Pvz., pasirinkite konkrečią prekę arba užsakymo operaciją, kurią norite pašalinti.
5.  Spustelėkite **Rodyti operacijas**. Puslapyje **Pašalinių reikšmių operacijos** išvardijamos operacijos, kurios atitinka jūsų užklausoje nurodytus kriterijus ir kurios apskaičiuojant poreikio prognozę bus pašalintos iš praeities duomenų.

**Pastaba:** taip pat galite sukurti užklausą, paremtą esama užklausa. Pasirinkite užklausą, kurią norite kopijuoti, tada spustelėkite **Dubliuoti**. Lauke **Užklausos data** identifikuojama versija. Užklausą galite naudoti tokią, kokia ji yra, arba galite spustelėti **Redaguoti užklausą** ir modifikuoti kriterijus. Neprivaloma: galite modifikuoti naujosios užklausos pavadinimą ir aprašą.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Poreikio prognozavimo apžvalga](introduction-demand-forecasting.md)

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)



