---
title: Tiekėjo sąskaitų faktūrų automatizavimo sąrankos parinktys (peržiūros versija)
description: Šioje temoje aprašomos parinktys, kurias galima naudoti nustatant ir konfigūruojant tiekėjo sąskaitų faktūrų automatizavimą.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4411e2c6113c7e42abd4247f79c59ed2cc47c7af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248115"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Tiekėjo SF automatizavimo sąrankos parinktys

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos parinktys, kurias galima naudoti nustatant ir konfigūruojant tiekėjo sąskaitų faktūrų automatizavimą. Sąskaitos faktūros automatizavimo funkcijos naudoja šių tipų sąrankos parametrus:

- Importuotų tiekėjo sąskaitų faktūrų pateikimo į darbo eigos sistemą ir užregistruotų produktų gavimo kvitų eilučių gretinimo su patvirtinimo laukiančiomis tiekėjo sąskaitos faktūros eilutėmis parametrai.
- Automatizavimo foninių užduočių apdorojimo parametrai. Proceso automatizavimo sistema naudojama pateikti importuotas tiekėjo sąskaitos faktūras į darbo eigos sistemą. Ji taip pat naudojama automatiškai sugretinti užregistruotas produkto gavimo dokumentų eilutes su laukiančios tiekėjo SF eilutėmis ir atliekant SF gretinimo tikrinimą patikrinti neautomatizuotas SF, kurios buvo automatiškai sugretintos su produkto gavimo dokumentų eilutėmis. Šią sistemą naudoja skirtingi verslo procesai, kad nustatytų, kaip dažnai turi būti vykdomas pasirinktas procesas. Galimi **Sugretinti produkto gavimo kvitą su sąskaitos eilutėmis** ir **Pateikti tiekėjo sąskaitas faktūras darbo eigai** dažniai yra **Valanda** ir **Kasdien**.

Norėdami konfigūruoti arba peržiūrėti informaciją apie foninę užduotį, eikite į **Sistemos administravimas \> Sąranka \> Proceso automatizavimai** ir pasirinkite skirtuką **Foninė užduotis**.

Norėdami užtikrinti bekontaktį automatizavimą importavimo procese vykdant tiekėjo sąskaitų faktūrų registravimą, turite sukonfigūruoti tiekėjo sąskaitos faktūros darbo eigą. Norėdami sukonfigūruoti darbo eigą, eikite į **Mokėtinos sumos > Sąranka > Mokėtinų sumų darbo eigos**. Norint užtikrinti, kad sąskaita faktūra galėtų būti apdorota nuo pradžios iki pabaigos be rankiniu būdu atliekamų veiksmų, į savo darbo eigos konfigūraciją turite įtraukti automatizuotą registravimo užduotį.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Importuotų tiekėjo sąskaitų faktūrų pateikimo į darbo eigos sistemą parametrai

Importuotų tiekėjo sąskaitų faktūrų pateikimui į darbo eigos sistemą taikomi specialus parametrai. Be to, kai kurie parametrai naudojami gretiant užregistruotų produktų gavimo kvito eilutes su patvirtinimo laukiančiomis tiekėjo sąskaitos faktūros eilutėmis. Skirtuke **Tiekėjo sąskaitų faktūrų automatizavimas**, kuris yra puslapyje **Mokėtinų sumų parametrai**, parametrai, kuriuos turite nustatyti, yra suskirstyti į toliau nurodytas dalis:

- Tiekėjo sąskaitų faktūrų darbo eiga
- Automatiškai gretinti produktų gavimo kvitus

Galimi tolesni parametrai.

- **Automatiškai pateikti importuotas sąskaitas faktūras darbo eigai** – jei nustatysite šios parinkties reikšmę **Taip**, importuotos sąskaitos faktūros bus automatiškai pateiktos darbo eigos sistemai. Jei šios parinkties reikšmė yra **Ne**, sąskaitas faktūras reikia pateikti rankiniu būdu. Nustatę šios parinkties reikšmę **Taip**, jūs suaktyvinsite bekontaktį rezultatų importavimo procesą vykdant registravimą.

    Šios parinkties reikšmę **Taip** galite nustatyti tik tada, jei jūsų juridiniam subjektui sukonfigūruota aktyvi tiekėjo sąskaitos faktūros darbo eiga. Norėdami sukonfigūruoti darbo eigą, eikite į **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų darbo eiga**.

