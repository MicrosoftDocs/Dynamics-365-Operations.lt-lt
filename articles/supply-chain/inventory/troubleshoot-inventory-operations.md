---
title: Atsargų operacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti klaidas, su kuriomis galite susidurti dirbdami su atsargų operacijomis.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967160"
---
# <a name="troubleshoot-inventory-operations"></a>Atsargų operacijų trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti klaidas, su kuriomis galite susidurti dirbdami su atsargų operacijomis.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nerandu atsargų žurnalų išplečiamojo dialogo lango „Darbo eiga”.

### <a name="issue-description"></a>Problemos aprašas

Nerandate išplečiamojo dialogo lango **Darbo eiga** žurnalo puslapyje arba susijusios darbo eigos operacijos negalimos.

Ši problema gali atsirasti dėl trijų priežasčių, pateikiamų šiuose poskyriuose.

### <a name="issue-resolution-1"></a>Problemos sprendimo būdas Nr. 1

Jei su problema susiduria visi vartotojai, tikėtina, kad ji kartojasi, nes darbo eigos patvirtinimas nebuvo priskirtas žurnalo pavadinime. Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Atsargų valdymas &gt; Sąranka &gt; Žurnalo pavadinimai &gt; Atsargos**.
1. Sąrašo srityje pasirinkite žurnalo pavadinimą, kad atidarytumėte nustatymus.
1. **Bendras** „FastTab“ skirtuke nustatykite **Patvirtinimo darbo eiga** parinktį į *Taip*. Jei atsirado pranešimas, raginantis patvirtinti pakeitimą, pasirinkite **Taip**.
1. Lauke **Darbo eiga** lauke pasirinkite darbo eigą, kurią norite naudoti pasirinktam žurnalo pavadinimui.

### <a name="issue-resolution-2"></a>Problemos sprendimo būdas Nr. 2

Jei jūsų darbo eigoje naudojamas pritaikytas kodas, atnaujinus sistemą, gali kilti problemų. Pavyzdžiui, žurnalo darbo eigoje mygtukas **Pateikti** gali būti neaktyvus, kad negalėtumėte jo paspausti pateikimui patvirtinti.

Jeigu mygtukas **Pateikti** neaktyvus, jūsų darbo eiga gali būti tinkinta, vadinasi, darbo eigos metodas `canSubmitToWorkflow()`  `FormDataUtil`buvo praplėstas. Norėdami išspręsti šią problemą, pakeiskite būdą, kuriuo praplečiate `canSubmitToWorkflow()`metodą, kad naudotumėte struktūrą pagal šį pavyzdį.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Problemos sprendimo būdas Nr. 3

Jei su problema susiduria tik keli konkretūs vartotojai, tie vartotojai gali neturėti saugos teisių, kurių reikia norint vykdyti darbo eigos operacijas atsargų žurnaluose. Patikrinkite, ar kiekvienas su problema susidūręs vartotojas turi *Tvarkyti atsargų žurnalo darbo eigą* saugos teisę. Pagal numatytuosius nustatymus, ši teisė priskiriama pareigai, užvadintai tuo pačiu pavadinimu, ir ši pareiga taikoma *Sandėlio darbuotojas* ir *Sandėlio vadovas* vaidmenims.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Mano atsargų žurnalo būsena – užrakinta sistemoje, o darbo eigos paketinė užduotis neveikia.

### <a name="issue-description"></a>Problemos aprašas

Vienas iš jūsų atsargų žurnalų užrakintas dėl tam tikros operacijos ir jis nėra atrakintas. Pavyzdžiui, jei registruojant įvyksta nežinoma klaida (tai yra sistemos užrakto operacija), žurnalo būsena gali išlikti sistemos užrakinta. Šiuo atveju darbo eigos darbo elementų apdorojimo programa parodys klaidą, kol tikrins užraktą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Prisijunkite prie „Supply Chain Management” „SQL Server” programos ir patikrinkite, ar **InventJournalTable.SystemBlocked** yra nustatyta *1*. Jei taip, įsitikinkite, kad žurnalo būsena nebūtų užrakinta, tada iš naujo nustatykite **InventJournalTable.SystemBlocked** *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Mano atsargų žurnalo darbo eiga niekada neužbaigiama ir žurnalo negalima redaguoti ar registruoti.

### <a name="issue-description"></a>Problemos aprašas

Kai pateikiate žurnalo patvirtinimo darbo eigą, darbo eigos apdorojimas nustoja reaguoti ir jūs negalite redaguoti ar apdoroti savo žurnalų.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Yra kelios priežastys, kodėl gali būti nebaigimas darbo eigos apdorojimas. Patikrinkite, ar yra šios problemos:

- Eikite į **Atsargų valdymas &gt; Sąranka&gt;Atsargų valdymo darbo eigos** ir peržiūrėkite paveiktos darbo eigos konfigūraciją. Daugiau informacijos žr. [Atsargų žurnalo patvirtinimo darbo eigos](inventory-journal-workflow.md).
- Gali įvykti darbo eigos išimtis arba klaida. Peržiūrėkite paveiktos darbo eigos darbo elementų retrospektyvą ir sužinokite, ar joje yra programos klaida, nutraukusi darbo eigą.
- Atsargų žurnalą galima atnaujinti arba redaguoti, tik jei jis patvirtintas. Jei atšaukimas aktyvus, galite bandyti atšaukti žurnalą. Darbo eigos paketinės užduoties vykdymas gali būti sustabdytas dėl kelių priežasčių. Kai kurios iš šių priežasčių galėjo kilti dėl darbo eigos sistemos problemos.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu

