---
title: Netikėtas užklausos ir seanso duomenų skirtumas tikrinant
description: Įvyko netikėtas skirtumas tarp užklausos ir seanso duomenų sandėlio programos užduoties tikrinimo rezultatuose.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456956"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Netikėtas užklausos ir seanso duomenų skirtumas tikrinant

Klaidos kodas: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Požymiai

Kai naudojate sandėlio programos [užduočių tikrinimo sistemą](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), validatorius pateikia tokį klaidos pranešimą:

> Netikėtas užklausos ir seanso duomenų skirtumas. Pažeistas sandėlio mobiliųjų įrenginių XML protokolas. REQUEST_XML_TAMPERING

## <a name="cause"></a>Priežastis

Ši klaida įvyksta, kai paskutinio žingsnio, kuris buvo sėkmingai atliktas tikrinimo vykdymo metu, išvestis neatitinka įrašyto kito veiksmo įvesties. Ši situacija gali kilti, nes užduočių validatorius naudoja ankstesnio veiksmo išvestį kaip paskesnio veiksmo įvestį. Vietoj to, įrašytas XML naudojamas kaip kiekvieno veiksmo įvestis.

Daugeliu atvejų klaida įvyksta iš naujo paleidus užduotį, tačiau tikrinimas reikalauja įrašų, kurie buvo modifikuoti arba pašalinti ankstesnio tos pačios užduoties vykdymo metu.

## <a name="resolution"></a>Paaiškinimas

Sandėlio programos užduoties tikrinimo paleidimas nėra idempotentinė operacija, bet modifikuojami rodomi duomenys. Todėl, prieš iš naujo pradėdami užduotį, jums gali tekti iš naujo nustatyti susijusius duomenis.

1. Peržiūrėkite paskutinio sėkmingo tikrinimo veiksmo išvesties XML, kad nustatytumėte, kur išjungtas tikrinimas.
1. Peržiūrėkite savo testą ir įsitikinkite, kad visi būtini pardavimo užsakymai, perkėlimo užsakymai, darbo antraštės ir kiti įrašai vis dar yra bei yra tikėtinos būsenos.
1. Iš naujo sukurkite arba redaguokite trūkstamus ar modifikuotus įrašus. Arba sukurkite naują tikrinimo nustatymą ir sukurkite testą, kad būtų naudojami tinkami esami įrašai.
