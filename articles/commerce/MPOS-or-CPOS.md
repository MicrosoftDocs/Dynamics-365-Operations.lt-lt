---
title: Pasirinkite „Modern POS“ (MPOS) arba „Cloud POS“
description: Šioje temoje pateikiama informacija apie pagrindinius skirtumus tarp „Modern POS“ (MPOS) ir „Cloud POS“. Joje taip pat aprašomi įvairūs veiksniai, į kuriuos mažmenininkai, diegiantys „Dynamics 365 Commerce“, turėtų atsižvelgti, kad galėtų pasirinkti geriausią sprendimą, atitinkantį jų poreikius.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: d636e80ba853191516b970ff3f1dece02ee771ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206876"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Pasirinkite „Modern POS“ (MPOS) arba „Cloud POS“

[!include [banner](includes/banner.md)]

Šioje temoje diegėjams pateikiama papildoma informacija, patarimai ir gairės apie veiksnius, į kuriuos jie turėtų atsižvelgti diegdami „Dynamics 365 Commerce“. Peržiūrėję šias gaires ir vadovaudamiesi jomis kaip diegimo proceso dalimi, diegėjai gali išvengti problemų, kurios gali turėti įtakos vartotojų pasitenkinimui arba našumui.

## <a name="insights"></a>Įžvalgos

„Commerce“ siūlomas platus diegimo ir topologijos variantų pasirinkimas. Todėl mažmenininkai gali pasirinkti komponentus ir konfigūraciją, kuri geriausiai atitinka jų verslo ir technologijų poreikius. Vienas diegimo aspektas, reikalaujantis didelio dėmesio, yra elektroninio kasos aparato (EKA) komponento platformos ir formos koeficiento pasirinkimas.

### <a name="pos-platform-and-form-factor-considerations"></a>EKA platformos ir formos koeficiento aspektai

„Commerce“ palaiko toliau nurodytas EKA parinktis.

- „Modern POS“ (MPOS), skirtas „Microsoft Windows“
- MPOS, skirta „Microsoft Windows Phone“
- MPOS, skirtas „Apple iPad“ arba „Google Android“ planšetiniam kompiuteriui
- „Cloud POS“ (CPOS), kuris palaiko „Microsoft Edge“, „Internet Explorer“ ir „Google Chrome“ naršykles

Visais atvejais EKA (MPOS ir CPOS) naudoja tą patį pagrindinį programos kodą. Tai yra svarbu dėl šių priežasčių:

- Vartotojo sąsaja (UI) yra nuosekli, nepriklausomai nuo platformos ar formos koeficiento.
- Daugelis funkcinių galimybių yra tokios pačios, nepriklausomai nuo platformos ar formos koeficiento. Tačiau yra keletas svarbių skirtumų. Šie skirtumai nurodyti šioje temoje.
- Konkrečioje parduotuvėje EKA variantus galima jungti ir vykdyti tuo pačiu metu. Pavyzdžiui, jos pagrindinių kasos aparatų kompiuteriuose, kuriuose įdiegta „Windows“, pardavėjas gali naudoti MPOS. Tačiau pardavėjas gali papildyti šiuos kasos aparatus naršyklėje veikiančiais terminalais arba mobiliaisiais įrenginiais.
- Tinkinimus ir plėtinius galima lengvai naudoti skirtingose platformose ir formos koeficientuose. Kadangi pagrindinis programos kodas naudojamas bendrai, užuot tinkinimus diegus kelis kartus, visus juos galima įdiegti vieną kartą.

### <a name="mpos-vs-cpos"></a>MPOS ir CPOS palyginimas

Nors MPOS ir CPOS iš esmės yra tas pats, yra keletas svarbių skirtumų, kuriuos būtina suprasti.

#### <a name="mpos"></a>MPOS

MPOS „Windows“, „iOS“ arba „Android“ įrenginyje yra programa, kuri yra sukomplektuota, įdiegta ir prižiūrima tame įrenginyje.

