---
title: Mobiliojo įrenginio vartotojo parametrai
description: Šioje temoje paaiškinama, kaip valdyti sandėlio darbuotojų mobiliojo įrenginio vartotojo parametrus.
author: MarkusFogelberg
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 77b4276cec5e046a19d6d001acf41fc410052fba
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049297"
---
# <a name="mobile-device-user-settings"></a>Mobiliojo įrenginio vartotojo parametrai

[!include [banner](../../includes/banner.md)]

Naujoje Sandėlio valdymo mobiliųjų įrenginių programėlėje yra programai skirtų parametrų rinkinys, padedantis pritaikyti vartotojų patirtį. Programą galima naudoti įvairių ekranų dydžių ir konfigūracijų (pvz., planšetinis kompiuteris, telefonas ar išmanusis laikrodis) įrenginiuose, todėl gali būti naudinga centralizuotai valdyti šiuos parametrus „Microsoft Dynamics 365 Supply Chain Management”.

*Mobiliojo įrenginio vartotojo parametrų* funkcija leidžia nustatyti visuotinius vartotojo parametrus, kurie bus naudojami visuose įrenginiuose. Taip pat galite nustatyti išsamesnius vartotojo parametrus, skirtus individualiems įrenginių prekių ženklams, įrenginių modeliams ir (arba) darbuotojams. Kai darbuotojas prisijungia prie Sandėlio valdymo mobiliųjų įrenginių programėlės, programa išrenką ir pritaiko konkrečių parametrų profilį, kuris saugomas „Supply Chain Management” ir yra atitinkamo prekės ženklo, įrenginio ir (arba) vartotojo ID.

Ši funkcija gali padėti darbuotojams greitai pradėti dirbti, kai tik jie pradeda naudoti naują įrenginį. Štai keletas pavyzdžių:

- Administratoriai gali nustatyti standartinį nuostatų rinkinį, kuris geriausiai veikia konkretaus gamintojo ir (arba) konkrečių įrenginių modelių įrenginiuose. Todėl darbuotojai gali pradėti naudoti naują įrenginį nekeisdami parametrų.
- Jei jūsų įmonėje yra identiškų įrenginių telkinys, kurį bendrai naudoja darbuotojai, darbuotojai matys norimą sąranką kiekvieną kartą prisijungdami, net jei jie niekada nenaudojo konkretaus fizinio įrenginio, kurį pasirinko nurodytą dieną.
- „Supply Chain Management” administratoriai gali peržiūrėti ir redaguoti visus išsaugotus parametrus, net ir atskirų darbuotojų. Ši galimybė gali padėti jiems pašalinti triktis arba tiksliai suderinti naujas funkcijas.

> [!IMPORTANT]
> *Mobiliojo įrenginio vartotojo parametrų* funkcija taikoma tik naujai Sandėlio valdymo mobiliųjų įrenginių programėlei. Jis neveikia senoje sandėlio programoje.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Mobiliojo įrenginio vartotojo parametrų funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Naujos sandėlio programos vartotojo parametrai, piktogramos ir veiksmų pavadinimai*

## <a name="create-and-manage-user-settings"></a>Vartotojo parametrų kūrimas ir valdymas

Norėdami kurti, peržiūrėti ir valdyti parametrų profilius visuose detalumo lygiuose, naudokite puslapį **Mobiliojo įrenginio vartotojo parametrai**. Pirmą kartą, kai darbuotojas redaguoja vartotojo parametrus naujame įrenginyje, naujas profilis automatiškai įtraukiamas į šį puslapį, jei jo dar nėra. Tada šis profilis atnaujinamas kiekvieną kartą, kai darbuotojas atlieka keitimą.

Taip pat galite nustatyti parametrų profilį, taikomą visiems įrenginių prekių ženklams, įrenginių modeliams ir (arba) darbuotojams. Tada galite padidinti detalumą pritaikydami daugiau konkrečių prekių ženklų, modelių ir (arba) darbuotojų parametrų.

Norėdami sukurti ir valdyti jūsų mobiliųjų įrenginių vartotojo nustatymus, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Mobilusis įrenginys \> Mobiliojo įrenginio vartotojo parametrai**.
1. Sąrašo srityje pasirinkite esamą vartotojo parametrų profilį, kad atidarytumėte jo įrašą. Arba, norėdami sukurti naują profilį, veiksmų srityje pasirinkite **Naujas**.

    Kiekvienas sąrašo srities profilis yra pažymėtas, kad nurodytų prekės ženklą, modelį ir (arba) vartotojo ID, kuriems taikomas profilis. Bendresnių profilių kai kurių arba visų šių charakteristikų reikšmė nustatyta į *Visi*.

1. Naujo ar pasirinkto parametrų profilio įrašo antraštės skyriuje nustatykite toliau pateiktus laukus.

    - **Įrenginio prekės ženklo pavadinimas** – pasirinkite įrenginio prekės ženklo pavadinimą, kuriam turi būti taikomas profilis. Jei profilis turi būti taikomas visiems prekių ženklams, palikite šį lauką tuščią. Reikšmių sąrašas apima visus jūsų sistemoje nustatytus prekės ženklus. Norėdami gauti informacijos apie tai, kaip apibrėžti prekių ženklų sąrašą, žr. kitą skyrių.
    - **Įrenginio modelio ID** – pasirinkite įrenginio modelį, kuriam turi būti taikomas profilis. Jei profilis turi būti taikomas visiems pasirinkto prekės ženklo modeliams, palikite šį lauką tuščią. Reikšmių sąraše pateikiami visi apibrėžti prekės ženklo, pasirinkto lauke **Įrenginio prekės ženklo pavadinimas**, modeliai. Norėdami gauti informacijos apie tai, kaip apibrėžti kiekvieno prekės ženklo modelių sąrašą, žr. kitą skyrių.
    - **Vartotojo ID** – pasirinkite sandėlio darbuotojo, kuriam turėtų būti taikomas parametrų profilis, vartotojo ID. Jei profilis turi būti taikomas visiems darbuotojams, palikite šį lauką tuščią.

