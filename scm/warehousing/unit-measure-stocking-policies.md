---
title: "Matavimo vienetų ir sandėliavimo strategijos"
description: "Šiame straipsnyje aprašoma, kaip, vykdant sandėlio procesus, naudojami numatytieji vienetai, vienetų sekos ir vienetų konvertavimas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: c9de16c49ff20788d12ad3701331ca6416b06625
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# Matavimo vienetų ir sandėliavimo strategijos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašoma, kaip, vykdant sandėlio procesus, naudojami numatytieji vienetai, vienetų sekos ir vienetų konvertavimas.

Vienetų sekų grupės – tai vienetų, kuriuos galima naudoti sandėlio operacijose, seka. Jos sukuriamos puslapyje **Vienetų sekų grupės**. Seka nurodo įvairių vienetų ryšį. Pavyzdžiui, saugote padėklus, kuriuose yra dėžės su atskiromis prekėmis. Tokiu atveju turite pateikti tris skirtingus vienetus ir loginę sluoksnių tvarką. Vienetų sekų grupės leidžia apibrėžti numerių lentelių grupavimo strategijas ir numatytuosius vienetus, kuriuos reikia naudoti įvairiems sandėlio procesams. Šis straipsnis taikomas ir išplėstiniam sandėliavimo sprendimui, prieinamam dalyje Sandėlio valdymas, ir paprastesniam sandėliavimo sprendimui, prieinamam dalyje Atsargų valdymas.

## Patvirtintų produktų vienetų sekų grupės
Jei norite naudoti patvirtintus produktus sandėlio darbo procesuose, jiems turi būti priskirta vienetų sekų grupė. Jei turite patvirtinti produktą, susietą su saugojimo dimensijų grupe, o Saugojimo dimensijų grupės parinktis **Naudoti sandėlio valdymo procesus** nustatyta kaip **Taip**, bus pateiktas klaidos pranešimas, jei produktui nenurodytas vienetų sekų grupės ID. Jei jūsų naudojamoje vienetų sekų grupėje yra kelios eilutės (taigi keli vienetai), turite nustatyti vienetų konvertavimo funkciją. Šis konfigūravimo procesas atliekamas puslapyje **Vienetų konvertavimas**. Mažiausias vienetas sekų grupėje, susietoje su išleistu produktų, turi atitikti atsargų vienetą, apibrėžtą atitinkamam produktui. Atsargų vienetas yra vienetas, naudojamas turimų atsargų skaičiavimams pagrįsti. Taip pat galite nustatyti bendrojo produkto variantų matavimo vienetų konvertavimo funkciją naudodami į parinktį **Įjungti matavimo vienetų konvertavimą**.

## Numerio lentelių grupavimas
Galite nurodyti, ar gavimus, mažesnius arba didesnius nei konkretus vienetas, reikia grupuoti į vieną numerio lentelę, ar skaidyti į numerio lenteles kiekvienam vienetui. Norėdami nustatyti tokią veikseną, naudokite puslapio **Vienetų sekų grupės** skirtuke **Eilutės informacija** esančią parinktį **Numerio lentelių grupavimas**. Jei darbą apdorodami mobiliuoju įrenginiu norėsite naudoti numerio lentelių grupavimo parinktį, meniu elemente **Mobilusis įrenginys** turėsite pasirinkti parinktį **Numerio lentelių grupavimas**. Pavyzdžiui, naudojate mobilųjį įrenginį prekei, susietai su vienetų sekų grupe, kuri turi dvi eilutes, registruoti. Pirmoji eilutė yra Dalys ir parinktis **Numerio lentelių grupavimas** nustatyta kaip **Taip**. Antroji eilutė yra Paletės vienetas ir parinktis **Numerio lentelių grupavimas** nustatyta kaip **Ne**. Tokiu atveju sistema gali automatiškai padėti skaidyti ir sukurti numerių lenteles po 100 vienetų.

## Vienetas ciklui skaičiuoti
Norėdami nurodyti, kokie vienetai turi būti naudojami kaip ciklo skaičiavimo procesų dalis, puslapyje **Vienetų sekų grupės** pasirinkite parinktį **Naudoti vienetą skaičiuojant ciklus**. Galite pasirinkti ne daugiau kaip keturis vienetus sekų grupėje. Jei pasirinksite daugiau nei keturis vienetus, papildomi vienetai nebus rodomi mobiliajame įrenginyje.

## Mobiliojo įrenginio gavimo procesų numatytieji vienetai
Norėdami nustatyti numatytuosius vienetus, kurie turi būti naudojami gavimo procesams mobiliuosiuose įrenginiuose, puslapyje **Vienetų sekų grupės** įjunkite parinktis **Numatytasis pirkimo ir perdavimo vienetas** ir **Numatytasis gamybos vienetas**. Pavyzdžiui, galite nurodyti, kad pagal numatytuosius nustatymus sistema turi naudoti padėklų kiekį, kai gaunamos pirkimo užsakymo turimos atsargos naudojant mobilųjį įrenginį, bet saugojimo vienetas turėtų būti Dalys. Norėdami gauti dalių, esančių kiekviename padėkle skaičiaus konvertavimą, turite apibrėžti vieneto konvertavimą, pvz.,100 vnt. = 1 PL.

## Numatytieji užsakymo parametrai
Kaip patvirtintų produktų kūrimo dalį, turite pasirinkti numatytuosius pirkimo, pardavimo ir atsargų vienetus, kad būtų galima apdoroti įvairius užsakymus. Galite nustatyti numatytuosius įvairių šaltinio dokumentų vienetus ir kiekius puslapiuose **Numatytieji užsakymo parametrai** ir **Nuo teritorijos priklausomi užsakymo parametrai**. Šiuos puslapius galite pasiekti iš puslapio **Patvirtinti produktai**.




