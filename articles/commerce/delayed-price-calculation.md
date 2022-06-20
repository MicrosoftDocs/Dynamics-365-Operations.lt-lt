---
title: Tikslaus kainos ir nuolaidos skaičiavimo atidėjimas našumo padidinimui
description: Šiame straipsnyje aprašomos atidėtos kainos skaičiavimo galimybės, kurias galima naudoti point Microsoft Dynamics 365 Commerce of sale (EKA) ir skambučių centre.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6926c288a91dbe66b6ffc2e6c06f866d3ebd7652
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845902"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Tikslaus kainos ir nuolaidos skaičiavimo atidėjimas našumo padidinimui

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomos atidėtos kainos skaičiavimo galimybės, kurias galima naudoti point Microsoft Dynamics 365 Commerce of sale (EKA) ir skambučių centre.

„Dynamics 365 Commerce” palaiko kelių eilučių nuolaidų, kurios taikomos sujungiant kelias pardavimo užsakymo arba pardavimo pasiūlymo eilutes, kūrimą. Šios nuolaidos apima nuolaidas prekių rinkiniui, ribinę vertę ir kiekio nuolaidas.

Kai tik į užsakymą įtraukiama nauja eilutė, „Commerce” kainų nustatymo mechanizmas įvertina visą krepšelį ir nustato, ar galima taikyti šias kelių eilučių nuolaidas. Dėl šio perskaičiavimo naujų eilučių pridėjimas gali turėti įtakos našumui didėjant pardavimo užsakymui.

Tačiau „verslas verslui” (B2B) įmonių ir kai kurių „verslas klientui” (B2C) įmonių užsakymų dydžiai dažnai yra milžiniški. Todėl gali ilgai užtrukti, kol kainų nustatymo mechanizmas perskaičiuos kainą kiekvieną kartą pridėjus prekę į krepšelį. Be to, dideliems užsakymams dažnai nėra labai svarbu, kad kiekvieną kartą į krepšelį pridėjus prekę būtų rodoma tiksli kaina ir nuolaida. Svarbu, kad vartotojai galėtų greitai pridėti prekes. Galimybė atidėti tikslų kainų ir nuolaidų skaičiavimą iki tol, kol vartotojas jo nepaprašo arba užsakymas yra užbaigtas, gali smarkiai padidinti našumą. Tai taip pat tai gali sumažinti laiką, reikalingą norint baigti užsakymo pateikimą.

Galimybė atidėti tikslų kainų ir nuolaidų skaičiavimą yra galima EKA jau kurį laiką. Nuo 10.0.22 „Commerce” versijos leidimo, ji taip galima ir skambučių centre.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Įjungti atidėtą kainų ir nuolaidų skaičiavimą, skirtą EKA

Norėdami įjungti atidėtą kainų ir nuolaidų skaičiavimą, skirtą EKA, atlikite šiuos veiksmus.

1. „Commerce” būstinėje eikite į funkcijų šabloną, susietą su faktine parduotuve.
1. Atidarykite „FastTab” **Suma**, įgalinkite **Apskaičiuoti kelių eilučių nuolaidas rankiniu būdu** konfigūraciją.
1. Atidarykite ekranų išdėstymo rengyklę registrams, kuriems turėtų būti įgalintas atidėtas skaičiavimas.
1. Įtraukite operacijos **Skaičiuoti bendrą sumą** mygtuką į norimą mygtuko tinklelį.
1. Paleiskite **„1070”** ir **„1090”** užduotis.

Dabar, kai prekės yra pridėtos prie operacijos, kelių eilučių nuolaidos nėra apskaičiuojamos, nebent kasininkas pasirenka **Skaičiuoti sumą** mygtuką. Pasirinkus **Skaičiuoti sumą** operacijai, jai visada bus skaičiuojamos kelių eilučių nuolaidos. Kasininkui nereikės vėl pasirinkti mygtuko, net jei į krepšelį bus pridėtos papildomos prekės. Sistema neleis kasininkui fiksuoti mokėjimo, kol **Skaičiuoti sumą** nebus pasirinkta.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Įjungti atidėtą kainų ir nuolaidų skaičiavimą, skirtą skambučių centrui

Norėdami įjungti atidėtą kainų ir nuolaidų skaičiavimą, skirtą skambučių centrui, atlikite šiuos veiksmus.

1. „Commerce“ būstinėje eikite į **Darbo sritys \> Funkcijų valdymas**.
1. Įgalinkite **Neleisti neplanuoto kainos skaičiavimo prekybos užsakymui** funkciją. Ši funkcija yra būtina atidėto kainų ir nuolaidų skaičiavimo galimybės sąlyga.

    > [!NOTE]
    > Naujiems diegimams **Neleisti neplanuoto kainos skaičiavimo prekybos užsakymui** funkcija yra įgalinta pagal numatytuosius nustatymus.

1. Eikite į **„Commerce” parametrai \> Kainos ir nuolaidos**.
1. Skyriuje **Įvairūs** įgalinkite **Apskaičiuoti kelių eilučių kainų ir nuolaidų skaičiavimą rankiniu būdu** konfigūraciją.

Dabar, kai skambučių centre yra kuriamas arba redaguojamas pardavimo užsakymas arba pardavimo pasiūlymas, atidedamas tikslus kainos ir nuolaidos skaičiavimas. Kainų nustatymo mechanizmas nagrinės tik tą pardavimo eilutę, kuri yra pridedama ar redaguojama, o visų kitų pardavimo eilučių nepaisys. Grynoji prekės suma apima kainos skaičiavimą ir paprastas nuolaidas (nuolaidos procentą arba atskiros prekės sumą). Tačiau nuolaidos prekių rinkiniui, ribinės vertės ir kiekio nuolaidos nebus taikomos. Skambučių centro vartotojai, kurie nori peržiūrėti tikslią kainą, įskaitant visas nuolaidas, gali pasirinkti vieną iš trijų mygtukų: **Perskaičiuoti**, **Suma** arba **Užbaigti**.

> [!NOTE]
> Skambučių centro užsakymams sistema rodo perspėjimo pranešimą, primenantį vartotojui, kad jis turėtų pasirinkti **Perskaičiuoti**, **Suma** arba **Užbaigti** mygtuką, kad būtų atliktas tikslus kainos ir nuolaidos skaičiavimas. Užsakymams, kuriems **Užbaigti** mygtukas nėra galimas, nėra jokio būdo skambučių centro vartotojui praleisti tikslaus kainos ir nuolaidos skaičiavimo, kadangi jis privalo pasirinkti **Užbaigti** užsakymo fiksavimo užbaigimui. Užsakymams, kuriems **Užbaigti** mygtukas nėra galimas, nėra veiksmo, rodančio užsakymo fiksavimo užbaigimą. Todėl skambučių centro vartotojas yra atsakingas už **Perskaičiuoti** arba **Suma** pasirinkimą prieš užbaigiant užsakymo fiksavimą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
