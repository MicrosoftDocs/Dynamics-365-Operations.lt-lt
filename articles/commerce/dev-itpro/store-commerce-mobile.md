---
title: "\"Store Commerce\" programa, skirta mobiliųjų įrenginių platformos"
description: Šiame straipsnyje aprašoma, kaip pradėti naudoti " Microsoft Dynamics 365 Commerce Store Commerce" programą, skirtą ir Android "iOS".
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/07/2022
ms.locfileid: "9641683"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>"Store Commerce" programa, skirta mobiliųjų įrenginių platformos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pradėti naudoti " Microsoft Dynamics 365 Commerce Store Commerce" programėles, skirtas ir Android "iOS".

Dynamics 365 Commerce Dėl Android "IOS" mobiliųjų programėlių ir "iOS" reikia iš karto ir paprastai įdiegti visus mobiliųjų įrenginių (EKA) įrenginius, kurie skirti jūsų mažmeninės prekybos aplinkai. "Store Commerce" mobiliosios programėlės suteikia visas "Store Commerce" programos, skirtos " [Windows](store-commerce.md) " telefono ir planšetiniams įrenginiams, galimybių ir galimybių galimybes. "Store Commerce" mobiliųjų programėlių galima įdiegti tiesiogiai iš "Skirtukas" ir "Automatiškai" programų parduotuvių ir nereikalaujama, kad programuotojas sukurtų naują programos paketą, kurį įdiegtų arba atnaujintų. 

"Store Commerce" mobiliosios programėlės visiškai atitinka dabartines "Retail" programėles. Be to, "Store Commerce for IOS" palaiko paskirtą aparatūros stotį, kad "iOS" įrenginiai galėtų palaikyti ryšį su tinklo mokėjimo terminalais, kvitų spausdintuvais ir kasos stalčiais, kuriems nereikia diegti bendrai naudojamos aparatūros stoties. 

