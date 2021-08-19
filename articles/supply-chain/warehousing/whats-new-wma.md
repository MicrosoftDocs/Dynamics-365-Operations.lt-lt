---
title: Kas nauja ar pasikeitė „Warehouse Management Mobile App” programėlėje
description: Šioje temoje pateikiamos naujos ir pakeistos kiekvienos išleistos „Warehouse Management Mobile App”, skirtos „Microsoft Dynamics 365 Supply Chain Management”, versijos funkcijos.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 43d1381e73d5659bfd6ae6c6d944b7e6918b681a4f89df7ad23abbed5b4a0d3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720089"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Kas nauja ar pasikeitė „Warehouse Management Mobile App” programėlėje

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos naujos kiekvienos išleistos „Warehouse Management Mobile App”, skirtos „Microsoft Dynamics 365 Supply Chain Management”, versijos funkcijos, klaidų taisymai ir žinomos problemos.

## <a name="2070"></a>2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>2.0.7.0 versijos naujos funkcijos, klaidų taisymai ir patobulinimai

- Įtraukta sekcija į **Apie** puslapį, kuriame tikrinama naujausia išleista programos versija.
- Kad būtų lengviau brūkštelėkite ir perbraukite tarp puslapių.
- Pakeitė darbų sąrašo didėjimo/mažėjimo mygtuko piktogramą.
- Sumažino kortelės **Informacija** maržas, kad ji galėtų pritaikyti daugiau informacijos.
- Pritaikė įvairūs našumo patobulinimus, siekiant sumažinti programos išdavimą, kuris laikui bėgant tampa lėtesnis.
- Jei yra daugiau valdiklių nei telpa ekane, dėl to buvo paslinkusi puslapių kaitos programa nebeslinks taip pat, kaip puslapis.
- Nustatykite pirmenybę, kad būtų rodoma paskutinė nuskaityta reikšmė virš užduoties pavadinimo verčių, todėl joms persidengus, užduoties pavadinimas bus sutrumpintas.
- Buvo išspręstos įvairios problemos, dėl kurių sistema nebereagavo.
- Kai kuriomis kalbomis tekstas įvairiose vietose nebeperskiriamas.
- Dabar programa veikia viso ekrano režimu pagal numatytuosius nustatymus.
- Ištaisyta problema, dėl kurios kai kurių įrenginių pagrindiniame puslapyje nuskaitymo gali būti nepaisoma.

### <a name="known-issues-in-version-2070"></a>Žinomos problemos 2.0.7.0 versijoje

- Kai kuriuose įrenginiuose, kai paleidžiate programą arba pradedate užduotį, gausite tokį klaidos pranešimą: "Nepavyksta rasti tinkamo nurodyto dydžio rodinio". Jei matote šį klaidos pranešimą bet kuriame savo įrenginyje, turite toliau naujinti „Warehouse Management“ mobiliąją programą į 2.0.6.0 versiją šiame įrenginyje ir palaukti, kol bus paleista kita programos versija.

## <a name="version-2060"></a>2.0.6.0 versija

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>2.0.6.0 versijos naujos funkcijos, klaidų taisymai ir patobulinimai

Šioje versijoje pristatomos toliau pateiktos naujos funkcijos, klaidų taisymai ir patobulinimai:

- Demonstracinis režimas dabar rodo visas žymas įrenginio kalba.
- Mažiau tikėtina, kad gausite šį klaidos pranešimą: „Nepavyksta rasti tinkamo nurodyto dydžio rodinio.”
- Padidintas minimalus darbo kortelių aukštis (atvejais, kai konfigūruojami trys ar mažiau laukų, kad jie būtų rodomi darbų sąraše).
- Patobulintos paraštės (palaipsniui išnykstančios) informacijos kortelių apačioje.
- Netinkami XML failų simboliai, kurie keičiasi serveryje, dabar yra apdorojami sėkmingai. (Pavyzdžiui, nespausdinamieji simboliai dabar tvarkomi labai sėkmingai ir nesukelia programos nereagavimo.)
- HTTP klaidos (pavyzdžiui, „klaida 503”), kai serverio užklausa pateikta, dabar tvarkomos labai sėkmingai.
- Kai rodoma klaida, automatiškai neberodomas pasirinktinio įvedimo lauko valdiklių parinkčių sąrašas.
- Programa daugiau nenustoja reaguoti dėl vartotojo parametruose pasirinktos ekrano padėties.
- Dabar produktų vaizdai yra rodomi savitarnos aplinkose. Šis pakeitimas taikomas tik mažos skiriamosios gebos versijoms. (Failų valdymo tarnyba nepalaiko viso dydžio vaizdų savitarnos aplinkose.)
- Buvo išspręsta problema, susijusi su nulinio kiekio trumpais paėmimais.
- Programa daugiau nenustoja reaguoti, kai informacijos kortelėje rodomi keli identiški laukai.

