---
title: Naujos ER konfigūracijos, skirtos ataskaitų generavimui „Word“ formatu, kūrimas
description: Šioje temoje paaiškinama, kaip vartotojai gali konfigūruoti naują elektroninių ataskaitų (ER) formatą generuoti ataskaitas kaip „Microsoft Word” dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094159"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Naujos ER konfigūracijos, skirtos ataskaitų generavimui „Word“ formatu, kūrimas

[!include [banner](../includes/banner.md)]

Norėdami generuoti ataskaitas kaip „Microsoft Word” dokumentus, turite sukurti ataskaitų šabloną naudodami, pavyzdžiui, „Word” darbalaukio programą. Tolesnė iliustracija rodo valdiklio ataskaitos, kurią galima sugeneruoti rodyti išsamią apdorotų tiekėjo mokėjimų informaciją, pavyzdinį šabloną.

![Valdiklio ataskaitos pavyzdinis šablonas „Word” darbalaukio programoje](./media/er-design-configuration-word-image1.png)

Norėdami naudoti „Word” dokumentą kaip ataskaitų „Word” formatu šabloną, galite sukonfigūruoti naują [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md). Šis sprendimas turi apimti ER [konfigūraciją,](general-electronic-reporting.md#Configuration) kurioje yra ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentas.

> [!NOTE]
> Kai kuriate naują ER formato konfigūraciją generuoti ataskaitoms „Word” formatu, turite pasirinkti **„Word”** kaip formato tipą išplečiamajame dialogo lange **Kurti konfigūraciją** arba palikti lauką **Formato tipas** tuščią.

![Formato konfigūracijos kūrimas puslapyje Konfigūracijos](./media/er-design-configuration-word-image2.gif)

Sprendimo ER formato komponente turi būti **„Excel”\\Failas** formato elementas ir jis turi būti susietas su „Word” dokumentu, kuris bus naudojamas kaip vykdymo aplinkoje sugeneruotų ataskaitų šablonas. Norėdami konfigūruoti ER formato komponentą, turite atidaryti sukurtos ER konfigūracijos [juodraščio](general-electronic-reporting.md#component-versioning) versiją ER formato dizaino įrankyje. Tada įtraukite **„Excel”\\Failas** elementą, pridėkite savo „Word” šabloną į redaguojamą ER formatą ir susiekite tą šabloną su **„Excel”\\Failas** elementu, kurį pridėjote.

> [!NOTE]
> Kai pridedate šabloną, turite naudoti [dokumento tipą](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), kuris buvo anksčiau [sukonfigūruotas](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametruose saugoti ER formatų šablonams.

![Šablono pridėjimas Formato kūrimo įrankio puslapyje](./media/er-design-configuration-word-image3.gif)

Galite pridėti **„Excel”\\Diapazonas** ir **„Excel”\\Langelis** įdėtuosius elementus **„Excel”\\Failas** elementui tam, kad nurodytumėte struktūrą duomenų, kurie bus įvesti generuojamuose ataskaitose vykdymo metu. Tada turite susieti tuos elementus su redaguojamo ER formato duomenų šaltiniais tam, kad galėtumėte nurodyti faktinius duomenis, kurie bus įvesti generuojamuose ataskaitose vykdymo metu.

![Įdėtųjų elementų pridėjimas Formato dizaino įrankio puslapyje](./media/er-design-configuration-word-image4.gif)

Įrašant ER formato pakeitimus kūrimo metu, hierarchinė formato struktūra yra saugoma pridėtame „Word” šablone kaip [pasirinktinė XML dalis](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) pavadinimu **Ataskaita**. Turite pasiekti modifikuotą šabloną, atsisiųsti jį iš „Finance”, išsaugoti vietinėje sistemoje ir jį atidaryti „Word” darbalaukio programoje. Šioje iliustracijoje vaizduojamas vietinėje sistemoje saugomas valdiklio su pasirinktine XML dalimi **Ataskaita** pavyzdžio šablonas.

![Pavyzdinio ataskaitos šablono peržiūra „Word” darbalaukio programoje](./media/er-design-configuration-word-image5.gif)

Kai vykdomi **„Excel”\\Diapazonas** ir **„Excel”\\Langelis** formato elementų susiejimai vykdymo aplinkoje, kiekvieno susiejimo atnešti duomenys atsiranda sugeneruotame „Word” kaip atskiras pasirinktinės XML dalies **Ataskaita** laukas. Norėdami įvesti vertes iš pasirinktinės XML dalies laukų sugeneruotame dokumente, turite pridėti atitinkamus „Word” [turinio valdiklius](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) į jūsų „Word” šabloną, kad jie būtų naudojami kaip vietos rezervavimo ženklai duomenims, kurie bus pildomi vykdymo metu. Norėdami nurodyti, kaip užpildyti turinio valdikliai, susiekite kiekvieną turinio valdiklį su atitinkamu pasirinktinės XML dalies **Ataskaita** lauku.

![Turinio valdiklių įtraukimas ir susiejimas „Word” darbalaukio programoje](./media/er-design-configuration-word-image6.gif)

Tada turite pakeisti pradinį redaguojamo ER formato „Word” šabloną modifikuotu šablonu, kuriame dabar yra „Word” turinio valdikliai, kurie buvo susieti su pasirinktinės XML dalies **Ataskaita** laukais.

![Šablono pakeitimas Formato kūrimo įrankio puslapyje](./media/er-design-configuration-word-image7.gif)

Kai vykdote sukonfigūruotą ER formatą, pridėtas „Word” šablonas naudojamas naujai ataskaitai generuoti. Faktiniai duomenys saugomi „Word” ataskaitoje kaip pasirinktinė XML dalis, pavadinta **Ataskaita**. Kai atidaroma sugeneruota ataskaita, „Word” turinio valdikliai užpildomi duomenimis iš **Ataskaita** pasirinktinės XML dalies.

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

**Klausimas:** Sukonfigūravau ER formatą spausdinti „Word” dokumentui, kuriame yra įmonės adresas. Į šio ER formato „Word” šabloną įterpiau raiškiojo teksto turinio valdiklį įmonės adreso rodymui. „Finance” aš įvedžiau įmonės adresą kaip kelių eilučių tekstą ir pasirinkau **Įvesti** pridėti grįžimą į eilutės pradžią kiekvienai įvestai eilutei. Todėl tikiuosi, kad sugeneruotuose dokumentuose įmonės adresas bus rodomas kaip kelių eilučių tekstas. Tačiau adresas rodomas kaip viena teksto eilutė su specialiais simboliais, o ne sugrįžimais į eilutės pradžią. Kas negerai su mano parametrais?

**Atsakymas:** Užuot naudoję raiškiojo teksto turinio valdiklį, turite naudoti paprastojo teksto turinio valdiklį ir pasirinkti **Leisti sugrįžimus į eilutės pradžią (keli paragrafai)** žymės langelį, esantį valdiklio ypatybėse.

## <a name="additional-resources"></a>Papildomi ištekliai

- [ER konfigūracijų su „Excel” šablonais, skirtų ataskaitų „Word” formatu generavimui, pakartotinis naudojimas](./tasks/er-design-configuration-word-2016-11.md)
- [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]