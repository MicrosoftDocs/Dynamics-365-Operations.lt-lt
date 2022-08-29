---
title: Indonezijos išskaitomo mokesčio ataskaita
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti ir generuoti indonezijos išskaitomo mokesčio ataskaitą.
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282442"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Indonezijos išskaitomo mokesčio ataskaita (ID-00005)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti ir sugeneruoti PPH išskaitomo mokesčio failą, kurį juridiniai subjektai naudoja Indonezijoje išskaitomo mokesčio operacijoms e-Bupot programoje kurti.

Indonezijos mokesčių inspekcija (DGT) nustato, kad apmokestinami naudojant e-Bupot taikymą, užregistruoti KPP Surinama kaip pajamų mokesčio rinkėjai (PPh) 23 straipsnis ir (arba) 26 straipsnis turi elektroniniu būdu pateikti pajamų mokesčio grąžinimo 23 ir 26 straipsnio ataskaitas. 

- **23 straipsnis** – Ataskaita apima visas išskaitomas operacijas iš tiekėjų, kurių pirminio adreso šalies/regiono kodas yra Indonezijos kodas.
- **26** straipsnis – Ataskaita apima visas išskaitomas operacijas iš tiekėjų, kur pirminio adreso šalies/regiono kodas nėra Indonezijos kodas.

## <a name="prerequisites"></a>Būtinieji komponentai

- Juridinio subjekto pagrindinis adresas turi būti Indonezijoje.
- Funkcijų valdymo **darbo srityje** turi būti įgalinta **visuotinių išskaitomų** mokesčių priemonė. Daugiau informacijos apie tai, kaip įjungti naujas funkcijas, žr. temoje [Funkcijų valdymo apžvalga.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Elektroninių ataskaitų konfigūracijų atsisiuntimas

Importavimo failo generavimas pagrįstas elektroninių ataskaitų (ER) konfigūracijoje. Daugiau informacijos apie galimybes ir konfigūruojamų ataskaitų sąvokas žr. [Elektroninių ataskaitų teikimas](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Norėdami naudoti gamybos ir vartotojo priėmimo tikrinimo (UAT) aplinkas, vadovaukitės instrukcijomis, [pateikiamomis atsisiųskite elektroninių ataskaitų konfigūracijas iš ciklo tarnybų](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Norėdami sugeneruoti importavimo failą iš saugyklos įkelkite šias konfigūracijas:

- **Mokesčių deklaracijos modelis.version.93.xml** arba naujesnė versija
- **Mokesčių deklaracijos modelio susiejimas.versija.93.153.xml** arba naujesnė versija
- **Koks PPh schemos importavimas (ID).version.93.14** ar naujesnė versija

## <a name="set-up-general-ledger-parameters"></a>Didžiosios knygos parametrų sąranka

1. Eiti į **Mokesčių** \> **nustatymo** \> **DK parametrus.**
2. Skirtuko Išskaitomas **mokestis lauke** Koks deklaracijos **formatas susiejimas pasirinkite** Koks **PPh schemos importavimas (ID).** 
3. Eikite **·** \> **·** \> **·** \> **·** **į Mokesčių nustatymo išskaitomo mokesčio išskaitomų mokesčių įplaukų tipus, norėdami nustatyti Kode Išskaitomo mokesčio įplaukų tipą Ir** tada priskirkite kodus susijusios prekės išskaitomo mokesčio grupėms. Kodai yra būtini, norint sugeneruoti integravimo failą naudojant e-Bupot programą. 

## <a name="generate-the-withholding-import-file"></a>Generuoti išskaitomo mokesčio importavimo failą

Tam tikro laikotarpio el. Bupot failo paruošimo ir generavimo procesas yra pagrįstas išskaitomo mokesčio operacijomis, kurios buvo užregistruotos sudengimo arba registravimo mokėjimo mokesčių užduoties metu.

Norėdami sugeneruoti failą, atlikite šiuos veiksmus.

1. Eiti į **Mokesčių deklaracijų** \> **·** \> **išskaitomo mokesčio** \> **PPH importo failo e-bupot 23 ir 26.**
2. Pasirinkite ataskaitos datą Nuo ir Iki, tada pasirinkite sudengimo laikotarpį.
3. Įveskite operacijos datą ir pasirinkite **Gerai**.
4. Pasirinkti kalbą. Visos ataskaitos verčiamos į JAV anglų (**en-us**) ir Į jaudą (**ID**).
5. Pasirinkite verslo tipą, o tada įveskite čekių ir dokumentų numerius. 
6. Patikrinkite, ar ataskaitą pasirašė vadovas. Ši informacija pranešama faile. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
