---
title: Inventoriaus matomumo papildinys
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114675"
---
# <a name="inventory-visibility-add-in"></a>Inventoriaus matomumo papildinys

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mirkopaslaugos, kuriso įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.

Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą. Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.

Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus. Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.

Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis. Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.

Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).

## <a name="install-the-inventory-visibility-add-in"></a>Įdiekite Inventoriaus matomumo papildinį

Jums reikia įdiegtį jį naudjant „Microsoft Dynamics Lifecycle Services“ (LCS). LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.

Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

- Gaukite LCS implementavimo projektą su mažiausiai viena patalpinta aplinka.
- Sukurkite beta raktus siūlydami LCS.
- Įjunkite beta raktus siūlydami LCS savo vartotojui.
- Susisiekite su „Microsoft Inventory Visibility“ produkto komanda ir pateikite aplinkos ID, kurioje norite talpinti papildinį.

Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Papildinio įdiegimas

Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

1. Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.
1. Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.
1. Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.
1. Aplinkos puslapyje eikite žemyn, kol pamatysite **Aplinkos papildiniai** skyrių. Jei skyrisu nematomas, įsitikinkite, kad būtinųjų sąlygų beta raktai yra visiškai sutvarkyti.
1. Skyriuje **Aplinkos papildiniai** rinkitės **Diegti naują papildinį**.
    ![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")
1. Rinkitės **Diegti naują papildinį** nuorodą. Esamų atvirų papildinių sąrašas.
1. Rinkitės **Inventoriaus paslaugos** iš sąrašo. (Atsiminkite, kad tai gali būti išvardyta kaip **Inventoriaus matomumo papildinys „Dynamics 365 Supply Chain Management“**.)
1. Įveskite tolesnes vertes tolesniiuose savo aplinkos laukeliuose:

    - **ĮTRAUKITE programos ID**
    - **ĮTRAUKITE nuomotojo ID**

    ![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")

1. Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.
1. Pasirinkti **Diegti**. Papildinio būsena bus rodoma kaip **diegiama**. Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.

### <a name="get-a-security-service-token"></a>Gaukite saugos paslaugų žymą

Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:

1. Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.
1. Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:
    - **„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metodas** - `GET`
    - **Teksto turinys (formos duomenys)**:

        | raktas | vertė |
        | --- | --- |
        | „client_id” | „${aadAppId}“ |
        | „client_secret” | „${aadAppSecret}“ |
        | „grant_type” | „client_credentials” |
        | ištekliai | „0cdb527f-a8d1-4bf8-9436-b352c68682b2“ |
1. Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Suformuluokite JSON užklausą, panašią į šią:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Kur:
    - Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.
    - Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.
    - Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.

1. Pateikite HTTP užklausą su šiomis ypatybes:
    - **„URL”** - `https://securityservice.operations365.dynamics.com/token`
    - **Metodas** - `POST`
    - **HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)
    - **Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.

1. Gausite  `access_token` atsakyme. Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API. Toliau pateikiamas pavyzdys.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Papildinio šalinimas

Norėdami išdiegti papildinį, pasirinkite **Išdiegti**. Paleiskite iš naujo LCS ir inventoriaus matomumo papildinys bus panaikintas. Išdiegimo procesas pašalins papildinio registraciją ir taip pat pradės darbą siekiant išvalyti visus verslo duomenis laikomus paslaugose.

## <a name="inventory-visibility-add-in-public-api"></a>Inventoriaus matomumo vieša API

Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus. Jis palaiko tris pagrindines sąveikos rūšis:

- Publikavimas turimų pakeitimų į papildinio formą išorės sistemoje.
- Laukimo turimi esami kiekiai iš išorės sistemos.
- Automatinis sinchronizavimas su „Supply Chain Management“ turimu.

Automatinis sinchronizavimas nėra viešos API dalis, tačiau vietoje to tvarkomas kontekste aplinkose, kurios įjungia inventoriaus matomumo papildinius.

### <a name="authentication"></a>Autentifikavimas

Platformos saugos žyma yra naudojama siekiant paskambinti inventoriaus matomumo papildiniui, todėl turite sukurti „Azure Active Directory“ žymą naudodami savo „Azure Active Directory“ programą.

Dėl daugiau informacijos apie tai, kaip gauti saugos žymą, žr. [Diegti inventoriaus matomumo papildinį](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Konfigūruoti Inventoriaus matomumo vieša API

Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose. Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos. Jis iš esmės turi keturias dalis:

- [Dalijimas](#partitioning)
- [Dimensijos konfigūravimai](#dimension-configurations)
- [Indeksavimas](#indexing)
- [Tinkintas matavimas](#custom-measurement)

#### <a name="partitioning"></a>Dalijimas

Dalijimas gali stipriai paveikti matomumo papildinio veikimą. Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.

Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*. Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensjia filtruose.

> [!NOTE]
> *Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume. „Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensijos konfigūravimai

Inventoriaus matomumas suteikia pagrindinų numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.

Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.

| Dimensijos tipas | Dimensijos pavadinimas |
|---|---|
| Produktas | `ColorId` |
| Produktas | `SizeId` |
| Produktas | `StyleId` |
| Produktas | `ConfigId` |
| Sekimas | `BatchId` |
| Sekimas | `SerialId` |
| Buvimo vieta | `LocationId` |
| Buvimo vieta | `SiteId` |
| Inventoriaus būsena | `StatusId` |
| Sandėliui konkretus | `WMSLocationId` |
| Sandėliui konkretus | `WMSPalletId` |
| Sandėliui konkretus | `LicensePlateId` |

> [!NOTE]
> Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais. Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.

Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.

Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius. Dėl integravimo, inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinš* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.

Tikslines nurodymas turi būti vienas iš:

- Numatyti nurodymai Inventoriaus matomumo
- Pasirinktinės dimensijos

Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai nurydmuose ir publikuoti įvykį su nurodymais.

#### <a name="indexing"></a>Indeksavimas

Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.

Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.

> [!NOTE]
> Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių. Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant implementuoti užtikrinant, kad atitiks jis jūsų verslo poreikius. Pavyzdžiui, jei norite laukti produktų tokia tvarka:

- Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.
- Kai kada norite tik laukti produkto bendrai.

Turite du indeksus nustatytus kaip:

- `["ColorId", "SizeId"]`
- `[]`

Tuštinkite skliaustelius pagal produkto ID su dalijimu.

Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus. Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`. Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.

Galite padėti savo laukimo kriterijus pagal būtiną tekstą.

Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Tinkintas matavimas

Numatytasis matavimo kiekiai yra susieti su „Supply Chain Management“, nepaisant to galite norėti turėti kiekį, kuris sudarytas iš numatytųjų priemonių derinių. Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimus laukimus.

Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.

Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Vartojimo sistema | Skaičiuotos priemonės | Duomenų šaltinis | Keitikas | Keitiko apskaičiavimo tipas |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Atimtis |

Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Išvestis `MyCustomAvailableforReservation` praemta apskaičiavimo nustatymais tinkintuose matavimuose:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Turimų keitimų publikavimas

Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono. Jo forma bus:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.

Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elementos duomenis su juo susietais. Pvz.:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Publikavimo turimų keitimų laukimo pavyzdys 1

Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.

Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose. Sistema automatiškai pavers tinkintas dimensijas į pagrindines.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Publikavimo turimų keitimų laukimo pavyzdys 2

Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją. Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reiškmės, tuščias ar balta erdvė.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON dokumento laukelip ypatybės

Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.

| Lauko ID | aprašymas |
|---|---|
| `id` | Unikalus ID konkrečiam keitimo įvykiui. Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart. |
| `organizationId` | Organizacijos identifikatorius susietas su įvykiu. Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID. |
| `productId` | Aptariamas produkto identifikatorius. |
| `quantity` | Kiekis, pagal kurį turimi poreikiai keičiami. Jei pavyzdžiui 10 naujų beigelių įtraukti į lentylą, vertė yra 10. Jei 3 beigeliai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3. |
| `dimensionDataSource` | Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje. Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio. Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas. Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimenseijas savo eilėse.   |
| `dimensions` | Dinaminis rakto maišas/verčių poros. Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos. |

### <a name="querying-current-on-hand"></a>Esamas turimas laukimas

Laukimo galutinis taškas esamame turimame bus panašus URL:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Jis bus laukiamas su HTTP `POST` metodu.

#### <a name="current-on-hand-query-example-1"></a>Esamas turimas laukimo pavyzdys 1

Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.

Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose. Sistema automatiškai pavers tinkintas dimensijas į pagrindines. Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`. Sistema automatiškai pavers tinkintas dimensijas į pagrindines.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Esamas turimas laukimo pavyzdys 2

Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją. Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reiškmės, tuščias ar balta erdvė.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Grįžtamojo rezultato pavyzdys

Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.
