---
title: Paskirtieji mokėjimo terminalai ir raginimai spausdintuvui ir kasos stalčiui
description: Šioje temoje pateikiama informacija apie galimybę turėti specialų mokėjimo terminalą ir raginti vartotoją pasirinkti kasos stalčių bei kvitų spausdintuvą.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 03cb68ede82668523e6970d33df676738e65fd83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414373"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Paskirtieji mokėjimo terminalai ir raginimai spausdintuvui ir kasos stalčiui

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie galimybę turėti specialų mokėjimo terminalą ir raginti vartotoją pasirinkti kasos stalčių bei kvitų spausdintuvą.

## <a name="overview"></a>Apžvalga

Šiuolaikiniai mažmenininkai ieško būdų, kaip supaprastinti atsiskaitymo parduotuvėje patirtį. Naujausios tendencijos kompiuterizuoti atsiskaitymo procesą, naudojant elektroninius mokėjimus, padeda ne tik suteikti pirkimo patirčiai sklandumo, bet ir sumažinti būtinybę turėti visą periferinių įrenginių rinkinį kiekvienam parduotuvės darbuotojui.

„Microsoft Dynamics 365 Commerce“ palaiko šias tendencijas, įgalindama scenarijų, kuriame elektroninio kasos aparato (EKA) įrenginys turi jam nuolat paskirtą mokėjimo terminalą, bet jis neprivalo turėti savo kvitų spausdintuvo ar kasos stalčiaus. Kai darbuotojams reikia atspausdinti kvitą arba priimti grynuosius pinigus, jie paraginami pasirinkti aparatūros stotį, kurioje sukonfigūruoti šie įrenginiai.

## <a name="key-terms"></a>Pagrindiniai terminai

| Terminas | Aprašymas |
|---|---|
| Registras | Objektas, naudojamas EKA kasos egzemplioriui konfigūruoti. |
| Įrenginys | Fizinio EKA kasoso aparato ir „Modern POS“ programos, kuriai jis priskirtas, egzemplioriaus atvaizdas. |
| Paskirta aparatūros stotis | Aparatūros stoties verslo logika yra įtaisyta „Windows“ skirtoje „Modern POS“ ir „Android“ skirtoje „Modern POS“ programose. |
| Stalčiaus „Kick“ (d/k) prievadas | Tradicinis kasos stalčiaus prijungimo prie kvitų spausdintuvo būdas. |
| Išoriniai tinklo įrenginiai | Integruotas tinklo mokėjimo terminalų, kvitų spausdintuvų ir grynųjų pinigų stalčių palaikymas. |

## <a name="supported-pos-clients-and-devices"></a>Palaikomi EKA klientai ir įrenginiai

Šioje temoje aprašytą funkciją palaiko „Modern POS“, skirta „Windows“, ir „Modern POS“, skirta „Android“ EKA klientams.

Ši funkcija palaiko prie tinklo prijungtus mokėjimo terminalus ir kvitų spausdintuvus. Galite suteikti kasos stalčiaus palaikymą, prijungdami kasos stalčių prie tinklo prijungto kvitų spausdintuvo per d/k prievadą.

