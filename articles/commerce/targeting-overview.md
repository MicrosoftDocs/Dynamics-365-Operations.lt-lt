---
title: Įrenginio, rinkos ir geografinės vietos tikslinimas
description: Šiame straipsnyje aprašoma, kaip kurti, redaguoti ir valdyti auditoriją ir tikslinius adresatus svetainės generatoriuje naudojant įrenginio, rinkos ir geografinės Microsoft Dynamics 365 Commerce vietos informaciją.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 90772fd942db30bbf4f65a87b1dca4b2aaacee1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881662"
---
# <a name="device-market-and-geolocation-targeting"></a>Įrenginio, rinkos ir geografinės vietos tikslinimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kurti, redaguoti ir valdyti auditoriją ir tikslinius adresatus svetainės generatoriuje naudojant įrenginio, rinkos ir geografinės Microsoft Dynamics 365 Commerce vietos informaciją.

„Dynamics 365 Commerce“ leidžia pritaikyti jūsų puslapio turinio (žinomo kaip tikslinia *adresatai*) variacijas konkrečioms klientų grupėms (žinomai kaip *auditorijos*) ad būtų padidintas vartotojo įsipareigojimas ir patenkinti. Pirmiausia galite sukurti auditoriją arba tikslinį pasiekti. Tačiau norint, kad tikslinio taikymo patirtis būtų sėkminga, reikia abiejų komponentų.

„Commerce" svetainių generatoriaus auditoriją kuriate ir valdote pagal kliento duomenis, pvz., vietą, įrenginio informaciją, prisijungimo būseną ir kitą dinamiškai išvestą informaciją iš kliento interneto užklausų. Be to, „Commerce" svetainių generatoriaus moduliuose ir fragmentuose galite kurti ir valdyti tikslinius adresatus.

**Atsakomybės atsisakymas:** jūs atsakote už šios funkcijos naudojimas laikantis visų taikomų įstatymų ir taisyklių, įskaitant susijusius su tikslinimu ir profiliu. 

## <a name="audiences"></a>Auditorijos

Auditorija yra vartotojų grupė, o narystę grupėje lemia dinaminių taisyklių rinkinys. Šios taisyklės yra paprasti logikos bandymai, atliekami pagal informaciją, kuri galima kliento užklausose arba kituose galimų segmentų segmentuose. Galite sujungti kelias taisykles naudodami AND/OR operatorius.

"Commerce" čia palaiko pagrindinius segmentus, pvz., įrenginio informaciją, prisijungimo būseną, persiuntimo priemonę ir užklausų eilučių parametrus. Taip pat ji palaiko extensible segmentus per ryšius su trečiųjų šalių teikėjais.

### <a name="basic-segments"></a>Pagrindiniai segmentai

Pagal numatytuosius nustatymus galimi ir įtraukti šie segmentai gali būti įtraukti į auditorijos apibrėžimus:

- **Prisiregistravę** - patikrinkite, ar vartotojas autentifikuotas.
- **Įrenginio platforma**– patikrinti šiuos įrenginio tipus:

    - Mobilusis įrenginys
    - Stalinis kompiuteris
    - Planšetinis kompiuteris
    - Kitas

- **Įrenginio OS** – tikrinti šias operacines sistemas:

    - Windows
    - „Linux“
    - iOS
    - „Android“, Kita

- **Užklausos eilutės parametrai** – patikrinti, ar užklausos URL užklausos eilutės parametre yra rakto verčių pora. Pvz., url `www.fabrikam.com/en-us/request?promo=true` atveju galima įrašyti taisyklę, norint patikrinti, ar akcijos **parametras** turi vertę kaip **teisingą**.
- **Slapukas** – testas, skirtas duomenų užklausai URL nustatytai domeno vertei. Pavyzdžiui, į Fabrikam.com gali būti tinkinimas, kurio pavadinimas **CustomLayout** ir vertė **1**. Slapukais testas tikrina, ar yra sausainis, bet konkrečiai nesukuria. Ankstesniame pavyzdyje "JavaScript" turi turėti anksčiau nustatytą **CustomLayout** sausainį iš kito modulio ar kito verslo proceso.

    > [!NOTE]
    > Įsitikinkite, kad jūsų naudojami sausainiai atitinka taikytinus įstatymus.

