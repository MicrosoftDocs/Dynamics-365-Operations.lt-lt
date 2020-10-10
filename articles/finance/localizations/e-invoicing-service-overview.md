---
title: Elektroninių SF išrašymo priedo apžvalga
description: Šioje temoje pateikiama informacija apie elektroninių SF išrašymo priedą „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b3445157efce6349b3febafb6c860260052f7d6c
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836000"
---
# <a name="electronic-invoicing-add-on-overview"></a>Elektroninių SF išrašymo priedo apžvalga

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Elektroninių SF išrašymo priedas, skirtas „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management” yra itin keičiamo dydžio kelių nuomotojų paslauga, įgalinanti konfigūruojamą elektroninių SF dokumentų apdorojimą ir konfigūruojamus dokumentų mainus. Apdorojimo ir integravimo taisyklės yra visiškai konfigūruojamos, o logika vykdoma už „Finance” ir „Supply Chain Management” ribų. Ši paslauga iš esmės skirta el. SF apdoroti verslo ir vyriausybės scenarijuose, bet ji gali būti pritaikyta ir sukonfigūruota kitiems tikslams.

Elektroninių SF išrašymo priedas gali padėti pasiekti toliau nurodytus tikslus.

- Greitas ir lengvas konkrečių šalių / regionų reikalavimų taikymas
- Standartizuoti elektroninių SF išrašymo priedo sprendimo diegimai
- Išplėstinis dokumentų retrospektyvos atsekamumas
- Trumpesnis diegimo ciklas
- Sumažintos bendros nuosavybės išlaidos (TCO)
- Lengvai koreguojamos konfigūracijos, nereikalaujančios kodo pakeitimų
- Supaprastintas konfigūracijos pakavimas
- Įtaisytas eksportavimas, importavimas ir integravimas bei lengvas išplečiamumas apdorojant el. SF dokumentus
- Paprastas pakartotinis tų pačių eksportavimo, importavimo ir integravimo konfigūracijų naudojimas visose įmonėse

