---
title: Sukonfigūruokite „BOPIS“ esantį „Dynamics 365 Commerce“ vertinimo aplinkoje
description: Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje (BOPIS) „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje, po to kai ji buvo parengta.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ec1c556a70ed92a40d3cb2bf45fb6156b7dbf7fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993480"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>Sukonfigūruokite „BOPIS“ esantį „Dynamics 365 Commerce“ vertinimo aplinkoje

[!include [banner](includes/banner.md)]

Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje (BOPIS) „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje, po to kai aplinka buvo parengta.

## <a name="prerequisite"></a>Būtinoji sąlyga

Pabaikite šio skyriaus procedūras po to, kai jūsų Komercijos vertinimo aplinka buvo parengta ir sukonfigūruota. Dėl informacijos, kaip parengti ir konfigūruoti savo aplinką, žr. [Parengti „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md) ir [Konfigūruoti „Dynamics 365 Commerce“ vertinimo aplinką](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).

Po to, kai jūsų „Commerce” aplinka visapusiškai parengta ir sukonfigūruota, galite pasinaudoti šia tema, kad įgalintumėte BOPIS scenarijus.

## <a name="configure-the-pos"></a>EKA konfigūravimas

### <a name="configure-modern-pos"></a>„Modern POS” konfigūravimas

BOPIS scenarijams, apimantiems mokėjimą kredito kortele, reikia aparatūros stoties. Aparatūros stotis yra įmontuota į „Windows“ ir „Android“ klientų „Modern POS“. Jei naudojate „Cloud POS“ arba „Modern POS“, skirtas „iOS“, elektroninio kasos aparato (EKA) klientas turi būti susietas su bendrai naudojama aparatūros stotimi. Šioje temoje paaiškinama, kaip sukonfigūruoti BOPIS, skirtą „Windows” ir „Android” klientams. Informacijos apie tai, kaip nustatyti bendrai naudojamą aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> Registrai**.
2. Pasirinkite registrą **SANFRAN-5**, tada pasirinkite **Redaguoti**.
3. Pakeiskite lauko **Aparatūros šablonas** reikšmę iš **HW002** į **HW001**, tada pasirinkite **Įrašyti**.
4. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**, kad sinchronizuotumėte pakeitimus.
5. Pasirinkite paskirstymo grafiką **1090**, tada veiksmų srityje pasirinkite **Vykdyti dabar**.
6. Pasirinkite **Taip** ir **Gerai**, kad būtų pradėtas duomenų sinchronizavimas. 

### <a name="install-modern-pos"></a>„Modern POS“ diegimas

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> Įrenginiai**.
2. Pasirinkite įrenginį **SANFRANCIS-5**.
3. Veiksmų srityje pasirinkite **Atsisiųsti**, tada – **Konfigūracijos failas**.
4. Pasirinkite **Atsisiųsti**, tada – **„Retail Modern POS”**. 
5. Kai **ModernPOSSetup.exe** failo atsisiuntimas baigtas, pasirinkite **Atidaryti failą**.

    ![Atidaryti failą](./dev-itpro/media/PAYMENTS/openfile.png)

6. Pasirinkite **Pirmyn**, kad būtų pradėtas diegimo procesas. Kai diegimas baigtas, pasirinkite **Uždaryti**.

### <a name="activate-modern-pos"></a>„Modern POS” aktyvinimas

