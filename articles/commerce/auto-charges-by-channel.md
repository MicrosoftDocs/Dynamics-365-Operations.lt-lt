---
title: Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą
description: Šioje temoje paaiškinama, kaip įgalinti ir konfigūruoti automatines išlaidas pagal kanalą „Microsoft Dynamics 365 Commerce”.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 23d02cf96faf3753303435acc148bf71e487d791
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799922"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą

Šioje temoje paaiškinama, kaip įgalinti ir konfigūruoti automatines išlaidas pagal kanalą „Microsoft Dynamics 365 Commerce”.

## <a name="overview"></a>Peržiūra

Gali būti scenarijų, kai perdirbimo ar kitus mokesčius reikia pritaikyti produktų, kurie parduodami visose arba kai kuriose tam tikros šalies parduotuvėse (pvz., Kalifornijoje), grupei. Funkcija **Įjungti automatinių išlaidų filtravimą pagal kanalą** programoje „Commerce“ leidžia nurodyti automatines išlaidas pagal kanalą (pvz., konkretų fizinį kanalą). Šią funkcija pasiekiama 10.0.10 arba vėlesnės versijos „Dynamics 365 Commerce“.

Norėdami įgalinti ir konfigūruoti automatines išlaidas pagal kanalą, turite atlikti toliau nurodytas užduotis.

- Įjunkite funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą**.
- Sukonfigūruokite organizacijos hierarchijos paskirtį.
- Nustatykite automatines išlaidas pagal kanalą.

