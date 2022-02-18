---
title: Optimizuokite BYOD suplanuotas paketines užduotis
description: Ši tema paaiškina kaip optimizuoti našumą, kai naudojate savo duomenų bazės naudojimo (BYOD) funkciją „Microsoft Dynamics 365 Human Resources” platformoje.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: a2f110d105b8c04f07f219f7f11a57d24e00ce4a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067784"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Optimizuokite BYOD suplanuotas paketines užduotis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ši tema paaiškina kaip optimizuoti našumą, kai naudojate savo duomenų bazės naudojimo (BYOD) funkciją. Norėdami gauti daugiau informacijos apie BYOD, žr. [Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Duomenų eksportavimo našumo apžvalga

Po to, kai objektai publikuoti paskirties duomenų bazėje, galite naudoti „Eksportavimo” funkciją, esančią **Duomenų valdymas** darbo srityje, kad perkeltumėte duomenis. „Eksportavimo” funkcija jums leidžia nustatyti duomenų perkėlimo užduotį, kurią apima vienas ar daugiau objektų. Norėdami gauti daugiau informacijos apie duomenų eksportavimą, žr. [Duomenų importavimo ir eksportavimo užduočių apžvalga](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Galite naudoti puslapį **Eksportavimas**, kad eksportuotumėte duomenis į skirtingus paskirties duomenų formatus, pavyzdžiui, kableliais atskirtų reikšmių (CSV) failą. Šis puslapis taip pat palaiko SQL duomenų bazes kaip kitą paskirties vietą.

Galite sukurti duomenų projektą, į kurį įeina keli objektai, ir naudoti paketinę užduotį, kad suplanuotumėte kada vykdyti šį duomenų projektą. Jeigu pasirinksite **Eksportuoti kaip paketą** parinktį, galite nustatyti grafiką periodiškai vykdyti duomenų eksportavimo užduotį.

Tam, kad padėtumėte išsaugoti BYOD eksportavimo bendrą patikimumą, būkite atsargus, kai į eksportavimo projektą pridedate kelis objektus. Kai nustatote kiek objektų pridėti į tą patį projektą, apsvarstykite šiuos parametrus:

- Objektų sudėtingumas
- Numatomas duomenų kiekis vienam objektui
- Bendras laikas, kurio reikės užbaigti eksportavimą užduoties lygiu

Siekiant optimaliausio našumo, venkite pridėti šimtus objektų vienam projektui. Rekomenduojame, kad sukurtumėte kelias užduotis, iš kurių kiekviena apima mažiau objektų.

## <a name="scheduling-byod-batch-jobs"></a>Paketinių užduočių BYOD planavimas

Kad padėtumėte sumažinti poveikį „Microsoft Dynamics 365 Human Resources” vartotojams, vykdykite BYOD paketines užduotis naktį arba po darbo valandų. Nepamirškite patikrinti laiko juostą pasikartojančioms paketinėms užduotims. Kai kurios paketinės užduotys gali naudoti Ramiojo vandenyno standartinį laiką (PST).

Kad padėtumėte išvengti našumo problemų, atsižvelkite į šiuos koeficientus, kai konfigūruosite BYOD paketinių užduočių vykdymo planavimo dažnumą.

- Laikas, kurio reikės užbaigti kiekvieną paketinę užduotį
- Įmonės poreikis gauti BYOD duomenis

Nustatykite dažnį kiekvienai paketinei užduočiai verte, kuri užtikrina, jog užduotis gali būti užbaigta tinkamai prieš tolesnį suplanuotą vykdymo laiką. Venkite kelių užduočių vykdymo lygiagrečiai, nes toks metodas gali neigiamai paveikti personalo našumą.

Siekiant optimaliausio našumo, visada naudokite **Eksportuoti kaip paketą** pasirinktį, esančią **Eksportavimas** puslapyje, kad suplanuotumėte BYOD paketines užduotis. Venkite pasikartojančių eksportavimų planavimo skiltyje **Tvarkyti \> Tvarkyti pasikartojančias duomenų užduotis**.

## <a name="incremental-export"></a>Papildantysis eksportas

Kai pridedate duomenų eksportavimo objektą, galite atlikti papildantį skirstymą (eksportą) arba visą skirstymą. Visas skirstymas panaikina visus BYOD duomenų bazėje esamus objekto įrašus. Tada jis įterpia dabartinį įrašų rinkinį iš personalo objekto.

Kad atliktumėte papildantį skirstymą, turite **Objektai** puslapyje kiekvienam objektui įjungti keitimų sekimą. Norėdami gauti daugiau informacijos, žr. [Įjunkite objektų keitimų sekimą](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Jei pasirenkate papildantį skirstymą, pirmasis skirstymas visada bus laikomas visu skirstymu. SQL seka pakeitimus šiame pirmajame ir visame skirstyme. Kai įterpiamas naujas įrašas, arba, kai įrašas yra atnaujinamas ar panaikinamas, pakeitimas atsispindi paskirties objekte.

## <a name="time-outs"></a>Skirtieji laikai

Čia rasite BYOD eksportavimų numatytuosius skirtuosius laikus:

- Dešimt minučių sutrumpinimo operacijoms
- Viena valanda įterpti didelį operacijų kiekį

Kai tomai yra dideli, šių skirtojo laiko parametrų gali nepakakti. Kad juos atnaujintumėte, eikite į **Duomenų valdymas \> Sistemos parametrai \> Savo duomenų bazės naudojimas**. Šie skirtieji laikai yra įmonei būdingi ir kiekvienai įmonei turi būti nustatyti atskirai.

## <a name="known-limitations"></a>Žinomi apribojimai

BYOD funkcijai taikomi šie apribojimai:

- Jūsų duomenų bazėje neturi būti aktyviųjų užraktų sinchronizavimo metu. Aktyvieji užraktai gali lėtinti įrašymus ar netgi padaryti klaidą eksportuojant duomenis į jūsų „Azure“ SQL duomenų bazę.
- Negalite eksportuoti sudėtinių objektų į jūsų duomenų bazę. Šiuo metu sudėtiniai objektai nėra palaikomi. Privalote eksportuoti atskirus objektus, kurie sudaro sudėtinį objektą. Tačiau galite eksportuoti abu objektus tame pačiame projekte.
- Objektai, neturintys unikalių raktų, negali būti eksportuojami naudojant papildantį skirstymą. Galite susidurti su šiuo apribojimu, ypač kai bandysite palaipsniui eksportuoti įrašus iš kelių parengtų objektų. Dėl to, kad šie objektai buvo sukurti įgalinti duomenų importavimą, jie neturi unikalaus rakto.

## <a name="troubleshooting"></a>Trikčių šalinimas

### <a name="incremental-push-doesnt-work-correctly"></a>Papildantysis skirstymas neveikia tinkamai

**Problema:** Kai objektui naudojamas visas skirstymas, matote didelį įrašų rinkinį BYOD, kai naudojate **Pasirinkti** aktą. Tačiau kai atliekate papildantį skirstymą, matote tik kelis įrašus BYOD. Atrodo, kad atliekant papildantį skirstymą, visi įrašai buvo panaikinti ir pridėti tik pakeisti įrašai į BYOD.

**Sprendimas:** SQL keitimų sekimo lentelės gali būti nenumatytoje būsenoje. Tokio tipo atvejais rekomenduojame išjungti objekto keitimų sekimą ir tada vėl jį įjungti. Norėdami gauti daugiau informacijos, žr. [Įjunkite objektų keitimų sekimą](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Išdėstymo lentelės nėra aiškios

**Problema:** naudojant projekto išdėstymą, išdėstymo lentelės netinkamai išvalomos. Tada duomenys lentelėse plečiami, dėl to kyla veikimo problemų.

**Sprendimas:** išdėstymo lentelėse tvarkomos septynios dienos iš retrospektyvos. Importavimo eksportavimo išdėstymo valymo paketinė užduotis automatiškai išvalo senesnius nei septynias dienas retrospektyvos duomenis iš **išdėstymo** lentelių. Jei ši užduotis bus įklijuota, lentelės nebus tinkamai išvalytos. Šios paketinės užduoties paleidimas iš naujo tęs procesą, kad išdėstymo lentelės būtų automatiškai išvalytos.

## <a name="see-also"></a>Taip pat žiūrėkite

[Duomenų valdymo apžvalga](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Duomenų importavimo ir eksportavimo užduočių apžvalga](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Objektų keitimų sekimo įjungimas](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