### <a name="issue-description"></a>Problemos aprašas

Ši problema gali kilti jei, pvz., bandysite išlaidų sumai nustatyti atsargų žurnalo darbo eigos sąlygą. Nustatykite sąlygą, kad 1-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra mažesnė nei 100. Tada nustatykite kitą sąlygą, kad 2-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra didesnė arba lygi 100. Tada, kai darbo eiga vykdoma, darbo eigos retrospektyvoje rodoma tik viena eilutė, o pirmoji sąlyga visuomet vertinama kaip *true* nepaisant pateiktosios vertės.

### <a name="issue-workaround"></a>Problemos sprendimas

Dabartiniame leidime atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu. Toks veikimo būdas yra numatytas. Rekomenduojame nustatyti sąlygos kriterijus tik žurnalo lygio atributams.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Turimų atsargų sąrašo puslapio filtravimo sritis nefiltruoja rezultatų, kurių tikiuosi.

### <a name="issue-description"></a>Problemos aprašas

Filtro srities filtrai **Turimas sąrašas**  puslapyje nefiltruoja rezultatų, kurių tikitės.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas.

 **Turimas sąrašas** puslapis sudėliotas iš detalizuotos turimų atsargų lentelės, kurioje pateiktos visos galimos dimensijos. Nepaisant to, sąrašas šiame puslapyje santrauka. Dėl to, tai gali apimti eilutes iš šaltinio lentelės apimant vertes pagal rodomas dimensijas.

Filtrai, nustatyti filtrų srityje, taikomi šaltinio lentelei, tačiau ne apibendrintam sąrašui. Šis veikimas kartais gali lemti netikėtus rezultatus kaip nurodyta [šiuose pavyzdžiuose](inventory-on-hand-list.md#examples).

Tačiau  [tinklelyje pateikti filtrai](inventory-on-hand-list.md#grid-filters) *atlikti*  taikomas apibendrintam sąrašui. Šie filtrai apima tiek „QuickFilter“ tinklelio viršuje, tiek filtrą kiekvieno stulpelio antraštėje.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Vienetas ir vienetų kiekis atsargų žurnale veikia netinkamai.

### <a name="issue-description"></a>Problemos aprašas

Kai dirbate su atsargų žurnalo vienetais ir kiekiais atsargų žurnale, galite susidurti su viena ar abiem problemomis.

- Nematote vienetų arba vienetų kiekių atsargų žurnale, kol vienetų konvertavimas nustatytas išleistam produktui, ir negalite pakeisti vieneto atsargų žurnale.
- Matote **Kiekis** ir **Vienetas** laukus atsargų žurnale, bet nematote lauko **Vieneto kiekis**. Jei pakeisite vienetą, įvesite kiekį ir užregistruosite žurnalą, žurnale vis tiek bus rodomas pradinis to kiekio matavimo vienetas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.

1. Darbo eigoje **Funkcijų valdymas** įsitikinkite, kad funkcija *Matavimo vienetų ir vienetų kiekio naudojimas atsargų žurnaluose* yra įjungta. Ši funkcija prideda laukus **Vienetas** ir **Vieneto kiekis** į žurnalą.
1. Įjungus šią funkciją, naudokite laukus **Kiekis**, **Vieneto kiekis** ir **Vienetas** laukus tokiu būdu:

    - **Kiekis** – nurodykite kiekį, naudodami numatytąjį vienetą, nurodytą išleistam produktui. Tačiau numatytasis vienetas čia nerodomas. Jei konvertavimas nustatytas tarp numatytojo vieneto ir vieneto, pasirinkto lauke **Vienetas**, laukas **Kiekis** yra automatiškai atnaujinimas pagal pasirinkimus laukuose **Vieneto kiekis** ir **Vienetas**.
    - **Vieneto kiekis** – nurodykite kiekį naudodami kiekį, pasirinktą lauke **Vienetas**.
    - **Vienetas** – pasirinkite vienetą, kurį norite taikyti vertei lauke **Vieneto kiekis**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Gaunu tokį klaidos pranešimą: „Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0.”

### <a name="issue-description"></a>Problemos aprašas

Kai bandote užregistruoti atsargų operaciją arba atsargų rezervavimą, gaunate tokį klaidos pranešimą: „Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0.”

Ši problema kyla tada, kai atsargų operacijos kiekis nurodomas kaip dešimtainė vertė, kuri yra mažesnė už lauke palaikomą tikslumo lygį. Pavyzdžiui, nurodytas atsargų operacijos *0,5* kiekis, bet tik sveikųjų skaičių kiekiai yra palaikomi. Todėl vertė turi būti *1* vietoje *0,5*.

### <a name="issue-resolution"></a>Problemos paaiškinimas

1. Paleiskite šį scenarijų „SQL Server” programoje, kad suapvalintumėte kiekius atsargų operacijose. Šis scenarijus pataisys lentelės **inventTrans** vertes.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Paleiskite turimo vientisumo patikrą, kai **taisyti klaidą** parinktis yra įjungta. Šis patikrinimas ištaisys vertes lentelėje **inventSum**.

> [!IMPORTANT]
> Itin rekomenduojame, kad atidžiai redaguotumėte scenarijų, kaip to reikalaujama jūsų aplinkoje, atliktumėte testavimą testavimo aplinkoje ir patikrintumėte rezultatų duomenis prieš paleisdami scenarijų gamybos aplinkoje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]