---
title: Atspausdinkite iš naujo ir panaikinkite bangos žymes
description: Šioje temoje paaiškinama, kaip panaikinti ir iš naujo atspausdinti bangos žymes.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: article
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 0efa9400a3bf29e4e0dd56d9138cf8c3825556c7
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/27/2020
ms.locfileid: "4434036"
---
# <a name="reprint-and-void-wave-labels"></a>Atspausdinkite iš naujo ir panaikinkite bangos žymes

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip valdyti žymes, kurios buvo sukurtos bangos apdorojimo metu. (Išsamiam aprašui ir konfigūravimo instrukcijoms, žr. [Konfigūruoti bangos žymės spausdinimą](../warehousing/configure-wave-label-printing.md).)

Galite atspausdinti bangos žymes bet kuriuo metu. Pavyzdžiui, galite atspausdinti vieną žymę, jei ji buvo pamesta ar pažeista. Kitu atveju, sandėlio darbuotojas ar vadovas gali atspausdinti visą etikečių ritinį, jei skaičiai ir (arba) visos serijos bangos etikečių skaičius ir sudėtis pasikeitę (pavyzdžiui, dėl inventoriaus trūkumo ar kitų priežasčių). Dažnai, net jei pasikeitė tik dėžių skaičius, visas ritinys turi būti perspausdintas tam, kad išsaugotumėte bendrą tikslų kiekvienos žymės skaičių „Dėžių X iš Y“ skyriuje.

Bangos etikečių naujo atspausdinimo savybė palaiko šias funkcijas:

- Etikečių naujas spausdinimas tiek sandėlio programoje, tiek ir praturtintame kliente.
- Naujas etikečių spausdinimas ir jų panaikinimas tuo pačiu metu. (Galimybė panaikinti žymes yra galima trumpo paėmimo scenarijuose.)
- Išvalykite bangos žymės istoriją.

Šiame skyriuje pateikiamas scenarijų rinkinys, kuris parodo, skirtingais pavyzdžiai, kaip dirbti su bangos žymės naujo spausdinimo savybe.

> [!IMPORTANT]
> Tam, kad dirbtumėte su scenarijais, kurie pateikti šiame skyriuje, privalote pirmiausia įjungti ir sukonfigūruoti reikiamą bangos spausdinimo savybę, kaip aprašyta [Bangos žymės spausdinimo konfigūravimas](../warehousing/configure-wave-label-printing.md). Keletas šios temos scenarijų taip pat reikalauja, kad jūs pirmiausia dirbtumėte su temos scenarijais sukurdami būtinųjų sąlygų pavyzdžio duomenis.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Scenarijus 1: Iš naujo spausdinkite žymes iš kliento žiniatinklio

Galite peržiūrėti ir iš naujo atspausdinti bangos žymes tolesniuose puslapiuose. Veiksmų juostoje kiekviename puslapyje, **Siuntimai** skirtuke, **Susijusi informacija** grupėje, pasirinkite **Bangos žymės**.

- Visi siuntimai \> Siuntimo informacija
- Visi krovimai \> Krovimo informacija
- Visos bangos
- Bangos žymės
- Bangos žymos retrospektyva

Bangos žymės naujam spausdinimui žiniatinklio kliente, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangą, iš kurios norite atspausdinti žymę.
1. Veiksmų juostoje, **Bangos** skirtuke, **Spausdinimo** grupėje, pasirinkite **Bangos žymės**.
1. Atlikite vieną ar abu žingsnius:

    - Žymės naujam spausdinimui, pasirinkite spausdintuvą **Spausdintuvo pavadinimo** laukelyje. (Palikite šį laukelį tuščią, jei tik norite atnaujinti bangos žymės informaciją be naujo jos atspausdinimo.)
    - Žymės atnaujinimui, pasirinkite **Atnaujinti bangos žymės informaciją** žymimą laukelį. (Palikite tuščią šį žymimą laukelį, jei tik norite iš naujo atspausdinti ankstenę žymę.)

    > [!NOTE]
    > Kas kartą, kai bangos žymė yra atspausdinama ar spausdinama iš naujo, jos duomenys yra konvertuojami per atitinkamą bangos žymės planą ir rezervuotos vietos yra pakeičiamos realiomis vertėmis. Pasirodžiusi juosta yra laikoma kaip įrašas bangos žymės istorijoje. **Atnaujinti bangos žymės informaciją** žymimas laukelis yra išvalytas, laikomi „Zebra Programming Language“ (ZPL) duomenys yra naudojami žymės naujo spausdinimo metu. Jei **Bangos žymės informacijos atnaujinimo** žymimas laukelis yra pasirinktas, naujoji juosta yra sukuriama. Esančios bangos žymės taip pat yra perskaičiuojamos ir per didelis jų kiekis (pavyzdžiui, jei susijės su darbo eilutemės, kurios buvo atšauktos ar pakeistos) yra pažymimos kaip **Panaikintos** ir atspausdintos iš naujo.

