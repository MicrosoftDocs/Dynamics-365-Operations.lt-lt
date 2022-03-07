---
title: Grąžinimų valdymo parametrai
description: Šioje temoje aprašomas grąžinimų valdymo parametrų puslapis. Šiame puslapyje yra parametrų, darančių įtaką registravimui, būsenos naujinimams, numeracijoms ir kitai elgsenai.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0665ce41233308c814a514fccf3b73e20de64098
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576693"
---
# <a name="rebate-management-parameters"></a>Grąžinimų valdymo parametrai

[!include [banner](../includes/banner.md)]

Puslapis **Grąžinimų valdymo parametrai** yra naudojamas nustatyti parametrams, taikomiems **Grąžinimų valdymo** modulyje. Šie parametrai daro įtaką registravimui, būsenos naujinimams, numeracijoms ir kitai elgsenai. Šiame puslapyje atlikti nustatymai yra bendrai naudojami tarp juridinių subjektų ir juos gali modifikuoti vartotojai, turintys atitinkamas saugos teises.

Norėdami atidaryti **Grąžinimų valdymo parametrų** puslapį, eikite **Grąžinimai ir atskaitymai \> Nustatymas \> Grąžinimų valdymo parametrai**. Tada nustatykite laukus, kaip aprašoma tolesniuose poskyriuose.

## <a name="rebate-management-tab"></a>Grąžinimų valdymo skirtukas

Tolesnė lentelė aprašo laukelius, kurie yra prienami **Grąžinimų valdymas** skirtuke, **Grąžinimų valdymo parametrų** puslapyje.

| Laukas | Aprašas |
|---|---|
| Numatytoji būsena | Pasirinkite numatytąją būseną visiems naujiems sandoriams. Norėdami apibrėžti pasirinkti galimų būsenos verčių rinkinį, naudokite [**Grąžinimo būsenų** puslapį](rebate-statuses.md). |
| Apdorojimas pagal dimensiją | Pasirinkite, ar parengimo, grąžinimo ir nurašymo operacijos turi būti apdorojamos pagal finansinę dimensiją. Kai ši parinktis įjungta, sistema naudoja finansines dimensijas iš šaltinio operacijų paskirties operacijose. |
| Patikrinti, ar anksčiau užregistruota | <p>Pasirinkite sistemos veikimo būdą, jeigu neregistruotos grąžinimo operacijos apdorojamos daugiau nei vieną kartą per tą patį laikotarpį:</p><ul><li>**Įspėjimas** – sistema leidžia vartotojams perrašyti pradines operacijų eilutes, tačiau rodomas įspėjimas.</li><li>**Klaida** – sistema neleidžia vartotojams perrašyti pradinių operacijų eilučių ir rodomas klaidos pranešimas. |
| Automatinis žurnalų registravimas | Pasirinkite, ar sistema turėtų automatiškai registruoti siūlomus žurnalus. Šie žurnalai apima dienos žurnalus, kurie naudojami parengimams ir kliento atskaitymams, taip pat, sąskaitos faktūros tiekėjų mokesčių žurnalus. |
| Automatinis laisvos formos sąskaitų faktūrų registravimas | Pasirinkite, ar sistema turėtų automatiškai registruoti laisvos formos sąskaitos faktūras. Ši parinktis taikoma tik laisvos formos sąskaitoms faktūroms, kurių mokėjimo tipas nustatytas į *Sąskaitos faktūros kliento mokesčių atskaitymai*. |
| Grąžinimo prekės užsakymo nuoroda | Pasirinkite grąžinimo nuorodą, kuri bus naudojama pardavimo ir pirkimo užsakymuose, generuojamuose iš grąžinimo proceso (*Nėra*, *Grąžinimo valdymo sandoris*, *Grąžinimo valdymo numeris*, *Grąžinimo operacijos numeris* arba *Dokumento pastabos*). |
| Pareikalavimų apdorojimo naudojimas | <p>Šią parinktį nustatykite į *Taip*, kad naudotumėte pareikalavimų procesą. Tokiu būdu galite pažymėti operacijas, kurias grąžinimų valdymas sukuria kaip pareikalautas arba nepareikalautas ir tada registruoja tik pareikalautas operacijas.</p><p>Pavyzdžiui, apskaičiuojate mėnesio vertės grąžinimų, bet klientui liko dvi dienos pareikalauti grąžinimo. Tokiu atveju nepareikalautos operacijos bus iš naujo sukurtos kitą kartą, kai vykdysite *Apdorojimo* funkciją kitam laikotarpiui.</p><p>Jei nustatote šią pasirinktį į *Ne*, registruojamos visos pareikalautos operacijos.</p> |
| Užsakymo tipo žurnalo įtraukimas | Sandoriams ar sandorių eilutėms, kurių operacijos tipas nustatytas kaip *Užsakymas*, ši parinktis kontroliuoja, ar turi būti įtrauktas *Žurnalo* tipo pardavimo užsakymas. Ji teikia lankstumo, jeigu šie užsakymų tipai naudojami scenarijuose, kuriuose grąžinimas dar neturi būti taikomas. |

