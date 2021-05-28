---
title: Sklandus dovanų kortelių ir pažymų operacijų perjungimas neprisijungus
description: Šioje temoje apžvelgiami patobulinimai, užtikrinantys sklandų tam tikrų mokėjimo tipų perjungimą neprisijungus.
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 47867447e6d16a0fb4542c17ab184068300b2c1c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019962"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Sklandus dovanų kortelių ir pažymų operacijų perjungimas neprisijungus

[!include [banner](../includes/banner.md)]

Jei elektroninio kasos aparato (EKA) įrenginys praranda ryšį su kanalo duomenų baze, dauguma vykdomų EKA operacijų gali būti vykdomos toliau, kasininkui gavus įspėjimą apie prarastą ryšį. Tačiau kai kuriais atvejais operacijose yra elementų, kurie remiasi tiesioginiu aptarnavimu, ir šie elementai nepalaikomi, kai EKA yra neprisijungęs. Šioje temoje aprašomos funkcijos, padedančios sumažinti ryšio praradimo įtaką, esant šiems scenarijams.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Dovanų kortelių operacijų užbaigimas neprisijungus

Vidinės dovanų kortelės priklauso nuo tiesioginio aptarnavimo, nes dovanų kortelių balansas turi būti centralizuotai tvarkomas „Microsoft Dynamics 365 Commerce“ būstinėje. Siekiant išvengti apgaulės arba kitų sinchronizavimo problemų, dovanų kortelės yra užrakinamos iš karto, įtraukus jas į operaciją. Užrakinimo funkcija užtikrina, kad dovanų kortelės nebus galima naudoti keliuose terminaluose tuo pačiu metu. Kai operacija baigiama, dovanų kortelė atnaujinama ir atrakinama.

Tačiau, jei EKA praranda ryšį įtraukus dovanų kortelę į operaciją, dovanų kortelė gali tapti netinkama naudoti. Siekiant išvengti šios situacijos „Dynamics 365 Commerce“ yra parametras, leidžiantis užbaigti operacijas, kuriose yra dovanų kortelės eilutė, kai EKA yra neprisijungęs. Įjungus šį parametrą, dovanų kortelių operacijos, kurios buvo priverstinai atliktos neprisijungus, bus įrašytos kartu su neprisijungus atliktomis operacijomis ir jos bus sinchronizuojamos su „Commerce“ būstine, sinchronizuojant neprisijungus atliktas operacijas. Sinchronizavus, taip pat bus atrakinta dovanų kortelė, kad ją būtų galima naudoti kitame terminale.

Norėdami įgalinti funkcijas, skirtas dovanų kortelių operacijoms užbaigti neprisijungus, eikite į puslapio **Prekybos parametrai** skirtuką **Registravimas**. Šiame skirtuke raskite „FastTab“ elementą **Dovanų kortelė** ir parinktyje **Leisti atlikti dovanų kortelių operacijas neprisijungus** nustatykite **Taip**.

![Dovanų kortelių nustatymas neprisijungus](../media/gift.png)

Prekybos parametrai paprastai saugomi talpykloje. Todėl atnaujinus šio parametro nustatymą ir inicijavus paskirstymo grafiką sinchronizuoti pakeitimą su kanalu, gali reikėti palaukti iki 24 val., kol pakeitimas įsigalios. Norėdami, kad pakeitimas įsigaliotų nedelsiant, iš naujo nustatykite „Microsoft“ informacines interneto paslaugas (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Kredito pažymos operacijų užbaigimas neprisijungus

Kaip ir vidinės dovanų kortelės, kredito pažymos centralizuotai tvarkomos „Commerce“ būstinėje. „Commerce“ yra parametras, leidžiantis užbaigti kredito pažymos operacijas, kai EKA yra neprisijungęs. Šis parametras veikia kaip dovanų kortelių parametras, kuris buvo paminėtas ankstesniame skyriuje. Įgalinus šį parametrą, kredito pažymų operacijos, kurios buvo priverstinai atliktos neprisijungus, bus sinchronizuojamos su kanalo duomenų baze kartu su kitomis operacijomis, kurios buvo atliktos, kai EKA buvo neprisijungęs.

Norėdami įgalinti funkcijas, skirtas kredito pažymų operacijoms užbaigti neprisijungus, eikite į puslapio **Prekybos parametrai** skirtuką **Registravimas**. Šiame skirtuke raskite „FastTab“ elementą **Kredito pažyma** ir parinktyje **Leisti atlikti kredito pažymų operacijas neprisijungus** nustatykite **Taip**.

![Kredito pažymos nustatymas neprisijungus](../media/creditmemo.png)

Prekybos parametrai paprastai saugomi talpykloje. Todėl atnaujinus šio parametro nustatymą ir inicijavus paskirstymo grafiką sinchronizuoti pakeitimą su kanalu, gali reikėti palaukti iki 24 val., kol pakeitimas įsigalios. Norėdami, kad pakeitimas įsigaliotų nedelsiant, iš naujo nustatykite IIS.

## <a name="related-topics"></a>Susijusios temos

- [Elektroninio kasos aparato (EKA) funkcijos neprisijungus](../pos-offline-functionality.md)
- [Elektroninio kasos aparato (EKA) operacijos, prisijungus ir neprisijungus prie interneto](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]