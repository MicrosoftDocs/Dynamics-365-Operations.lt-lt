---
title: Pasirinkimas tarp „Store Commerce“ ir „Cloud POS“
description: Šiame straipsnyje paaiškinami pagrindiniai parduotuvės "Commerce" ir "Cloud POS" skirtumai ir aprašomi įvairūs mažmenininkai, Dynamics 365 Commerce kurie turi atsižvelgti į savo poreikius, kad padėtų jiems geriausiai pasirinkti poreikius.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26f6e94b13b3058ac42c4c7b83dcf7179bae18e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854011"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Pasirinkimas tarp „Store Commerce“ ir „Cloud POS“

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinami pagrindiniai parduotuvės "Commerce" ir "Cloud POS" skirtumai ir aprašomi įvairūs mažmenininkai, Dynamics 365 Commerce kurie turi atsižvelgti į savo poreikius, kad padėtų jiems geriausiai pasirinkti poreikius. Be to, diegėjai suteikiama papildomų fonų, patarimų ir patarimų, faktorių, į kuriuos jie turi atsižvelgti diegdami Dynamics 365 Commerce. Peržiūrėję šias gaires ir vadovaudamiesi jomis kaip diegimo proceso dalimi, diegėjai gali išvengti problemų, kurios gali turėti įtakos vartotojų pasitenkinimui arba našumui.

## <a name="insights"></a>Įžvalgos

„Commerce“ siūlomas platus diegimo ir topologijos variantų pasirinkimas. Todėl mažmenininkai gali pasirinkti komponentus ir konfigūraciją, kuri geriausiai atitinka jų verslo ir technologijų poreikius. Vienas diegimo aspektas, reikalaujantis didelio dėmesio, yra elektroninio kasos aparato (EKA) komponento platformos ir formos koeficiento pasirinkimas.

### <a name="pos-platform-and-form-factor-considerations"></a>EKA platformos ir formos koeficiento aspektai

„Commerce“ palaiko toliau nurodytas EKA parinktis.

- "Store Commerce", skirta Microsoft Windows
- "Store Commerce", skirta "IOS" ir Android
- Debesies EKA (CPOS), palaikančios ir Microsoft Edge Chromuotas naršykles
- ModernŪS EKA (MPOS) Microsoft Windows (MPOS) bus pasenusi 2023 m. spalio mėn. 

Visais atvejais EKA ("Store Commerce" ir CPOS) bendrai naudoti tą patį pagrindinį programos kodą. Tai yra svarbu dėl šių priežasčių:

- Vartotojo sąsaja (UI) yra nuosekli, nepriklausomai nuo platformos ar formos koeficiento.
- Daugelis funkcinių galimybių yra tokios pačios, nepriklausomai nuo platformos ar formos koeficiento. Tačiau yra keletas svarbių skirtumų. Šie skirtumai yra pažymėti šiame straipsnyje.
- Kiekvienoje parduotuvėje EKA variacijas galima derinti ir veikti vienu metu. Pavyzdžiui, pagrindiniai savo registrai, mažmenininkas gali naudoti parduotuvės "Commerce" kompiuteriuose, kuriuose veikia "Windows". Tačiau pardavėjas gali papildyti šiuos kasos aparatus naršyklėje veikiančiais terminalais arba mobiliaisiais įrenginiais.
- Tinkinimus ir plėtinius galima lengvai naudoti skirtingose platformose ir formos koeficientuose. Kadangi pagrindinis programos kodas naudojamas bendrai, užuot tinkinimus diegus kelis kartus, visus juos galima įdiegti vieną kartą.

### <a name="store-commerce-vs-cpos"></a>Parduotuvės komercijos ir CPOS

Nors "Store Commerce" ir CPOS atitinka tuos pačius, yra keletas svarbių skirtumų, kuriuos reikia suprasti.

#### <a name="store-commerce"></a>„Store Commerce“

"Store Commerce" yra darbalaukio programa, įdiegta ir aptarnaujama įrenginyje.

