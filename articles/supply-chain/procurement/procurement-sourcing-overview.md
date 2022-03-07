---
title: Įsigijimo ir šaltinio pasirinkimo apžvalga
description: Šiame straipsnyje apžvelgiamos modulyje Įsigijimas ir šaltinio pasirinkimas prieinamos funkcijos.
author: Henrikan
ms.date: 05/06/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "58021"
- intro-internal
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7be7696716e887a7fa4ea4af234db20c6e161b5
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984225"
---
# <a name="procurement-and-sourcing-overview"></a>Įsigijimo ir šaltinio pasirinkimo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamos modulyje Įsigijimas ir šaltinio pasirinkimas prieinamos funkcijos.

Įsigijimo ir šaltinio parinkimo procesas apima visus veiksmus nuo produktų ir paslaugų poreikio nustatymo iki produktų įsigijimo, gavimo, SF išrašymo ir mokėjimo apdorojimo su tiekėjais. Įsigijimo procesus galima konfigūruoti pagal konkrečius verslo poreikius, apibrėžiant pirkimo strategijas ir darbo eigas.

## <a name="identifying-a-need-for-product-and-services"></a>Produktų ir paslaugų poreikio nustatymas

Produktų ar paslaugų poreikį gali lemti *paraiškos*, pvz., kai darbuotojui reikia produkto. Gali būti nustatyti *Produktų katalogai*, kad jiems padėtų pasirinkti galimus produktus, arba gali būti teikiamos produktų, kurių kataloge dar nėra, užklausos, tokiu būdu leidžiant padaliniui apsvarstyti produkto tiekimo galimybes.  

*Išlaidų limitai* gali būti naudojami paraiškos išlaidoms apriboti, o *pirkimo darbo eiga* suteikia galimybę prieš užsakymo vykdymą reikalauti patvirtinimo. Taip pat galima nurodyti biudžeto lėšų paskirstymą, jei reikia.  

Įsigijimo padalinys identifikuoja reikiamų produktų ir paslaugų tiekėjus, o tai gali apimti *pasiūlymo patvirtinimo* siuntimą keliems potencialiems tiekėjams. Galima bendrai naudoti prašomo produkto specifikacijas ir tiekėjai gali jas matyti bei įvertinti, ar jie gali pristatyti produktą, atsižvelgdami į tas specifikacijas. Tiekėjai pateikia savo pasiūlymus, kuriuos įsigijimo padalinys tada peržiūri, o tada pasirenkamas tiekėjas, iš kurio norima įsigyti.  

Pirkimo užsakymuose yra galimybė *pirkimo užklausą* tiekėjui siųsti kaip išsamesnio pirkimo pasiūlymo proceso alternatyvą. Pirkimo užklausą galima naudoti siekiant nustatyti sąlygas, pvz., kainas, nuolaidas ir užsakymo pristatymo datą. Jei nustatyta, kad tiekėjai gali naudoti portalą **Tiekėjas**, pirkimo užklausos funkcija išjungta. Užsakymas yra bendrai naudojamas portale **Tiekėjas**, todėl išsiuntus *patvirtinimo užklausą* tiekėjas gali tiesiogiai užsakymą patvirtinti.  

*Tiekėjų katalogai* gali būti naudojami informacijai apie produktų asortimentą, kurį tiekėjai gali teikti, surinkti. Tiekėjai gali publikuoti savo katalogą, todėl katalogą naujinti lengviau. Prie produkto galima pridėti *patvirtintų tiekėjų sąrašą*, kuris atidarant naujus pirkimo užsakymus padėtų pasirinkti tiekėjus ir neleistų naudoti nepageidaujamų tiekėjų.

## <a name="procurement"></a>Įsigijimas

*Pirkimo užsakymus* galima kurti keliais skirtingais būdais:

- Kaip bendrojo planavimo, kurį naudojant nurodytas poreikis pirkimui, rezultatas. Naudojant šį procesą sukuriami suplanuoti pirkimo užsakymai, o kai jie išleidžiami, sukuriami pirkimo užsakymai.
- apdorojant pirkimo paraiškas, kurios lemia įsigijimą;
- apdorojant pirkimo sutartis, kai pirkimo užsakymai kuriami kaip iš sutarčių išleisti užsakymai. Tai būdinga tada, kai bendrieji užsakymai sudaromi naudojant pirkimo sutartis;
- neautomatiniu būdu, kai sukurtas pirkimo užsakymas nėra pagrįstas kitu dokumentu.

Pirkimo užsakymai, sukonfigūruoti naudojant *pirkimo patvirtinimo darbo eigas*, turi būti patvirtinti prieš juos užregistruojant kaip patvirtintus, o tai reikia atlikti norint tęsti užsakymo apdorojimą.

Pirkimo užsakymai yra *patvirtinti* siekiant nustatyti, kad su tiekėju buvo sudaryta sutartis. Tada pirkimo užsakymas bus padorojamas palaipsniui keliais etapais, kol galiausiai bus išrašyta jo SF arba jis bus atšauktas.  

Kai kuriate pirkimo užsakymą, daug laukų yra užpildomi tiekėjo numatytosiomis reikšmėmis, kurios įrašytos puslapyje **Tiekėjai**. Todėl pardavimo užsakyme jums reikia užpildyti ribotą skaičių laukų, nors numatytųjų reikšmių galite ir nepaisyti.

### <a name="prices-and-discounts"></a>Kainos ir nuolaidos

