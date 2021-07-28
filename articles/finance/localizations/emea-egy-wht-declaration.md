---
title: Egipto išskaitomo mokesčio deklaracija
description: Šioje temoje paaiškinama, kaip sukonfigūruoti ir sugeneruoti Egipto išskaitomo mokesčio deklaracijas.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: afb9f95458089e854335399ea3d14ba229c02bbd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349878"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Egipto išskaitomo mokesčio deklaracija (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Peržiūra
Šioje temoje paaiškinama, kaip nustatyti ir generuoti išskaitomo mokesčio deklaraciją ir 41 ir 11 juridinių subjektų išskaitomo mokesčio deklaravimo formas Egipte 

Visi Egipto subjektai turi parengti 41 formą, kurioje susumuojami visi mokesčiai, saugomi iš vietinių tiekėjų ir paslaugų teikėjų. Be 41 formos, 11 formą reikia sugeneruoti taip, kad išsamiai būtų sugeneruoti visi užsienio teikėjų išskirstyti mokesčiai. 

Ataskaita **Išskaitomo mokesčio deklaracija**, esanti „Dynamics 365 Finance“, apima tokias ataskaitas:

- Deklaracijos formos Nr. 41
- Deklaracijos formos Nr. 11
    
    
## <a name="prerequisites"></a>Būtinieji komponentai
Pagrindinis juridinio subjekto adresas turi būti Egipte.
Darbo srityje **Funkcijų valdymas** reikia įjungti toliau pateikiamą funkciją.

   - **Visuotinis išskaitomas mokestis**

