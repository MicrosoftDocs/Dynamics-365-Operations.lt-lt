---
title: Įmonės koncepcija „Dataverse“
description: Šiame straipsnyje aprašomas įmonės duomenų integravimas tarp finansų ir operacijų bei Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2bdd99b581be453616e71d0f0f95a7daf75a253a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289781"
---
# <a name="company-concept-in-dataverse"></a>Įmonės koncepcija „Dataverse“

[!include [banner](../../includes/banner.md)]




Finansų ir operacijų atveju įmonės koncepcija yra ir *teisinis* konstruktas, ir verslo konstruktas. Ji taip pat apibrėžia duomenų saugos ir matomumo ribas. Vartotojai visada dirba vienos įmonės kontekste, o dauguma duomenų yra įmonės suskirstyti.

„Dataverse“ nenaudojama lygiavertė koncepcija. Artimiausia koncepcija yra *verslo struktūros vienetas*, kuris pirmiausia apima vartotojo duomenų saugos ir matomumo ribas. Ši koncepcija neturi tokios pačios teisinės ar verslo reikšmės kaip įmonės koncepcija.

Verslo struktūros vienetas ir įmonė nėra lygiavertės koncepcijos, todėl „Dataverse“ integracijos tikslais negalima taikyti jų vienas su vienu (1:1) susiejimo. Tačiau vartotojai turi, kaip numatyta, galėti peržiūrėti tas pačias eilutes programoje ir „Dataverse“, todėl „Microsoft“ pristatė naują lentelę „Dataverse”, pavadintą cdm\_Company. Ši lentelė yra lygiavertė įmonės lentelei programoje. Siekiant užtikrinti eilučių matomumo lygiavertiškumą pradėjus naudoti programą ir „Dataverse“, rekomenduojame toliau pateiktus „Dataverse“ duomenų nustatymus.

+ Kiekvienai finansų ir operacijų įmonės eilutei, kuri įgalinta dvigubo rašymo atveju, sukuriama susijusi cdm\_ įmonės eilutė.

+ Sukūrus cdm\_Company eilutę ir įgalinus dvigubam rašymui, sukuriamas numatytasis verslo struktūros vienetas tuo pačiu pavadinimu. Nors tam verslo vienetui automatiškai sukuriama numatytoji savininko komanda, verslo vienetas nėra naudojamas.
+ Sukuriama atskira savininko komanda, kurios pavadinimas toks pat, naudojant dvigubo rašymo sufiksą. Ji taip pat susiejama su verslo struktūros vienetu.

+ Pagal numatytuosius nustatymus, bet kurios eilutės, kuri sukuriama ir įrašoma dvigubu rašymu „Dataverse“, savininkas nustatomas į „DW Owner“ komandą, kuri susiejama su susijusiu verslo struktūros vienetu.

Tolesnėje iliustracijoje pateikiamas šio duomenų nustatymo „Dataverse“ pavyzdys.

![Duomenų nustatymas „Dataverse“.](media/dual-write-company-1.png)

Dėl tokios konfigūracijos bet kokia eilutė, susieta su USMF įmone, priklauso komandai, kuri yra susieta su USMF verslo struktūros vienetu „Dataverse“. Todėl tas eilutes gali matyti bet kuris vartotojas, kuris turi prieigą prie to verslo struktūros vieneto pasitelkiant saugos vaidmenį, kuris nustatytas verslo struktūros vieneto lygio matomumui. Toliau pateikiamas pavyzdys, kaip komandos gali būti naudojamos norint suteikti tinkamą prieigą prie tų eilučių.

+ Vaidmuo „Pardavimo vadybininkas“ priskiriamas „USMF pardavimas“ komandos nariams.
+ Vartotojai, turintys vaidmenį „Pardavimo vadybininkas“, turi prieigą prie visų paskyros eilučių, kurios yra to paties verslo struktūros vieneto nariai.
+ „USMF pardavimas“ komanda susiejama su anksčiau minėtu USMF verslo struktūros vienetu.
+ Todėl USMF pardavimo komandos nariai gali matyti bet kokią sąskaitą, kurią valdo "USMF DW" vartotojas, kuris būtų ateitas iš USMF įmonės lentelės, finansinėse ir operacijose.

![Komandų naudojimas.](media/dual-write-company-2.png)

Kaip parodyta ankstesnėje iliustracijoje, šis 1:1 susiejimas tarp verslo struktūros vieneto, įmonės ir komandos yra tik pradžios taškas. Tolesniame pavyzdyje naujas verslo struktūros vienetas „Europa“ rankiniu būdu sukuriamas „Dataverse“ kaip DEMF ir ESMF pirminis elementas. Šis naujas šakninis verslo struktūros vienetas nėra susijęs su dvigubu rašymu. Tačiau jis gali būti naudojamas siekiant suteikti „EUR pardavimas“ komandos nariams prieigą prie paskyros duomenų tiek DEMF, tiek ESMF nustatant duomenų matomumą į **Pirminis/antrinis BU** susietam saugos vaidmeniui.

