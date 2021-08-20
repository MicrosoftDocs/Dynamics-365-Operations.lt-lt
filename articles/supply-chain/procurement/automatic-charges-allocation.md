---
title: Automatinis išlaidų paskirstymas
description: „Microsoft Dynamics 365 Supply Chain Management” išlaidų funkcija padeda automatiškai paskirstyti išlaidas pirkimo arba pardavimo užsakymuose.
author: dasani-madipalli
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 04e17947073fca63ab68f0b5d0d72eb8366a1600117f61851179e8b0ed2c8184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753944"
---
# <a name="automatic-allocation-of-charges"></a>Automatinis išlaidų paskirstymas

[!include [banner](../includes/banner.md)]

Atsižvelgdami į klientą, su kuriuo dirbate, arba į prekę, kurią parduodate, galbūt norėsite taikyti konkrečias papildomas išlaidas. „Microsoft Dynamics 365 Supply Chain Management” *išlaidų* funkcija padeda automatiškai paskirstyti išlaidas pirkimo arba pardavimo užsakymuose.

Automatinės išlaidos taikomos automatiškai jums kuriant pardavimo arba pirkimo užsakymą. Galite nustatyti automatines išlaidas konkretiems tiekėjams, klientams arba tiekėjų ar prekių grupėms. Taip pat galite nustatyti automatines išlaidas, taikomas visiems tiekėjams, klientams arba prekėms.

## <a name="set-up-charges-codes"></a>Išlaidų kodų nustatymas

Norėdami paskirstyti išlaidas, pirmiausia turite nurodyti išlaidų kodus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Dirbdami su pirkimo užsakymais, eikite į **Mokėtinos sumos \> Išlaidų sąranka \> Išlaidų kodas**.
    - Dirbdami su pardavimo užsakymais, eikite į **Gautinos sumos \> Išlaidų sąranka \> Išlaidų kodas**.

1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti išlaidų kodą.
1. Naujojo įrašo antraštėje nustatykite toliau pateiktus laukus.

    - **Išlaidų kodas** – įveskite išlaidų kodą.
    - **Aprašas** – įveskite išlaidų aprašą.
    - **Prekės PVM grupė** – pasirinkite prekės PVM grupę, jei taikoma.
    - **Paskirstyti proporcingai** – nustatykite šią parinktį į *Taip*, norėdami proporcingai paskirstyti jūsų išlaidas. Šią parinktį galima naudoti tik dirbant su pardavimo užsakymais.
    - **Didžiausia suma** – įveskite didžiausią leistiną išlaidų kodo sumą. Šis laukas naudojamas tiekėjo SF išlaidoms tikrinti. Jis taikomas tik pirkimo užsakymuose.

        > [!NOTE]
        > Norėdami įjungti pirkimo užsakymų išlaidų tikrinimo funkciją, eikite į **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**. „FastTab” **SF tikrinimas** dalyje **SF tikrinimas** nustatykite parinktį **Įgalinti SF gretinimo tikrinimą** į *Taip*.

1. „FastTab” **Registravimas** apima dalis **Debetas** ir **Kreditas**. Nustatyti toliau pateiktus laukus, atsižvelgdami į didžiąją knygą, kurioje norite registruoti išlaidas.

    - **Tipas** – pasirinkite sąskaitos, kurioje registruojate, tipą (*Didžioji knyga*, *Klientas* arba *Prekė*).
    - **Registravimas** – pasirinkite kuriamų registravimų tipą (pvz., *Brokerio mokestis* arba *Kliento sudengimas*).
    - **Sąskaita** – pasirinkite sąskaitą, kurioje norite registruoti išlaidas.

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="create-charge-groups"></a>Išlaidų grupių kūrimas

Išlaidų grupės automatiškai paskirsto konkrečias klientų arba tiekėjų grupės išlaidas. Tolesniuose poskirsniuose aprašoma, kaip kurti ir priskirti šias išlaidų grupes.

### <a name="charge-groups-for-purchase-orders"></a>Pirkimo užsakymų išlaidų grupės

Norėdami sukurti pirkimo užsakymų mokesčių grupes, atlikite toliau pateiktus veiksmus.