- **Sugretinti produktų gavimo kvitus su sąskaitos faktūros eilutėmis prieš pateikiant automatiškai** – jei nustatysite šios parinkties reikšmę **Taip**, importuotos sąskaitos faktūros negalės būti automatiškai pateiktos darbo eigos sistemai, jei kiekis gretinamame produkto gavimo kvite nesutaps su sąskaitos faktūros kiekiu. Nustačius šios parinkties reikšmę **Taip**, suaktyvinamas automatinis užregistruoto produkto gavimo kvitų sugretinimas su sąskaitos faktūros eilutėmis, kurioms nustatyta trišalė atitikimo strategija. Šis procesas bus vykdomas, kol sugretinto produkto gavimo kvito kiekis bus lygus SF kiekiui. Šiuo metu sąskaita faktūra automatiškai pateikiama darbo eigos sistemai.

    Parinktis „Sugretinti produktų gavimo kvitus su sąskaitos faktūros eilutėmis prieš pateikiant automatiškai“ pasiekiama tik tada, jei pasirinkta parinktis **Įjungti SF gretinimo tikrinimą**. Pasirinkus šią parinktį, automatiškai pasirenkama parinktis **Automatiškai sugretinti produkto gavimo kvitus su SF eilutėmis**.

- **Vykdant automatinį darbo eigos pateikimą reikalauti, kad apskaičiuotos bendrosios vertės būtų lygios importuotoms bendrosioms vertėms** – jei nustatysite šios parinkties reikšmę **Taip**, sąskaita faktūra negali būti automatiškai pateikiama darbo eigos sistemai, kol apskaičiuotos sąskaitos faktūros bendrosios vertės nėra lygios importuotoms bendrosioms vertėms. Jei šios parinkties reikšmė yra **Ne**, sąskaita faktūra gali būti automatiškai pateikta darbo eigos sistemai, tačiau ji negali būti užregistruota, kol apskaičiuotos bendrosios vertės nebus pakoreguotos, kad atitiktų importuotas bendrąsias vertes. Jei sąskaitos faktūros sumos arba PVM sumos neimportuojate, nustatykite šios parinkties reikšmę **Ne**.
- **Automatiškai sugretinti produktų gavimo kvitus su SF eilutėmis** – jei nustatysite šios parinkties reikšmę **Taip**, vykdant foninį apdorojimą galima atlikti automatinį užregistruotų produktų gavimo kvitų sugretinimą su sąskaitos faktūros eilutėmis, kurioms nustatyta atitikimo strategija. Šis procesas bus vykdomas, kol gretinamas produkto gavimo kvito kiekis taps lygus sąskaitos faktūros kiekiui arba kol bus pasiekta lauke **Automatinio gretinimo bandymų skaičius** nurodyta reikšmė. Procesas gali būti vykdomas tol, kol į darbo eigos sistemą bus pateikta sąskaita faktūra.

    Ši parinktis galima tik pasirinkus parinktį **Įjungti SF gretinimo tikrinimą**.

    Jei nustatysite parinkties **Sugretinti produktų gavimo kvitus su sąskaitos faktūros eilutėmis prieš automatiškai sugretinant** reikšmę **Taip**, šios parinkties reikšmės **Ne** nebus galima nustatyti. Norėdami nustatyti šios parinkties reikšmę **Ne**, pirmiausia turite nustatyti parinkties **Sugretinti produktų gavimo kvitus su sąskaitos faktūros eilutėmis prieš automatiškai sugretinant** reikšmę **Ne**.

- **Automatinio gretinimo bandymų skaičius** – nustatykite, kiek kartų sistema turi bandyti sugretinti produktų gavimo kvitus su sąskaitos faktūros eilute iki tol, kol procesas bus nesėkmingai užbaigtas. Pasiekus nurodytą bandymų skaičių, sąskaita faktūra pašalinama iš automatino apdorojimo.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]