Kainos ir nuolaidos apima informaciją apie kainas, nuolaidas ir siūlomas grąžinimo sąlygas. Kainos ir nuolaidos gali būti apibrėžtos kaip *prekybos sutartis*. Prekybos sutartys atitinka tiekėjo kainoraščius su kainomis arba nuolaidomis ir joms taikomas konkretus galiojimo datų rinkinys. Dėl kainų ir nuolaidų galima derėtis ir jas apibrėžti naudojant *pirkimo sutartis* su sąlygomis, pavyzdžiui, įsipareigojimus nupirkti tam tikrą kiekį arba už tam tikrą pinigų sumą kaip išankstines derybų sąlygas. *Grąžinimo sutartys* gali būti kuriamos su tiekėjais, kai įsigyjant konkrečių produktų ar produktų grupių gali būti vykdomas grąžinimas iš tiekėjo, priklausomai nuo pirkimo sumos arba kiekio.

### <a name="delivery-options"></a>Pristatymo parinktys

Galima naudoti įvairias su pirkimo užsakymu susieto pristatymo proceso parinktis. Užsakytus produktus galima skaidyti į *pristatymo* grafikus, kai dalį užsakyto kiekio gali būti planuojama pristatyti skirtingu laiku. Pristatymas taip pat galia apimti pardavimo užsakymo inicijuojamą *tiesioginį pristatymą*; pardavimo užsakyme generuojamas važtaraštis tuo pat metu, kai pardavimo užsakyme registruojamas produkto gavimo kvitas. Pirkimo užsakymai taip pat gali būti *vidinės įmonės užsakymų* grandinės dalis, dar vadinama vidinės įmonės pirkimo užsakymais, kai produktai yra užsakomi iš atitinkamo vidinės įmonės pardavimo užsakymo. Šiuo atveju kai kurie abiejų susijusių vidinės įmonės užsakymų veiksmai yra atliekami automatiškai.

### <a name="supplementary-items"></a>Papildomos prekės

Galima nustatyti, kad į produktus būtų įtrauktos *papildomos prekės*. Taip galima siūlyti produktus, kurie yra susiję su užsakomu produktu. Papildomi produktai gali būti privalomi arba pasirenkami. Kai kuriais atvejais papildomos prekės gali būti įtrauktos kaip nemokami produktai, kai įmonė perka kitų produktų.

### <a name="purchase-order-charges"></a>Pirkimo užsakymo mokesčiai

Išlaidos gali būti priskirtos pirkimo užsakymui. Tai gali įvykti automatiškai, nustatant automatines išlaidas, arba įtraukiant išlaidas neautomatiniu būdu. Išlaidos gali būti priskirtos užsakymui antraštės lygyje arba užsakymo eilutės lygyje. Galima naudoti kelis išlaidų apskaitos nustatymo būdus. Pavyzdžiui, galite nustatyti mokestį taikyti kaip produkto kainą. Tokiu atveju, prieš patvirtinant užsakymą, išlaidos turi būti priskirtos užsakymo eilutės lygyje. Yra galimybė lengviau išlaidas paskirstyti iš užsakymo antraštės į eilutes.

## <a name="product-receipt-and-invoicing"></a>Produkto gavimo kvitas ir SF išrašymas

Paprastai pirkimo užsakymų, apimančių faktinius produktus, *gavimo registracija* atliekama sandėlyje, o po to užregistruojamas užsakymo *produkto gavimo kvitas*. Pirkimo užsakymus, kurių produktai atitinka paraiškas, galima sukonfigūruoti taip, kad produktų reikalaujantis darbuotojas taip pat turėtų pateikti *gavimo patvirtinimą*.  

Kai kurie pirkimo užsakymai apima produktus, kurie yra paslaugos arba kiti nefiziniai produktai, už kuriuos sandėliui kvito pateikti nereikia. Tokių užsakymų produktus galima kurti kaip paslaugas arba galima tiesiogiai pirkimo užsakyme naudoti *įsigijimo kategorijas*. Tokių užsakymų produkto gavimo kvito apskaita kartais yra praleidžiama ir užsakymo SF yra išrašoma tiesiogiai arba vykdoma produkto gavimo kvito registracija neatliekant išankstinės gavimo registracijos.  

Produktų gavimas gali lemti automatinį konkretaus tikslo suvartojimą. Tai apima netiesioginį suvartojimą ir tiesioginį pristatymą, į projektą orientuotą suvartojimą arba produkto kaip ilgalaikio turto apskaitą.  

Iš tiekėjo gavus *tiekėjo SF*, pirmiausia ją galima įrašyti į *SF registrą*, nepriklausomai nuo pirkimo užsakymo, o vėliau pagal pirkimo užsakymą patvirtinti kaip įrašą. Tiekėjo SF su pirkimo užsakymu registravimas apima produkto gavimo kvito ir SF gretinimą.  

*Apskaitos paskirstymus* gali būti nustatyti pirkimo užsakyme, siekiant nurodyti, kaip vykdyti DK apskaitą, ir jie taip pat gali nurodyti, kaip gaunamas biudžeto lėšų paskirstymas, kai jis yra įtrauktas į jūsų konfigūraciją.  

Pirkimo užsakymai, kurių SF išrašytos, mokėtinų sumų įsipareigojimą įrašo į tiekėjo sąskaitą, kurioje galima apdoroti *tiekėjo mokėjimą*.

## <a name="vendor-performance"></a>Tiekėjo darbo našumas

Pirkimo veikla ir peržiūra yra palaikoma naudojant *įsigijimo ir mokėtinų sumų ataskaitas*, kurios apima išlaidų analizę ir tiekėjo efektyvumo analizę.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]