- **„Windows“**. MPOS programoje, skirtoje „Windows“, yra visas programos kodas ir įdėtoji „Commerce Runtime“ (CRT). 
- **iOS/Android** Šiose platformose programa veikia kaip CPOS programos kodo pagrindinis kompiuteris. Kitaip tariant, programos kodas ateina iš CPOS serverio, esančio „Microsoft Azure“ arba „Commerce Scale Unit“. Norėdami gauti daugiau informacijos, žr. [„Commerce Scale Unit“ apžvalga](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Kadangi CPOS veikia naršyklėje, programa įrenginyje neįdiegta. Vietoj to naršyklės pasiekia programos kodą iš CPOS serverio. Todėl CPOS negali tiesiogiai prieiti prie EKA aparatūros arba dirbti neprisijungus.

### <a name="store-deployment-considerations"></a>Parduotuvės diegimo aspektai

Be platformos ir formos koeficiento, mažmenininkai taip pat turi pasirinkti diegimo parinktį parduotuvėje. Tolesnėje lentelėje nurodomos galimos kiekvienos EKA parinkties konfigūracijos.

| EKA programa         | „Commerce Scale Unit“ | Pasiekiama neprisijungus |
|-------------------------|---------------|-------------------|
| MPOS, skirtas „Windows“        | Debesies arba RSSU | Taip               |
| MPOS, skirta „iOS“ arba „Android“ | Debesies arba RSSU | Ne                |
| „Cloud POS“               | Debesies arba RSSU | Ne                |

#### <a name="commerce-scale-unit"></a>„Commerce Scale Unit“

„Commerce Scale Unit“ yra komponentas, kuriame yra CRT. CRT aplinkoje yra visa verslo logika, kurą naudoja EKA, ir ji suteikia prieigą prie kanalo duomenų bazės. Kol jie prisijungę, visi parduotuvėje esantys EKA klientai naudojasi „Commerce Scale Unit“. „Commerce Scale Unit“ galima įdiegti debesyje arba parduotuvėje.

#### <a name="offline-mode"></a>Atjungties režimas

MPOS, skirtas „Windows“, palaiko atjungties režimą. Neprisijungus, EKA gali ir toliau tvarkyti pardavimus, net jei jis yra atjungtas nuo „Commerce Scale Unit“. Atkūrus ryšį, jį galima sinchronizuoti su kanalo duomenų baze. MPOS naudoja savo įdėtąjį CRT egzempliorių ir laikinai naudoja savo vietinį duomenų šaltinį (ne tinkle esančią „SQL Server“ duomenų bazę). Daugiau informacijos apie atjungties režimo funkcijas žr. [EKA atjungties režimo funkcijos](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>EKA periferinės (aparatinės) įrangos aspektai

Mažmenininkai taip pat turi apsvarstyti, kaip EKA pasieks įrenginius ir periferinius įrenginius, pvz., spausdintuvus, kasos stalčius ir mokėjimo terminalus. Tik MPOS, skirtas „Windows“, palaiko tiesioginį ryšį su šiais įrenginiais. MPOS, skirtas „Windows Phone“, „iOS“ arba „Android“, ir „Cloud POS“ reikia aparatūros stoties, kad galėtų gauti prieigą prie šių įrenginių. Aparatūros stotys gali būti skirtos EKA kasos aparatui arba bendrai naudojamos parduotuvės kasos aparatų. Išsamesnės informacijos apie aparatūros stotis žr. [„Retail“ aparatūros stoties konfigūracija ir diegimas](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Diegimo aplinkybės

Planuodami EKA diegimą parduotuvėse, atsižvelkite į toliau nurodytą informaciją.

- **Funkciniai reikalavimai**. Pagrindiniai verslo procesai ir galimybės yra tos pačios, nepriklausomai nuo platformos, formos koeficiento ar diegimo topologijos. Todėl daugumai mažmenininkų nereikia atsižvelgti į funkcinius reikalavimus, kai jie planuoja diegimą.
- **Jungiamumas** – tinklo prieinamumas (teritorinis tinklas \[WAN\] ir vietinis tinklas \[LAN\]) yra pagrindinis veiksnys, kurį reikia kruopščiai įvertinti. Bet kokia nauda išlaidų ir paprastumo požiūriu, kurią suteikia diegimo nereikalaujantis, debesyje veikiantis sprendimas, prarandama, jei sistema negalima svarbiems verslui procesams vykdyti.

    Išskyrus atvejus, kai tam tikro įrenginio jungiamumas yra labai patikimas ir atsparus arba jei tam tikras prastovos kiekis pardavėjui priimtinas, rekomenduojame vieną iš toliau nurodytų parinkčių:

    - Naudokite MPOS sistemoje „Windows“ ir įgalinkite atjungties režimą.
    - „Commerce Scale Unit“ diegimas patalpose.

    Šios dvi galimybės nėra nesuderinamos. Siekdami patikimiausios topologijos, mažmenininkai gali įdiegti vietinį RSSU, kad sumažintų priklausomybę nuo interneto ryšio arba „Azure“ prieinamumo. Jie taip pat gali įdiegti EKA kasos aparatus, kuriuose įgalintas atjungties režimas, jeigu kiltų vietinio serverio ar tinklo problema.

- **Aparatūros įrenginiai arba išoriniai įrenginiai**. Vienas svarbus „Retail POS“ sistemos aspektas yra jos galimybė naudoti EKA periferinius įrenginius, pvz., spausdintuvus, kasos stalčius ir mokėjimo terminalus. Nors visi galimi EKA variantai naudoja periferinius įrenginius, tik MPOS, skirtas „Windows“, palaiko juos tiesiogiai. Naudojant visas kitas programas, būtina viena arba daugiau aparatūros stočių. Nors šis metodas padidina lankstumą, būtina įdiegti, sukonfigūruoti ir prižiūrėti papildomus komponentus.
- **Sistemos reikalavimai**. EKA programos sistemos reikalavimai skiriasi. Prieš priimdami sprendimą, būtinai patikrinkite naujausią informaciją. Pavyzdžiui, kadangi CPOS veikia naršyklėje, jis palaiko daugiau operacinių sistemų. Daugiau informacijos apie sistemos reikalavimus žr. [Sistemos reikalavimai įdiegtims debesyje](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Diegimas ir priežiūra**. Diegimo ir priežiūros reikalavimų sudėtingumas gali skirtis, atsižvelgiant į programos ir diegimo pasirinkimus. Pavyzdžiui, diegiant debesies CPOS nereikia įdiegti ir atnaujinti kiekviename įrenginyje. Todėl šis metodas labai sumažina sudėtingumą ir išlaidas. Tačiau jei diegiate MPOS kiekviename kasos aparate ir įgalinate atjungties režimą bei taip pat diegiate bendrai naudojamas aparatūros stotis, gerokai padidinate galinių punktų, kuriuos reikia valdyti, skaičių.


[!INCLUDE[footer-include](../includes/footer-banner.md)]