1. „Windows” darbalaukyje pasirinkite mygtuką **Pradžia** ir įveskite **„Retail Modern POS”**.
2. Pasirinkite **„Retail Modern POS”** programą, kad būtų pradėtas aktyvinimas.
3. Pasirinkite **Toliau**. Laukai **Serverio URL**, **Įrenginio ID** ir **Registro numeris** turi būti nustatyti iš anksto naudojant konfigūracijos failo, atsisiųsto atliekant ankstesnę procedūrą, informaciją.
4. Pasirinkite **Aktyvinti**.
5. Pasirodo autentifikavimo dialogo langas. Pasirinkite sąskaitą, kuri naudoja el. pašto adresą, anksčiau susietą su darbuotoju **000713 - Andrew Collette**.

    > [!NOTE]
    > Jei dar nesusiejote darbuotojo su jūsų tapatybe, aktyvinimas bus nesėkmingas. Tuo atveju, atlikite žingsnius „Su jūsų tapatumu susijęs darbuotojas“ skyriuje [Konfigūruoti „Dynamics 365 Commerce“ vertinimo aplinką](cpe-post-provisioning.md#associate-a-worker-with-your-identity) temoje.
    
6. Kai būsite paraginti leisti jūsų organizacijai valdyti įrenginį, pasirinkite **Tik šią programą**.
7. Kai aktyvinimas baigtas, pasirinkite **Pradžia**.

### <a name="enable-bopis-in-modern-pos"></a>BOPIS įgalinimas „Modern POS”

1. Prisijunkite prie „Modern POS” naudodami **000713** kaip operatoriaus ID ir **123** kaip slaptažodį.
2. Kol leidžiamas įvadinis supažindinimo vaizdo įrašas, pažymėkite du žymės langelius, esančius apatiniame kairiajame dialogo lango kampe, ir uždarykite dialogo langą.
3. Jei nebūsite paraginti uždaryti pamainos, slinkite į dešinę puslapyje **Sveiki**, pasirinkite **Uždaryti pamainą** ir vėl prisijunkite prie EKA.
4. Kai prisijungsite ir būsite paraginti, pasirinkite **Atlikti ne stalčiaus operaciją**.
5. Puslapyje **Sveiki** slinkite į dešinę ir pasirinkite operaciją **Pasirinkti aparatūros stotį**.
6. Pasirinkite **Valdyti**, nustatykite pasirinktį **Naudoti aparatūros stotį** į **Įjungta** ir pasirinkite **Gerai**.
7. Atsijunkite nuo EKA ir vėl prisijunkite.
8. Po to, kai prisijungsite, pasirinkite **Atidaryti naują pamainą** ir tada – **Stalčius**.

## <a name="complete-a-bopis-scenario"></a>BOPIS scenarijaus baigimas

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Parduotuvėje paimamo parduotuvės užsakymo kūrimas

1. Eikite į URL, kurį nurodėte veiksmo [El. prekybos inicijavimas](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) metu atliekant aplinkos konfigūravimą.
2. Pasirinkite prekę, tada – **Įtraukti į krepšelį**.
3. Pirkinių krepšelio puslapyje pasirinkite **Paimti** ką tik įtrauktoje užsakymo eilutėje.
4. Dialogo lange **Pasirinkti parduotuvę** įveskite **San Fransiskas** ir pasirinkite mygtuką **Paieška**.
5. Rezultatų sąraše suraskite San Francisko parduotuvę ir pasirinkite **Paimti čia**.
6. Pirkinių krepšelio puslapyje pasirinkite **Užbaigti pirkimą kaip svečias**. 

    > [!NOTE]
    > Norėdami tęsti pirkimo užbaigimą, turite sutikti su slapukų pranešimu. Šis pranešimas rodomas kaip reklaminė juosta pirkimo užbaigimo puslapio viršuje.

7. Mokėjimo kredito kortele būdo atveju įveskite toliau nurodytą informaciją.

    - **Kortelės savininko vardas:** įveskite bet kokį vardą.
    - **Kortelės numeris:** įveskite **4111-1111-1111-1111**.
    - **Galiojimo data:** įveskite **10/20**.
    - **Kortelės tikrinimo vertės (CVV) kodas**: įveskite **737**.

    > [!IMPORTANT]
    > Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.

8. Tęskite pirkimo užbaigimą įvesdami sąskaitų siuntimo adreso informaciją, tada pasirinkite **Įrašyti ir tęsti**.
9. Kai užsakymas paruoštas, pasirinkite **Užbaigti pirkimą**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Internetinių užsakymų sinchronizavimas su tarnybiniu biuru

Informacijos apie tai, kaip sinchronizuoti internetinius užsakymus, žr. [Pardavimo ir mokėjimų internetu registravimas](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).

### <a name="pick-up-an-order-in-the-store"></a>Užsakymo paėmimas parduotuvėje

1. Prisijunkite prie EKA.
2. **Darbo pradžios** ekrane pasirinkite **Užsakymo įvykdymas**
3. Paimamų prekių sąraše pasirinkite užsakymo, kuris buvo pateiktas internetu, eilutę.
4. Pasirinkę užsakymo eilutę pasirinkite **Paimti**.

    Eilutės elementas įtraukiamas į operacijos ekraną, o **0,00 USD** rodoma kaip mokėtinas balansas.

5. Pasirinkite mokėtiną **0,00 USD** balansą arba bet kokį mokėjimo būdą operacijai atlikti.

## <a name="troubleshooting"></a>Trikčių šalinimas

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Internetiniai užsakymai, kurie nuskaitomi EKA, turi ne nulinį mokėtiną balansą

Kai užsakymas nuskaitomas paėmimui iš parduotuvės, jei mokėtinas balansas nėra 0 (nulis), įsitikinkite, kad naudojama „Modern POS” ir kad aparatūros stotis yra aktyvi. Jei naudojama „Cloud POS“ arba „Modern POS“, skirtos „iOS“, įsitikinkite, kad bendrai naudojama aparatūros stotis yra aktyvi. Norint nuskaityti mokėjimus, atliktus internetu, reikia tam tikros aktyvios aparatūros stoties.

### <a name="general-issues-with-payment-capture"></a>Problemos, susijusios su mokėjimo fiksavimu

Susidūrę su problemomis pirmiausia perskaitykite „Modern POS” arba informacinių interneto paslaugų (IIS) aparatūros stoties įvykių žurnalus. Šiuos žurnalus galite rasti toliau nurodytuose „Windows” įvykių žurnalo mazguose.

- Programų ir paslaugų žurnalai \> „Microsoft” \> „Dynamics” \> „Commerce-ModernPOS”
- Programų ir paslaugų žurnalai \> „Microsoft” \> „Dynamics” \> „Commerce-Hardware Station”

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)

[„Dynamics 365 Commerce“ vertinimo aplinkos DUK](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)

[„Adyen“ mokėjimo jungtis](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Internetinių mokėjimo priemonių įrašymas naudojant „Adyen“ jungtį](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Integruotų kanalų mokėjimų apžvalga](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]