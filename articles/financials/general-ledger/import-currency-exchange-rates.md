---
title: "Importuoti valiutų kursus"
description: "Jei juridinis subjektas gavo SF užsienio valiuta, svarbu užsienio valiutą konvertuoti į vietos valiutą. Todėl reikalingi naujausi skirtingų valiutų kursai. Šioje temoje pateikiama informacija apie užsienio valiutų kursų nuorodų, kurias internete skelbia valiutų kursų teikėjai (pvz., Europos centrinis bankas ir Rusijos centrinis bankas), importavimo reikiamus parametrus ir apdorojimą."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c80f6eec7c4d5129337b6f7869fbd8a4cc978acd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="import-currency-exchange-rates"></a>Importuoti valiutų kursus

[!include[banner](../includes/banner.md)]


Jei juridinis subjektas gavo SF užsienio valiuta, svarbu užsienio valiutą konvertuoti į vietos valiutą. Todėl reikalingi naujausi skirtingų valiutų kursai. Šioje temoje pateikiama informacija apie užsienio valiutų kursų nuorodų, kurias internete skelbia valiutų kursų teikėjai (pvz., Europos centrinis bankas ir Rusijos centrinis bankas), importavimo reikiamus parametrus ir apdorojimą.

Toliau pateikiamuose skyriuose aprašomas informacijos, kuri naudojama nustatant ir apdorojant užsienio valiutų kursų importavimo procesą, srautas.

## <a name="configure-an-exchange-rate-provider"></a>Valiutų kursų teikėjo konfigūravimas
Prieš importuodami valiutų kursus turite nustatyti informaciją, kurios reikia valiutų kursų teikėjams. Naudokite puslapį **Konfigūruoti valiutų kursų teikėjus**, norėdami pasirinkti valiutų kursų teikėjus. Kai kurie valiutų kursų teikėjai yra įtraukti į „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ demonstracinius duomenis. Toliau esančioje lentelėje pateikiami šio puslapio valdiklių aprašymai.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Laukas** | **Aprašas**                                                                                                                                                                                                             |
| **Pavadinimas**  | Valiutų kursų teikėjo pavadinimas.                                                                                                                                                                                     |
| **Raktas**   | Teikėjo reikalaujamas unikalus kiekvienos konfigūracijos informacijos dalies identifikatorius. Ši informacija automatiškai įtraukiama ir priskiriama kiekvienam valiutų kursų teikėjui, kurį įtraukiate spustelėdami mygtuką **Įtraukti**. |
| **Vertė** | Kiekvieno rakto informacija. Ši informacija įtraukiama ir priskiriama kiekvienam valiutų kursų teikėjui, kurį įtraukiate spustelėdami mygtuką **Įtraukti**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importuoti valiutų kursus
Galite importuoti valiutų kursus iš valiutų kursų teikėjų šaltinio ir juos nustatyti puslapyje **Valiutų kursai**. Naudokite puslapį **Importuoti valiutų kursus**, norėdami importuoti valiutų kursus. Toliau esančioje lentelėje pateikiami laukų, reikalingų importavimo procesui sėkmingai atlikti, aprašai.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Laukas**                              | **Aprašas**                                                                                                                                                                                                                                                                                                                                                             |
| **Valiutos kurso tipas**                 | Valiutos kurso tipas.                                                                                                                                                                                                                                                                                                                                                      |
| **Valiutų kursų teikėjas**             | Valiutų kursų teikėjas.                                                                                                                                                                                                                                                                                                                                                  |
| **Importuoti kaip**                       | Pagal šį parametrą nustatoma, ar importuoti šios dienos, ar datų intervalo valiutų kursus. Jei norite naudoti datų intervalą, Įveskite arba pasirinkite pradžios ir pabaigos datas.                                                                                                                                                                                                                |
| **Sukurti būtinas valiutų poras**    | Pagal šį žymės langelį nustatomas automatinis valiutų porų kūrimas, jei importuojamų valiutų porų nėra. Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima.                                                                                                                                                                                               |
| **Nepaisyti esamų valiutų kursų**   | Pagal šį žymės langelį nustatomas esamo valiutų poros kurso naujinimas, kai tam tikros datos valiutos kursas jau nustatytas. Jei šio žymės langelio nepažymėsite, tam tikrų datų valiutos kursas nebus importuotas, kai nustatytas kitas valiutos kursas.                                                                                       |
| **Neleisti importuoti nacionalinės šventės metu** | Pagal šį žymės langelį nustatomas datos, kuri yra valstybinė šventė, valiutos kurso importavimas. Pavyzdžiui, jei pažymėsite šį žymės langelį ir kaip valiutų kursų teikėją naudosite Europos centrinį banką, sistema nenaujins valiutos kurso per valstybinę šventę, susijusią su dabartiniu juridiniu subjektu. Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima. |