Sąrankos nereikalaujantį šios funkcijos palaikymą teikia [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Tačiau kitos mokėjimų jungtys gali būti palaikomos naudojant „Commerce Software Development Kit“ (SDK) mokėjimams. Palaikomus kvitų spausdintuvus sudaro prie tinklo prijungti „Star Micronics“ ir „Epson“ kvitų spausdintuvai.

Norėdami nustatyti „Star Micronics“ kvitų spausdintuvus, naudokite „Star Micronics Printer Utility“, kad sukonfigūruotumėte įrenginį taip, kad jį būtų galima naudoti tinkle. Ši programa taip pat suteiks įrenginiui IP adresą.

Norėdami nustatyti „Epson“ kvitų spausdintuvus, naudokite „Epson ePOS-Print“ programą, kad sukonfigūruotumėte įrenginį naudoti tinklo protokolus.

Daugiau informacijos apie tai, kaip nustatyti tinklo periferinius įrenginius, žr [Tinklo periferinių įrenginių palaikymo apžvalga](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Paskirtojo mokėjimų terminalo ir raginimo spausdintuvui bei grynųjų pinigų stalčiui nustatymas

### <a name="set-up-hardware-profiles"></a>Aparatūros šablonų nustatymas

Turite turėti du aparatūros profilio tipus. Pirmasis priskirta kasos aparatui. Antrasis priskirtas aparatūros stočiai parduotuvės lygmenyje ir naudojamas logiškai grupuoti tinklo kvitų spausdintuvams ir grynųjų pinigų stalčiams.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Kasos aparato aparatūros profilio nustatymas

Norėdami nustatyti kasos aparatui priskirtą aparatūros profilį, atlikite tolesnius veiksmus.

1. Dalyje „Dynamics 365 Commerce“ susiraskite **Aparatūros profilis**.
2. Pasirinkite **Naujas**.
3. Priskirkite aparatūros profilio numerį ir įveskite aprašymą. Šis aparatūros profilis bus priskirtas pačiam kasos aparatui. Todėl, pakaks tokio aprašo, kaip **Paskirtasis su atsarga**.
4. Įvairių įrenginių tipų „FastTab“ skirtukuose nustatykite tolesnius įrenginių tipus.

    | Įrenginys | Tipas | Įrenginio pavadinimas | Papildoma informacija |
    |---|---|---|---|
    | Spausdintuvas | Atsarginis | *Bet kuris* | Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės. **Kvitų profilio ID** turi būti toks pat, kaip **Kvitų profilio ID**, kuris yra susietas su tinklo spausdintuvu, kuris yra susietas su aparatūros profiliu, priskirtu aparatūros stočiai kanalo lygmeniu. |
    | Kasos stalčius | Atsarginis | *Bet kuris* | Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės. Nustatykite parinktį **Naudoti bendrą pamainą** į **Taip**. |
    | EFT paslauga | „Adyen“ | Netaikoma | Informacijos apie tai, kaip nustatyti naują „Adyen“ jungtį, žr. [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Kitos mokėjimų jungtys gali būti palaikomos naudojant [„Commerce Software Development Kit“ (SDK) mokėjimams](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension). |
    | PIN rinkiklis | Tinklas | **MicrosoftAdyenDeviceV001** | Nėra. |

5. Programoje „Dynamics 365 Commerce“ susiraskite **Kasos aparatai**.
6. Pasirinkite kasos aparatą pasirinkdami kasos aparato numerį ir pasirinkite **Redaguoti**.
7. Priskirkite ką tik sukurtą aparatūros profilį kasos aparate, kuris turėtų naudoti paskirtąjį mokėjimo terminalą. Įrenginys, susietas su šiuo kasos aparatu, turi naudoti programą „Modern POS“, skirtą Windows, arba „Modern POS“, skirtą „Android“.
8. Pasirinkite **Įrašyti**.
9. Veiksmų srities skirtuke **Kasos aparatai** pasirinkite **Konfigūruoti IP adresus**.
10. „FastTab“ skirtuke **PIN rinkiklis** įveskite mokėjimo terminalo IP adresą. Daugiau informacijos apie tai, kaip gauti mokėjimo terminalo IP adresą naudojant „Adyen“ jungtį, žr [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. Pasirinkite **Įrašyti**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Aparatūros profilio nustatymas kvitų spausdintuvui ir grynųjų pinigų stalčiui

Norėdami nustatyti aparatūros profilį, naudojamą tinklo kvitų spausdintuvui ir grynųjų pinigų stalčiui sugrupuoti, atlikite tolesnius veiksmus.

1. Dalyje „Dynamics 365 Commerce“ susiraskite **Aparatūros profilis**.
2. Pasirinkite **Naujas**.
3. Priskirkite aparatūros profilio numerį ir įveskite aprašymą. Šis aparatūros profilis bus naudojamas kvitų spausdintuvui ir grynųjų pinigų stalčiui sugrupuoti. Todėl pakaks tokio aprašymo, kaip **Tinklo spausdintuvas ir grynųjų pinigų stalčius**.
4. Įvairių įrenginių tipų „FastTab“ skirtukuose nustatykite tolesnius įrenginių tipus.

    | Įrenginys | Tipas | aprašymas | Papildoma informacija |
    |---|---|---|---|
    | Spausdintuvas | Tinklas | **„Epson“** arba **„Star“** | Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės. **Kvitų profilio ID** turi būti toks pat, kaip **Kvitų profilio ID**, kuris yra susietas su spausdintuvu, kuris yra susietas su aparatūros profiliu, priskirtu kasos aparatui. |
    | Kasos stalčius | Tinklas | **„Epson“** arba **„Star“** | Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės. Nustatykite parinktį **Naudoti bendrą pamainą** į **Taip**. |

5. Pasirinkite **Įrašyti**.

### <a name="set-up-hardware-stations"></a>Aparatūros stočių nustatymas

Turite turėti dvi aparatūros stotis. Pirmoji bus susieta su kasos aparatu. Antroji bus pasirinkta kaip reikalinga, kai reikia atspausdinti kvitą arba atidaryti grynųjų pinigų stalčių.

#### <a name="register-a-hardware-station"></a>Kasos aparato aparatūros stotis

1. Programoje „Dynamics 365 Commerce“ susiraskite **Visos parduotuvės**.
2. Pasirinkite parduotuvę pasirinkdami jos **Mažmeninės prekybos kanalo ID** reikšmes ir pasirinkdami **Redaguoti**.
3. „FastTab“ skirtuke **Aparatūros stotys** pasirinkite **Įtraukti**.
4. Nustatykite **Aparatūros stoties tipo** lauką į **Paskirtasis**.
5. Įveskite aprašymą, bet nenustatykite jokių kitų šios aparatūros stoties verčių. Ši aparatūros stotis bus naudojama kasos aparatui visą laiką. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Aparatūros stoties nustatymas kvitų spausdintuvui ir grynųjų pinigų stalčiui

1. Programoje „Dynamics 365 Commerce“ susiraskite **Visos parduotuvės**.
2. Pasirinkite parduotuvę pasirinkdami jos **Mažmeninės prekybos kanalo ID** reikšmes ir pasirinkdami **Redaguoti**.
3. „FastTab“ skirtuke **Aparatūros stotys** pasirinkite **Įtraukti**.
4. Nustatykite **Aparatūros stoties tipo** lauką į **Paskirtasis**.
5. Įvesti aprašymą. Ši aparatūros stotis bus naudojama kvitų spausdintuvui ir grynųjų pinigų stalčiui.
6. Lauke **Aparatūros profilis** pasirinkite aparatūros profilį, kurį anksčiau sukūrėte kvitų spausdintuvui ir grynųjų pinigų stalčiui.
7. Pasirinkite **Įrašyti**.
8. Kol aparatūros stotis kvitų spausdintuvui ir grynųjų pinigų vis dar renkama, pasirinkite **Konfigūruoti IP adresus**.
9. Sužinokite spausdintuvo IP adresą ir įveskite jį kaip IP adresą, skirtą kvitų spausdintuvui ir grynųjų pinigų stalčiui.
10. Pasirinkite **Įrašyti**
11. Susiraskite **Paskirstymo grafikai**.
12. Pasirinkite paskirstymo grafiką **1090**, tada pasirinkite **Vykdyti dabar**.
13. Pasirinkite paskirstymo grafiką **1070**, tada pasirinkite **Vykdyti dabar**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Nustatymas, kad sistema ragintų pasirinkti kvitų spausdintuvą ir grynųjų pinigų stalčių, kai jo prireikia

1. Palaikomame EKA kliente uždarykite dabartinę pamainą, jei pamaina atidaryta.
2. Prisijunkite ir pasirinkite **Stalčiaus operacijos be stalčiaus**.
3. Naudokite operaciją **Valdyti aparatūros stotis**, kad aparatūros stočiai įjungti.
4. Pasirinkite aparatūros stotį, kurią sukūrėte kasos aparatui, kad taptų aktyvi.
5. Atsijunkite nuo EKA, vėl prisijunkite ir atidarykite pamainą.

Mokėjimo terminalas, kuris priskirtas aparatūros profiliui, nuo šiol visada bus aktyvus, o jūs būsite raginami, jei prireiktų kvitų spausdintuvo arba kasos stalčiaus.

Daugelis pardavėjų, kurie prašė šios funkcijos, siekia mažinti atliekų kiekį, siųsdami kvitus el. paštu ir ragindami atsiskaityti elektroniniu būdu. Priklausomai nuo EKA konfigūracijos, parduotuvių darbuotojai raginami pasirinkti kvitų spausdintuvą arba grynųjų pinigų stalčių tik tada, kai klientas nori gauti fizinį kvitą arba nori atsiskaityti grynaisiais pinigais.

Parduotuvės darbuotojai raginami pasirinkti aparatūros stotį tik vieną kartą per operaciją, išskyrus atvejus, kai reikia atspausdinti kvitą ir atsikaitoma grynaisiais pinigais, bet anksčiau pasirinktame aparatūros profilyje neįtraukti abu įrenginiai. Tokiu atveju parduotuvės darbuotojas bus paragintas dar kartą, kad pasirinktų aparatūros stotį, kurią galima naudoti operacijai atlikti.

## <a name="related-articles"></a>Susiję straipsniai

- [Programos „POS Hybrid“ nustatymas sistemose „Android“ ir „iOS“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Tinklo periferinių įrenginių palaikymo apžvalga](https://go.microsoft.com/fwlink/?linkid=2129965)