### <a name="known-issues-in-version-2060"></a>Žinomos problemos 2.0.6.0 versijoje

Šioje versijoje yra tokios žinomos problemos:

- Programa (ypač darbų sąrašas) laikui bėgant tampa lėtesni.
- **„Windows” versija:** Kai USB ginklas naudojamas nuskaitymui „Windows”, nenuoseklūs rezultatai sukelia nuskaitytų simbolių sumaišymą.

## <a name="version-2050"></a>2.0.5.0 versija

Šioje versijoje pristatomos toliau pateiktos naujos funkcijos, klaidų taisymai ir patobulinimai:

- Ryšio parametrų nustatyme nebeslepiamas kliento slaptasis raktas.
- Dabar galite ilgai paspausti ant bet kokio teksto, kad jį pilnai pamatytumėte.
- Patobulintas klaidos pranešimas, kai trūksta saugojimo teisių.
- Kai kuriems srautams buvo įtrauktos naujos valdiklių sekos.
- Pateikimo mygtukas daugiau neteisingai netampa tinkamas dėl lango dydžio.
- Kai naudojami didesni mygtukų dydžiai, slankikliai gali toliau veikti mažesniuose ekranuose.
- Keturių mygtukų perdanga nebėra nutraukiama.
- Dabar klaviatūra palaiko naikinimo mygtuką.
- Ryškumo problema, kuri galėjo įvykti paspaudus klaviatūrą, buvo išspręsta.
- Buvo išspręstos įvairios demonstracinių duomenų problemos.
- Problema, kuri veikdavo informacijos puslapio skaitinius laukus, buvo ištaisyta.
- Ekrano klaviatūra daugiau nebepradingsta kai kuriuose įrenginiuose.
- Įvairios vartotojo sąsajos (UI) klaidos buvo ištaisytos, pavyzdžiui, klaidos, veikusios fono spalvą ir padėtį.
- Patobulinta rusų kalbos vartotojo sąsaja.
- Buvo išspręstos įvairios problemos, dėl kurių sistema nebereaguodavo.
- Buvo išspręsta problema, susijusi su skaičiuotuvo atidarymu iš naujo.
- **„Android” versija:** Problema, dėl kurios „4.4 Android” nustojo reaguoti į paleistį, buvo ištaisyta.
- **„Android” versija:** Minimalus mastelio keitimas sumažintas iki 50 procentų.

## <a name="version-2040"></a>2.0.4.0 versija

2.0.4.0 versija buvo pirmasis bendrai pasiekiamas „Warehouse Management Mobile App” programėlės leidimas.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>2.0.4.0 versijos naujos funkcijos, klaidų taisymai ir patobulinimai

Šioje versijoje pristatomos naujos funkcijos, klaidų taisymai ir patobulinimai, kurių nebuvo peržiūros versijoje:

- Jei išsamios informacijos kortelėje yra dvi žymos, kurių duomenys vienodi, viena iš žymų yra paslėpta.
- Specialieji simboliai dabar rodomi pagal numatytuosius nustatymus,o jų paslėpimo parinktis buvo pašalinta iš vartotojo parametrų.
- Išjungti pateikimo mygtukai dabar rodomi kaip negalimi kompaktiniame rankiniame rodinyje.
- Keitimas į sekos logiką valdikliams užtikrina sklandesnį mastelio keitimą įrenginiams. Todėl yra mažesnis poreikis koreguoti šriftų arba mygtukų dydį.
- Numatytoji spalvos tema buvo pakeista į *Tamsią*.
- Trūkstama išjungto pateikimo mygtuko piktograma įtraukta į juostos rodinį.
- Pasibaigusio skirtojo laiko išimtys dabar perkels jus į ryšio puslapį, o ne rodys eilutės klaidą.
- Jei negalimas joks pateikimo veiksmas (pavyzdžiui, **GERAI**, **Taip**, **Priimti**, **Įvykdyta** arba **Baigta**), pateikimo mygtukas bus išjungtas.
- Patobulintas programos stabilumas.
- Yra sprendimas saugumo pažeidžiamumui [„CVE-2021-26701”](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **„Windows” versija:** „Windows” problema, kai meniu nereaguoja pakeitus lango dydį, buvo išspręsta.

### <a name="known-issue-in-version-2040"></a>Žinoma problema 2.0.4.0 versijoje

Šioje versijoje yra tokia žinoma problema:

- Šioje versijoje yra problema su įrenginiais, kurie naudoja „Android 4.4”. Naudojant programą su šia „Android” versija, gali kilti problemų.
