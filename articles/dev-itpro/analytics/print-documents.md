---
title: Dokumento spausdinimas
description: „Microsoft Dynamics 365 for Finance and Operations“ dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Šiame straipsnyje pateikiama dokumentų spausdinimo apžvalga.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc45865b55b4794202408ca19a0776440382fdd
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850076"
---
# <a name="document-printing"></a>Dokumento spausdinimas

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Šiame straipsnyje pateikiama dokumentų spausdinimo apžvalga.

## <a name="printing-overview"></a>Spausdinimo apžvalga

„Microsoft Dynamics 365 for Finance and Operations“ pateikiamos integruotos tarnybos ir kliento programos, kurias naudojant lengva kurti, saugoti ir platinti dokumentus, kurie palaiko verslo veiklą. „Finance and Operations“ dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Be to, „Finance and Operations“ puslapius ir ataskaitas galite eksportuoti tiesiogiai iš kliento kaip PDF failus arba „Microsoft Office“ dokumentus. Galiausiai, paskirstytas darbo krūvis suteikia galimybę spausdinti verslo dokumentus tiesiai iš mobiliojo įrenginio naudojant tinklo išteklius. Nors spausdinimo reikalavimai gali skirtis, visose pramonės šakose paprastai turi būti sukurtos popierinės verslo dokumentų kopijos naudojant „Finance and Operations“. Dokumentų spausdinimas per tinklo įrenginius iš nuomojamų programų sukelia unikalių problemų. Štai keletas pavyzdžių:

- Vartotojo įrenginyje gali nebūti spausdinimo tvarkyklių.
- Vartotojo įrenginys gali būti neprijungtas prie įmonės tinklo.

Naudodami specialiai tam skirtą pagrindinį kompiuterį ir vykdydami šiuos lengvus veiksmus, sistemos administratoriai gali konfigūruoti įdiegtis, kad vartotojai galėtų spausdinti tiesiai iš verslo programų per tinklo įrenginius.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Spausdinimas „Finance and Operations“ programose

Toliau nurodytoje lentelėje aprašomi trys pirminio spausdinimo scenarijai „Finance and Operations“ programose.

| Scenarijus                        | Tikslas                                                      | Sprendimas |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Matomo vaizdo spausdinimas        | Spausdinkite tai, kas šiuo metu rodoma naršyklėje.             | Sugeneruojama spausdinti tinkama naršyklės ekrano versija. |
| 2. Interaktyvus spausdinimas         | Spausdinkite tikslų dokumentą vietiniame prijungtame įrenginyje. | Galite eksportuoti ataskaitos PDF versiją ir atsisiųsti ją į naršyklę. |
| 3. Spausdinimas tinklo įrenginyje | Išsiųskite tikslų dokumentą į domeno spausdintuvo įrenginį.     | Tikslus dokumentas siunčiamas į kliento programą, veikiančią serveryje, kuris nuomojamas kliento domene. |

Kadangi sprendimas priklauso nuo konkrečios situacijos, „Finance and Operations“ programos suteikia integruotas tarnybas ir įrankius, kad vartotojai galėtų lengviau pasiekti savo tikslus.

- **1 scenarijų** palaiko HTML5 kliento naršyklės atvaizdavimas.
- **2 scenarijų** naudoja kliento programos ir „Microsoft Office 365“ tarnybos.
- **3 scenarijui** būtinas palaikymas iš kliento programų ir paslaugų, kurios nuomojamos „Microsoft Azure“.

Be platformos, kuri yra įdiegta „Azure“ prenumeratoje, „Finance and Operations“ programos suteikia klientams integruotą „Azure“ programą, kuri jiems padeda lengviau naudoti domene nuomojamus įrenginius dokumentams spausdinti.

## <a name="service-overview"></a>Tarnybos apžvalga
Nors nuomojamų programų sukuriami dokumentai turi būti spausdinami per tinklą prijungtame įrenginyje, jie saugomi „Azure“ dvejetainio didelio objekto saugykloje. [Dokumento maršruto planavimo agentas](install-document-routing-agent.md) naudoja „Azure“ autentifikavimą, kad sukurtų saugų prieigos prie „Azure“ tarnybų kanalą.

**Vykdymo seka**

1. Ataskaitą generuoja „Microsoft SQL Server Reporting Services“ (SSRS) ir ji saugoma „Azure“ dvejetainio didelio objekto saugykloje. Pridėti spausdintuvo parametrai saugomi kartu su dokumentu.
2. Dokumento maršruto planavimo agentas teikia aktyvių užduočių užklausas „Azure Service Bus“ eilei.
3. Dokumento maršruto planavimo agentas atsisiunčia dokumentą ir dokumentas yra įkeliamas į tinklo spausdintuvą.

Kliento sprendimas suteikia galimybę klientams valdyti spausdinimo poreikių mastą. Klientai, kurie turi spausdinti labai daug dokumentų, gali įdiegti daug dokumento maršruto planavimo agentų, kad padidintų vienu metu vykstančių spausdinimo operacijų skaičių. Be to, kai kuriems klientams reikia įdiegti labai mažai dokumento maršruto planavimo agentų savo spausdinimo poreikiams patenkinti.

### <a name="service-components-for-network-printing"></a>Spausdinimo per tinklą tarnybos komponentai

Toliau nurodytoje diagramoje pateikiami pagrindiniai komponentai, kurie padeda palaikyti spausdinimo per tinklą operacijas.

[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Atkreipkite dėmesį, kad vieną spausdintuvą galime užregistruoti keliuose dokumento maršruto planavimo agentuose. Spausdintuvo nuostatoms suderinti nuomojama tarnyba naudoja tinklo maršrutą, kuris unikaliai identifikuoja kiekvieną tinklo spausdintuvą. Todėl net tada, kai spausdintuve užregistruojami keli klientai, jis rodomas kaip viena „Finance and Operations“ programų spausdintuvų sąrašo parinktis.
