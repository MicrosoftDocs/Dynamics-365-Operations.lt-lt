---
title: Mokesčių skaičiavimas (peržiūros versija)
description: Šioje temoje paaiškinama bendroji Mokesčių skaičiavimo galimybės apimtis ir funkcijos.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bab6e0e0ea1b9fb7f598e37843b52e3ba9c7f94e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336637"
---
# <a name="tax-calculation-preview"></a>Mokesčių skaičiavimas (peržiūros versija)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mokesčių skaičiavimas yra hiper išplečiama kelių nuomotojų paslauga, įgalinanti „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą. Visiškai konfigūruotinas mokesčių modulis. Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę. Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.

Mokesčių skaičiavimas integruojamas su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.

> [!IMPORTANT]
> Kai įgalinate mokesčių skaičiavimo tarnybą, kai kurios su susijusiais duomenimis susijusios operacijos gali būti atliekamos ne duomenų centre, kuris prižiūri jūsų aptarnavimo duomenis. Prieš [įgalindami mokesčių](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) skaičiavimo tarnybą, peržiūrėkite sąlygas. Mes rūpinamės jūsų privatumu. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

Mokesčių skaičiavimas yra mikrotarnyba pagrįstas mokesčių variklis, siūlantis eksponentinį išplečiamumą. Galite atlikti šias užduotis:

- Konfigūruokite Mokesčių skaičiavimą per „Regulatory Configuration Service“ (RCS). RCS yra patobulinta elektroninių ataskaitų (ER) dizaino įrankio versija, galima naudoti kaip atskirą paslaugą.
- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.
- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatytas registracijos numeris.
- Konfigūruokite mokesčių skaičiavimo konstruktorių, kad būtų galima apibrėžti formules ir sąlygas.
- Juridiniuose subjektuose bendrai naudoti mokesčių nustatymo ir skaičiavimo sprendimą.

Norėdami naudoti mokesčių skaičiavimo tarnybą, įdiekite mokesčių skaičiavimo tarnybos priedą iš ciklo tarnybų „Microsoft Dynamics Lifecycle Services“ (LCS) projekto. Tada užbaikite RCS nustatymą ir įjunkite mokesčių skaičiavimo paslaugą „Finance and Supply Chain Management“. Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Prieinamumas

Mokesčių skaičiavimas galimas tik smėlio dėžės aplinkose ir tik pasirinktiems klientams, naudojant viešosios peržiūros versijos programą. Galiausiai ji bus bendrai pasiekiama visiems klientams ir gamybos aplinkoje.

Atsiras vis naujos funkcijas, tad nepamirškite dažnai peržvelgti naujausią dokumentaciją, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.

Mokesčių skaičiavimas yra įdiegtas toliau nurodytose „Azure" geografinėse srityse. Ji taip pat bus įdiegta į daugiau „Azure" geografinių diagramų, atsižvelgiant į kliento poreikius:

- Jungtinės Valstijos
- Europa

> [!NOTE]
> Mokesčių skaičiavimas nepalaiko „Dynamics 365" vietinių diegimų. Tai nepalaiko ir ankstesnių versijų, pvz., „Dynamics AX 2012".

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.
- Kelių mokesčių registracijos numerių palaikymas
- Perkėlimo užsakymo palaikymas nustatant mokesčius ir skaičiuojant
- Perkėlimo užsakymo palaikymas nustatant kelių mokesčių registracijos numerius

## <a name="supported-transactions"></a>Palaikomos operacijos

Mokesčių skaičiavimą gali įgalinti juridinis subjektas ir operacija. Palaikomos toliau nurodytos operacijos:

- Pardavimo procesas

    - Pardavimo pasiūlymas
    - Pardavimo užsakymas
    - Patvirtinimas
    - Išrinkimo dokumentas
    - Važtaraštis
    - Pardavimo sąskaita faktūra
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė

- Pirkimo procesas

    - Pirkimo užsakymas
    - Patvirtinimas
    - Gavimų sąrašas
    - Gavimo dokumentas
    - Pirkimo SF
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Pirkimo paraiška
    - Papildomos pirkimo paraiškos eilutės išlaidos
    - Pasiūlymo patvirtinimas
    - Pasiūlymo patvirtinimo antraštės papildomos išlaidos
    - Pasiūlymo patvirtinimo eilutės papildomos išlaidos

- Atsargų procesas

    - Perlaidos užsakymas - siuntimas
    - Perlaidos užsakymas - gavimas

## <a name="related-resources"></a>Susiję ištekliai

[Darbo su mokesčių paslaugomi pradžia](./global-get-started-with-tax-calculation-service.md)

[Kelių PVM registracijų numeris](./emea-multiple-vat-registration-numbers.md)

[Mokesčių priemonės perkėlimo užsakymo palaikymas](./tasks/tax-feature-support-for-transfer-order.md)

[Kaip sukurti plėtinį mokesčių tarnybose](./tax-service-add-data-fields-tax-integration-by-extension.md)
