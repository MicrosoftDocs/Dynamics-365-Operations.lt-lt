---
title: "KS ir formulių eilučių išdavimas į sandėlį"
description: "Šioje temoje aprašomas KS eilučių ir formulės eilučių žaliavų išdavimo į sandėlį procesas."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: 2bccabb033f5ba142b145e69930ce516aad596f2
ms.contentlocale: lt-lt
ms.lasthandoff: 05/23/2018

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>KS ir formulių eilučių išdavimas į sandėlį

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas KS eilučių ir formulės eilučių žaliavų išdavimo į sandėlį procesas. Kai į sandėlį išduodate KS arba formulės eilutę, sistema pirmiausia nustato, ar medžiagos jau yra gamybos įvesties vietoje ceche, kur medžiaga bus naudojama gamybos proceso metu.

- Jei medžiagos yra gamybos įvesties vietoje, ji paimama iš tos vietos iš karto davus signalą išduoti medžiagą į sandėlį.
- Jei medžiagos gamybos įvesties vietoje nėra, medžiagos išdavimas nurodo, kad medžiagą reikia perkelti iš sandėlio vietų į gamybos įvesties vietą. Medžiaga perkeliama naudojant žaliavų paėmimo sandėlio darbą. Todėl žaliavų paėmimo sandėlio procesus reikia sukonfigūruoti. Daugiau informacijos žr. [Papildymas](../warehousing/replenishment.md) ir [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>KS ir formulės eilučių išdavimo būdai

Galite konfigūruoti KS ir formulės eilučių išdavimą, kad jis būtų vykdomas kaip gamybos užsakymo arba paketinio užsakymo dalis. Taip pat išdavimą galima valdyti naudojant paketinę užduotį arba neautomatiškai.

KS ir formulės eilučių išdavimo būdą valdo parametras **Gamybos eilutės išdavimas**. Šį parametrą galite rasti pasirinkę **Gamybos valdymas**\>**Sąranka**\>**Gamybos parametrai**.

- **KS ir formulės eilučių kaip gamybos arba paketinio užsakymo išdavimas** – naudojant šį būdą, gamybos arba paketinio užsakymo KS ir formulės eilutės išduodamos kaip užsakymo išdavimo proceso dalis. Paprastai vykdant gamybos arba paketinio užsakymo išdavimą, gamybos užduotys išduodamos cecho darbuotojams, o gamybos dokumentai išspausdinami. Šio proceso metu užsakymo būsena taip pat pakeičiama į **Išduota**.
- **KS ir formulės eilučių išdavimas naudojant paketinę užduotį arba neautomatiškai** – naudojant šį metodą, KKS ir formulės eilutes galima išduoti tik per paketinę užduotį **Automatinio KS ir formulės eilučių išdavimas** arba neautomatiškai. Norėdami neautomatiškai išduoti KS ir formulės eilutes, gamybos užsakymų sąrašo puslapio arba gamybos užsakymo informacijos puslapio veiksmų srityje pasirinkite **Išduoti į sandėlį**.

Trumpa demonstracija, kaip išleisti KS ir formulės eilutes į gamybą naudojant paketinę užduotį, parodyta šiame trumpame „YouTube“ vaizdo įraše: [Gamybos išrinkimas sandėlyje naudojant paketą](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>KS ir formulės eilučių išdavimas naudojant paketinę užduotį

Paketinė užduotis **Automatinis KS ir formulės eilučių išdavimas** apdoroja pasirinktas KS ir formulės eilutes, turinčias likusio kiekio, kurį reikia išduoti. Užduotis tikrina tik užsakymus, kurių būsena yra **Išduota**, **Pradėta** arba **Paskelbta baigtu**. Jei KS arba formulės eilutėje yra likusio kiekio, kurį reikia išduoti, užduotis išduoda kiekį, kurį gali padengti jau faktiškai rezervuotas kiekis ir faktiškai turimas kiekis.

### <a name="example-of-a-batch-job-release"></a>Paketinės užduoties išdavimo pavyzdys

| Scenarijus | Likęs išleistinas kiekis | Faktiškai rezervuotas kiekis | Faktiškai turimas kiekis | Paketinės užduoties išduotas kiekis |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Paketinės užduoties sąranka

Paketinės užduoties **Automatinis KS ir formulės eilučių išdavimas** užklausoje galite nustatyti filtravimo kriterijus, norėdami nurodyti, prieš kiek dienų užduotis turi ieškoti eilučių, turinčių neišduoto kiekio. Užduoties užklausos lauke **Žaliavų reg. data** naudokite funkciją **(LessThanDate())** kaip filtravimo kriterijų.

Tolesniame pavyzdyje rodomas gamybos užsakymas, kuriame yra dvi užduotys, 10 ir 20, apimančios gamybos užsakymo surinkimą ir pakavimą. Kiekviena užduotis nustatoma sunaudoti medžiagos kiekį. Šiame pavyzdyje išdavimo laiko riba, kurią nurodo žalia rodyklė po laiko eilute, lygi dienų, nurodytų kriterijuje **(LessThanDate())** skaičiui. Pvz., **(LessThanDate(2))** nurodo, kad užduotis turi ieškoti neišduotų kiekių tik dviejų dienų laikotarpyje.

![Gamybos užsakymo, kuriame yra dvi paketinės užduotys, pavyzdys](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Medžiagos išdavimas pagal operacijos numerį arba proporcingai baigtų prekių kiekiui

Jei medžiagas išduosite naudodami parametro nustatymą **Išduodant gamybos užsakymą**, vykdydami neautomatinį išdavimą galėsite pasirinkti iš dviejų medžiagų išdavimo valdymo parinkčių, nurodytų toliau.

- Išduoti medžiagą pagal operacijos numerį.
- Išduoti medžiagą proporcingai baigtų prekių kiekiui.

### <a name="release-material-per-operation-number"></a>Medžiagos išdavimas pagal operacijos numerį

Norėdami valdyti operacijas, į kurias medžiagos turi būti išduotos, naudokite puslapį **Išduoti į sandėlį**.

- Pasirinkite **Gamybos valdymas** \> **Gamybos užsakymai** \> **Visi gamybos užsakymai**, pasirinkite gamybos užsakymą, tada skirtuke **Sandėlis** pasirinkite **Išduoti į sandėlį**. Tada naudokite laukus **Nuo Oper. nr.** ir **iki Oper. nr.**, kad nurodytumėte operacijos numerių intervalą.

Tolesniame pavyzdyje parodytas gamybos užsakymas, kuriame yra dvi operacijos, 10 ir 20. Šiame pavyzdyje, jei išdavimą į operaciją apribosite iki 10, bus išduota tik medžiaga M9203.

![Medžiagos išdavimo pagal operacijos numerį pavyzdys](media/two-operations.PNG)

Trumpa demonstracija, kaip išduoti medžiagą proporcingai baigtų prekių kiekiui, parodyta šiame trumpame „YouTube“ vaizdo įraše: [Gamybos užsakymo išleidimo proceso patobulinimai programoje „Dynamics 365 for Finance and Operations“](https://www.youtube.com/watch?v=Rm3ojAz6Zu0)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Medžiagos išdavimas, proporcingas baigtų prekių kiekiui

Galite išduoti dalinio baigtų prekių kiekio arba konkretaus vieneto žaliavas.

- Norėdami išduoti dalinio baigtų prekių kiekio žaliavas, pasirinkite **Gamybos valdymas** \> **Gamybos užsakymai** \> **Visi gamybos užsakymai**, pasirinkite gamybos užsakymą, tada skirtuke **Sandėlis** pasirinkite **Išduoti į sandėlį**. Tada įveskite kiekį lauke **Kiekis**.

    Pvz., sukuriamas gamybos užsakymas ir numatoma pagaminti 1 000 vienetų (vnt.). Cecho prižiūrėtojas planuoja 100 vnt. gamybą, skirtą kitai pamainai, ir nori, kad būtų išduotos tik tai pamainai skirtos medžiagos. Tokiu atveju prižiūrėtojas gali naudoti lauką **Kiekis**, kad išduotų medžiagas, skirtas 100 vnt., kuriuos planuojama pagaminti per kitą pamainą.

- Norėdami išduoti konkretaus vieneto žaliavas, pasirinkite **Gamybos valdymas** \> **Gamybos užsakymai** \> **Visi gamybos užsakymai**, pasirinkite gamybos užsakymą, tada skirtuke **Sandėlis** pasirinkite **Išduoti į sandėlį**. Tada naudokite lauką **Vienetas** ir pasirinkite baigtos prekės medžiagos išdavimo vienetą.

    Galimi vienetai yra nustatyti baigtos prekės vienetų sekų grupėje.

    Pavyzdžiui, toliau nurodytas baigtos prekės vieneto konvertavimo santykis tarp svarų ir padėklų (PL): 1 PL = 100 svarų. Norėdami kurti gamybos užsakymą, skirtą 10 000 svarų baigtų prekių pagaminti, galite išduoti žaliavas pagal padėklų, kuriuos ketinate pagaminti, skaičių. Kaip vienetą pasirinkite **PL** ir tada pasirinkite atitinkamą skaičių lauke **Kiekis**.

