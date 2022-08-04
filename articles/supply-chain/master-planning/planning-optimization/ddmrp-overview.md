---
title: Poreikio valdomas medžiagų poreikių planavimo (DDMRP) peržiūra
description: Šiame straipsnyje pateikiama informacija apie poreikio valdomas medžiagų poreikių planavimą (DDMRP), planavimo metodologiją, pagrįstą tiekimo ir poreikio atsieavimu.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186595"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Poreikio valdomas medžiagų poreikių planavimo (DDMRP) peržiūra

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Metams įmonės naudoja medžiagų poreikių planavimą (MRP) kaip medžiagų ir komponentų, reikalingų produktui gaminti, apskaičiavimo sistemą. Tačiau tiekimo grandinės dabar pasikeitė. Dalių gamybos laikas ilgesnis, nes jos yra šaltinis iš užjūrio. Dėl to daugelis įmonių pranešė apie neįrašytas atsargas ar perpildas, nes ji nežino, kiek atsargų yra atsargose. Taip pat yra daugiau rinkos svyravimų (kartais tiksliai prognozuojama) ir klientai per trumpą gamybos laiką reikalauja produktų. Dėl to visame pasaulyje trūksta tiekimo grandinės. Be to, MRP įrankiai dažnai pateikia planuotojas 0 veiksmų. Todėl yra tiksliai žinoti, ką sutelkti į tai. Dažnai daugelio šių problemų sprendimas yra pereiti į poreikio turimo medžiagų poreikio planavimą (DDMRP).

DDMRP yra planavimo metodologija, pagrįsta tiekimo ir poreikio iššiomu. Šis atsiejimas pasiekiamas nustatant prekių atsiejimo taškus. Šioms prekėms buferiai tvarkomi siekiant užtikrinti, kad bus saugomas tinkamas atsargų kiekis. Tiekimo ir poreikio iššišiavimas padeda išvengti "nepavykusio", nes nuokrypis per grandinę nėra perduodamas. (Gamybos *poveikis* nurodo, kaip maži poreikio svyravimai mažmeninės prekybos lygiu gali progresyviškai padidinti poreikio svyravimus didmeninio pardavimo, platintojo, gamintojo ir žaliavų tiekėjų lygiuose.) Kiekvienas buferis yra skirtas padengti vidutinį dalies naudojimą, jį taip pat galima koreguoti, norint padengti paklausos svyravimus.

DDMRP patvirtintas kaip vertinga planavimo metodologija kintamoms aplinkai, kur leistino kliento nuokrypio laikas yra trumpesnis už kaupiamąjį gamybos laiką.

## <a name="the-five-components-of-ddmrp"></a>Penki DDMRP komponentai

DDMRP turi penkis nuoseklius komponentus (žingsnius). Pirmieji trys komponentai iš esmės apibrėžia originalią ir per daug reikalaujamo medžiagų poreikio planavimo modelio konfigūraciją. Paskutiniai du komponentai apibrėžia kasdienę metodologijos operaciją.

1. **[Strateginių atsargų padėties nustatymu](ddmrp-inventory-positioning.md)** – nustatyti iššiuos taškus tiekimo grandinės tinkle. Iššiupimo taškai yra konkretūs jūsų tiekimo grandinės taškai, kurių atsargų buferį jūs stebite ir papildote.
2. **[Buferio profiliai ir lygiai – kiekviename iššiupimo taške nustatykite buferio dydžius](ddmrp-buffer-profile-and-levels.md)** (minimalų kiekį, maksimalų kiekį ir užsakymo vietos) bei užsakymo perdavimo kiekį.
3. **[Dinaminis buferio](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** koregavimas – koreguokite buferio lygius, atsižvelgdami į kintančius valdymo parametrus arba suplanuotus būsimus įvykius.
4. **[Poreikio planavimas – generuoti](ddmrp-planning.md)** tiekimo užsakymus, kai to reikia. Šie tiekimo užsakymai apima gamybos užsakymus, pirkimo užsakymus ir atsargų perkėlimo užsakymus
5. **[Labai suplanuotas ir matomas](ddmrp-visual-and-collaborative-execution.md)** vykdymas – vykdyti tiekimo užsakymus, naudojant vizualizaciją.

DDMRP paprastai naudojamas gamintojų, kurie turi kelių lygių komplektavimo specifikacijas (KS). Tačiau ji taip pat gali būti taikoma paskirstymui ir mažmeninės prekybos tinklus.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP, Dynamics 365 Supply Chain Management

DDMRP įtraukiamas į "Microsoft Dynamics 365 Supply Chain Management " ir nereikia papildomų licencijos mokesčių. Tiekimo grandinės valdymo metu DDMRP funkcija pridėta prie esamo bendrojo **planavimo modulio**. Tačiau reikia naudoti planavimo optimizavimo priedą. 

DDMRP yra integruotas į esamus tiekimo grandinės valdymo planavimo nustatymus ir yra naudojamas kartu su šiais nustatymais, siekiant pasiekti tinkamą jūsų verslo planavimo konfigūraciją. Jį kontroliuoja naujas padengimo kodas, kuris skiriasi nuo laikotarpio, min. / maks., poreikio ir t. t. Tai nėra naujas modulis ir jis nepakeičia esamų planavimo funkcijų. Tačiau, suteikia jums daugiau funkcijų naudoti.
