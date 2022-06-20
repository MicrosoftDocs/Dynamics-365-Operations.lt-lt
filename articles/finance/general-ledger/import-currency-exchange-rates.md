---
title: Importuoti valiutų kursus
description: Šiame straipsnyje pateikiama informacija apie užsienio valiutos kursų importavimo reikalavimus, kuriuos publikuoja valiutų kursų teikėjai.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 27f9b06646d9ce948a6b4528c38c5df9784b24b2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894941"
---
# <a name="import-currency-exchange-rates"></a>Valiutų kursų importavimas

[!include [banner](../includes/banner.md)]

Jei juridinis subjektas gavo SF užsienio valiuta, užsienio valiuta turi būti konvertuojama į vietos valiutą. Todėl reikalingi naujausi skirtingų valiutų kursai. Šiame straipsnyje pateikiama parametrų apžvalga ir apdorojimas, reikalingas norint importuoti užsienio valiutų nuorodų kursus, kuriuos skelbia valiutų kursų teikėjai, tokie kaip Europos centrinis bankas ir Rusijos centrinis bankas.

Toliau pateikiamuose skyriuose aprašomas informacijos, kuri naudojama nustatant ir apdorojant užsienio valiutų kursų importavimo procesą, srautas.

## <a name="configure-an-exchange-rate-provider"></a>Valiutų kursų teikėjo konfigūravimas
Prieš importuodami valiutų kursus turite nustatyti informaciją, kurios reikia valiutų kursų teikėjams. Naudokite puslapį **Konfigūruoti valiutų kursų teikėjus**, norėdami pasirinkti valiutų kursų teikėjus. Kai kurie valiutų kursų teikėjai yra įtraukti į demonstracinius duomenis programoje "Dynamics 365 Finance". Toliau esančioje lentelėje pateikiami šio puslapio valdiklių aprašymai.

| Laukas | Aprašas                   |
|-----------|-----------------------------------|
| **Pavadinimas**  | Valiutų kursų teikėjo pavadinimas.                                                                                                                                                                                     |
| **Raktas**   | Teikėjo reikalaujamas unikalus kiekvienos konfigūracijos informacijos dalies identifikatorius. Ši informacija automatiškai įtraukiama kiekvienam valiutų kursų teikėjui, kurį įtraukiate. |
| **Value** | Kiekvieno rakto informacija. Ši informacija įtraukiama kiekvienam valiutų kursų teikėjui, kurį įtraukiate.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valiutų kursų importavimas
Galite importuoti valiutų kursus iš valiutų kursų teikėjų šaltinio ir juos pridėti puslapyje **Valiutų kursai**. Naudokite puslapį **Importuoti valiutų kursus**, norėdami importuoti valiutų kursus. Toliau esančioje lentelėje pateikiami laukų, reikalingų importavimo procesui sėkmingai atlikti, aprašai.

| Laukas | Aprašas                   |
|-----------|-----------------------------------|
| **Valiutos kurso tipas**                 | Valiutos kurso tipas.                                                                                                                                                                                                                                                                                                                                                      |
| **Valiutų kursų teikėjas**             | Valiutų kursų teikėjas.                                                                                                                                                                                                                                                                                                                                                  |
| **Importuoti kaip**                       | Pagal šį parametrą nustatoma, ar importuoti šios dienos, ar konkretaus datų intervalo valiutų kursus. Jei norite naudoti datų intervalą, Įveskite arba pasirinkite pradžios ir pabaigos datas.                                                                                                                                                                                                                |
| **Sukurti būtinas valiutų poras**    | Pagal šį žymės langelį nustatomas automatinis valiutų porų kūrimas, jei importuojamų valiutų porų nėra. Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima.                                                                                                                                                                                               |
| **Nepaisyti esamų valiutų kursų**   | Pagal šį žymės langelį nustatomas esamo valiutų poros kurso naujinimas, kai tam tikros datos valiutos kursas jau nustatytas. Jei šio žymės langelio nepažymėsite, tam tikrų datų valiutos kursas nebus importuotas, kai nustatytas kitas valiutos kursas.                                                                                       |
| **Neleisti importuoti nacionalinės šventės metu** | Pagal šį žymės langelį nustatomas datos, kuri yra valstybinė šventė, valiutos kurso importavimas. Pavyzdžiui, jei pažymėsite šį žymės langelį ir kaip valiutų kursų teikėją naudosite Europos centrinį banką, sistema nenaujins valiutos kurso per valstybinę šventę, susijusią su dabartiniu juridiniu subjektu. Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima. |
| **Praėjusios dienos kursas** | Šis žymės langelis yra pasiekiamas, jei puslapyje **Funkcijų valdymas** įgalinate funkciją **ECB importavimas esamą arba praėjusią dieną**. Šį žymės langelį gali naudoti tik teikėjas, *Europos centrinis bankas*. Pažymėkite šį žymės langelį, jei norite importuoti valiutos keitimo kursą, kurį Europos Centrinis Bankas paskelbė praėjusią darbo dieną maždaug 16:00 val. Vidurio Europos laiku. Šis žymės langelis yra pažymėtas pagal numatytuosius nustatymus. Išvalykite šį žymės langelį, jei norite importuoti tą pačią darbo dieną publikuotus valiutų kursus.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]