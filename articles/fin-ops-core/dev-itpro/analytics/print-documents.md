---
title: Dokumento spausdinimo apžvalga
description: Dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Šiame straipsnyje pateikiama dokumentų spausdinimo apžvalga.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom:
- "69161"
- intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5a0d26836043ea225b9a6d3e62980ada2dc49b0a01a6dacec739b50f28e17bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728243"
---
# <a name="document-printing-overview"></a>Dokumento spausdinimo apžvalga

[!include [banner](../includes/banner.md)]

Dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Šiame straipsnyje pateikiama dokumentų spausdinimo apžvalga.

## <a name="printing-overview"></a>Spausdinimo apžvalga

Programoje pateikiamos integruotos tarnybos ir kliento programos, kurias naudojant lengva kurti, saugoti ir platinti dokumentus, kurie palaiko verslo veiklą. Dokumentus galima spausdinti naudojant vietinį spausdintuvą arba per tinklą prijungtą įrenginį. Be to, puslapius ir ataskaitas galite eksportuoti tiesiogiai iš kliento kaip PDF failus arba „Microsoft Office“ dokumentus. Galiausiai, paskirstytas darbo krūvis suteikia galimybę spausdinti verslo dokumentus tiesiai iš mobiliojo įrenginio naudojant tinklo išteklius. Nors spausdinimo reikalavimai gali skirtis, visose pramonės šakose paprastai turi būti sukurtos popierinės verslo dokumentų kopijos naudojant programą. Dokumentų spausdinimas per tinklo įrenginius iš nuomojamų programų sukelia unikalių problemų. Štai keletas pavyzdžių:

- Vartotojo įrenginyje gali nebūti spausdinimo tvarkyklių.
- Vartotojo įrenginys gali būti neprijungtas prie įmonės tinklo.

Naudodami specialiai tam skirtą pagrindinį kompiuterį ir vykdydami šiuos lengvus veiksmus, sistemos administratoriai gali konfigūruoti įdiegtis, kad vartotojai galėtų spausdinti tiesiai iš verslo programų per tinklo įrenginius.

### <a name="application-printing-scenarios"></a>Spausdinimo scenarijai programose 

Šioje lentelėje aprašomi trys pirminiai spausdinimo scenarijai.

| Scenarijus                        | Tikslas                                                      | Sprendimas |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Matomo vaizdo spausdinimas        | Spausdinkite tai, kas šiuo metu rodoma naršyklėje.             | Sugeneruojama spausdinti tinkama naršyklės ekrano versija. |
| 2. Interaktyvus spausdinimas         | Spausdinkite tikslų dokumentą vietiniame prijungtame įrenginyje. | Galite eksportuoti ataskaitos PDF versiją ir atsisiųsti ją į naršyklę. |
| 3. Spausdinimas tinklo įrenginyje | Išsiųskite tikslų dokumentą į domeno spausdintuvo įrenginį.     | Tikslus dokumentas siunčiamas į kliento programą, veikiančią serveryje, kuris nuomojamas kliento domene. |

Kadangi sprendimas priklauso nuo scenarijaus, programos suteikia integruotas tarnybas ir įrankius, kad vartotojai galėtų lengviau pasiekti savo tikslus.

- **1 scenarijų** palaiko HTML5 kliento naršyklės atvaizdavimas.
- **2 scenarijus** naudoja kliento programas ir „Microsoft 365“ tarnybas.
- **3 scenarijui** būtinas palaikymas iš kliento programų ir paslaugų, kurios nuomojamos „Microsoft Azure“.

Be platformos, kuri yra įdiegta „Azure“ prenumeratoje, Finance and Operations programos suteikia klientams integruotą „Azure“ programą, kuri jiems padeda lengviau naudoti domene nuomojamus įrenginius dokumentams spausdinti.

## <a name="service-overview"></a>Tarnybos apžvalga
Nors nuomojamų programų sukuriami dokumentai turi būti spausdinami per tinklą prijungtame įrenginyje, jie saugomi „Azure“ dvejetainio didelio objekto saugykloje. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](install-document-routing-agent.md) naudoja „Azure“ autentifikavimą, kad sukurtų saugų prieigos prie „Azure“ tarnybų kanalą.

**Vykdymo seka**

1. Ataskaitą generuoja „Microsoft SQL Server Reporting Services“ (SSRS) ir ji saugoma „Azure“ dvejetainio didelio objekto saugykloje. Pridėti spausdintuvo parametrai saugomi kartu su dokumentu.
2. Dokumento maršruto planavimo agentas teikia aktyvių užduočių užklausas „Azure Service Bus“ eilei.
3. Dokumento maršruto planavimo agentas atsisiunčia dokumentą ir dokumentas yra įkeliamas į tinklo spausdintuvą.

Kliento sprendimas suteikia galimybę klientams valdyti spausdinimo poreikių mastą. Klientai, kurie turi spausdinti labai daug dokumentų, gali įdiegti daug dokumento maršruto planavimo agentų, kad padidintų vienu metu vykstančių spausdinimo operacijų skaičių. Be to, kai kuriems klientams reikia įdiegti labai mažai dokumento maršruto planavimo agentų savo spausdinimo poreikiams patenkinti.

### <a name="service-components-for-network-printing"></a>Spausdinimo per tinklą tarnybos komponentai

Toliau nurodytoje diagramoje pateikiami pagrindiniai komponentai, kurie padeda palaikyti spausdinimo per tinklą operacijas.

[![service-components-for-network-printing”\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Atkreipkite dėmesį, kad vieną spausdintuvą galime užregistruoti keliuose dokumento maršruto planavimo agentuose. Spausdintuvo nuostatoms suderinti nuomojama tarnyba naudoja tinklo maršrutą, kuris unikaliai identifikuoja kiekvieną tinklo spausdintuvą. Todėl net tada, kai spausdintuve užregistruojami keli klientai, jis rodomas kaip viena programų spausdintuvų sąrašo parinktis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]