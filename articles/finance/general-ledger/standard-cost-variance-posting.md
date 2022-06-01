---
title: Standartinių išlaidų nuokrypio registravimas
description: Šioje temoje pateikiama informacija apie standartinės įkainojimo registravimo šablonų nustatymą.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804643"
---
# <a name="standard-cost-variance-posting"></a>Standartinių išlaidų nuokrypio registravimas

Kai savo organizacijoje naudojate standartinį vieno ar daugiau produktų įkainojimo kaštus, turite [sukonfigūruoti būtinas standartinio įkainojimo sąlygas](/supply-chain/cost-management/prerequisites-standard-costs.md). Šioje temoje paaiškinamos registravimo sąskaitos, kurių reikia 3 iš būtinųjų komponentų žingsniui, "Priskirkite DK sąskaitas prekių registravimui, kurie yra susiję su standartinės savikainos nuokrypiais".

Gali atsirasti skirtingų tipų pirkimo ir gamybos užsakymų nuokrypiai. Gamybos nuokrypių pavyzdžių ieškokite bendrieji [gamybos nuokrypių šaltiniai](/supply-chain/cost-management/common-sources-of-production-variances.md). Pirkimo užsakymo kainų nuokrypiai atsiranda, kai įsigytai prekei naudojate standartinę savikainą, o pirkimo užsakyme yra skirtumas tarp produkto standartinės savikainos ir sumos, už kurią išrašyta SF.

## <a name="sample-posting-profile-configuration"></a>Registravimo šablono konfigūracijos pavyzdys

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų pavyzdžiai. Ji apima pagrindinių sąskaitų ir aprašų pavyzdį.

- Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai yra debetas, ar kreditas. Kai kuriais atvejais operacija gali registruoti debetus arba kreditus.
- Stulpelyje Kliringo sąskaita nurodoma, kad registravimo tipas yra tarpuskaitos sąskaita. Kitaip tariant, šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.
- Stulpelis P/F nurodo registravimo tipą. "P" rodo faktiškai užregistravimą, o "F" reiškia finansinį registravimą.
- Stulpelyje Sekti nurodoma, ar registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo pagrindinė sąskaita. Tiksliau nurodo registravimo tipą, kuris paprastai naudojamas.

> [!NOTE]
> Lentelėje pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Pirkimo kainų nuokrypis | 510310 | Pirkimo kainų nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai yra nuokrypis tarp pirkimo kainos ir standartinės pirkimo užsakymo savikainos. |
| Atsargų išlaidų perkainojimas | 510330 | Atsargų išlaidų perkainojimas | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai suaktyvinama nauja įkainojimo versija, kad standartinė išlaidų prekė perkainoti turimos atsargos. |
| Išlaidų pokyčio nuokrypis | 510320 | Išlaidų pokyčio nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai standartinės savikainos atsiranda tarp teritorijų arba kai prekė grąžinama ir esama pradinio standartinių išlaidų ir dabartinio produkto standartinių išlaidų pokytis. |
| Gamybos partijos dydžio nuokrypis | 510370 | Gamybos partijos dydžio nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai skiriasi komplektavimo specifikacijos (KS) skaičiavimo pagrindas ir faktinis kiekis, naudojamas skaičiuojant gamybos užsakymo išlaidas. |
| Gamybos kainų nuokrypis | 510340 | Gamybos kainų nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai skiriasi įvertintos išlaidos ir faktinės gamybos užsakymo išlaidos. |
| Gamybos kiekio nuokrypis | 510350 | Gamybos kiekio nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai yra skirtumų tarp įvertintos savikainos ir faktinių gamybos užsakymo išlaidų. |
| Gamybos pakaitalo nuokrypis | 510360 | Gamybos pakaitalo nuokrypis | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai gamybos užsakyme yra netikėtas suvartojimas. |
| Apvalinimo nuokrypis | 618160 | Apvalinimo skirtumas | Išlaidos | Arba | Ne | Pn. | Netaikoma | Ši sąskaita naudojama, kai yra apvalinimo skirtumas, kai gamybos išlaidos skaičiuojamos iš standartinių išlaidų. |