- **Persiuntimo priemonė** – jei vartotojas seka saitas į užklausos puslapį, susijęsis yra puslapio, kuriame yra saitas, URL.

### <a name="extensible-segments"></a>Išplėstiniai segmentai

„Commerce" leidžia išplėsti galimų segmentų sąrašą jungiantis prie trečiųjų šalių segmentavimo teikėjų. Segmentavimo teikėjas aprašys galimų segmentų tipus. Norėdami gauti daugiau informacijos apie tai, kaip prisijungti prie geografinio paskirstymo ar segmentavimo teikėjo, žr. [Konfigūruoti ir įgalinti jungtis](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Jei išorinis teikėjas yra įgalintas, jis gali prisijungti prie paslaugos, kuri turi neprognozuojamą našumą. Siekiant užtikrinti geresnį vartotojų patirtį, jei vartotojas prašo puslapio, kuriame yra nukreipimas, ir šis puslapis nurodo auditoriją, kuri tikrina trečiosios šalies segmentų teikėją, rodoma numatytoji puslapio versija.
> - Vartotojas turi sutikti leisti sausainius. Vartotojo naršyklė tada prašo visų segmentų iš atitinkamų teikėjų, o rezultatai pateikiami slaptažodį, kuris grąžinamas vartotojui. Tolesnėse puslapio užklausose ši informacija bus naudojama vartotojui skirtame turinyje. Daugiau informacijos apie atitikimą sausainių atitikimui [žr. Privatumo atitikimas](cookie-compliance.md).