- **"Windows** " – "Store Commerce for Windows" programoje yra visi programų kodai Commerce Runtime (CRT) ir aparatūros stotis (HWS).
- **iOS/Android** Šiose platformose programa veikia kaip CPOS programos kodo pagrindinis kompiuteris. Kitaip tariant, programos kodas gaunamas iš CPOS serverio, kuris yra "Commerce Scale Unit". Norėdami gauti daugiau informacijos, žr. [„Commerce Scale Unit“ apžvalga](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Kadangi CPOS veikia naršyklėje, programa įrenginyje neįdiegta. Vietoj to naršyklės pasiekia programos kodą iš CPOS serverio. Todėl CPOS negali tiesiogiai prieiti prie EKA aparatūros arba dirbti neprisijungus.

### <a name="store-deployment-considerations"></a>Parduotuvės diegimo aspektai

Be platformos ir formos koeficiento, mažmenininkai taip pat turi pasirinkti diegimo parinktį parduotuvėje. Tolesnėje lentelėje nurodomos galimos kiekvienos EKA parinkties konfigūracijos.

| EKA programa            | „Commerce Scale Unit“ | Pasiekiama neprisijungus | Vietinis HWS palaikymas |
|----------------------------|---------------------|-------------------|-------------------|
| Parduotuvės "Commerce", skirta "Windows" | Debesies arba RSSU       | Taip               | Taip               |
| "Store Commerce", skirta Android | Debesies arba RSSU       | Ne                | Taip               |
| "Store Commerce", skirta "IOS"     | Debesies arba RSSU       | Ne                | Ne                |
| „Cloud POS”                  | Debesies arba RSSU       | Ne                | Ne                |

#### <a name="commerce-scale-unit"></a>„Commerce Scale Unit“

„Commerce Scale Unit“ yra komponentas, kuriame yra CRT. CRT aplinkoje yra visa verslo logika, kurą naudoja EKA, ir ji suteikia prieigą prie kanalo duomenų bazės. Kol jie prisijungę, visi parduotuvėje esantys EKA klientai naudojasi „Commerce Scale Unit“. „Commerce Scale Unit“ galima įdiegti debesyje arba parduotuvėje.

#### <a name="offline-mode"></a>Atjungties režimas

"Store Commerce", skirta "Windows", palaiko atjungties režimą. Neprisijungus, EKA gali ir toliau tvarkyti pardavimus, net jei jis yra atjungtas nuo „Commerce Scale Unit“. Atkūrus ryšį, jį galima sinchronizuoti su kanalo duomenų baze. "Store Commerce" naudoja savo įdėtąjį sistemos egzempliorių CRT ir laikinai naudoja savo vietinį duomenų šaltinį (autonominę SQL serverio duomenų bazę). Daugiau informacijos apie atjungties režimo funkcijas žr. [EKA atjungties režimo funkcijos](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>EKA periferinės (aparatinės) įrangos aspektai

Mažmenininkai taip pat turi apsvarstyti, kaip EKA pasieks įrenginius ir periferinius įrenginius, pvz., spausdintuvus, kasos stalčius ir mokėjimo terminalus. Aparatūros stotys gali būti skirtos EKA kasos aparatui arba bendrai naudojamos parduotuvės kasos aparatų.

| EKA programa            | Vietinės HWS OEKA | Išoriniai tinklo įrenginiai | Bendrinamas HWS palaikymas |
|----------------------------|----------------|---------------------|--------------------|
| Parduotuvės "Commerce", skirta "Windows" | Taip            | Taip                 | Taip                |
| "Store Commerce", skirta Android | Ne             | Taip                 | Taip                |
| "Store Commerce", skirta "IOS"     | Ne             | Ne                  | Taip                |
| „Cloud POS”                  | Ne             | Ne                  | Taip                |

Išsamesnės informacijos apie aparatūros stotis žr. [„Retail“ aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Diegimo aplinkybės

Planuodami EKA diegimą parduotuvėse, atsižvelkite į toliau nurodytą informaciją.

- **Funkciniai reikalavimai**. Pagrindiniai verslo procesai ir galimybės yra tos pačios, nepriklausomai nuo platformos, formos koeficiento ar diegimo topologijos. Todėl daugumai mažmenininkų nereikia atsižvelgti į funkcinius reikalavimus, kai jie planuoja diegimą.
- **Jungiamumas** – tinklo prieinamumas (teritorinis tinklas \[WAN\] ir vietinis tinklas \[LAN\]) yra pagrindinis veiksnys, kurį reikia kruopščiai įvertinti. Bet kokia nauda išlaidų ir paprastumo požiūriu, kurią suteikia diegimo nereikalaujantis, debesyje veikiantis sprendimas, prarandama, jei sistema negalima svarbiems verslui procesams vykdyti.

    Išskyrus atvejus, kai tam tikro įrenginio jungiamumas yra labai patikimas ir atsparus arba jei tam tikras prastovos kiekis pardavėjui priimtinas, rekomenduojame vieną iš toliau nurodytų parinkčių:

    - Naudokite "Store Commerce" "Windows" ir įjunkite atjungties režimą.
    - „Commerce Scale Unit“ diegimas patalpose.

    Šios dvi galimybės nėra nesuderinamos. Siekdami patikimiausios topologijos, mažmenininkai gali įdiegti vietinį RSSU, kad sumažintų priklausomybę nuo interneto ryšio arba „Azure“ prieinamumo. Jie taip pat gali įdiegti EKA kasos aparatus, kuriuose įgalintas atjungties režimas, jeigu kiltų vietinio serverio ar tinklo problema.

- **Aparatūros įrenginiai arba išoriniai įrenginiai**. Vienas svarbus „Retail POS“ sistemos aspektas yra jos galimybė naudoti EKA periferinius įrenginius, pvz., spausdintuvus, kasos stalčius ir mokėjimo terminalus. Nors visos galimos EKA pasirinktys gali naudoti periferinius įrenginius, tik parduotuvės "Commerce for Windows" juos palaiko tiesiogiai. Naudojant visas kitas programas, būtina viena arba daugiau aparatūros stočių. Nors šis metodas padidina lankstumą, būtina įdiegti, sukonfigūruoti ir prižiūrėti papildomus komponentus.
- **Sistemos reikalavimai**. EKA programos sistemos reikalavimai skiriasi. Prieš priimdami sprendimą, būtinai patikrinkite naujausią informaciją. Pavyzdžiui, kadangi CPOS veikia naršyklėje, jis palaiko daugiau operacinių sistemų. Daugiau informacijos apie sistemos reikalavimus žr. [Sistemos reikalavimai įdiegtims debesyje](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Diegimas ir priežiūra**. Diegimo ir priežiūros reikalavimų sudėtingumas gali skirtis, atsižvelgiant į programos ir diegimo pasirinkimus. Pavyzdžiui, diegiant debesies CPOS nereikia įdiegti ir atnaujinti kiekviename įrenginyje. Todėl šis metodas labai sumažina sudėtingumą ir išlaidas. Tačiau jei "Store Commerce" diegiate kiekviename kasos aparate ir įgalinate atjungties režimą bei bendrai naudojamas aparatūros stotis, labai padidėja galinių punktų, kuriuos reikia valdyti, skaičius.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
