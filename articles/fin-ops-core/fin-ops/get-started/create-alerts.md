---
title: Įspėjimo taisyklių kūrimas
description: Šioje temoje pateikiama informacija apie įspėjimus ir paaiškinama, kaip kurti įspėjimo taisyklę, kad būtumėte įspėti apie įvykius, pvz., atėjusią tam tikrą dieną arba konkretų įvykusį pasikeitimą.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: c37ddc52ef576a15dd35cc155e99821c74631a46
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180719"
---
# <a name="create-alert-rules"></a>Įspėjimo taisyklių kūrimas

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Darbo pradžia

Prieš nustatydami įspėjimo taisyklę nuspręskite, kada ar kokiais atvejais norite gauti įspėjimus. Kai žinote, apie kokį įvykį norite būti įspėti, raskite puslapį, kuriame pateikiami duomenys, esantys to įvykio priežastimi. Įvykis gali būti tam tikra atėjusi diena arba atliktas konkretus pakeitimas. Todėl turite rasti puslapį, kuriame nurodyta data arba vietą, kurioje rodomas pasikeitęs laukas arba sukurtas naujas įrašas. Turėdami šią informaciją, galite kurti įspėjimo taisyklę.

Kai sukuriate įspėjimo taisyklę, nustatote kriterijus, kuriuos reikia įvykdyti prie suaktyvinant įspėjimą. Žinokite, kad kriterijus yra įvykio buvimo ir nurodytų sąlygų tenkinimo sutapimas. Kai įvykis įvyksta, sistema pradeda tikrinti atsižvelgdama į nustatytas sąlygas.

## <a name="events"></a>Įvykiai

Įvykis, kuris suaktyvina įspėjimo taisyklę, gali būti atėjusi tam tikra diena arba konkretus įvykęs pasikeitimas. Įvykių paleidikliai apibrėžti dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai**. Konkrečiam laukui priskirti įvykiai priklauso nuo pasirinkto paleidiklio.

Pavyzdžiui, jei nustatote įspėjimo taisyklę, skirtą laukui **Pradžios data**, tinkami termino įvykiai. Todėl tipo **terminas** įvykis priskiriamas tam laukui. Tačiau tokiam laukui kaip **Išlaidų centras** termino tipo įvykis nėra tinkamas. Todėl tipo **terminas** įvykis nepriskiriamas tam laukui. Priskiriamas tipo **pasikeitė** įvykis.

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

Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane ir** galite nurodyti, kuris vartotojas turėtų gauti įspėjimo gauti įspėjimų pranešimus. Pagal numatytuosius parametrus pasirinktas jūsų vartotojo ID. Šią parinktį gali naudoti tik organizacijos administratoriai.

## <a name="create-an-alert-rule"></a>Įspėjimo taisyklės kūrimas

1. Atidarykite puslapį, kuriame yra norimi stebėti duomenys.
2. Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti įspėjimo taisyklę**.
3. Dialogo lango **Įspėjimo taisyklės kūrimas** lauke **Laukas** pasirinkite lauką, kurį norite stebėti.
4. Lauke **Įvykis** pasirinkite tinkamumo įvykio tipą.
5. „FastTab“ **Įspėti mane dėl** pasirinkite parinktį.
6. Jei norite, kad nuo tam tikros dienos įspėjimo taisyklė būtų neaktyvi, „FastTab“ **Įspėti mane iki** pasirinkite pabaigos datą.
7. „FastTab“**Įspėti mane ir** lauke **Tema** pasirinkite numatytąją el. laiško antraštės temą arba įveskite naują temą. Tekstas yra naudojamas kaip temos antraštė el. laiške, kurį gausite, kai bus suaktyvintas įspėjimas.
8. Lauke **Pranešimas** įveskite pasirinktinį pranešimo tekstą. Tekstas yra naudojamas kaip pranešimas, kurį gausite, kai bus suaktyvintas įspėjimas.
9. Pasirinkite **Gerai** norėdami išsaugoti parametrus ir sukurti įspėjimo taisyklę.