Daugiau informacijos apie tai, kaip įjungti naujas funkcijas, žr. temoje [Funkcijų valdymo apžvalga.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Eikite į **Mokesčiai** > **Nustatymas** > **Parametrai** > **Didžiosios knygos parametrai** ir skirtuke **Išskaitomas mokestis** parinktį **Įjungti visuotinį išskaitomą mokestį** nustatykite kaip **Taip**.
2. Darbo srityje **Elektroninių ataskaitų teikimas** importuokite šį elektroninių ataskaitų teikimo formatus iš saugyklos:

    - WHT deklaravimas „Excel“ faile (EG)

    > [!NOTE]
    > Šis formatas grindžiamas **Mokesčių deklaracijos modeliu** ir naudoja **Mokesčių deklaracijos modelio susiejimą**. Ši papildoma konfigūracija importuojama automatiškai.

Daugiau informacijos apie elektroninių ataskaitų teikimo konfigūracijų importavimą, žr. [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektroninių ataskaitų konfigūracijų atsisiuntimas

Egipto WHT deklaracijos formos diegimas grindžiamas elektroninės ataskaitos (ER) konfigūracijomis. Daugiau informacijos apie galimybes ir konfigūruojamų ataskaitų sąvokas žr. [Elektroninių ataskaitų teikimas](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Norėdami rasti gamybos ir naudotojo priėmimo tikrinimo (UAT) aplinkas, vadovaukitės instrukcijomis, pateikiamomis temoje [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Norėdami sugeneruoti išskaitomo mokesčio deklaracijas Egipto juridiniame subjekte, turite įkelti šias konfigūracijas:

- Mokesčių deklaracija model.version.82.xml arba naujesnė versija
- Mokesčių deklaracija model.mapping.version.82.133.xml arba naujesnė versija
- WHT deklaracijos „Excel“ (EG).version.82.21 ar naujesnė versija

Baigę parsisiųsti ER konfigūracijas iš „Lifecycle Services“ (LCS) arba visuotinės saugyklos, atlikite nurodytus veiksmus.

1. Eikite į darbo sritį **Elektroninės ataskaitos** ir pasirinkite plytelę **Ataskaitų konfigūracijos**.
1. Puslapyje **Konfigūracijos**, veiksmų srityje pasirinkite **Keisti > Įkelti iš XML failo**.
1. Įkelti visus failus tokia tvarka, kokia jie yra išvardyti ankstesniuose punktuose. Įkėlus visas konfigūracijas, srityje „Finansai“ turėtų būti konfigūracijos medis.

## <a name="set-up-application-specific-parameters"></a>Konkrečios programos parametrų nustatymas

Konkretaus prašymo parametrų pasirinktis naudotojams leidžia nustatyti kriterijus, pagal kuriuos mokesčių operacijos bus klasifikacijos ir skaičiuojamos kiekvienoje sugeneruotos ataskaitos eilutėje, atsižvelgiant į **išskaitomo mokesčio prekės grupės** konfigūraciją ar kitus kriterijus, nustatytus peržvalgos apibrėžime.

Išskaitomo mokesčio deklaracijos 41 formoje yra konkretus stulpelis, kuriame išskaitomo mokesčio operacija turi būti klasifikuojama pagal mokesčių inspekcijos klasifikacijos, pavadintos **Nuolaidos kodo tipas**, pavadinimą. Užuot šias naujas klasifikacijas įtraukus kaip naujus įvesties duomenis, kai paskeliami sandoriai, klasifikacijos apibrėžiamos pagal skirtingas peržvalgas, kurios buvo įvestos pasirinkus **Konfigūracijos** > **Konkrečios programos parametrų nustatymas** > **Sąranka**, atsižvelgiant į Egipto PVM išskaičiavimų ataskaitų reikalavimus. 

Klasifikuojant operacijas 41 išskaitomo mokesčio deklaracijos formoje naudojama ši konfigūracija:

- **DiscountTaxTypeLookup**-> 18 stulpelis 

Norėdami nustatyti skirtingas peržvalgas, naudojamas WHT deklaravimo ir susijusių knygų ataskaitoms generuoti, atlikite nurodytus veiksmus. 

1. Darbo srityje **Elektroninės ataskaitos** pasirinkite **Konfigūracijos** > **Sąranka**, kad nustatytumėte taisykles, skirtas operacijoms klasifikuoti WHT deklaracijos ataskaitoje. 
2. Pasirinkite dabartinę versiją ir „FastTab“ skirtuke **Peržvalgos** pasirinkite peržvalgos pavadinimą. Pvz., **DiscountTaxTypeLookup**. Ši peržvalga nustato nuolaidų tipų, kurių reikalauja mokesčių inspekcija, sąrašą.
3. „FastTab“ skirtuke **Sąlygos** pasirinkite **Pridėti** ir naujoje eilutėje, stulpelyje **Peržvalgos rezultatas** pasirinkite susijusią eilutę, kuri vaizduoja klasifikaciją **18 stulpelyje**.
4. Stulpelyje **Išskaičiuojamų mokesčių elementų grupė** pasirinkite susijusį kodą, kuris naudojamas klasifikacijai nustatyti. Pavyzdžiui, **Leidžiama nuolaida**.  
5. Visoms galimoms peržvalgoms pakartokite 3 ir 4 veiksmus.
6. Dar kartą pasirinkite **Pridėti**, jei norite įtraukti paskutinio įrašo eilutę, o stulpelyje **Peržvalgos rezultatas** pasirinkite **Netaikoma**. 
7. Likusiuose stulpeliuose pasirinkite **Ne tuščia**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Didžiosios knygos parametrų sąranka

Jei norite generuoti WHT deklaracijos formos ataskaitas programoje „Microsoft Excel“, apibrėžkite ER formatą puslapyje **Didžiosios knygos parametrai**.

1. Eikite į **Mokesčiai** > **Sąranka** > **Didžiosios knygos parametrai**.
2. Skirtuko **Išskaitomas mokestis** lauke **WHT deklaracijos formato susiejimas** pasirinkite **WHT deklaracija „Excel“ formatu (EG)**. Jei laukelį paliekate tuščią, standartinė pardavimų mokesčių ataskaita bus generuojama SSRS formatu.


![Deklaracijos forma.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Išskaitomo mokesčio deklaracijų formų deklaravimas
Tam tikro laikotarpio išskaitomo mokesčio formos paruošimo ir pateikimo procesas yra paremtas išskaitomo mokesčio operacijomis, užregistruotomis sudengimo ir mokėjimo registravimo mokesčio užduoties metu. Daugiau informacijos apie visuotinį išskaitomą mokestį ieškokite skyriuje [Visuotinis išskaitomas mokestis](../general-ledger/global-withholding-tax-overview.md).

Atlikite šiuos veiksmus, kad sugeneruotumėte mokesčių deklaracijos ataskaitą.

1. Eikite į **Mokestis** > **Deklaracijos** > **Išskaitomas mokestis** > **Išskaitomo mokesčio mokėjimas*.
2. Pasirinkite sudengimo laikotarpį ir tada pasirinkite ataskaitos pradžios datą. 
3. Įveskite sandorio datą ir pasirinkite **Gerai**.
4. Atidaromame dialogo lange pasirinkite vieną ar daugiau formų tipų **Forma 41**, **Forma 11** arba **Nėra**. Jei pasirinksite **Nėra**, bus sugeneruota standartinė ataskaita. 
5. Pasirinkti kalbą. Visos ataskaitos yra verčiamos į **en-us** ir **ar-eg** kalbas.
6. Įveskite banko, kuriame bus mokami mokesčiai, filialą ir pavadinimą.
7. Pasirinkite verslo tipą ir įveskite čekių ir dokumentų numerius. 
8. Įveskite objekto tipą. 
9. Įveskite asmens, kuris buvo užregistruotas formai priskirti, vardą ir pavardę, o norėdami patvirtinti ataskaitos generavimą paspauskite **Gerai**. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