1. Pasirinkite **OK** pasirinkimo patvirtinimui.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Scenarijus 2: Iš naujo spausdinkite etiketes iš sandėlio programos

Šis scenarijus dažniausiai pritaikomas, jei žyms ritinys buvo prarastas ar pažeistas. Jis pateikia pavyzdį, kuris parodo, kaip nustatyti mobilaus prietaiso meniu elementus, leidžiančius darbuotojas iš naujo atspausdinti vieną ar daugiau žymių. Tuomet jis rodo, kaip naudoti minėtus naujus meniu elementus dirbant su mobiliu prietaisu.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Nustatykite reikiamus meniu elementus ir meniu mobiliame prietaise

Prieš tai, kai darbuotojai gali atspausdinti iš naujo žymes mobiliame prietaise, privalote nustatyti meniu elementus tam, kad ši funkcija būtų įjungta ir tuomet įtraukti minėtus elementus į sandėlio programos meniu.

#### <a name="create-new-mobile-device-menu-items"></a>Sukurkite naujus mobilaus prietaiso meniu elementus

Atlikite šiuos žingsnius tam, kad sukurtumėte naują meniu elementų kolekciją žymių naujam atspausdinimui iš sandėlio programos.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sukurkite meniu elementą ir nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Atspausdinti iš naujo vieną bangos žymę*
    - **Pavadinimas:** *Atspausdinti iš naujo vieną bangos žymę*
    - **Režimas:** *Netiesioginis*
    - **Veiksmų kodas:** *Atspausdinti iš naujo vieną bangos žymę*

1. Sukurkite antrą meniu elementą ir nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Atspausdinti iš naujo žymes (elementą)*
    - **Pavadinimas:** *Atspausdinti iš naujo bangos žymes (elementą)*
    - **Režimas:** *Netiesioginis*
    - **Veiksmų kodas:** *Atspausdinti iš naujo keletą bangos žymių*
    - **Rodyti darbo sąrašo grupių filtrą:** *Taip*
    - **Sistemos grupavimo laukas:** *Siuntimo identifikavimo kodas*
    - **Sistemos grupavimo žymę:** *Siuntimo identifikavimo kodas*
    - **Spausdinimo režimas:** *Produktas*

1. Veiksmų juostoje pasirinkite **Lauko sąrašas** tam, kad atidarytumėte puslapį, kuriame galite pasirinkti rodomus laukelius, padedančius darbuotojams nustatyti tinkamą žymės ritinį.
1. Galite parodyti ne daugiau kaip septynis laukelius. Naudokite iškrentančius sąrašas tam, kad pasirinktumėte lauką rodomą kiekvienoje esančioje padėtyje. Palikite visus jums nereikalingus laukelius tuščius. 

    Toliau pateikiamas pavyzdys.

    - **Rodyti laukelį:** *Žymės elemento identifikavimo kodas*
    - **Rodyti laukelį: 2** *Žymės elemento pavadinimas*
    - **Rodyti laukelį: 3** *Inventoriaus kiekis*
    - **Rodyti laukelį: 4** *Žymės elemento padalinio identifikavimo kodas*

1. Uždarykite puslapį.
1. Sukurkite trečią meniu elementą ir nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Atspausdinti iš naujo žymes (E-skaičių)*
    - **Pavadinimas:** *Atspausdinti iš naujo bangos žymes (e-skaičių)*
    - **Režimas:** *Netiesioginis**
    - **Veiksmų kodas:** *Atspausdinti iš naujo keletą bangos žymių*
    - **Rodyti darbo sąrašo grupių filtrą:** *Taip*
    - **Sistemos grupavimo laukas:** *Siuntimo identifikavimo kodas*
    - **Sistemos grupavimo žymę:** *Siuntimo identifikavimo kodas*
    - **Spausdinimo režimas:** *E-žymėjimas*

1. Veiksmų juostoje pasirinkite **Laukelio sąrašas** ir tuomet naudokite iškrentantį meniu tam, kad pasirinktumėte laukelius, kurie bus rodomi padedant darbuotojams nustatyti tinkamą žymės ritinį (pavyzdžiui *Žymės elemento identifikavimo kodas*, *Žymės elemento pavadinimas*, *Inventoriaus kiekis*, *Žymės padalinio identifikavimo kodas* ir *Žymių skaičius*).
1. Uždarykite puslapį.
1. Sukurkite ketvirtą meniu elementą ir nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Atspausdinti iš naujo žymes (pagal paskutinį)*
    - **Pavadinimas:** *Atspausdinti iš naujo bangos žymes (pagal paskutinį)*
    - **Režimas:** *Netiesioginis*
    - **Veiksmų kodas:** *Atspausdinti iš naujo keletą bangos žymių*
    - **Rodyti darbo sąrašo grupių filtrą:** *Taip*
    - **Sistemos grupavimo laukas:** *Siuntimo identifikavimo kodas*
    - **Sistemos grupavimo žymę:** *Siuntimo identifikavimo kodas*
    - **Spausdinimo režimas:** *Paskutinės prekės bangos žymės identifikavimo numeris*