1. Eikite į **Mokėtinos sumos \> Išlaidų sąranka \> Tiekėjo išlaidų grupė**.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami įtraukti eilutę į tinklelį ir nustatyti toliau pateiktus laukus.

    - **Išlaidų grupė** – įveskite išlaidų grupės pavadinimą.
    - **Aprašas** – įveskite išlaidų grupės aprašą.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai** ir atidarykite esamą tiekėją arba sukurkite naują tiekėją.
1. „FastTab” **Pirkimo užsakymo numatytosios reikšmės** dalyje **Pirkimo užsakymas** nustatykite lauką **Išlaidų grupė** į jūsų ką tik sukurtą išlaidų grupę.

### <a name="charge-groups-for-sales-orders"></a>Pardavimo užsakymų išlaidų grupės

Norėdami sukurti pardavimo užsakymų mokesčių grupes, atlikite toliau pateiktus veiksmus.

1. Pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Klientų išlaidų grupės**.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami įtraukti eilutę į tinklelį ir nustatyti toliau pateiktus laukus.

    - **Išlaidų grupė** – įveskite išlaidų grupės pavadinimą.
    - **Aprašas** – įveskite išlaidų grupės aprašą.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai** ir atidarykite esamą klientą arba sukurkite naują klientą.
1. „FastTab” **Pirkimo užsakymo numatytosios reikšmės** dalyje **Pardavimo užsakymas** nustatykite lauką **Išlaidų grupė** į jūsų ką tik sukurtą išlaidų grupę.

## <a name="define-auto-charges"></a>Automatinių išlaidų nustatymas

Nustatę jūsų išlaidų kodus, atlikite toliau pateiktus veiksmus, norėdami nustatyti automatines išlaidas.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Dirbdami su pirkimo užsakymais, eikite į **Paraiškos \> Sąranka \> Išlaidos \> Automatinės išlaidos**.
    - Dirbdami su pardavimo užsakymais, eikite į **Gautinos sumos \> Sąranka \> Išlaidų sąranka \> Automatinės išlaidos**.

1. Sąrašo srities lauke **Lygis** pasirinkite lygį, kuriame taikomos jūsų automatinės išlaidos.

    - *Pagrindinis* – pritaikyti išlaidas užsakymo antraštei.
    - *Eilutės* – pritaikyti išlaidas užsakymo eilutėms.

1. Pasirinkite esamas automatines išlaidas, kurias norite redaguoti, arba pasirinkite **Naujas**, norėdami nustatyti naujas automatines išlaidas.
1. Sąraše **Sąskaitos kodas** pasirinkite vieną iš toliau pateiktų reikšmių, norėdami nurodyti sąskaitų, kurios bus paveiktos, aprėptį.

    - *Lentelė* – priskirti išlaidas konkrečiam klientui arba tiekėjui.
    - *Grupė* – priskirti išlaidas papildomų mokesčių grupei.
    - *Visi* – priskirti išlaidas visiems klientams arba tiekėjams.

1. Lauke **Kliento ryšys** arba **Tiekėjo ryšys** pasirinkite konkretų klientą arba klientų grupę, jei nustatėte lauką **Sąskaitos kodas** į *Lentelė*. Jei nustatėte lauką **Sąskaitos kodas** į *Grupė*, pasirinkite kliento arba tiekėjo išlaidų grupę.
1. Lauke **Prekės kodas** pasirinkite vieną iš toliau pateiktų reikšmių, norėdami nurodyti prekių, kurios bus paveiktos, aprėptį. Prekės kodą galite pasirinkti tik tada, jei automatines išlaidas nustatote eilutės lygiu.

    - *Lentelė* – priskirti išlaidas konkrečiai prekei.
    - *Grupė* – priskirti išlaidas prekės išlaidų grupei.
    - *Visi* – priskirti išlaidas visoms prekėms.

