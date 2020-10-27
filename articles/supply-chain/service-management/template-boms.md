---
title: Šabloninės KS
description: Komplektavimo specifikacijos (KS) šablone pateikiamas standartizuotas komponentų sąrašas, skirtas aptarnavimo objektams, kurie aptarnaujami reguliariai.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985773"
---
# <a name="template-boms"></a>Šabloninės KS    

[!include [banner](../includes/banner.md)]


Komplektavimo specifikacijos (KS) šablone jums pateikiamas standartizuotas komponentų sąrašas, skirtas aptarnavimo objektams, kurie aptarnaujami reguliariai. Komponentai, išvardyti šabloninėse KS, reiškia individualius aptarnavimo objekto papildomus komponentus. Aptarnavimo objektui pritaikę šabloninę KS, galite įrašyti papildomus aptarnavimo komponentus, pakeistus aptarnavimo objekte.

Norėdami taikyti šablono KS aptarnavimo sutarčiai ar aptarnavimo užsakymui, pridėkite jį prie aptarnavimo objekto ryšio.


> [!NOTE]
> <P>Aptarnavimo objektui galite pritaikyti tik vieną šabloninę KS.</P>

## <a name="create-a-template-bom"></a>Šabloninės KS kūrimas

Toliau pateiktoje lentelėje pateikiama informacija apie įvairius metodus, kuriuos galite naudoti šabloninei KS sukurti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Metodas</p></th>
<th><p>aprašymas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Gamyba</p></td>
<td><p>Šabloninė KS yra paremta gamybos užsakymu. Ši parinktis taikoma tik tada, kai dirbate gamybos aplinkoje. Privalumas ta, kad turite dabartinį išsamų prekę sudarančių komponentų sąrašą.</p></td>
</tr>
<tr class="even">
<td><p>BOM prekė</p></td>
<td><p>Šabloninė KS yra paremta prekės KS. Prekės KS, kitaip nei gamybos KS, yra statinis prekę sudarančių komponentų sąrašas.</p></td>
</tr>
<tr class="odd">
<td><p>Esamas šablonas</p></td>
<td><p>Šablonas paremtas esama šablonine KS.</p></td>
</tr>
<tr class="even">
<td><p>Neautomatinis</p></td>
<td><p>Jei tiksliai žinote, kokios aptarnavimo objekto dalys įprastai keičiamos, galite sukurti neautomatinį šabloninės KS kūrimą. Šis būdas padeda užtikrinti, kad į šabloną įtraukti komponentai atitiks konkrečius jūsų darbo vietos reikalavimus.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Šabloninės KS taikymas aptarnavimo sutarčiai arba aptarnavimo užsakymui

Šabloninę KS galite taikyti aptarnavimo sutarčiai, aptarnavimo užsakymui arba abiems. Aptarnavimo sutartis paprastai aprėpia ilgalaikį ryšį su klientu. Pakeitimų retrospektyvos, įrašytos į aptarnavimo KS, duomenys gali būti naudingi aptarnavimo sutarčiai.

Šabloninę KS taip pat galite taikyti aptarnavimo užsakymui, kad atlikto aptarnavimo retrospektyvą įrašytumėte į aptarnavimo objektą.

## <a name="copy-the-history-of-a-service-bom"></a>Aptarnavimo KS retrospektyvos kopijavimas

Aptarnavimo KS eilutės retrospektyvą galite nukopijuoti iš vienos aptarnavimo sutarties į kitą. Kopijuodami aptarnavimo retrospektyvą iš vienos aptarnavimo sutarties į kitą, galite išsaugoti prekės pakeitimų įrašą.

**Pavyzdys**

Sudarėte kliento automobilio trijų metų aptarnavimo sutartį. Per šį laikotarpį klientas pripranta prie gero įmonės teikiamo aptarnavimo. Todėl pasibaigus sutarties galiojimo laikui, klientas nori nustatyti naują. Dabar galite derėtis dėl palankesnės įmonei sutarties. Pakeistų komponentų įrašas gali būti naudingas ateityje, todėl galite nusikopijuoti aptarnavimo KS retrospektyvą į naują sutartį.

## <a name="modify-the-template-bom"></a>Šabloninės KS modifikavimas

Jei šabloninė KS nepridėta prie aptarnavimo objekto, galite modifikuoti arba panaikinti objekte esančias eilutes. Pridėję šablono KS prie aptarnavimo objekto galite modifikuoti tik vietinę KS versiją. Jei norite dubliuoti vietinės šablono KS versijos nustatymą, galite kurti naują šablono KS pagal vietinę versiją. Daugiau informacijos žr. [Aptarnavimo KS modifikavimas](modify-service-bom.md).

Jei keisite KS esančią prekę, pakeitimą galėsite užregistruoti KS eilutėje arba KS konstruktoriuje. Pasirinktinai galite sukurti pakeitimo objekto aptarnavimo užsakymo eilutę. Jei sukursite aptarnavimo užsakymo eilutę, galėsite išrašyti pakeitimo prekės SF. Jei nesukursite pakeitimo aptarnavimo užsakymo eilutės, pakeitimo registracija bus išsaugota tarp jūsų įrašų aptarnavimo objekto retrospektyvai sekti.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Informacijos pateikimo KS eilutėje keitimas

Galite pakeisti viso šablono ir KS eilutėje rodomos aptarnavimo KS informacijos pateikimo būdą. Pakeitimai bus taikomi visoms šabloninėms KS ir aptarnavimo KS. Tai taikoma ir prie aptarnavimo objektų pridėtoms KS.

## <a name="set-up-number-sequences-for-template-boms"></a>Šabloninių KS numeracijų nustatymas

Norėdami naudoti šablonines KS, turite nustatyti dvi skaičių numeracijas. Vieną numeraciją nustatykite šabloninei KS, o kitą – šabloninės KS retrospektyvos eilutės numeriui.


> [!NOTE]
> <P>Numeracijos naudojamos norint priskirti identifikatorius tiems įrašams, kuriems jų reikia. Prieš priskirdami numeraciją šabloninei KS arba šabloninės KS retrospektyvos eilutės numeriui, turite nustatyti numeracijos kodus.</P>


## <a name="set-up-number-sequences"></a>Nustatyti numeraciją

1.  Sąrašo puslapyje **Numeracijos** sukurkite šabloninių KS ir KS retrospektyvos eilutės numerio numeracijas. 

2.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.

3.  Spustelėkite **Numeracijos**, tada numeracijos nuorodoms, kurias sukūrėte formoje **Numeracijos**, parinkite numeracijos kodą.

4.  Uždarę formą įrašysite savo pakeitimus.


> [!NOTE]
> <P>KS retrospektyvos eilutės numeris bus reikalingas sistemai, kad KS retrospektyvos operacijas būtų galima susieti su aptarnavimo sutartimi ar aptarnavimo užsakymu. Numeris nebus rodomas vartotojo sąsajoje.</P>



## <a name="see-also"></a>Taip pat žiūrėkite

[Šabloninės KS kūrimas](create-template-bom.md)

[Objekto ryšių šabloninių KS valdymas](manage-template-boms-on-object-relations.md)

[Aptarnavimo KS modifikavimas](modify-service-bom.md)

 