1. Veiksmų juostoje pasirinkite **Laukelio sąrašas** ir tuomet naudokite iškrentantį meniu tam, kad pasirinktumėte laukelius, kurie bus rodomi padedant darbuotojams nustatyti tinkamą žymės ritinį (pavyzdžiui *Žymės elemento identifikavimo kodas*, *Žymės elemento pavadinimas*, *Inventoriaus kiekis*, *Žymės padalinio identifikavimo kodas* ir *Žymių skaičius*).
1. Uždarykite puslapį.

#### <a name="set-up-the-mobile-device-menu"></a>Nustatykite mobilaus prietaiso meniu

Atlikite šiuos žingsnius tam, kad įtrauktumėte naujus meniu elementus į sandėlio programos meniu.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Pasirinkite esasntį **Siunčiama** meniu.
1. Kairiajame sąraše suraskite naujo spausdinimo meniu elementus, kuriuos kątik sukūrėte ir tuomet naudokite dešinės rodyklės mygtuką tam, kad įtrauktumėte juos į sąrašą dešinėje.
1. Uždarykite puslapį.

### <a name="use-cases"></a>Atvejų naudojimas

Naudokite atvejus, kurie pateikti šiame dokumente kaip pavyzdžiui, rodančius kaip naudotie įvairius mobilaus prietaiso meniu elementus, kuriuos nustatėte įgalindami darbuotojus atspausdinti bangos žymes.

Prieš pradėdami dirbti su šiais naudojamais atvejais šios būtinosios sąlygos turi būti sudarytos:

