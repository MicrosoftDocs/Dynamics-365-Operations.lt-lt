---
title: Elektroninio kasos aparato (EKA) komisinių sekimas naudojant pardavimo grupes
description: Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b020618036951e7033baadbf58b806df7877bdb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976594"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Elektroninio kasos aparato (EKA) komisinių sekimas naudojant pardavimo grupes

[!include [banner](includes/banner.md)]

Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą.

Sekant pardavimo atstovo pardavimus matuojamos atstovo pardavimo galimybės, o iš kasininko pardavimų galima spręsti apie greitį ir našumą. Pardavimo atstovo sekami pardavimai taip pat dažnai naudojami norint apskaičiuoti komisinius arba kitas paskatas.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Darbuotojo konfigūravimas būti EKA pardavimo atstovu

Kai darbuotojas įtraukiamas į pardavimo grupę, jam gali būti paskiriami komisiniai ir sistemoje jis gali būti identifikuojamas kaip pardavimo atstovas. Darbuotojui, kuris nėra pardavimo grupėje, komisiniai negali būti skiriami ir jis nebus įtraukiamas į elektroninio kasos aparato (EKA) programos sąrašus kaip pardavimo atstovas. EKA pardavimo atstovų sąrašai sudaromi iš visų pardavimo grupių, kuriose yra bent vienas parduotuvei priskirtas darbuotojas. Sąrašas rodomas EKA kaip pardavimo grupės ID ir pavadinimo (ID : Pavadinimas) derinys. Numatytąją pardavimo grupę darbuotojams galima priskirti norint, kad būtų palaikomi scenarijai, kai mažmenininkas nusprendžia pardavimo atstovą nustatyti automatiškai EKA eilutėse. Vartotojai gali pasirinkti bet kurią pardavimo grupę, kurioje darbuotojas yra narys.

## <a name="functionality-profile-settings"></a>Funkcijų šablono parametrai

Yra keletas parduotuvės funkcijų šablono parametrų, kuriuos naudojant nustatomas EKA srautas ir procesas ir kurie skirti pardavimo atstovams.

<table>
<thead>
<tr>
<th>Šablonas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pagal numatytuosius nustatymus nustatyti kasininką, kai įmanoma</td>
<td>Jei ši parinktis įjungta, EKA automatiškai sukuria operacijų eilutes, kuriose nurodoma dabartinio kasininko numatytoji pardavimo grupė. Jei numatytoji kasininko pardavimo grupė nenurodyta, vertė nenustatoma. Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką.</td>
</tr>
<tr>
<td>Raginimas nurodyti pardavimo atstovą</td>
<td>Galimos trys šios parinkties vertės:
<ul>
<li><strong>Ne</strong> – pasirinkus šią parinktį vartotojas nebus raginamas pasirinkti pardavimo grupės. Vertę vis tiek galima nustatyti naudojant numatytąją kasininko pardavimo grupę („Sales“) arba mechaniškai naudojant EKA mygtukyno mygtuką.</li>
<li><strong>Operacijos pradžia</strong> – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis <strong>Pagal numatytuosius nustatymus nustatyti kasininką</strong>, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, kiekvienos operacijos pradžioje vartotojas bus paragintas pasirinkti pardavimo grupę. Pasirinkus pardavimo grupę pagal šį raginimą visos kitos pasirinktos pardavimo grupės eilutės bus numatytosios. Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką.</li>
<li><strong>Kiekvienai eilutei</strong> – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis <strong>Pagal numatytuosius nustatymus nustatyti kasininką</strong>, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, įtraukęs kiekvieną eilutę vartotojas bus paragintas pasirinkti pardavimo grupę. Vartotojas vis tiek gali pats nustatyti pardavimo grupę („Sales“) naudodamas EKA mygtukyno mygtuką.</li>
</ul>
</td>
</tr>
<tr>
<td>Reikia</td>
<td>Ši parinktis taikoma tik tada, kai sukonfigūruota, jog EKA ragintų nurodyti pardavimo atstovą. Jei parinktis įjungta, norėdamas tęsti vartotojas turės pasirinkti pardavimo grupę. Priešingu atveju vartotojas paraginamas, bet gali atšaukti ir tęsti nepasirinkęs. Įtraukus eilutę reikiamą kiekį leidimų turintis vartotojas vis tiek gali pašalinti pardavimo grupę iš eilutės. Šiuo atveju parinktis „Prašyti pardavimo atstovo“ nėra priverstinė.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Informacijos apie pardavimo atstovą rodymas EKA operacijų ekrane

EKA operacijos ekraną ir turinį galima konfigūruoti naudojant ekrano išdėstymo kūrimo priemonę ir priskirti ekrano išdėstymus parduotuvėms, registrams arba darbuotojams. Laukelis **Prekybos atstovas** gali būti įtrauktas į eilučių skirtuką kvito juostoje.  Jis rodys konkrečios prekybos grupės ID kiekvienai eilutei transakcijos ekrane.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Pardavimo atstovo operacijų įtraukimas į EKA mygtukynus

Naudodamiesi EKA vartotojai gali konfigūruoti į ekrano išdėstymus įtraukiamus mygtukynus, kad juose būtų pateikiama prieiga prie EKA operacijų. Toliau nurodytas EKA operacijas galima priskirti pardavimo atstovams skirtiems mygtukyno mygtukams.

| Operacija                                 | aprašymas |
|-------------------------------------------|-------------|
| Nustatyti pardavimo atstovą eilutėje          | EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas. Prekybos grupės pasirinkimas iš sąrašo nustatys vertę esamoje transakcijos eilutėje. |
| Išvalyti pardavimo atstovą eilutėje        | Atliekant šią EKA operaciją iš dabartinės operacijos eilutės pašalinama dabartinė pardavimo grupės („Sales“) vertė. |
| Nustatyti operacijos pardavimo atstovą   | EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas. Prekybos grupės pasirinkimas iš sąrašo nustatys numatytą vertę esamoje transakcijos eilutėje. Nustatomos visos esamos eilutės, kurioms nepriskirta pardavimo grupė, taip pat visos vėliau įtrauktos eilutės. |
| Išvalyti operacijos pardavimo atstovą | Atliekant šią EKA operaciją iš dabartinės operacijos pašalinama dabartinė numatytoji pardavimo grupės („Sales“) vertė. Tai neturi įtakos kitoms jau esamoms operacijos eilutėms. |

## <a name="calculating-commissions"></a>Komisinių skaičiavimas

Nurodytų pardavimo grupių darbuotojų komisiniai skaičiuojami registruojant išrašą arba pardavimo užsakymą. Komisinio mokesčio sąskaita yra nustatoma pagal darbuotojo komisinę dalį, kaip nustatyta prekybos grupėje ir susieto komisinio mokesčio skaičiavimo nustatymuose klientui ir (arba) produktams transakcijoje.