**Atsakomybės atsisakymas**: jei įgalinsite šią funkciją, jūsų duomenys bus bendrai naudojami su jūsų pasirinktomis trečiųjų šalių sistemomis. Jūs kontroliuojate, kokie duomenys, jei yra, suteikiate trečiajai šaliai. Jūs žinote, kad trečiosios šalies duomenų tvarkymo ir atitikties standartai gali skirtis nuo „Microsoft Dynamics 365 Commerce“ standartų. „Microsoft“ yra svarbus jūsų privatumas. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą ir slapukai dėl privatumo](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Auditorijos kūrimas svetainės generatoriuje

Norėdami sukurti naują auditoriją „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Auditorijos**.
1. Pasirinkite **Naujas**.
1. Įveskite auditorijos pavadinimą. Taip pat galite pasirinktinai pridėti žymes ir aprašymą.
1. Pasirinkite **Kurti**, tada **Įtraukti naują taisyklės bloką**. Taisyklės blokas yra taisyklių, kurias sujungia AND sąlygos, rinkinys. Taip pat galite sukurti keletą taisyklės blokų, kurie turi OR sąlygas.
1. Pasirinkite segmentų duomenų šaltinį ir tada nurodykite segmento pavadinimą, operatorių ir vertes. Taisyklių bloke galite kurti ir naikinti daugiau taisyklių arba galite kurti ir naikinti visus taisyklių blokus. Jei reikia, taisyklių blokus galite perkelti aukštyn arba žemyn.

    > [!NOTE]
    > Sąraše gali būti iki 100 verčių, o kiekvienoje sąrašo prekėje gali būti iki 50 simbolių.

1. Jei auditorijos konfigūracija jus tenkina, pasirinkite **Baigti redaguoti**. Tada galėsite pasirinkti **Publikuoti**, kad auditoriją būtų galima naudoti tiesioginėje paskirties svetainėje. Taip pat galite publikuoti auditoriją kartu su tikslu. 

Norėdami redaguoti auditoriją, skirtuke **Auditorija** pasirinkite jo hipersaitą, tada rodomame auditorijos **doroklyje** pasirinkite Redaguoti. Norėdami peržiūrėti tikslinių adresatų ir puslapių, kurie nurodo auditoriją, sąrašą, pasirinkite auditoriją auditorijos sąrašo rodinyje, tada pasirinkite **Peržiūrėti priskyrimus**. Norėdami panaikinti auditoriją auditorijų sąrašo rodinyje arba auditorijos rengyklėje, nepublikuokite jos, jei ji jau publikuota, tada **komandų** juostoje pasirinkite Naikinti.

> [!NOTE]
> Tai svetainės lygio koncepcija "Commerce" svetainės generatoriuje. Tą pačią auditoriją galima bendrai naudoti keliuose tiksliniuose adresatuose.

### <a name="rename-an-audience-in-site-builder"></a>Pervardyti auditoriją svetainės generatoriuje

Norėdami pervardyti esamą "Commerce" svetainės generatoriaus auditoriją, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Auditorijos**.
1. Pasirinkite auditorijos segmento, kurį norite pervardyti, pavadinimą.
1. Norėdami **pradėti redaguoti** auditoriją, pasirinkite Redaguoti.
1. Auditorijos ypatybės srityje pasirinkite rašiklio simbolį, esantį šalia auditorijos pavadinimo.
1. Redaguoti auditorijos pavadinimą pagal poreikį.
1. Pažymėkite žymės langelį, norėdami patvirtinti pavadinimo keitimą.
1. Pasirinkite **Baigti redagavimą**.

## <a name="targets"></a>Tikslai

Tikslas – tai vartotojo patirtis, rodoma vieno ar daugiau pasirinktos auditorijos nariams. Joje gali būti vieno ar daugiau modulių variantų puslapyje ar fragmente. 

Galite apibrėžti tikslinių adresatų planą, kad nurodykite, kiek laiko jie turėtų išlikti aktyvūs. Atkreipkite dėmesį, kad šis veiksmas yra atskiras nuo publikavimo grupės planavimo veiksmo, kuris apibrėžia, kada bus publikuojamas turinio rinkinys. Taip pat galite peržiūrėti savo tikslinius adresatus ir pamatyti, kaip jie atrodys pasirinktos auditorijos nariams. Be to, galite nustatyti prioritetą savo tiksliniams adresatams, kad nurodydami, kuris tikslas turi būti rodomas konflikto atveju.

### <a name="create-a-target"></a>Tikslo kūrimas

Norėdami kurti tikslo kiautą modulio puslapiui „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Kairiojoje naršymo srityje pasirinkite **Puslapiai**. Tada pasirinkti puslapio, kuriame yra norimi nukreipti moduliai, hipersaitą.
1. Norėdami redaguoti puslapį, pasirinkite **Redaguoti**.
1. Paskirties meniu **pasirinkite** Nauja paskirties vieta, kad **sukurtumėte** naują paskirties aplinką. Jei reikia, puslapyje galite sukurti keletą tikslinių adresatų.
1. Įveskite naujos išankstinės parinkties pavadinimą ir savo tikslą ir pasirinkite **Toliau**.
1. Pasirinkite **Įtraukti**, kad būtų įtraukta auditorija, kuri matys tikslinį turinį arba neįtraukti auditorijos. Tada rinkitės **Kitas**.

    > [!NOTE]
    > Auditorijos priskyrimas yra pasirinktinis žingsnis kuriant tikslą. Tačiau prieš publikuodami tikslinį turinį turite įtraukti bent vieną auditoriją, kad užtikrinti, jog tikslinės vartotojų grupės matys numatomą turinį.

1. Apibrėžkite tikslo rodymo laiko langą pasirinkdami laiko juostą, pradžios ir pabaigos datas bei laiką. Galite nustatyti tikslinį dydį taip, kad jis būtų rodomas bet kada lange, arba galite pasirinkti tam tikras dienas ir laiką. Jums pabaigus, pasirinkite **Toliau**.

    > [!NOTE]
    > Jūsų nurodytas laikas ir laiko juosta yra visuotiniai. Jei norite nukreipti skirtingas vietas skirtingu laiku arba skirtingose laiko juostose, turite sukurti skirtingus tikslinius adresatus ir nustatyti norimą kiekvienos vietos grafiką.

1. Peržiūrėkite išsamią informaciją ir, kai viskas atrodo tinkamai, pasirinkite **Sukurti paskirties patirtį** ir tada **Pereiti į paskirties vietos**. Sukurta paskirties vieta. Dabar prie jo galite pridėti modulių.
1. Pasirinkite modulį, kuris bus tikslinis, pasirinkite daugtaškį (**...**), ir tada rinkitės **Įtraukti esamą tikslą**. Kai naudojate pirminį modulį, visi jo antriniai modulis tampa to tikslinio objekto dalimi. Tiksliniai moduliai išryškinti žaliai.
1. Atlikite būtinus tikslinio modulio turinio naujinimus ir pridėkite prie tikslinio modulio daugiau modulių, kaip jums reikia. Tada rinkitės **Įrašyti**, kad įrašytumėte visus pakeitimus.
1. Prieš publikuodami tikslinį sąrašą, būtinai pasirinkite **Peržiūrą** komandų juostoje, kad ją peržiūrėtumėte. Tada galite pasirinkti vieną iš toliau nurodytų parinkčių.

    - **Pagrindinė peržiūra** – pasirinkite šią pasirinktį, norėdami peržiūrėti tik pasirinktą variaciją (numatytąjį puslapį ar tikslinį), be jokių susijusių auditorijų.
    - **Papildoma peržiūra**– pasirinkite šią pasirinktį, jei puslapyje yra keli tiksliniai adresatai ir norite juos peržiūrėti kaip vartotoją, kuris priklauso pasirinktam auditorijų rinkinį, arba konkrečią datą / laiką. Pasirinkite **Pirmyn**, norėdami pasirinkti iš atitinkamos auditorijos sąrašo. Taip pat galite pašalinti filtrą, kurį norite pasirinkti iš visų auditorijų.

1. Jei jus tenkina paskirties vietos konfigūracija, turite publikuoti puslapį, kad paskirties vieta būtų tiesioginė. Jei **norite** kad tiksliniai tikslą būtų galima nedelsiant vykti, pasirinkite Skelbti. Taip pat galite naudoti publikavimo grupę, norėdami planuoti, kada puslapis vyksta. Informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).

