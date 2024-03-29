---
title: Įspėjimo taisyklių kūrimas
description: Šiame straipsnyje pateikiama informacija apie įspėjimus ir paaiškinama, kaip sukurti įspėjimo taisyklę.
author: RichdiMSFT
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a420c5b2a036ac63a1a179f93462d152c3941fda
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124231"
---
# <a name="create-alert-rules"></a>Įspėjimo taisyklių kūrimas

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Darbo pradžia

Prieš nustatydami įspėjimo taisyklę nuspręskite, kada ar kokiais atvejais norite gauti įspėjimus. Kai žinote, apie kokį įvykį norite būti įspėti, raskite puslapį, kuriame pateikiami duomenys, esantys to įvykio priežastimi. Įvykis gali būti tam tikra atėjusi diena arba atliktas konkretus pakeitimas. Todėl turite rasti puslapį, kuriame nurodyta data arba vietą, kurioje rodomas pasikeitęs laukas arba sukurtas naujas įrašas. Turėdami šią informaciją, galite kurti įspėjimo taisyklę.

Kai sukuriate įspėjimo taisyklę, nustatote kriterijus, kuriuos reikia įvykdyti prie suaktyvinant įspėjimą. Kriterijus iš esmės yra įvykio buvimo ir nurodytų sąlygų tenkinimo sutapimas. Kai įvykis įvyksta, sistema pradeda tikrinti atsižvelgdama į nustatytas sąlygas.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Įsitikinkite, kad įspėjimų paketinės užduotys vykdomos

Norint, kad būtų apdorotos įspėjimų sąlygos ir siunčiami pranešimai, reikia vykdyti duomenų keitimo ir terminų įspėjimų paketines užduotis. Norėdami vykdyti paketines užduotis, eikite į **Sistemos administravimas** > **Periodinės užduotys** > **Įspėjimai** ir įtraukite naują paketinę užduotį **Keisti pagrįstus įspėjimus** ir / arba **Termino įspėjimai**. Jei reikia, kad paketinė užduotis būtų vykdoma ilgai ir dažnai, pasirinkite **Pasikartojimas** ir nustatykite **Nėra pabaigos datos**, kurios **Pasikartojimo šablonas** būtų **Minutės**, o **Skaičius** – **1**.

## <a name="events"></a>Įvykiai

Įvykis, kuris suaktyvina įspėjimo taisyklę, gali būti atėjusi tam tikra diena arba konkretus įvykęs pasikeitimas. Įvykių paleidikliai apibrėžti dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai**. Konkrečiam laukui priskirti įvykiai priklauso nuo pasirinkto paleidiklio.

Pavyzdžiui, jei nustatote įspėjimo taisyklę, skirtą laukui **Pradžios data**, tinkami termino įvykiai. Todėl `is due in` (termino) tipo įvykis galimas tam laukui. Tačiau tokiam laukui kaip **Išlaidų centras** termino tipo įvykis nėra tinkamas. Todėl `is due in`(termino) tipo įvykis negalimas tam laukui. Vietoj to, `has changed` (pasikeitė) tipo įvykis yra galimas.

## <a name="event-types"></a>Įvykių tipai

Toliau nurodyti trijų tipų įvykiai, kurie gali įvykti.

- **Kūrimo ir naikinimo tipų įvykiai** – šie įvykiai suaktyvina įspėjimą, kai sukuriamas arba panaikinamas įrašas.
- **Naujinimo tipo įvykiai** – šie įvykiai suaktyvina įspėjimą, kai pasikeičia konkretaus lauko duomenys.
- **Termino tipo įvykiai** – šie įvykiai suaktyvina įspėjimą, kai ateina tam tikra diena.
    
Įvykusius pakeitimus gali inicijuoti vartotojas. Pavyzdžiui, vartotojas pakeičia pirkimo užsakymo pristatymo datą. Be to, pakeitimai gali įvykti kaip proceso dalis. Pavyzdžiui, puslapio laukas **Būsena** pasikeičia, kad atspindėtų įvairių sistemos procesų ciklą.

## <a name="conditions"></a>Sąlygos

Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane dėl** galite naudoti sąlygas, kad valdytumėte, kada jus įspėti apie įvykius.

Pavyzdžiui, galite nurodyti, kad sistema turėtų jus įspėti, kai pasikeičia pirkimo užsakymų būsena, tačiau tik jei būsena atitinka tam tikrą sąlygų rinkinį. Pavyzdžiui, jūs norite, kad jus įspėtų, kai pirkimo užsakymo būsena pasikeičia į **Gauta**. Šis būsenos pasikeitimas yra įvykis, kuri suaktyvina įspėjimą.

Taip pat turite nuspręsti, apie kuriuos pirkimo užsakymus reikia jus įspėti. Pavyzdžiui, galite pasirinkti vieną iš toliau nurodytų parinkčių. Šios pasirinktis nurodo įspėjimo taisyklės sąlygas.