- Demo duomenys turi būti įdiegti ir privalote pasirinkti **USMF** juridinį asmenį.
- Bangos žymės spausdinimas turi būti sukonfigūruotas ir keletas žymių turi būti sukurta kaip aprašyta [Konfigūruoti bangos žymės spausdinimą](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Naudokite atvejį 2.1: Viena bangos žymė yra įbrėžta ir turi būti atspausdinta iš naujo.

1. Prisijunkite prie sandėlio programos kaip vartotojas, kuris turi prieigą prie sandėlio *62*. (Standartiniuose demonstracijos duomenyse galite prisijungti nauudodamas vartotojo identifikavimo kodą *62* ir slaptažodį *1*.)
1. Eikite į **Siunčiamas \> Atspausdinti vieną bangos žymę**.
1. Įveskite ir nuskaitykite bangos žymės identifikavimo kodą.
1. Pasirinkite spausdintuvą, kuriame spausdinsite dar kartą.
1. Pasirinkite **OK** veiksmo patvirtinimui.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Naudojimo atvejis 2.2: Keletas žymių to paties elemento dėžėms buvo pažeistos ir turi būti atspausdintos iš naujo. Visos žymės turi produkto brūkšninį kodą, tačiau jokio e-numerio ar SSCC numerio.

1. Prisijunkite prie sandėlio programos kaip vartotojas, kuris gali prieiti prie sandėlio *62*. (Standartiniuose demonstracijos duomenyse galite prisijungti nauudodamas vartotojo identifikavimo kodą *62* ir slaptažodį *1*.)
1. Eikite į **Siunčiamas \> Atspausdinti iš naujo žymes (elementą)**.
1. Įveskite ar nuskaitykite siuntimo identifikavimo kodą.
1. Pasirinkite pavadinimą, kuris turi teisingą žymės ritinį jo atspausdinimui iš naujo.
1. Nuskaitykite produkto brūkšninį kodą iš esančios žymės tam, kad patvirtintumėte pasirinktą teisingą eilutę.
1. Įveskite spausdinamų iš naujo žymių skaičių.
1. Pasirinkite spausdintuvą, kuriame spausdinsite dar kartą.
1. Pasirinkite **OK** veiksmo patvirtinimui.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Naudojimo atvejis 2.3: Keletas žymių dėžėms nebuvo atspausdintos dėl spausdintuvo užsikišimo. Kadangi žymės turi e-numeraciją, galite nustatyti iš naujo spausdinamą dėžės intervalą.

1. Prisijunkite prie sandėlio programos kaip vartotojas, kuris gali prieiti prie sandėlio *62*. (Standartiniuose demonstracijos duomenyse galite prisijungti nauudodamas vartotojo identifikavimo kodą *62* ir slaptažodį *1*.)
1. Eikite į **Siunčiamas \> Atspausdinti iš naujo žymes (e-numeris)**.
1. Įveskite ar nuskaitykite siuntimo identifikavimo kodą.
1. Pasirinkite pavadinimą, kuris turi teisingą žymės ritinį jo atspausdinimui iš naujo.
1. Įveskite pirmą dėžę, kuriai spausdinsite dar kartą žymę.
1. Įveskite paskutinę dėžę, kuriai spausdinsite dar kartą žymę. Kitu atveju, palikite tuščią laukelė tam, kad spausdintumėte iš naujo žymes dėžėms po to, kai bus pasirinkta pirmoji dėžė.
1. Pasirinkite spausdintuvą, kuriame spausdinsite dar kartą.
1. Pasirinkite **OK** veiksmo patvirtinimui.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Naudojimo atvejis 2.4: Keletas žymių dėžėms nebuvo atspausdintos dėl spausdintuvo užsikišimo. Paskutinė prekės žymė turi bangos žymės identifikavimo numerį, kuris atspausdintas kaip brūkšninis kodas.

1. Prisijunkite prie sandėlio programos kaip vartotojas, kuris gali prieiti prie sandėlio *62*. (Standartiniuose demonstracijos duomenyse galite prisijungti nauudodamas vartotojo identifikavimo kodą *62* ir slaptažodį *1*.)
1. Eikite į **Siunčiamas \> Atspausdinti iš naujo žymes (pagal paskutinį)**.
1. Įveskite ar nuskaitykite siuntimo identifikavimo kodą.
1. Pasirinkite pavadinimą, kuris turi teisingą žymės ritinį jo atspausdinimui iš naujo.
1. Įveskite ar nuskaitykite paskutinės prekės bangos žymės bangos žymės identifikavimo numerį. Programa nustato kitą žymę tokia seka, pagal kurią bus atspausdinta pirmosios dėžės žymė.
1. Įveskite paskutinę dėžę, kuriai spausdinsite dar kartą žymę. Kitu atveju, palikite tuščią laukelė tam, kad spausdintumėte iš naujo žymes dėžėms po to, kai bus pasirinkta pirmoji dėžė.
1. Pasirinkite spausdintuvą, kuriame spausdinsite dar kartą.
1. Pasirinkite **OK** veiksmo patvirtinimui.

## <a name="scenario-3-short-pick-and-reprint"></a>Scenarijus 3: Trumpas paėmimas ir atspausdinimas iš naujo

Prieš pradėdami dirbti su šiais naudojamais atvejais šis scenarijus turi būti sudarytas:

- Demo duomenys turi būti įdiegti ir privalote pasirinkti **USMF** juridinį asmenį.
- Bangos žymės spausdinimas turi būti sukonfigūruotas ir keletas žymių turi būti sukurta kaip aprašyta [Konfigūruoti bangos žymės spausdinimą](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Nustatyti darbo išimtis

Darbo išimtys kontroliuojančios trumpo paėmimo elgesį. Atlikite šiuos žingsnius tam, kad nustatytumėte darbo išimtį.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbas \> Darbo išimtys**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Darbo išimties kodas:** *Trumpas paėmimas ir spausdinimas*
    - **išimties tipas:** *Trumpas paėmimas*
    - **Siūlomas bangos žymių naujas atspausdinimas:** *Taip*

### <a name="void-and-reprint-after-a-short-pick"></a>Pašalinimas ir spausdinimas iš naujo po trumpo paėmimo

1. Prisijunkite prie sandėlio programos kaip vartotojas, kuris gali prieiti prie sandėlio *62*. (Standartiniuose demonstracijos duomenyse galite prisijungti nauudodamas vartotojo identifikavimo kodą *62* ir slaptažodį *1*.)
1. Atidarykite proceso srautą prekybos užsakymui, kuris buvo sukurtas, kai bangos žymės buvo pirmą kartą atspausdintos.
1. Pasirinkite **Trumpas paėmimas**.
1. Pasirinkite darbo išimties kodą, kurį sukūrėte šiam scenarijui.
1. Jei pasirinkote tinkamą išimtį, **Panaikinti ir atspausdinti iš naujo** žymimas laukelis turi būti prieinamas. Pasirinkite šį laukelį ir patvirtinkite. Po patvirtinimo, žymės ritinio seką nustato **Žymės kūrėjo identifikavimo kodo** laukelis, kuris yra perskaičiuojamas pagal pakeistą darbo linijos kiekį. Tuomet jis atspausdinamas iš naujo nurodytame spausdintuve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]