Taip pat galite tikslinius fragmentus. Procedūra panaši. Tačiau 1 veiksme pažymite **fragmentus**, o **puslapius** kairiojoje naršymo srityje.

> [!NOTE]
> Kad išvengtumėte neigiamo poveikio jūsų metrikai, galite turėti arba eligiaminius, arba tikslinius adresatus puslapyje arba fragmente. Negalima turėti ir anksumentų, ir tikslinių adresatų.

### <a name="manage-targets"></a>Tvarkyti tikslus

Norėdami redaguoti, dubliuoti arba naikinti tikslinius adresatus, eikite į numatytąjį puslapį ar fragmentą ir atlikite šiuos veiksmus.

1. Išplečiamajame meniu pasirinkite **Tikslas** tada – **Tvarkyti tikslinius adresatus** .
1. Pasirinkite paskirties vietos, jei norite redaguoti, dubliuoti arba panaikinti.
1. Jei tame pačiame modulyje yra keletas tikslinių adresatų arba jei keliuose tiksliniuose adresatuose yra nesuderinamų grafikų, pasirinkite **Nustatyti tikslinius adresatus** pagal prioritetus, kad nurodykite jų rodytiną tvarką. Jei puslapyje arba fragmente pridedate daugiau nei vieną **paskirties vietos adresatą** prioritetų tikslinių adresatų mygtukas taip pat rodomas pranešimų juostoje, kad primintų jums nustatyti uždavinių prioritetus. Jei nenurodytas joks prioritetas, naujausias tikslas pasirenkamas pagal numatytąjį nustatymą.

### <a name="localize-targets"></a>Lokalizuoti tikslinius adresatus

Tiksliniai adresatai puslapiuose ir fragmentuose automatiškai įtraukiami, kai XLIFF failai eksportuojami ir importuojami lokalizavimo tikslais. Tačiau jei kurių nors lokalių nereikia, importuotus lokalizuotus XLIFF failus galite panaikinti jų tikslinius adresatus.

> [!NOTE]
> Tiksliniai adresatai valdomi pagal kanalą ir lokalę. Pakeitimai, kuriuos atliekate vieno kanalo ar vietos tiksliniuose adresatuose, nėra automatiškai perkelti į kitus kanalus ar lokales.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