- **Dabartinis pasirinktas įrašas** – gaunate įspėjimą, kai konkretaus pirkimo užsakymo būsena pasikeičia į **Gauta**.
- **Visi įrašai** – gaunate įspėjimą, kai prekės pirkimo užsakymo būsena pasikeičia aktyvaus puslapio rodinyje. Kurdami tam tikrų įrašų taisykles galite naudoti puslapyje pateiktus išplėstinius filtrus. Pavyzdžiui, galite kurti įspėjimą, kuris suaktyvinamas, kai pasikeičia visų pirkimo užsakymų, susijusių su konkrečios klientų grupės klientais, būsena.
    
## <a name="expiry-of-rule"></a>Taisyklės galiojimo pabaiga

Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane iki** galite nurodyti, kiek laiko įspėjimo taisyklė turėtų būti aktyvi.

## <a name="alert-contents"></a>Įspėjimo turinys

Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane nurodant** galite nurodyti pranešimo temą ir tekstą, kurios bus naudojamos įspėjimų pranešimuose.

## <a name="user-id"></a>Vartotojo ID

Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane ir** galite nurodyti, kuris vartotojas turėtų gauti įspėjimo gauti įspėjimų pranešimus. Pagal numatytuosius parametrus pasirinktas jūsų vartotojo ID. Galimybė pakeisti įspėjimą gaunantį vartotoją yra apribota organizacijos administratoriais.

## <a name="alerts-as-business-events"></a>Įspėjimai kaip verslo įvykiai

Galite siųsti įspėjimus išoriškai naudodami verslo įvykių sistemą. Kurdami įspėjimą, nustatykite **Organizacijos mastu** kaip **Ne**, o **Siųsti į išorę** kaip **Taip**. Gavę verslo įvykio įspėjimą, galite įjungti eigą, Power Automate **įtaisytą** naudojant verslo įvykį, kai verslo įvykis paleidžiamas finansų ir operacijų jungtyje, **arba tiesiogiai nusiųsti įvykį verslo įvykių galui per verslo įvykių katalogą**.

## <a name="create-an-alert-rule"></a>Įspėjimo taisyklės kūrimas

0. Įsitikinkite, kad įspėjimų paketinės užduotys vykdomos (žr. viršuje).
1. Atidarykite puslapį, kuriame yra norimi stebėti duomenys.
2. Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti įspėjimo taisyklę**.
3. Dialogo lango **Įspėjimo taisyklės kūrimas** lauke **Laukas** pasirinkite lauką, kurį norite stebėti.
4. Lauke **Įvykis** pasirinkite tinkamumo įvykio tipą.
5. „FastTab“ **Įspėti mane dėl** pasirinkite norimą parinktį. Jei norite siųsti įspėjimą kaip verslo įvykį, nustatykite **Organizacijos mastu** reikšmę į **Ne**.
6. Jei norite, kad nuo tam tikros dienos įspėjimo taisyklė būtų neaktyvi, „FastTab“ **Įspėti mane iki** pasirinkite pabaigos datą.
7. „FastTab“**Įspėti mane ir** lauke **Tema** pasirinkite numatytąją el. laiško antraštės temą arba įveskite naują temą. Tekstas tampa temos antrašte el. laiške, kurį gausite, kai bus suaktyvintas įspėjimas. Jei norite siųsti įspėjimą kaip verslo įvykį, nustatykite **Siųsti į išorę** kaip **Taip**.
8. Lauke **Pranešimas** įveskite pasirinktinį pranešimo tekstą. Tekstas tampa pranešimu, kurį gausite, kai bus suaktyvintas įspėjimas.
9. Pasirinkite **Gerai** norėdami išsaugoti parametrus ir sukurti įspėjimo taisyklę.

## <a name="limitations-and-workarounds"></a>Apribojimai ir problemų sprendimai

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Įspėjimų kūrimo formos antriniuose duomenų šaltiniuose problemos sprendimas
Negalite kurti įspėjimų kai kuriuose formų antrinių duomenų šaltiniuose. Pavyzdžiui, kuriant įspėjimus kliento arba tiekėjo registravimo šablonų formoje, galimi tik antraštės laukai (CustLedger arba VendLedger), o ne dimensijų sąskaitos. Šio apribojimo problemos sprendimas yra naudoti **SysTableBrowser**, kad ši lentelė būtų atidaryta kaip pirminis duomenų šaltinis. 
1. Atidarykite lentelę formoje **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Sukurkite įspėjimą iš formos SysTableBrowser.

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a>Pokyčiais grįsti įspėjimai neveikia partijos būsenos pakeitimams
Pokyčiu grįsti įspėjimai neveikia su partijos būsenos pakeitimais, nes jie išjungti dėl našumo priežasčių. Todėl turėtumėte nustatyti **paketo įspėjimų** galimybę. Daugiau informacijos rasite skyriuje [Patobulintų paketinių formų įspėjimų nustatymas](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
