---
title: Sandėlio nustatymas naudojant sandėlio konfigūracijos šabloną
description: Šiame straipsnyje paaiškinama, kaip nustatyti sandėlį naudojant sandėlio konfigūracijos šabloną.
author: yufeihuang
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: dafd51a46b19f3709963ffc12b3c8c77b6c809ac
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070446"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Sandėlio nustatymas naudojant sandėlio konfigūracijos šabloną

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti sandėlį naudojant sandėlio konfigūracijos šabloną. Galima naudoti kelis iš anksto nustatytus konfigūracijos šablonus. Informacijos apie tai, kaip naudoti šiuos šablonus, žr. [Konfigūracijos duomenų šablonai](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Atvejai, kada konfigūracijos šablonai gali būti naudingi

Konfigūracijos šablonai gali būti naudingi daugeliu atvejų. Štai keletas pavyzdžių:

- Jūs atlikote bei patikrinote konfigūracijos sąranką tikrinimo aplinkoje ir dabar norite kopijuoti sąranką į gamybos aplinką.
- Norite naudoti sandėlio sąranką keliuose juridiniuose subjektuose arba kurti naują sandėlį tame pačiame juridiniame subjekte.
- Norite greitai parengti sandėlio funkcijų demonstracinius duomenis.
- Norite, kad esami sandėliai ir prekės naudotų sandėlio valdymo funkcijas, o ne atsargų valdymo funkcijas.

Šiame straipsnyje sutelkiamas dėmesys pirmajame iš šių scenarijų. Joje parodoma, kaip galite naudoti konfigūracijos šabloną, norėdami konfigūracijos sąranką kopijuoti iš tikrinimo aplinkos į gamybos aplinką.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Konfigūracijos sąrankos kopijavimas iš tikrinimo aplinkos į gamybos aplinką

Šiuo atveju sandėlio ir kai kurių operacijų procesų konfigūracijos sąranka jau yra tikrinimo aplinkoje. Norite kopijuoti sandėlio konfigūracijos sąranką iš tikrinimo aplinkos į gamybos aplinką.

> [!NOTE]
> Kai kopijuojate konfigūracijos sąranką, svarbu įtraukti kitus susijusius sąrankos duomenis. Pavyzdžiui, norite nustatyti produktus kopijuodami sąranką iš tikrinimo aplinkos. Tačiau negalite nustatyti fiksuotos produkto paėmimo vietos, kol produktas nesukurtas. Nors atskiri konfigūracijos šablonai nepalaiko šio tipo priklausomybės, tam tikri numatytieji duomenų šablonai ją palaiko. Šiuos numatytuosius duomenų šablonus galite lengvai įtraukti į konfigūravimo procesą.

### <a name="export-a-default-warehouse-template"></a>Numatytojo sandėlio šablono eksportavimas 

1. Atidarykite darbo sritį **Duomenų valdymas**.

    > [!NOTE]
    > Jei naudojate šią darbo sritį pirmą kartą, prieš tęsdami turite įkelti visus duomenų objektus.

2. Pasirinkite plytelę **Šablonai**, tada pasirinkite **Įkelti numatytuosius šablonus**, kad įkeltumėte numatytuosius šablonus.

    > [!NOTE]
    > Parinktis **Įkelti numatytuosius šablonus** galima tik pasirinkus rodinį **Patobulintas**. Pasirinkite **Sistemos parametrai**, tada lauke **Peržiūrėti numatytąsias reikšmes** pasirinkite **Patobulintas rodinys**.

3. Įkėlus numatytuosius šablonus, galite juos keisti taip, kad jie atitiktų jūsų verslo poreikius.

    > [!NOTE]
    > Norėdami įkelti numatytuosius šablonus ir importuoti šablonus, turite turėti sistemos administratoriaus prieigos teisės. Šis reikalavimas padeda užtikrinti, kad visi objektai yra tinkamai įkelti į šabloną.

4. Įsitikinkite, kad naudojate juridinį subjektą, iš kurio norite eksportuoti konkrečios įmonės duomenis.
5. Darbo srityje pasirinkite **Eksportuoti**.
6. Kurkite naują eksportavimo projektą.
7. Pasirinkite **+ Įtraukti šabloną** ir raskite numatytąjį sandėlio šabloną **400 – WMS**. Šiame šablone įtraukti sandėlio konfigūracijos duomenų objektai.

    > [!NOTE]
    > Jei eksportuojami duomenys turi būti filtruojami (pavyzdžiui, norite eksportuoti tik duomenis, kurie yra susiję su konkrečiu sandėliu), turite įvertinti kiekvieną duomenų objektą ir įtraukti filtrus naudodami užklausą. Taip pat galite eksportuoti visus duomenis ir tada naikinti įrašus, kurie neprivalo būti paskirties failuose.

8. Pasirinkite **Eksportuoti**. Eksportuojami duomenys, susiję su visais duomenų objektais projekte.

Galite atsisiųsti duomenų paketo ZIP failą. Šiame faile visi duomenys pateikiami pasirinktu formatu (pvz., „Excel“ formatu). Kaip nurodyta, kai kurių įrašų duomenis duomenų paketo failuose gali reikėti atnaujinti, prieš importuojant juos į gamybos aplinką. Jei atnaujinate įrašą, įsitikinkite, kad nepakeičiate failo vardo.

### <a name="import-a-warehouse-configuration-setup"></a>Sandėlio konfigūracijos sąrankos importavimas

1. Įsitikinkite, kad paskirties aplinkoje pasirinkote įmonę, į kurią norite importuoti į sandėlio duomenis.

    > [!NOTE]
    > Prieš importuodami, turi identifikuoti visas duomenų priklausomybes. Pvz., šablonas **Sandėlio valdymas** apima duomenų objektą, pavadintą **Sandėlio perdavimo kodai**. Šiame objekte yra duomenys, susiję su sąrankos puslapiu **Perdavimo kodai** (**Sandėlio valdymas** > **Sąranka** > **Mobilusis įrenginys** > **Perdavimo kodai**). Jei esamoje sąrankoje jau tvarkomas pardavimo užsakymų grąžinimo procesas, lauko **Grąžinimo perdavimo kodas** reikšmė nurodyta. Šiame lauke pateiktas perdavimo kodas yra susijęs duomenų objektų **Perdavimo kodas**, kuris yra šablono **Pardavimas ir rinkodara** dalis. Jei duomenų importavimas iš duomenų objekto **Perdavimo kodas** nėra importuojamas prieš importuojant duomenis iš lauko **Sandėlio perdavimo kodai**, importavimas nepavyks.

2. Darbo srityje **Duomenų valdymas** pasirinkite **Importavimas**.
3. Kurkite naują importavimo projektą.
4. Pasirinkite **+ Įtraukti failą** ir nusiųsti duomenų paketo ZIP failą.
5. Pasirinkite **Importuoti**. Rodinyje **Patobulintas** galite naudoti parinktį **Filtras**, norėdami greitai peržiūrėti problemas, kurios gali kilti importuojant.

Žurnale **Vykdymo peržiūra** pateikiama išsami informacija apie kiekvieną duomenų objektą, kuris yra importuotas. Galite naudoti išdėstymo duomenų rodinį, norėdami greitai pasiekti paskirties duomenis. Tokiu būdu galite peržiūrėti, kaip importuoti duomenys rodomi susijusiuose programos puslapiuose. Naudojant numatytuosius duomenų šablonus, kiekvieno duomenų objekto importavimo seka vykdoma iš anksto nustatytu būdu, siekiant užtikrinti, kad pirmiausia importuojami visi priklausomi duomenys. Jei pasirinktiniai duomenų objektai yra projekto dalis, turite įsitikinti, kad apibrėžta teisinga seka. Daugiau informacijos žr. [ Konfigūracijos duomenų šablonai](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

Norėdami daugiau sužinoti, kaip naudoti sandėlio šabloną sandėlio konfigūracijai kopijuoti iš vienos įmonės į naują to paties egzemplioriaus įmonę, žr. šį 3 minučių YouTube [vaizdo įrašą apie tai, kaip naudoti sandėlio šabloną kopijuoti finansų ir operacijų konfigūraciją](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-article"></a>Susijęs straipsnis

[Konfigūracijos duomenų šablonai](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
