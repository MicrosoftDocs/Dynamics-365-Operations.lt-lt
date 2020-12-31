---
title: Organizacijos administravimo pagrindinis puslapis
description: Šioje temoje nurodyti ištekliai, kurie padės organizacijoje naudotis.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53a2abad03ab9349834aaafbec572d17d96df9c1
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694007"
---
# <a name="organization-administration-home-page"></a>Organizacijos administravimo pagrindinis puslapis

[!include [banner](../includes/banner.md)]

Šios temos turinys padės patyrusiems naudotojams ir administratoriams sistemą sukonfigūruoti taip, kad ji jūsų organizacijoje ir įmonėje veiktų sklandžiai bei efektyviai.

Didelė čia pateikto turinio dalis taikoma modulio **Organizacijos administravimas** funkcijoms. Tačiau yra keletas užduočių, pavyzdžiui, įrašo šablono kūrimo ir naudojimo, kurias galima atlikti bet kokiame modulyje, kad organizacija galėtų veikti efektyviau.

## <a name="number-sequences"></a>Numeravimai

Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti. Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas *nuoroda*. Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.

- [Numeracijų apžvalga](number-sequence-overview.md)
- [Numeracijų nustatymas naudojant vedlį](tasks/set-up-number-sequences-wizard.md) (Užduočių vedlys)
- [Atskirų numeracijų nustatymas](tasks/set-up-number-sequences-individual-basis.md) (Užduočių vedlys)

## <a name="organizations"></a>Organizacijos

Organizacija yra grupė žmonių, kurie dirba kartu vykdydami verslo procesą arba siekdami tikslo. Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą.

Prieš nustatydami organizacijas ir hierarchijas, būtinai suplanuokite, kaip bus modeliuojamas jūsų verslas. Organizacijos modelis turi didelės įtakos įgyvendinimui ir verslo procesams.

- [Organizacijų ir organizacijų hierarchijų apžvalga](organizations-organizational-hierarchies.md)
- [Organizacijos hierarchijos planavimas](plan-organizational-hierarchy.md)
- [Organizacijos hierarchijos kūrimas](tasks/create-organization-hierarchy.md) (Užduočių vedlys)
- [Juridinio subjekto kūrimas](tasks/create-legal-entity.md) (Užduočių vedlys)
- [Valdymo vieneto kūrimas](tasks/create-operating-unit.md) (Užduočių vedlys)

## <a name="address-books"></a>Adresų knygelės

Visuotinė adresų knygelė yra centralizuota saugykla, kurioje turi būti saugomi visų vidinių ir išorinių asmenų bei organizacijų, su kuriais įmonė bendrauja, bendrieji duomenys. Duomenys, susieti su šalies įrašais, apima šalies pavadinimą, adresą ir kontaktinę informaciją.

Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai.

- [Visuotinės adresų knygelės apžvalga](overview-global-address-book.md)
- [Visuotinės adresų knygelės ir kitų adresų knygelių planavimas](plan-configuration-global-address-book-additional-address-books.md)
- [Visuotinės adresų knygelės konfigūravimas](tasks/configure-global-address-book.md)
- [DUK apie adresų knygeles](qa-address-books.md)

## <a name="workflow"></a>Darbo eiga

Darbo eiga yra sistema, kurią galite naudoti atskiroms darbo eigoms arba verslo procesams kurti. Kurdami darbo eigą nurodote, kaip dokumentas juda sistemoje, parodydami, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą.

- [Darbo eigos sistemos apžvalga](overview-workflow-system.md)
- [Darbo eigos elementai](workflow-elements.md)
- [Darbo eigos patvirtinimo procesų veiksmai](workflow-actions.md)
- [Darbo eigų kūrimo apžvalga](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniniai parašai

Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę. Kai kuriose pramonės šakose elektroninis parašas turi tokią pat teisinę galią kaip parašas ranka. Elektroniniai parašai yra reglamentus atitinkantis reikalavimas kai kurioms reguliuojamoms pramonės šakoms, pvz., vaistų, maisto ir gėrimų, aviacijos ir gynybos.

Galite naudoti elektroninius parašus svarbiems verslo procesams. Kai kuriuose procesuose yra įdiegtos elektroninio parašo galimybės. Taip pat galite sukurti pasirinktinius parašo reikalavimus bet kuriai duomenų bazės lentelei ir laukui.

- [Elektroninių parašų apžvalga](electronic-signature-overview.md)
- [Elektroninių parašų nustatymas](tasks/set-up-electronic-signatures.md) (Užduočių vedlys)

## <a name="case-management"></a>Atvejų valdymas

Planuojant, sekant ir analizuojant atvejus galima sukurti efektyvius sprendimus, skirtus panašioms problemoms spręsti. Pavyzdžiui, kai klientų aptarnavimo atstovai arba personalo srities darbuotojai kuria atvejus, informacijos, padėsiančios efektyviau dirbti su atveju ar jį spręsti, jie gali rasti informaciniuose straipsniuose.

- [Atvejų valdymo apžvalga](cases.md)
- [Atvejų kategorijų saugos, atvejų procesų ir atvejų kategorijų planavimas](plan-case-management.md)

## <a name="record-templates"></a>Įrašų šablonai

Įrašų šablonai gali padėti greičiau kurti įrašus. Galite sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių.

- [Įrašų šablonų apžvalga](record-templates.md)
- [Įrašo šablono sukūrimas, kad būtų paprasčiau įvesti duomenis](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (užduočių vedlys)
- [Naujo įrašo kūrimas naudojant įrašo šabloną](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Užduočių vedlys)

## <a name="general-organization-administration"></a>Bendrasis organizacijos administravimas

- [Keisti reklaminę juostą arba logotipą](../get-started/tasks/change-banner-or-logo.md) (Užduočių vedlys)
- [Dokumentų valdymo konfigūravimas](configure-document-management.md)
- [El. pašto konfigūravimas ir siuntimas](configure-email.md)
- [Datos / laiko duomenys ir laiko juostos](date-time-zones.md)