> [!IMPORTANT]
> Parduotuvės "Commerce" programėlės, skirtos "Windows", ir "iOS" yra kito generavimo EKA programos, Android skirtos Dynamics 365 Commerce. Dabartinė "Modern POS" (MPOS) [programa ir "Retail" pasenusios](hybridapp.md) mobiliųjų įrenginių programėlės 2023 m. spalio mėn. bus pasenusios. "Microsoft" rekomenduoja naudoti "Store Commerce" arba "Cloud POS" (CPOS) diegiant visus naujus EKA. Esami klientai turi suplanuoti perkelti iš "Retail" parduotuvės "Commerce" programos. Daugiau informacijos apie MPOS ir "Retail [" programėlių pasenusių grafiką ieškokite parduotuvės technologijų Dynamics 365 Commerce dėklo modernizavimas](https://www.microsoft.com/download/details.aspx?id=103896). 

## <a name="app-architecture"></a>Programos architektūra

"Store Commerce" mobiliosios programėlės naudoja tą pačią topologiją kaip ir "Store Commerce" programa, skirta "Windows", kai ji diegiama paleisties režimu. "Store Commerce" mobiliosios programėlės yra shell programos, kurios generuoja CPOS tiesiogiai iš "Commerce Scale Unit" (CSU) ir prisijungs prie "Headless Commerce" ir "Commerce Headquarters" per CSU. "Shell" programos modelis leidžia "Store Commerce" programoms palaikyti paskirtą aparatūros stotį, kad būtų galima tiesiogiai integruoti su mokėjimo terminalu, spausdintuvu, kasų stalčiumi ir kitais išoriniais įrenginiais. Jums nereikia nustatyti bendrai naudojamos aparatūros stoties, kad būtų galima naudoti aparatūros įrenginius. 

Norėdami atnaujinti "Store Commerce" mobiliąją programą, tik atnaujinkite CSU. Programa automatiškai gaus visas naujas EKA funkcijas ir funkcijas. Norėdami gauti daugiau informacijos apie CSU atnaujinimą, [žr. Taikyti naujinimus ir plėtinius "Commerce Scale Unit" (debesis).](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)

Shell programėlės aptarnaujamos naudojant programų parduotuvės naujinimus. Kai smulki versija pasiekia bendrą pasiekiamumą (GA), "Microsoft" ją paskelbs programų parduotuvėse. "Microsoft" taip pat gali publikuoti pataisas tarp smulkių versijų naujinimų, kad būtų atlaisvinto didelio prioriteto klaidos pataisos.

## <a name="prerequisites"></a>Būtinieji komponentai

"Store Commerce" mobiliųjų programėlių Dynamics 365 Commerce reikia, ypač "Commerce Headquarters" ir CSU komponentų. Toliau esančioje lentelėje pateikiamos mažiausios operacinės sistemos (OS) ir CSU Android versijos, kurių reikia pagal "iOS" mobiliąsias programėles. 

| Būtinoji sąlyga | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS versija   | 7.0          | 15.0 |
| CSU versija  | 9.38.22266.8 | Reikia apibrėžti  |

## <a name="install-the-app"></a>Programos diegimas

"Store Commerce" mobiliųjų programėlių galite įdiegti tiesiogiai iš "Vykdykės" parduotuvės arba "Sg App Store". 

- [Parduotuvės "Commerce" programa, skirta Android](https://aka.ms/storecommerceandroid)
- "Store Commerce" programa, skirta "iOS" (greit pasiekiama)

Iš Android ciklo tarnybų bendrai naudojamo turto bibliotekos taip pat galima atsisiųsti programos (.vykdyklė) ir "Turimos" programos (.ipa) paketus Microsoft Dynamics. 

## <a name="device-and-register-setup"></a>Įrenginio ir registro nustatymas

Kad būtų galima suaktyvinti "Store Commerce" mobiliųjų programėlių registrą, turite nustatyti įrenginį ir registrą "Commerce Headquarters". Daugiau informacijos ieškokite Įrenginiai [ir registrai](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Įrenginio nustatymas

Norėdami sukurti ir nustatyti naują įrenginį, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į "**Retail" ir "Commerce \> Channel" nustatymo \> EKA nustatymo įrenginius \>**. 
1. Sukurkite naują įrenginį **ir pasirinkite "Modern POS" arba " Android** **Modern POS" – "IOS** " kaip programos tipą, atsižvelgiant į diegiamą mobiliąją programą. 

    > [!NOTE] 
    > " **Modern POS" – Android** ir " **Modern POS" – "IOS** " programų tipai taip pat naudojami diegiant dabartines "Apps" Android ir "iOS". Baigus MPOS **Android** **, šių programų tipų etiketės bus atnaujintos į parduotuvės komercijos – ir "Modern POS" – iOS.** 

### <a name="register-setup"></a>Registro sąranka

Galite sukurti naują kasos aparatą ir susieti jį su sukurtu įrenginiu arba galite susieti esamą registrą su savo nauju įrenginiu. Norėdami gauti daugiau informacijos apie registrus, žr [. Kurti ir susieti registrus](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Ekrano maketo nustatymas

Dynamics 365 Commerce Jei iš naujo sukuriate ekrano maketą, įtrauktą į demonstracinius duomenis, kurie pateikiami su licencija, "Store Commerce" programa automatiškai pasirinks įtrauktą fiskalinį maketą, jei jūsų įrenginio ekrano skiriamoji geba yra mažesnė nei 480 &times; 853 pikselių stačioje padėtyje. Tačiau jei kuriate ekrano maketą nuo pradžių arba jei jūsų mobiliajame įrenginys naudoja didesnę skiriamąją gebą, nei palaikomas kompaktinis maketas, įsitikinkite, kad kuriate skiriamąją gebą ir susietus mygtukų tinklelius, tinkamus telefono ar planšetiniam kompiuteriui, kurį planuojate diegti. Daugiau informacijos apie ekrano maketo konfigūracijas ieškokite [EKA vartotojo sąsajos vaizdinės konfigūracijos](../pos-screen-layouts.md). 

Sukonfigūrę įrenginius ir registrus, "Commerce Headquarters **" eikite į "Retail" ir "Commerce Retail" ir "Commerce \> ID \> " paskirstymo** grafikus ir vykdykite kasos aparatų užduotį.

## <a name="activate-a-device"></a>Įrenginio aktyvinimas

Norėdami aktyvinti įrenginį "Store Commerce" mobilioje programoje, atlikite šiuos veiksmus.

1. Atidarykite programą mobiliajame įrenginyje.
1. Įveskite CPOS URL, kurį galite rasti aplinkos informacijos puslapyje ciklo tarnybose arba **"Commerce Headquarters" (** **\> mažmeninės prekybos ir komercijos \> kanalo nustatymo kanalo profilių) puslapyje Kanalo profiliai.**
1. Prisiregistruokite naudodami darbuotojo, kuris turi teisę valdyti įrenginius, kredencialus.
1. Pasirinkite parduotuvę, susietą su kasos aparatu, kurį sukūrėte arba pakartotinai naudojate "Commerce Headquarters".
1. Pasirinkite registrą, kurį susieto su įrenginiu, kurį sukūrėte "Commerce Headquarters".
1. Jūsų įrenginys dabar turi būti suaktyvintas. Galite prisiregistruoti prie kasos aparato naudodami darbuotojo, susijusio su pasirinkta parduotuve, operatoriaus ID ir slaptažodį. 

Daugiau informacijos apie įrenginio aktyvinimą ieškokite įrenginio aktyvinimą [naudojant point of sale (EKA](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation)).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Funkcijų lygumas su parduotuvės "Commerce", skirta "Windows"

Toliau pateiktoje lentelėje palyginamos parduotuvės "Commerce" programos "Windows Android" ir "IOS" platformos galimybės.

| Funkcija                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Paskirta aparatūros stotis                                                            | Taip     | Taip     | Taip |
| Bendrai naudojama aparatūros stotis                                                               | Taip     | Taip     | Taip |
| Ryšys su tinklo išoriniais įrenginiais (mokėjimo terminalas, spausdintuvas ir kasos stalčius) | Taip     | Taip     | Taip |
| Pardavimo vietos (OEKA) išorinių įrenginių OLE per vietinę aparatūros stotį             | Taip     | Ne      | Ne  |
| Atjungties režimas                                                                          | Taip     | Ne      | Ne  |

## <a name="additional-resources"></a>Papildomi ištekliai

[„Store Commerce“ programa](store-commerce.md)

[Pasirinkimas tarp „Store Commerce“ ir „Cloud POS“](../mpos-or-cpos.md)

[Parduotuvės "Commerce" nustatymo ir diegimo trikčių šalinimas](../troubleshoot/store-commerce-setup-installation.md)