Galutinis aptariamas straipsnis yra tai, kaip dvigubo rašymo metu nurodoma, kuriai savininko komandai jis turėtų priskirti eilutes. Šią veikseną kontroliuoja stulpelis **Numatytoji komanda savininkė** eilutėje cdm\_Company. Kai cdm\_Company eilutė yra įgalinta dvigubam rašymui, priedas automatiškai sukuria susietą verslo struktūros vienetą ir savininko komandą (jei jos dar nėra) ir nustato **Numatytoji komanda savininkė** stulpelį. Administratorius gali pakeisti šį stulpelį kita reikšme. Tačiau administratorius negali išvalyti stulpelio tol, kol lentelei įgalintas dvigubas rašymas.

> [!div class="mx-imgBorder"]
![Stulpelis Numatytoji komanda savininkė.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Įmonės paskirstymas ir įkėlimas

„Dataverse“ integracija suteikia įmonės lygiavertiškumą naudojant įmonės identifikatorių, skirtą paskirstyti duomenis. Kaip parodyta toliau pateiktoje iliustracijoje, visos konkrečios įmonės lentelės išplečiamos taip, kad su cdm\_Company lentele turėtų ryšį „daugelis su vienu“ (N:1).

> [!div class="mx-imgBorder"]
![N:1 ryšys tarp konkrečios įmonės ir cdm_Company lentelių.](media/dual-write-bootstrapping.png)

+ Įtraukus ir įrašius įmonę eilučių reikšmė tampa skirta tik skaityti. Todėl vartotojai turėtų įsitikinti, kad pasirinko tinkamą įmonę.
+ Tik tos eilutės, kurios apima įmonės duomenis, gali būti dvigubo rašymo tarp programos ir „Dataverse“.
+ Esamiems „Dataverse“ duomenims netrukus bus teikiama administratoriaus vadovaujama įkėlimo patirtis.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Automatinis įmonės pavadinimo įvedimas „Customer engagement” programoms

Yra keli būdai automatiškai įvesti įmonės pavadinimą „Customer Engagement” programose.

+ Jei esate sistemos administratorius, galite nustatyti numatytąją įmonę eidami į **Išplėstiniai nustatymai > Sistema > Sauga > Vartotojai**. Atidarykite formą **Vartotojas** ir skyriuje **Organizacijos informacija** nustatykite **Įmonė kaip numatytoji formose** reikšmę.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Numatytosios įmonės nustatymas skyriuje Organizacijos informacija.":::

+ Jei turite **Rašymo** prieigą prie **„SystemUser”** lentelės **Verslo vieneto** lygiu, tada galite pakeisti numatytąją įmonę bet kurioje formoje pasirinkdami įmonę iš išplečiamojo meniu **Įmonė**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Įmonės vardo keitimas naujoje paskyroje.":::

+ Jei turite **Rašymo** prieigą prie daugiau nei vienos įmonės duomenų, tada galite keisti numatytąją įmonę pasirinkdami eilutę, priklausančią kitai įmonei.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Eilutės pasirinkimas pakeičia numatytąją įmonę.":::

+ Jeigu esate sistemos konfigūratorius arba administratorius ir norite įvesti įmonės pavadinimą automatiškai pasirinktinėje formoje, galite naudoti [formų įvykius](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Pridėkite JavaScript nuorodą į **msdyn_/DefaultCompany.js** ir naudokite šiuos įvykius. Galite naudoti bet kurią visiškai parengtą formą, pavyzdžiui **Paskyra** formą.

    + **„OnLoad”** įvykis formai: nustatykite **„defaultCompany”** stulpelį.
    + **„OnChange”** įvykis **Įmonės** stulpeliui: nustatykite **„updateDefaultCompany”** stulpelį.

## <a name="apply-filtering-based-on-the-company-context"></a>Filtravimo, paremto įmonės kontekstu, taikymas

Norėdami taikyti filtravimą, paremtą įmonės kontekstu Jūsų pasirinktinėse formose arba pasirinktiniuose peržvalgos stulpeliuose, pridėtuose standartinėse formose, atidarykite formą ir naudokite skyrių **Susijusių įrašų filtravimas** įmonės filtro taikymui. Turite tai nustatyti kiekvienam peržvalgos stulpeliui, kuriam reikalingas filtravimas, paremtas esančia įmone pasirinktoje eilutėje. Parametras rodomas dalyje **Paskyra** šioje iliustracijoje.

:::image type="content" source="media/apply-company-context.png" alt-text="Įmonės konteksto taikymas.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