1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Mygtukų padėtis** – pasirinkite, kaip mygtukus reikia išdėstyti įrenginyje. Programos elementai bus perkelti, kad geriau atitiktų darbuotojo nuostatas arba naudojimą. Galimos parinktys yra *Apačioje dešinėje (numatytoji)*, *Apačioje kairėje*, *Viršuje dešinėje* ir *Viršuje kairėje*.
    - **Ekrano padėtis** – pasirinkite ekrano padėtį, kuri programoje turi būti taikoma pagal numatytuosius nustatymus.
    - **Nuskaityti naudojant kamerą** – nustatykite šią parinktį į *Taip*, kad įvesties laukams nuskaityti būtų naudojama įrenginio kamera, kai pageidaujamas įvesties režimas nustatytas į *Nuskaitymas*. Jei jūsų įrenginyje yra įdiegtas skaitytuvas, nustatykite šią parinktį į *Ne*, kad naudotumėte skaitytuvą.
    - **Rodyti produkto nuotrauką** – pasirinkite, ar turi būti rodomos išleisto produkto nuotraukos, jei jų yra. Daugiau informacijos apie tai, kaip pridėti produkto vaizdus, žr. [Vaizdo pridėjimas prie produkto](../pim/tasks/add-image-product.md).
    - **Rodyti spalvų temą** – pasirinkite įrenginio spalvų temą.
    - **Garsumo lygis** – pasirinkite įrenginio garsumo lygį. Pasirinkite vertę nuo 0 (nulio) iki 10. Vertė *0* reiškia, kad nėra jokio garsumo, o vertė *10* reiškia didžiausią garsumą. Numatytoji vertė yra *4*.
    - **Vibracijos lygis** – pasirinkite įrenginio vibracijos lygį. Pasirinkite vertę nuo 0 (nulio) iki 5. Vertė *0* reiškia, kad nėra jokios vibracijos, o vertė *5* reiškia didžiausią vibraciją. Numatytoji vertė yra *1*.
    - **Teksto dydis procentais** – nurodykite teksto dydį standartinio dydžio procentais. Įveskite vertę nuo 70 iki 400. Vertė *70* reiškia mažiausią teksto dydį, o vertė *400* reiškia didžiausią teksto dydį. Numatytoji vertė yra *100*.
    - **Mygtukų dydis procentais** – nurodykite mygtukų dydį standartinio dydžio procentais. Įveskite vertę nuo 50 iki 200. Vertė *50* reiškia mažiausią mygtukų dydį, o vertė *200* reiškia didžiausią mygtukų dydį. Numatytoji vertė yra *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Mobiliojo įrenginio prekių ženklų kūrimas ir valdymas

Norėdami peržiūrėti, kurti ir valdyti įrenginio prekių ženklus ir modelius, kuriuos galima naudoti su jūsų parametrų profiliais, naudokite puslapį **Mobiliojo įrenginio prekių ženklai**. Mobiliųjų įrenginių programėlė automatiškai nuskaito ir pateikia vietinio prekės ženklo pavadinimą ir modelio ID pirmą kartą, kai darbuotojas redaguoja parametrus konkrečiame įrenginyje. Todėl dauguma šių įrašų paprastai bus sugeneruoti automatiškai. Tačiau taip pat galite valdyti visus įrašus šiame puslapyje. Pavyzdžiui, galite suteikti naudingesnius kiekvieno prekės ženklo ir modelio aprašymus, kad būtų lengviau atskirti panašius ar užšifruotus modelių ID.

Norėdami kurti ir valdyti jūsų mobiliųjų įrenginių prekių ženklus ir modelius, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Mobilusis įrenginys \> Mobiliojo įrenginio prekių ženklai**.
1. Sąrašo srityje pasirinkite mobiliojo įrenginio prekės ženklą, kad atidarytumėte jo įrašą. Arba, norėdami sukurti naują prekės ženklą, veiksmų srityje pasirinkite **Naujas**.
1. Naujo ar pasirinkto įrenginio prekės ženklo įrašo antraštės skyriuje nustatykite toliau pateiktus laukus.

    - **Įrenginio prekės ženklo pavadinimas** – įrenginio prekės ženklo pavadinimas, pvz., *„Microsoft Corporation”*.
    - **Aprašas** – aprašą galima įvesti norint padėti atskirti prekių ženklų pavadinimus.

1. „FastTab” **Mobiliojo įrenginio modeliai** rodomi visi pasirinkto įrenginio prekės ženklo modeliai. Naudokite mygtukus įrankių juostoje, norėdami įtraukti eilučių į tinklelį arba pašalinti jas. Kiekvienai eilutei nustatykite toliau pateiktus laukus.

    - **Įrenginio modelio ID** – įrenginio modelio ID, pvz., *„Surface Book 2”*.
    - **Aprašas** – aprašą galima įvesti norint padėti atskirti modelių ID.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas](install-configure-warehouse-management-app.md)
- [„Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas](step-icons-titles.md)