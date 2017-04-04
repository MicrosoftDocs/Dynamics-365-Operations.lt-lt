---
title: "Importuoti valiutų kursus"
description: "Jei juridinis asmuo gavo SF užsienio valiuta, būtina paversti vietine valiuta užsienio valiuta. Tai reiškia, kad naujausią skirtingų valiutų keitimo kursai yra reikalaujama. Šioje temoje pateikta apžvalga reikiamus parametrus bei perdirbti skirtų keitimo orientaciniai kursai skelbiami internetu kursas teikėjų, pvz., Europos centrinio banko ir Rusijos centrinio banko."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Importuoti valiutų kursus

Jei juridinis asmuo gavo SF užsienio valiuta, būtina paversti vietine valiuta užsienio valiuta. Tai reiškia, kad naujausią skirtingų valiutų keitimo kursai yra reikalaujama. Šioje temoje pateikta apžvalga reikiamus parametrus bei perdirbti skirtų keitimo orientaciniai kursai skelbiami internetu kursas teikėjų, pvz., Europos centrinio banko ir Rusijos centrinio banko.

Šiuose skyriuose aprašoma informacija, kuri naudojama kuriant ir apdorojant užsienio valiutų kursų importas srautą.

## <a name="configure-an-exchange-rate-provider"></a>Konfigūruoti kursas teikėjas
Prieš galite importuoti valiutų kursus, jūs turite nustatyti informacija, kurios reikia iš paslaugų teikėjų, kurie siūlo valiutos kursų. Naudoti su **konfigūruoti kursas teikėjų** puslapį ir pasirinkite keitimo kursas paslaugų teikėjai. Kai kursas teikėjai yra įtraukti su Microsoft Dynamics 365 operacijoms parodomuosiuose duomenyse. Šioje lentelėje pateikiami šio puslapio valdiklių aprašymai.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Valiutų kursų teikėjo pavadinimas.                                                                                                                                                                                     |
| **Raktas**   | Teikėjo reikalaujamas unikalus kiekvienos konfigūracijos informacijos dalies identifikatorius. Ši informacija automatiškai įtraukiama kiekvieno keitimo kursas teikėjo, įtraukti kai jūs spustelėkite į **pridėti** mygtuką. |
| **Value** | Kiekvieno rakto informacija. Ši informacija įtraukiama už kiekvieną valiutos kurso teikėjas, įtraukti kai jūs spustelėkite į **pridėti** mygtuką.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importuoti valiutų kursus
Galite importuoti valiutų kursus iš valiutos kurso teikėjams šaltinis, ir nustatyti juos į **valiutos kurso** puslapis. Naudoti su **importuoti valiutų kursai** puslapis importo valiutų kursai. Šioje lentelėje pateikiami aprašymai, kurių reikia norint sėkmingai baigti importavimo procesą laukų.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Valiutos kurso tipas.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Kursas teikėjas.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Šis parametras valdo ar importuoti šiandienos data arba datos ribas. Jei norite naudoti datos diapazoną, įveskite arba pasirinkite pradžios ir pabaigos datos.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Šis žymės langelis valdo automatiškai sukurti valiutų porų, jei nėra valiutų porų, kurios yra importuojamos. Kai kurie paslaugų teikėjai šios parinkties gali nebūti.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Šis žymės langelis valdo naujinti esamus valiutų poros kursas kai kursas konkrečią datą jau egzistuoja. Jei nepažymėsite šio žymės langelio, konkrečių datų kursas nėra importuojama, jei kito keitimo kursas jau yra.                                                                                       |
| **Prevent import on national holiday** | Šis žymės langelis valdo importuoti valiutų keitimo kursą už datą, kuri yra valstybinė šventė. Pavyzdžiui, jei pažymėkite šį žymės langelį ir naudoti Europos centrinio banko kursas teikėjas, sistema neatnaujins valiutos kursas švente, kuri yra susijusi su šiuo juridiniu asmeniu. Kai kurie paslaugų teikėjai šios parinkties gali nebūti. |