1. Lauke **Prekės ryšys** pasirinkite konkrečią prekę, jei nustatėte lauką **Prekės kodas** į *Lentelė*. Jei nustatėte lauką **Prekės kodas** į *Grupė*, pasirinkite prekės išlaidų grupę.
1. **Tik dirbant su pardavimo užsakymais:** lauke **Pristatymo būdo kodas** pasirinkite vieną iš toliau pateiktų reikšmių, norėdami nurodyti pristatymo būdų, kurie bus paveikti, aprėptį.

    - *Lentelė* – priskirti išlaidas konkrečiam pristatymo būdui.
    - *Grupė* – priskirti išlaidas pristatymo būdų grupei.
    - *Visi* – priskirti išlaidas visiems pristatymo būdams.

1. **Tik dirbant su pardavimo užsakymais:** lauke **Pristatymo būdo ryšys** pasirinkite konkretų pristatymo būdą, jei nustatėte lauką **Pristatymo būdo kodas** į *Lentelė*. Jei nustatėte lauką **Pristatymo būdo kodas** į *Grupė*, pasirinkite pristatymo būdų grupę.
1. „FastTab“ **Eilutės** nustatykite išlaidas ir išlaidų tarifus, kurie bus naudojami, kai bus taikomos dabartinės automatinės išlaidos. Galite naudoti šiame „FastTab” esančią įrankių juostą, kad įtrauktumėte tiek eilučių, kiek jums reikia. Nustatykite toliau pateiktus laukus kiekvienoje eilutėje.

    - **Valiuta** – pasirinkite valiutą, kuri turėtų būti naudojama apskaičiuojant išlaidas.
    - **Išlaidų kodas** – pasirinkite išlaidų kodą.
    - **Kategorija** – pasirinkite vieną iš toliau pateiktų reikšmių.

        - *Fiksuota* – išlaidos eilutėje įvedamos kaip fiksuota suma. Fiksuotos išlaidos gali būti naudojamos išlaidoms užsakymo antraštėje ir užsakymo eilutėse.
        - *Vnt.* – išlaidos yra pagrįstos vienetu. Šios išlaidos gali būti naudojamos tik užsakymo eilutėse. Jos bus rodomos, kai skaičiuojate bendrą užsakymo sumą.
        - *Procentas* – išlaidos eilutėje įvedamos kaip procentinė dalis. Išlaidos procentais gali būti naudojamos išlaidoms užsakymo antraštėje ir užsakymo eilutėse.
        - *Vidinės įmonės procentas* – išlaidos eilutėje įvedamos kaip vidinės įmonės užsakymų procentinė dalis. Išlaidos vidinės įmonės procentais gali būti naudojamos tik užsakymo eilutėse.
        - *Išorinė* – išlaidos apskaičiuojamos pagal trečiųjų šalių paslaugą, susietą su vienu ar daugiau siuntų vežėjų.

    - **Išlaidų vertė** – įveskite išlaidų vertę, kuri priklauso nuo jūsų pasirinktos kategorijos.
    - **Išlaidų valiutos kodas** – nurodykite išlaidų valiutą, jei norite naudoti kitą valiutą nei tą, kurią nurodėte lauke **Valiuta**. Kitą valiutą galima naudoti tik tuo atveju, jei pasirinkto išlaidų kodo laukas **Debeto tipas** arba **Kredito tipas** nustatytas į *DK sąskaita* arba *Prekė*.
    - **Suma Nuo** – nurodykite pradinę sumą, kuriai bus taikomos automatinės išlaidos. Šiame kontekste suma reiškia bendrą užsakymo sumą.
    - **Suma Iki** – nurodykite pabaigos sumą, kuriai bus taikomos automatinės išlaidos. Šiame kontekste suma reiškia bendrą užsakymo sumą.
    - **PVM grupė** – nurodykite PVM grupę.
    - **Vieta** ir **Sandėlis** – nurodykite vietą ir sandėlį, jei išlaidos turi būti taikomos tik konkrečiai vietai ir sandėliui.
    - **Išlaikyti** – pažymėkite šį žymės langelį, norėdami po SF išrašymo išlaikyti išlaidų operacijas, kad išlaidos būtų taikomos kiekvieną kartą, kai sukuriate naują pasirinktos kliento sąskaitos SF.

1. **Tik dirbant su pardavimo užsakymais:** jei norite skaičiuoti pakopines išlaidas, žr. [Pakopinės pardavimų užsakymų išlaidos](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders).