> [!NOTE]
> Funkcija **Įjungti automatinių išlaidų filtravimą pagal kanalą** veikia tik tada, jei įjungta išplėstinė automatinių išlaidų funkcija. Informacijos apie tai, kaip įjungti išplėstinę automatinių išlaidų funkciją, žr. [Integruoto kanalo išplėstinės automatinės išlaidos](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Įjunkite funkciją Įjungti automatinių išlaidų filtravimą pagal kanalą.

Norėdami įjungti automatines išlaidas pagal kanalą programoje „Commerce“, atlikite toliau pateiktus veiksmus.

1. Eikite į **Sistemos administratorius \> Darbo sritys \> Funkcijų valdymas**.
1. Skirtuko **Neįjungta** sąraše **Funkcijos pavadinimas** raskite ir pasirinkite **Įjungti automatinių išlaidų filtravimą pagal kanalą**.
1. Apatiniame dešiniajame kampe pasirinkite **Įjungti dabar**. Kai funkcija įjungta, ji bus rodoma skirtuko **Visi** sąraše.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Kairiojoje srityje raskite ir pasirinkite **1110** (**visuotinės konfigūracijos**) užduotį.
1. Veiksmų srityje pasirinkite **Vykdyti dabar**, kad būtų paskirstyti konfigūracijos pakeitimai.

> [!WARNING]
> Jei jau naudojote funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą** ir ją išjungsite, laukas **Mažmeninės prekybos kanalų ryšys** dalyje **Automatinės išlaidos** nebebus rodomas ir neteksite visų esamų konfigūracijų. Jei **Mažmeninės prekybos kanalų ryšys** konfigūracijų pašalinimas sukels automatinių išlaidų taisyklių dubliavimą, funkcijos išjungti nepavyks. Prieš išjungdami funkciją įsitikinkite, kad peržiūrėjote visas automatinių išlaidų taisykles ir atlikote reikalingus pakeitimus.

## <a name="configure-the-organization-hierarchy-purpose"></a>Organizacijos hierarchijos paskirties konfigūravimas

Siekiant valdyti automatinių išlaidų hierarchiją pagal kanalą, sukurta nauja organizacijos hierarchijos paskirtis, kurios pavadinimas **Mažmeninės prekybos automatinės išlaidos**.

Norėdami priskirti numatytąją hierarchiją organizacijos hierarchijos paskirčiai programoje „Commerce“, atlikite toliau pateiktus veiksmus.
        
1. Eikite į **Organizacijos administravimas \> Organizacijos \> Organizacijos hierarchijos paskirtis**.
1. Kairiojoje srityje pasirinkite **Mažmeninės prekybos automatinės išlaidos**.
1. Dalyje **Priskirtos hierarchijos** pasirinkite **Įtraukti**.
1. Dialogo lange **Organizacijų hierarchijos** pasirinkite organizacijos hierarchiją (pvz., **Mažmeninės prekybos parduotuvės pagal regioną**) ir pasirinkite **Gerai**.
1. Dalyje **Priskirtos hierarchijos** pasirinkite **Nustatyti kaip numatytąjį**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Kairiojoje srityje raskite ir pasirinkite **1040** (**produktų**) užduotį.
1. Veiksmų srityje pasirinkite **Vykdyti dabar**.
1. Pakartokite ankstesnius du veiksmus, norėdami paleisti **1070** (**kanalo konfigūraciją**) ir **1110** (**visuotinės konfigūracijos**) užduotis.

![Mažmeninės prekybos automatinių išlaidų organizacijos hierarchijos paskirties konfigūracija](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Automatines išlaidų nustatymas pagal kanalą

Įjungus funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą** ir sukonfigūravus **Mažmeninės prekybos automatinių išlaidų** organizacijos hierarchijos paskirtį, automatinės išlaidos pagal kanalą gali būti nurodytos arba užsakymo antraštės lygiu, arba užsakymo eilutės lygiu.

Norėdami nustatyti automatines išlaidas pagal kanalą programoje „Commerce“, atlikite toliau pateiktus veiksmus.

1. Pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Automatinės išlaidos**.
1. Kairiosios srities lauke **Lygis** pasirinkite **Antraštė** arba **Eilutė**, atsižvelgdami į savo verslo poreikius.
1. Lauke **Mažmeninės prekybos kanalo kodas** pasirinkite reikiamą kanalo kodą (pvz., **Lentelė** arba **Grupė**). Jei naudojamas numatytasis parametras **Visi**, išlaidų taisyklės taikomos visiems kanalams.

    - Jei pasirinksite **Grupė**, įsitikinkite, kad mažmeninės prekybos kanalo išlaidų grupė yra sukurta **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Išlaidos \> Mažmeninės prekybos kanalo išlaidų grupės**.
    - Jei pasirinksite **Lentelė**, lauke **Mažmeninės prekybos kanalų ryšys** galite pasirinkti konkretų kanalą, pvz., **San Franciskas**.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Kairiojoje srityje raskite ir pasirinkite **1040** (**produktų**) užduotį.
1. Veiksmų srityje pasirinkite **Vykdyti dabar**.
1. Pakartokite ankstesnius du veiksmus, norėdami paleisti **1070** (**kanalo konfigūraciją**) ir **1110** (**visuotinės konfigūracijos**) užduotis.
    
![Automatinės išlaidos, nustatytos pagal kanalą](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Toliau pateiktame pavyzdyje aprašomi veiksmai, kurių reikia produktui sukonfigūruoti, kad būtų taikomi perdirbimo mokesčiai, kai produktas parduodamas naudojant San Francisko fizinį kanalą. Taip pat pavyzdyje rodoma, kaip automatinės išlaidos bus rodomos „Commerce” elektroninio kasos aparato (EKA) programoje.

Organizacija apibrėžia išlaidų kodą, kurio pavadinimas **PERDIRBIMAS**, kaip parodyta toliau pateiktoje iliustracijoje.

![Išlaidų kodas PERDIRBIMAS](media/Auto-charges-charge-code.png)

Sukuriamos automatinės išlaidos eilutės lygiu. Jam būdinga toliau pateikta konfigūracija.

- Laukas **Sąskaitos kodas** nustatomas į **Visi**.
- Laukas **Prekės kodas** nustatomas į **Lentelė**.
- Laukas **Prekės ryšys** nustatomas į produkto ID **91001**.
- Laukas **Pristatymo kodo režimas** nustatomas į **Visi**.
- Laukas **Mažmeninės prekybos kanalo kodas** nustatomas į **Lentelė**.
- Laukas **Mažmeninės prekybos kanalo ryšys** nustatomas į **San Francisko** parduotuvę.

Sukuriama automatinių išlaidų eilutė. Jam būdinga toliau pateikta konfigūracija.

- Laukas **Valiuta** nustatytas į **USD**.
- Laukas **Išlaidų kodas** nustatomas į **PERDIRBIMAS**.
- Laukas **Kategorija** nustatytas į **Fiksuotas**.
- Laukas **Išlaidos** nustatytas į **6,25 USD**.

![Automatinių išlaidų eilutės lygiu ir automatinių išlaidų eilutės konfigūracija](media/Auto-charges-recyclingfee-line-fee.png)

EKA programos **San Francisko** parduotuvės kanale sukuriamas pardavimo užsakymas. Eilutėje **Išlaidos** nurodytas **6,25 USD** perdirbimo mokestis.

EKA programoje pasirinkę **Operacijų parinktys \> Išlaidos \> Valdyti išlaidas** galite peržiūrėti perdirbimo mokesčio išlaidų kodą ir aprašymą.

![Perdirbimo mokestis EKA programoje](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Integruoto kanalo išplėstinės automatinės išlaidos](omni-auto-charges.md)

[Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]