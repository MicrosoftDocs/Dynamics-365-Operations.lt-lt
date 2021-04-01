---
title: Pareigų biudžeto trikčių šalinimas
description: Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali kilti, kai konfigūruojate pareigų biudžetą. Ji skirta dažnai užduodami klausimai apie tai, kaip sukurti biudžeto išlaidų elementus, kompensacijų grupes ir kompensavimo tinklelius.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f03ab1437d7b4af38b3594892310e27771c829d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241447"
---
# <a name="position-budgeting-troubleshooting"></a>Pareigų biudžeto trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali kilti, kai konfigūruojate pareigų biudžetą. Ji skirta dažnai užduodami klausimai apie tai, kaip sukurti biudžeto išlaidų elementus, kompensacijų grupes ir kompensavimo tinklelius. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Kodėl modulyje Personalas nerandu prognozuojamų pareigų puslapio?
---------------------------------------------------------------

Prognozuojamos pareigos perkeltos į modulį Biudžeto sudarymas.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Kodėl negaliu panaikinti biudžeto išlaidų elemento?
Negalite panaikinti biudžeto išlaidų elemento, kuris priskirtas prognozuojamoms pareigoms. Biudžeto išlaidų elemento panaikinti negalėsite tol, kol jo nepašalinsite iš visų prognozuojamų pareigų. **Patarimas.** Norėdami rasti visas pareigas, kurioms priskirtas biudžeto išlaidų elementas, tą išlaidų elementą pasirinkite puslapyje **Biudžeto išlaidų elementai** ir spustelėkite **Naujinti pareigas**. Pareigos, naudojančios išlaidų elementą yra pateiktos viršutiniame tinklelyje.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Kaip pašalinti išlaidų elementą iš kelių prognozuojamų pareigų neatidarius kiekvienos?
Išlaidų elemento pašalinti negalite. Tačiau, jei pakeisite pradžios ir pabaigos datas taip, kad jos nepatektų į biudžeto planavimo ciklo datų intervalą, išlaidų elementas nebebus priskirtas prognozuojamoms pareigoms tame biudžeto planavimo cikle. Norėdami atlikti šį keitimą, atidarykite biudžeto išlaidų elementą, „FastTab‟ skirtuke **Išlaidų skaičiavimas** spustelėkite **Keisti datas** ir pakeiskite įsigaliojimo datą arba galiojimo pabaigos datą. Tada spustelėkite **Gerai** – bus automatiškai atnaujintos visos prognozuojamos pareigos, kurioms priskirtas išlaidų elementas. **Patarimas.** Jei naudosite šį metodą, turėkite omenyje, kad jis pašalina biudžeto išlaidų elementą iš **visų** prognozuojamų pareigų, kurių pradžios ir pabaigos datos nebėra reikiamame intervale. Jei tai yra ne tai, ką norite padaryti, turėsite atidaryti visas prognozuojamas pareigas, iš kurių norite pašalinti biudžeto išlaidų elementą ir rankiniu būdu atlikti pakeitimus.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Kodėl biudžeto išlaidų elemento „FastTab‟ skirtuke Išlaidų skaičiavimas negalima įvesti metinės sumos?
Metinės sumos negalite įvesti, jei biudžeto išlaidų elementai yra „FastTab‟ skirtuke **Skaičiavimo pagrindas**, nes sistemai reikia procentų reikšmei apskaičiuoti. Norėdami reikšmę pakeisti, iš „FastTab‟ skirtuko **Skaičiavimo pagrindas** pašalinkite visus biudžeto išlaidų elementus.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Kodėl negaliu keisti biudžeto išlaidų tipo „uždarbis“ į kitą biudžeto išlaidų tipą?
Kai kurie biudžeto išlaidų elementai išlaidų elementą „uždarbis“ naudoja kaip skaičiavimo pagrindą. Norėdami lauką **Biudžeto išlaidų tipas** pakeisti, iš visų biudžeto išlaidų elementų „FastTab‟ skirtukų **Skaičiavimo pagrindas** pašalinkite uždarbio išlaidų elementą.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Kodėl negaliu keisti d tos biudžeto išlaidų elemento biudžeto išlaidų elemento eilutėse?
Negalite pakeisti datos biudžeto išlaidų elementų eilutėje, kai biudžeto išlaidų elementas naudojamas prognozuojamoms pareigoms. Šis apribojimas skirtas užtikrinti, kad prognozuojamos pareigos visada yra biudžeto išlaidų elemento gairėse. Norėdami datą pakeisti, „FastTab‟ skirtuke **Išlaidų skaičiavimas** spustelėkite **Keisti datas** ir įveskite naująsias datas. Tada spustelėkite **Gerai** – bus atnaujintos pareigos, kurioms priskirtas išlaidų elementas.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Kodėl negaliu keisti biudžeto išlaidų elemento išlaidų puslapyje Kompensacijų grupė?
Kurti ir keisti biudžeto išlaidų elementus galite tik puslapyje **Biudžeto išlaidų elementai**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Kodėl gaunu klaidos pranešimą, kai keičiu išlaidų elemento datą prognozuojamoms pareigoms?
Datos prognozuojamų pareigų išlaidų elemento eilutėje turi tilpti į tolesnius intervalus.

-   Pareigų aktyvinimo ir galiojimo pabaigos datos.
-   Biudžeto išlaidų elemento aktyvinimo ir galiojimo pabaigos datos.
-   Biudžeto ciklo, susieto su biudžeto planavimo procesu prognozuojamoms pareigoms, pradžios ir pabaigos datos.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]