## <a name="allocate-charges-from-the-header-to-a-line"></a>Antraštės išlaidų paskirstymas eilutėje

Toliau pateikta procedūra nurodo, kaip paskirstyti antraštės lygio išlaidas eilutėje. Prieš pradėdami šią procedūrą turite turėti *fiksuotos sumos* tipo antraštės lygio išlaidas ir užsakymą, kuriame taikomos šios išlaidos. Be to, užsakyme jau turi būti bent viena eilutės prekė.

1. Atidarykite pirkimo arba išlaidų užsakymą.
1. Veiksmų srityje atlikite vieną iš toliau pateiktų veiksmų.

    - Dirbdami su pirkimo užsakymais, skirtuko **Pirkimas** grupėje **Išlaidos** pasirinkite **Paskirstyti išlaidas**.
    - Dirbdami su pardavimo užsakymais, skirtuko **Pardavimas** grupėje **Išlaidos** pasirinkite **Paskirstyti išlaidas**.

1. Dialogo lange **Paskirstyti išlaidas užsakymo eilutėse** nustatykite toliau pateiktus laukus.

    - **Išlaidų paskirstymas** – pasirinkite vieną iš toliau pateiktų reikšmių, kad nurodytumėte, kaip paskirstyti išlaidas.

        - *Grynoji suma* – paskirstyti išlaidas pagal kiekvieną eilutės sumą, susijusią su bendra grynąja suma.
        - *Kiekis* – paskirstyti išlaidas pagal kiekvienos eilutės, susijusios su bendru vienetų skaičiumi, vienetų skaičių.
        - *Pagal eilutes* – paskirstyti išlaidas tolygiai pagal bendrą eilučių skaičių.

    - **Paskirstyti išlaidas eilutėse** – pasirinkite reikšmę, norėdami nurodyti, ar išlaidos turi būti priskirstytos visose eilutėse, ar tik teigiamose eilutėse, ar tik neigiamose eilutėse.
    - **Paskirstyti viską** – pasirinkite šį žymės langelį, norėdami paskirstyti išlaidas užsakymo eilutėse, net jei išlaidų kodo debeto tipas yra ne *Prekė*.
    - **Gauta** – pasirinkite šį žymės langelį, jei norite paskirstyti išlaidas tik gautų užsakymų eilutėse.
    - **Laikoma** – pasirinkite šį žymės langelį, jei norite paskirstyti išlaidas tik inventorizuotų užsakymų eilutėse.
    - **Rodyti pasirinkimus ir išvalyti konkrečias eilutes** – pažymėkite šį žymės langelį, norėdami pašalinti konkrečias eilutes iš šio paskirstymo. Pažymėjus šį žymės langelį, atidaromas tinklelis **Pasirinkti eilutes, kurias reikia pašalinti iš paskirstymo**. Šis tinklelis apima tik tas eilutes, kurios atitinka parametrų **Paskirstyti išlaidas eilutėse** ir **Laikoma** nustatytus kriterijus. Pavyzdžiui, jei nustatote lauką **Paskirstyti išlaidas eilutėse** į *Teigiamos eilutės* ir pažymite žymės langelį **Laikoma**, tinklelyje rodomos tik tos eilutės, kurios yra teigiamos ir inventorizuotos. Be to, tinklelis automatiškai filtruoja visas eilutes, kurių visas kiekis jau gautas. Kol tinklelis atidarytas, išvalykite kiekvienos eilutės, kuri turi būti pašalinta iš paskirstymo, žymės langelį **Įtraukti**. 

        > [!IMPORTANT]
        > Kai dirbate su tinkleliu **Pasirinkti eilutes, kurias reikia pašalinti iš paskirstymo**, įsitikinkite, kad tinklelis lieka atidarytas jums pasirinkus **Paskirstyti**. Jei prieš pasirinkdami **Paskirstyti** tinklelį uždarysite, tinklelio nustatymai bus prarasti. Todėl išlaidos bus paskirstytos pagal jūsų anksčiau apibrėžtus kriterijus.

1. Pasirinkite **Paskirstyti**, norėdami pritaikyti jūsų nustatymus ir uždaryti dialogo langą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]