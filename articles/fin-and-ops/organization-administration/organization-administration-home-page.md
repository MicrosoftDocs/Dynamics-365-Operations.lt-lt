---
title: Organizacijos administravimo pagrindinis puslapis
description: "Šioje temoje nurodyti ištekliai, kurie padės organizacijoje naudoti „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: eb8674a6401b11e8e33d3cba54add1fb4bca1cd3
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="organization-administration-home-page"></a>Organizacijos administravimo pagrindinis puslapis

[!include[banner](../includes/banner.md)]


Šioje temoje nurodytas turinys, patyrusiems vartotojams ir administratoriams padėsiantis konfigūruoti „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“. Šis turinys jiems padės sistemą sukonfigūruoti taip, kad ji jūsų organizacijoje ir įmonėje veiktų sklandžiai bei efektyviai.

Didelė čia pateikto turinio dalis taikoma modulio **Organizacijos administravimas** funkcijoms. Tačiau yra keletas užduočių, pavyzdžiui, įrašo šablono kūrimo ir naudojimo, kurias galima atlikti bet kokiame modulyje, kad organizacija galėtų veikti efektyviau. 

<a name="number-sequences"></a>Numeravimai
----------------
Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti. Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas *nuoroda*. Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.

-   [Numeracijos apžvalga](number-sequence-overview.md)
-   [Nustatyti numeracijas naudojant vedlį](tasks/set-up-number-sequences-wizard.md) (Užduočių vedlys)
-   [Atskirų numeracijų nustatymas](tasks/set-up-number-sequences-individual-basis.md) (Užduočių vedlys)

## <a name="organizations"></a>Organizacijos
Organizacija yra grupė žmonių, kurie dirba kartu vykdydami verslo procesą arba siekdami tikslo. Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą.

Prieš sprendime „Finance and Operations“ nustatydami organizacijas ir hierarchijas, būtinai suplanuokite, kaip bus modeliuojamas jūsų verslas. Organizacijos modelis turi didelės įtakos „Finance and Operations“ diegimui ir verslo procesams.

-   [Organizacijos ir organizacijų hierarchijos](organizations-organizational-hierarchies.md)
-   [Organizacijos hierarchijos planavimas](plan-organizational-hierarchy.md)
-   [Organizacijos hierarchijos kūrimas](tasks/create-organization-hierarchy.md) (Užduočių vedlys)
-   [Juridinio subjekto kūrimas](tasks/create-legal-entity.md) (Užduočių vedlys)
-   [Valdymo vieneto kūrimas](tasks/create-operating-unit.md) (Užduočių vedlys)

## <a name="address-books"></a>Adresų knygelės
Visuotinė adresų knygelė yra centralizuota saugykla, kurioje turi būti saugomi visų vidinių ir išorinių asmenų bei organizacijų, su kuriais įmonė bendrauja, bendrieji duomenys. Duomenys, susieti su šalies įrašais, apima šalies pavadinimą, adresą ir kontaktinę informaciją. 

Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai. 

-   [Visuotinė adresų knygelė](overview-global-address-book.md)
-   [Planavimas, kaip konfigūruoti visuotinę adresų knygelę ir papildomas adresų knygeles](plan-configuration-global-address-book-additional-address-books.md)
- [Visuotinės adresų knygelės konfigūravimas](tasks/configure-global-address-book.md)
-   [DUK apie adresų knygeles](qa-address-books.md)


## <a name="workflow"></a>Darbo eiga
Darbo eiga yra su „Finance and Operations“ įdiegta sistema, kurią naudodami galite kurti atskiras darbo eigas ar verslo procesus. Kurdami darbo eigą nurodote, kaip dokumentas juda sistemoje, parodydami, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą. 

-   [Darbo eigos apžvalga](overview-workflow-system.md)
-   [Darbo eigos elementai](workflow-elements.md)
-   [Darbo eigos veiksmai](workflow-actions.md)
-   [Darbo eigos kūrimas](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniniai parašai
Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę. Kai kuriose pramonės šakose elektroninis parašas turi tokią pat teisinę galią kaip parašas ranka. Elektroniniai parašai yra reglamentus atitinkantis reikalavimas kai kurioms reguliuojamoms pramonės šakoms, pvz., vaistų, maisto ir gėrimų, aviacijos ir gynybos.

Programoje „Finance and Operations“ galite naudoti elektroninius parašus svarbiems verslo procesams. Kai kuriuose procesuose yra įdiegtos elektroninio parašo galimybės. Taip pat galite sukurti pasirinktinius parašo reikalavimus bet kuriai duomenų bazės lentelei ir laukui.

-   [Elektroninio parašo apžvalga](electronic-signature-overview.md)
-   [Elektroninių parašų nustatymas](tasks/set-up-electronic-signatures.md) (Užduočių vedlys)

## <a name="case-management"></a>Atvejų valdymas
Planuojant, sekant ir analizuojant atvejus galima sukurti efektyvius sprendimus, skirtus panašioms problemoms spręsti. Pavyzdžiui, kai klientų aptarnavimo atstovai arba personalo srities darbuotojai kuria atvejus, informacijos, padėsiančios efektyviau dirbti su atveju ar jį spręsti, jie gali rasti informaciniuose straipsniuose. 

-   [Atvejų valdymo apžvalga](cases.md)
-   [Atvejų saugos, procesų ir kategorijų konfigūravimas](plan-case-management.md)

## <a name="record-templates"></a>Įrašų šablonai
Įrašų šablonai gali padėti greičiau kurti įrašus. Galite sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių. 

-   [Įrašų šablonai](record-templates.md)
- [Įrašo šablono sukūrimas, kad būtų paprasčiau įvesti duomenis](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (užduočių vedlys)
- [Naujo įrašo kūrimas naudojant įrašo šabloną](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (užduočių vedlys)

## <a name="general-organization-administration"></a>Bendrasis organizacijos administravimas
-   [Keisti reklaminę juostą arba logotipą](../get-started/tasks/change-banner-or-logo.md) (Užduočių vedlys)
- [Dokumentų valdymo konfigūravimas](configure-document-management.md)
- [El. pašto konfigūravimas ir siuntimas](configure-email.md)
-   [Datos / laiko duomenys ir laiko juostos](date-time-zones.md)