Norėdami naudoti elektroninių SF išrašymo priedą, turite jį įdiegti iš jūsų projekto, esančio „Microsoft Dynamics Lifecycle Services” (LCS). Tada atlikite nustatymo procedūrą, norėdami įjungti integravimą su „Finance” arba „Supply Chain Management”. Daugiau informacijos žr. [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="availability"></a>Prieinamumas

Iš pradžių elektroninių SF išrašymo priedas pasiekiamas pasirinktiems klientams peržiūros programoje. Vėliau peržiūra bus pasiekiama daugiau klientų. Galiausiai paslauga taps visuotinai prieinama. Kadangi funkcijos, vykdančios konkrečių šalių / regionų reikalavimus, gali būti ribojamos skirtinguose leidimo etapuose, visada turite patikrinti naujausius dokumentus, nurodančius konkrečių šalių / regionų palaikomų sprendimų padengimą ir aprėptį.

Elektroninių SF išrašymo priedas diegiamas toliau nurodytuose „Azure” regionuose.

- Jungtinės Valstijos
- Europa

> [!NOTE]
> Elektroninių SF išrašymo priedas nepalaiko vietinių visuotinių diegimų.

## <a name="extended-configurability"></a>Išplėstinis konfigūravimas

Elektroninių SF išrašymo priedas gali būti naudojamas scenarijuose, kai turite sukurti ir siųsti elektroninį dokumentą nurodytoms šalims. Jis sukurtas tam, kad būtų galima konfigūruoti apdorojimo veiksmų srautą, remiantis gautais duomenimis. Konfigūravimo parinktys, pasiekiamos „Finance” ir „Supply Chain Management”, leidžia atlikti tik dokumentų transformaciją. Paslauga praplečia šias parinktis įtraukdama joje pasiekiamus konfigūruojamus integravimus. Be to, visos elektroninių SF funkcijos, kurios anksčiau buvo prieinamos, pvz., Brazilijos „Nota fiscal eletrônica” (NF-e), Meksikos „Comprobante Fiscal Digital por Internet” (CFDI) arba kitos Vakarų Europos universaliosios verslo kalbos (UBL) / „Pan-European Public Procurement OnLine” (PEPPOL) funkcijos, naudos konfigūracijas eksportavimui ir importavimui bei integracijų su išorinėmis žiniatinklio tarnybomis įjungimui.

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

- Parengtas naudoti integravimas su „Finance” ir „Supply Chain management”
- Nuosekli vartotojo patirtis vykdant visų šalių ar regionų el. SF išrašymo konfigūracijos ir stebėjimo procesus
- Spartesnis, lengvesnis ir pigesnis elektroninių SF išrašymo priedo sprendimų taikymas naujose šalyse ar regionuose
- Paslaugos konfigūravimas naudojant „Regulatory Configuration Services” (RCS) ir globalizacijos funkcijos nustatymą
- Verslo duomenų transformavimas į kelis el. SF formatus (XML, „JavaScript Object Notation“ \[JSON\], TXT ir kableliais atskirtų reikšmių \[CSV\]) naudojant konfigūracijas, apibrėžtas RCS:

    - Elektroninių ataskaitų formatai, pasiekiami šalyse arba regionuose, kuriuose negalima konfigūruoti el. SF transformavimo

- Konfigūruojamas elektroninių SF pateikimas išorinėms žiniatinklio tarnyboms, įskaitant sertifikavimo tvarkymą naudojant skaitmeninius parašus:

    - Įtaisytas, lengvai išplečiamas ir konfigūruojamas integravimas su papildomu kelių šalių turiniu

    > [!NOTE]
    > Šiuo metu palaikomas ribotas tiesioginių pateikimų skaičius. Daugiau informacijos žr. ankstesniame šios temos skyriuje [Pasiekiamumas](#availability). Palaikymas bus išplėstas ateityje.

- Atsakymų iš žiniatinklio tarnybų tvarkymas, įskaitant konfigūruojamų išimties pranešimų tvarkymą
- Elektroninių parašų palaikymas (pvz., naudojant XMLDSig pasirašymo algoritmą)
- El. SF pranešimų paketinis apdorojimas

## <a name="architecture-and-data-flow"></a>Architektūra ir duomenų srautai

Kai elektroninių SF išrašymo priedas įdiegtas iš LCS, o reikiamas nustatymas baigtas visose būtinose programose, sukuriamas saugus ryšys. Šiuo metu paslauga yra duomenų centruose Jungtinėse Valstijose ir Europoje. Todėl paslaugos vieta gali skirtis nuo susijusio „Finance” ar „Supply Chain Management” egzemplioriaus vietos. Atlikus elektroninių SF išrašymo priedo nustatymą ir įjungus integravimą, kaskart siunčiant elektroninę SF, bendrieji duomenys ir su konkrečiu dokumentu susiję operacijų duomenys siunčiami į elektroninių SF išrašymo priedą.

> [!NOTE]
> Jeigu jūsų elektroninėje SF ar kitame dokumente yra asmeninių duomenų, patikrinkite, šios funkcijos naudojimas atitinka bendrąjį duomenų apsaugos reglamentą (GDPR) ir kitus reglamentus, susijusius su asmeninių duomenų perkėlimu.

### <a name="high-level-description-of-the-data-flow"></a>Išsamus duomenų srauto aprašas

1. Klientas išsiunčia kanoninį verslo dokumentą į paslaugą.
2. Atsižvelgdama į konteksto informaciją, gaunamą iš kliento, paslauga pasirenka taikytiną apdorojimo srautą.
3. Paslauga vykdo apdorojimo veiksmus. Šie veiksmai gali apimti verslo dokumento transformavimą į elektroninę SF, elektroninio parašo taikymą ir dokumento pateikimą į išorinę žiniatinklio tarnybą.
4. Visi gauti ir apdoroti dokumentai saugomi kliento „Azure“ didelių dvejetainių objektų saugykloje.
5. Visi nuomotojo slaptieji raktai ir sertifikatai, kurie buvo naudojami apdorojimo metu, saugomi kliento „Azure” raktų saugykloje.
6. Paslauga pagal poreikį pateikia klientui informaciją apie išsiųsto verslo dokumento apdorojimo būseną.
7. Klientas gauna informaciją apie užbaigtą apdorojimo vykdymą ir pateikia visą žurnalo informaciją. Be to, jis pateikia dokumentą, sukurtą arba gautą srauto apdorojimo metu.

Toliau pateiktame paveikslėlyje vaizduojama, kaip duomenų srautai juda į ir iš elektroninių SF išrašymo priedo.

![Elektroninių SF išrašymo priedo duomenų srautas](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Privatumo pranešimas
Įgalinant ir naudojant elektroninių SF išrašymą gali reikėti siųsti ribotus duomenis, įskaitant organizacijos mokesčių registracijos ID. Jie bus persiųsti mokesčių inspekcijų patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF iš anksto nustatytais formatais, reikalingais integravimui su šiomis vyriausybės žiniatinklio tarnybomis. Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md)
- [Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia](e-invoicing-bra-get-started.md)
- [Darbo su Meksikos elektroninių SF išrašymo priedu pradžia](e-invoicing-mex-get-started.md)
- [Darbo su Italijos elektroninių SF išrašymo priedu pradžia](e-invoicing-ita-get-started.md)
- [Elektroninių SF išrašymo priedo nustatymas](e-invoicing-setup.md)