## <a name="number-sequences-tab"></a>Numeracijų skirtukas

Naudokite skirtuką **Numeracija**, esantį **Grąžinimo valdymo parametrų** puslapyje, norėdami priskirti numeracijos kodus skirtingoms numeracijoms, kurias naudoja grąžinimo valdymas. Toliau pateikiamoje lentelėje aprašoma kiekvienos iš šių numeracijų paskirtis. Daugiau informacijos apie numeracijas rasite [Numeracijų apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) ir susijusiose temose.

| Nuoroda | Aprašas |
|---|---|
| Grąžinimų valdymo sandoris | Numeracija priskiria unikaliąją rakto reikšmę kiekvienam grąžinimo sandoriui. Šis raktas naudojamas sandorių kūrimo metu. |
| Grąžinimų valdymo numeris | Numeracija priskiria unikaliąją rakto reikšmę kiekvienam grąžinimui. Šis raktas yra naudojamas grąžinimo santykiams identifikuoti. |
| Grąžinimo operacijos numeris | Numeracija priskiria unikaliąją rakto reikšmę kiekvienai grąžinimo operacijai. Šis raktas yra naudojamas grąžinimo operacijoms identifikuoti. |
| Mokesčio sąskaita faktūra | Numeracija priskiria unikaliąją rakto reikšmę kiekvienai grąžinimo sąskaitai faktūrai. Šis raktas yra naudojamas, kai automatiškai registruojami grąžinimo žurnalai. |

## <a name="feature-visibility-tab"></a>Funkcijų matomumo skirtukas

Grąžinimo valdymas keliuose dažnai naudojamuose „Microsoft Dynamics 365 Supply Chain Management“ puslapiuose prideda savybių (laukų ir funkcijų). Šie puslapiai apima puslapius, susijusius su pardavimo užsakymais ir pardavimo pasiūlymais. Jei naudojate grąžinimų valdymą, šios funkcijos turi būti matomos visur, kad galėtumėte jomis pasinaudoti. Jei nenaudojate grąžinimų valdymo, galite paslėpti funkcijas, kad jos netrukdytų.

Skirtuke **Funkcijų matomumas**, esančiame puslapyje **Grąžinimų valdymo parametrai**, parinktį **Įjungti** nustatykite į *Taip*, kad grąžinimų valdymo funkcijos būtų matomos tada, kai tik jas bus galima naudoti. Nustatykite tai į *Ne*, kad paslėptumėte funkcijas bendrai naudojamuose puslapiuose už **Grąžinimo valdymo** modulio ribų. Tačiau net parinktį nustačius į *Ne*, pats modulis, įskaitant **Grąžinimų valdymo parametrų** puslapį lieka prieinamas vartotojams, turintiems atitinkamus jo prieigos leidimus.
