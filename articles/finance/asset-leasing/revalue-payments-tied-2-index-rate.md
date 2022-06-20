---
title: Nuomos mokesčių, susietų su indeksuojama palūkanų norma, pervertinimas
description: Šiame straipsnyje aprašomas koregavimas, atliktas išperkant įsipareigojimus naudojimo dešinėje (RUBLI) turtui, kai kintantis nuomos mokėjimas dėl indekso tarifo pakeitimo.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903253"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Nuomos mokesčių, susietų su indeksuojama palūkanų norma, pervertinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas koregavimas, atliktas naudojimo teisės (RUBLI) turto nuomos įsipareigojimui, kai dėl indekso tarifo pakeitimo kinta kintamieji nuomos mokėjimai. Nuomos įsipareigojimas ir naudojimo teise valdomas turtas bus pakoreguoti taip, kad būtų atsižvelgta į naujas mokesčių sumas. Pagal apskaitos standartų kodifikavimas temą Nr. 842 (ASC 842), kuri yra standartas, priimtas JAV bendrai priimamuose apskaitos principuose (US GAAP), tik kintami mokėjimai pasikeičia, kai mokėjimai padidėja arba sumažėja dėl pasikeitusios indekso kainos, išskyrus atvejus, kai grynųjų pinigų srautai papildomi. Šie papildomi pakeitimai gali apimti nuomos sąlygų pokytį, susijusį su palūkanų normomis. Norėdami gauti daugiau informacijos, žr. ASC 842-10-55-225 ir tarptautinio finansinės atskaitomybės standarto Nr. 16 (IFRS 16) 42(b) dalį.

## <a name="adjust-lease-payments"></a>Nuomos mokėjimų koregavimas

Atlikite šiuos veiksmus, kad iš naujo įvertintumėte nuomos mokesčius, susietus su indeksuojama palūkanų norma.

1. Norėdami vykdyti nuomos indekso perkainojimo procesą, eikite **Turto nuoma \> Periodiškai \> Indeksuojamos palūkanų normos perskaičiavimas**.

    Pasirodo puslapis **Indeksuojamos palūkanų normos perskaičiavimas** ir parodomi visi anksčiau atlikti nuomos indeksuojamos palūkanų normos perskaičiavimo procesai. Šiame puslapyje pateikiama informacija apima proceso ID, kuris buvo sugeneruotas iš numeracijos nustatymo, juridinio subjekto, pakoreguotų išperkamosios nuomos knygų skaičiaus, bendrosios atsakomybės koregavimų dėl IFRS 16 nuomos ir visų kintamųjų mokėjimų, kurie buvo pakoreguoti dėl ASC 842 nuomos.

2. Norėdami vykdyti perkainojimą, veiksmų srityje pasirinkite **indeksuojamos palūkanų normos perskaičiavimas**.

    Pasirodo dialogo langas **Indeksuojamos palūkanų normos perskaičiavimo parametrai**. Čia galite filtruoti ir pasirinkti, kurios nuomos, išperkamosios nuomos grupės arba kiti kriterijai turėtų būti naudojami, kai pasirenkate vertę iš naujo. Be to, skirtuke **Vykdyti fone** galima nustatyti indeksuojamos palūkanų normos perskaičiavimo procesą, kad jis būtų vykdomas pakete.

4. Pasirinkite išperkamosios nuomos, kuri turėtų būti įtraukta į foninį apdorojimą, filtrus ir pasirinkite **Gerai**.

    Pasirodo dialogo langas **Indeksuojamos palūkanų normos perskaičiavimo peržiūra** ir rodoma nuoma, kuri bus perskaičiuota. Joje taip pat parodomi turto ir įsipareigojimų koregavimai arba kintamosios mokėjimo korekcijos.

5. Kad nuoma nebūtų perskaičiuojama, pasirinkite nuomą, kurią **reikėtų** perskaičiuoti. Jei nepasirenkate jokios nuomos, visas nuomos sutartis bus perkainota. Kai pabaigsite pasirinkite **Gerai** tam, kad perskaičiuotumėte nuomos mokėjimus.
6. Norėdami peržiūrėti operacijas, kurios buvo sukurtos tam indeksuojamos palūkanų normos perskaičiavimo procesui, pasirinkite proceso ID ir pasirinkite **Operacijos**.

    Pasirodo dialogo langas ir rodoma informacija apie operacijas, kurios buvo sukurtos apdorojant.

> [!NOTE]
> Gali būti perkainota tik tokia nuomos suma, kuri turi perkainojimo datą, kuri yra sistemos datą ar anksčiau. Sistema automatiškai ignoruoja visas nuomos sutartis, kurių perkainojimo data vėlesnė už sistemos datą.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 nuoma – indeksuojamos palūkanų normos perskaičiavimas

Norėdami peržiūrėti nuomos perkainojimo proceso įtaką ASC 842 nuomai, atsidarykite nuomos įmokų grafiką. Puslapyje rodomi tik kintamųjų mokėjimai, kurie buvo atlikti arba po perkainojimo datos, pasikeitė dėl indekso perkainojimo. Amortizavimo ir nusidėvėjimo grafikai nesikeičia. Kai sukuriate SF su kintamu mokėjimu, kintamas mokėjimas debetuojamas į kintamosios įmokos registravimo sąskaitą. Taip pat kintamoji mokėjimo suma pridedama prie kredito įrašo, kuris registruojamas tiesiogiai tiekėjui arba registruojama mokėtinų sumų pažymose, atsižvelgiant į nuomos knygos nustatymą.

Išperkamosios nuomos informacijos puslapyje esančių darbo grafiko eilutės atnaujinamos automatiškai naudojant naują eilutę, kurioje nurodytas naujas indekso koeficientas. Be to, stulpelis nurodo, ar eilutė buvo sukurta neautomatiniu būdu, ar indekso perkainojimo procese.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 nuoma – indeksuojamos palūkanų normos perskaičiavimas

Norėdami peržiūrėti nuomos perkainojimo proceso įtaką IFRS 16 nuomai, atsidarykite koreguotos nuomos informaciją. Buvo atnaujinti laukai **Nuomos laikotarpis** ir **Turto naudingo naudojimo laikas**, siekiant parodyti, kad laikas praėjo nuo pradžios datos arba modifikavimo datos iki perkainojimo datos. Be to, mokėjimo grafiko eilutės atnaujintos, kad atsispindėtų nauji nuomos mokėjimai, naujas indekso koeficientas ir eilutės sukūrimo data.

Galite peržiūrėti naujai sugeneruotą įmokų grafiką, kuris pradedamas skaičiuoti nuo perkainojimo datos, ir rodyti visą atnaujintą apmokėjimo sumą. Taip pat sukurtas naujas nuomos įsipareigojimų amortizavimo grafikas ir turto nusidėvėjimo grafikas, siekiant atsižvelgti į pakoreguotą mokėjimo grafiką.

Žurnalo įrašas automatiškai užregistruoja derinimo žurnalo įrašą, skirtą pakeisti nuomos mokėjimus, susietus su indekso perkainojimu.

> [!NOTE]
> **Jei paskirstymo mokėjimo** **sumos** parinktis įgalinta informacijos apie nuomą puslapio Bendrajame **FastTab**, o susijusi knyga yra IFRS 16, **indekso** perkainojimo procesas automatiškai įtraukia įrašą į mokėjimo sumos išskaidimo dialogo langą. Suma atspindės pakeitimą, kuris atliktas mokėjimui dėl indekso perkainojimo. Įrašas bus pažymėtas kaip Naudojamas **IRFS 16 indekso perkainojimui**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
