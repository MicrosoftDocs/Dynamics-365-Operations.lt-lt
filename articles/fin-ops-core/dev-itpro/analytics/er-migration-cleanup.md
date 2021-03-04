---
title: ER perkėlimo valymas
description: Šioje temoje paaiškinama, kaip galima naudoti funkciją ER perkėlimo valymas problemoms, esančioms ER šablonuose, išspręsti.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686373"
---
# <a name="er-migration-cleanup"></a>ER perkėlimo valymas 

[!include[banner](../includes/banner.md)]

Valdydami „Finance“ egzempliorius, galbūt nuspręsite perkelti jūsų dabartinį egzempliorių į kitą vietą. Pavyzdžiui, galite perkelti gamybos egzempliorių į naują smėlio dėžės aplinką. Jei sukonfigūruosite, kad Elektroninių ataskaitų (ER) sistema saugotų šablonus „Microsoft Azure” didelių dvejetainių objektų saugykloje, **DocuValue** lentelėje, esančioje naujojoje smėlio dėžės aplinkoje, bus nuoroda į didelių dvejetainių objektų saugyklos egzempliorių gamybos aplinkoje. Tačiau šio egzemplioriaus negalima pasiekti iš smėlio dėžės aplinkos, nes perkėlimo procesas nepalaiko artefaktų perkėlimo didelių dvejetainių objektų saugykloje. Vietoje to tikimasi, kad naujoje smėlio dėžės aplinkoje nurodysite smėlio dėžės aplinkos didelių dvejetainių objektų saugyklos egzempliorių, kuris dar negauna ER šablonų.

Pasirinkus ER formatą, kuris naudoja šabloną generuoti verslo dokumentams, įvyksta išimtis ir informuojama apie trūkstamą šabloną. Taip pat rekomenduojama naudoti parinktį ER perkėlimo valymas, kad panaikintumėte, o tada iš naujo importuotumėte ER konfigūraciją, kurioje yra šablonas.

[![ER formato vykdymas](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Gausite panašią klaidą, jei pereisite į puslapį **Konfigūracijos** (**Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**) ir konfigūracijų medyje bandysite panaikinti ER formato konfigūraciją, naudojančią šabloną.

[![ER formato naikinimas](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Atlikite toliau pateiktus veiksmus, kad išspręstumėte ER šablonų problemas, kurių negalite pasiekti.

1.  Eikite į puslapį **Organizacijos administravimas** \> **Periodinis** \> **Perkėlimo valymas**.
2.  Pasirinkite ER formato konfigūraciją, kurios negalima įvykdyti arba panaikinti.
3.  Pasirinkite **Naikinti**.
4.  Patvirtinkite pasirinktos ER formato konfigūracijos naikinimą.
5.  [Importuokite](download-electronic-reporting-configuration-lcs.md) panaikintas ER formato konfigūracijas į dabartinį „Finance“ egzempliorių.

## <a name="applicability"></a>Taikymas

> [Svarbu] Parinktis **Perkėlimo valymas** taikoma tik toms ER formato konfigūracijoms, kuriose yra neprieinamų ER šablonų. Kai panaikinate ER formato konfigūraciją naudodami parinktį **Perkėlimo valymas**, ER panaikina šablonus, susijusius su konfigūracijos artefaktais vienintelėje programos duomenų bazėje. Tinkamų fizinių failų didelių dvejetainių objektų saugykloje buvimas netikrinamas. Vietoje to laikoma, kad jų nėra. Todėl nenaudokite parinkties **Perkėlimo valymas** kaip ER konfigūracijos naikinimo parinkties puslapyje **Konfigūracijos** alternatyvos. Naudokite parinktį **Perkėlimo valymas** tik tada, kai ER konfigūracijos naikinimo parinktis puslapyje **Konfigūracijos** žlunga.
>
> Jei naudojate parinktį **Perkėlimo valymas** panaikinti ER formato konfigūraciją, kai nurodytas šablonas pasiekiamas didelių dvejetainių objektų saugykloje, panaikinate tik susijusius konfigūracijos artefaktus programos duomenų bazėje. Fizinis šablono failas išlieka didelių dvejetainių objektų saugykloje. Didelių dvejetainių objektų saugykloje nebeleidžiamas failų perrašymas. Daugiau informacijos rasite [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Be to, nebegalėsite iš naujo importuoti konfigūracijų, panaikintų šioje aplinkoje naudojant parinktį Perkėlimo valymas. Norėdami išspręsti šią problemą, turite rasti atitinkamą failą didelių dvejetainių objektų saugykloje ir jį panaikinti neautomatiniu būdu.

[![ER formato importavimas](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Panaši problema gali kilti, jei perkeliate programos egzempliorių į kitą vietą, kuri buvo naudojama kaip perkėlimo paskirtis daugiau nei vieną kartą ir kurios didelių dvejetainių objektų saugykloje jau yra ER šablono failai.

Kadangi gali būti kelios ER formato konfigūracijos, šis procesas gali užtrukti. Todėl pageidaujama naudoti funkciją [ER šablonų atsarginių kopijų saugykla](er-backup-storage-templates.md) automatiškai atkurti šablonus, kuriuose yra neveikiančių nuorodų.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]