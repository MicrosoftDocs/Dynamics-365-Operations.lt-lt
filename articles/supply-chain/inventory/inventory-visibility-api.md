---
title: Atsargų matomumo viešos API
description: Šioje temoje aprašomos viešos API, kurios pateikiamos pagal atsargų matomumą.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343637"
---
# <a name="inventory-visibility-public-apis"></a>Atsargų matomumo viešos API

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos viešos API, kurios pateikiamos pagal atsargų matomumą.

Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus. Jis palaiko keturis pagrindines sąveikos rūšis:

- Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas
- Turimų atsargų kiekių nustatymas arba nepaisimas prie išorinės sistemos priedo
- Publikavimas rezervavimo įvykių į papildinio formą išorės sistemoje
- Dabartinių turimų kiekių užklausos iš išorės sistemos

Toliau pateiktoje lentelėje nurodytos API esamos parinktys:

| Kelias | Metodas | Aprašas |
|---|---|---|
| /api/aplinka/{environmentId}/turi būti | Skelbti | [Kurti vieną turimos informacijos pakeitimo įvykį](#create-one-onhand-change-event) |
| /api/aplinka/{environmentId}/turi būti/bendras | Skelbti | [Kurti kelis pakeitimo įvykius](#create-multiple-onhand-change-events) |
| /api/aplinka/{environmentId}/stovintis/{inventorySystem}/bendras | Skelbti | [Nustatyti/nepaisyti turimos informacijos kiekių](#set-onhand-quantities) |
| /api/aplinka/{environmentId}/turi būti/rezervavimas | Skelbti | [Kurti vieną rezervavimo įvykį](#create-one-reservation-event) |
| /api/aplinka/{environmentId}/turi būti/rezervavimas/bendras | Skelbti | [Kurti kelis rezervuoti įvykius](#create-multiple-reservation-events) |
| /api/aplinka/{environmentId}/turi būti/indekso užklausa | Gauti | [Užklausa naudojant skelbimo metodą](#query-with-post-method) |
| /api/aplinka/{environmentId}/turi būti/indekso užklausa | Skelbti | [Užklausa naudojant gavimo metodą](#query-with-get-method) |

„Microsoft" pateikė "out-of-box *Paštininko* užklausų rinkinį. Šį rinkinį galite importuoti į savo *paštininko* rango programinę įrangą naudodami šį bendrai naudojamą saitą: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Rasti galinį punktą pagal „Lifecycle Services“ aplinką

Atsargų matomumo mikrotara įdiegta „Microsoft Azure Service Fabric“ regionams ir keliuose regionuose. Šiuo metu nėra centrinio galinio punkto, kuris gali automatiškai nukreipti jūsų prašymą į atitinkamą geografijos ir regiono informaciją. Todėl informacijos dalis turite sus sudaro į URL naudodami šį šabloną:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Trumpą regiono pavadinimą galima rasti ciklo „Microsoft Dynamics Lifecycle Services“ (LCS) aplinkoje. Toliau pateiktoje lentelėje regioniniai API esamos parinktys.

| „Azure“ regionas | Trumpas regiono pavadinimas |
|---|---|
| Rytų Australija | eau |
| Pietryčių Australija | seau |
| Centrinė Kanada | cca |
| Rytų Kanada | eca |
| Šiaurės Europa | neu |
| Vakarų Europa | weu |
| Rytų JAV | eus |
| Vakarų JAV | wus |
| Pietų UK | Suk |
| Vakarų JK | sąrašas |

Salos numeris yra ten, kur jūsų LCS aplinka įdiegta „Service Fabric“. Šiuo metu nėra būdo gauti šią informaciją iš vartotojo pusės.

„Microsoft“ sukūrė vartotojo sąsają (UI) tam, kad gautumėte „Power Apps“ visą mikroservice galinį punktą. Daugiau informacijos žr. [Surasti paslaugų galinį tašką](inventory-visibility-power-platform.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikavimas

Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo viešui API iškviesti. Todėl turite sugeneruoti _„Azure Active Directory“ („Azure AD“) atpažinimo ženklą_, naudodami savo „Azure AD“ programą. Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte _prieigos atpažinimo ženklą_.

Gaukite saugos paslaugų žymą atlikdami taip.

1. Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` vertes Jūsų „Dynamics 365 Supply Chain Management“ programa.
1. Iškvieskite „Azure AD” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metodas:** `GET`
    - **Teksto turinys (formos duomenys):**

        | Raktas | Reikšmė |
        |---|---|
        | „client_id” | „${aadAppId}“ |
        | „client_secret” | „${aadAppSecret}“ |
        | „grant_type” | „client_credentials” |
        | ištekliai | „0cdb527f-a8d1-4bf8-9436-b352c68682b2“ |

    Kaip atsakymą turėtumėte „Azure AD“ gauti (`aadToken`) atpažinimo ženklą. Ji turi atitikti šį pavyzdį.

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

1. Formuluoja „JavaScript" objekto notacijos (JSON) užklausą, panašią į šį pavyzdį.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Atkreipkite dėmesį į toliau nurodytus punktus.

    - Vertė `client_assertion` turi būti „Azure AD“ žetonas (`aadToken`) kurį gavote ankstesniame veiksme.
    - Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.
    - Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.

1. Pateikite HTTP užklausą su šiomis ypatybes:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Metodas:** `POST`
    - **HTTP antraštė:** įtraukite API versiją. (Raktas `Api-Version`yra, o vertė yra `1.0` .)
    - **Teksto turinys:** įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.

    Kaip atsakymą turėtumėte (`access_token`) atsakymas. Turite naudoti šį žetoną dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API. Toliau pateikiamas pavyzdys.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

Vėlesniuose skyriuose naudokite `$access_token` norėdami pateikti atpažinimo ženklą, kuris buvo rastas paskutiniame veiksme.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Kurti vieną turimos informacijos pakeitimo įvykius

Yra du API, skirti turimos informacijos keitimo įvykiams kurti:

- Vieno įrašo kūrimas: `/api/environment/{environmentId}/onhand`
- Kurti kelis įrašus: `/api/environment/{environmentId}/onhand/bulk`

Šioje lentelėje apibendrinama kiekvieno JSON turinio lauko reikšmė.

| Lauko ID | Aprašas |
|---|---|
| `id` | Unikalus ID konkrečiam keitimo įvykiui. Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart. |
| `organizationId` | Organizacijos identifikatorius susietas su įvykiu. Ši vertė patalpina „Supply Chain Management“ organizacijas ar duomenų srities. |
| `productId` | Produkto identifikatorius. |
| `quantities` | Kiekis turi būti pakeistas pagal turimą kiekį. Pavyzdžiui, jei į lentyną įtraukiama 10 naujų knygų, ši vertė bus `quantities:{ shelf:{ received: 10 }}`. Jei iš lentynos arba parduodamos pašalinamos trys knygos, ši vertė bus `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje. Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio. Atsargų matomumas su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas. Jei ne `dimensionDataSource` vertė yra nurodyta, galite naudoti tik bendrą [pagrindines dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension) jūsų užklausose. |
| `dimensions` | Dinaminis rakto verčių poros. Vertės yra susietos su kai kurioms „Supply Chain Management“ dimensijoms. Tačiau galite įtraukti ir pasirinktines dimensijas (pvz.,, _Šaltinis_) ad nurodydami, ar įvykis įvyko iš „Supply Chain Management“ ar iš išorinės sistemos. |

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Kurti vieną turimos informacijos pakeitimo įvykį

Api sukuria vieną turimos informacijos pakeitimo įvykį.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys. Šiame pavyzdyje turite užregistruoti *marškinėlių* produkto keitimo įvykį. Šis įvykis įvyko iš kasos punkto (EKA) sistemos, o klientas grąžino raudoną marškinėlę atgal į jūsų parduotuvę. Dėl šio įvykio marškinėlių *produkto* kiekis bus padidintas 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys `dimensionDataSource`.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Kurti kelis pakeitimo įvykius

API gali kurti kelis įrašus vienu metu. Vienintelis skirtumas tarp šios API ir [vieno įvykio API](#create-one-onhand-change-event) yra `Path` ir `Body` vertės. Šiai API `Body` pateikiamas įrašų masyvas.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Nustatyti/nepaisyti turimos informacijos kiekių

Rinkinys _turimos_ API nepaiso dabartinių nurodyto produkto duomenų.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys. Šios API veikimo būdas skiriasi nuo API, kurie aprašyti [Kurti turimos medžiagos įvykius, veikimo](#create-onhand-change-event) anksčiau šioje temoje skyriuje. Šiame pavyzdyje, dėl šio įvykio marškinėlių *produkto* kiekis bus 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Kurti vieną rezervavimo įvykiai

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Norėdami naudoti *rezervo* API, turite atidaryti rezervavimo funkciją ir baigti konfigūruoti rezervavimą. Dėl daugiau informacijos, žr. [Rezervavimo konfigūracija (pasirinkti)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Kurti vieną rezervavimo įvykį

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys.

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Kurti kelis rezervuoti įvykius

Api yra masinis vieno [įvykio API variantas](#create-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>Turimos užklausos

_Turimų atsargų_ API užklausa naudojama surasti dabartinius jūsų produktų turimų atsargų duomenis.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Užklausa naudojant skelbimo metodą

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Užklausa naudojant gavimo metodą

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Čia pateikiamas URL gauti pavyzdys. Ši gavimo užklausa yra lygiai tokia pati, kaip ir anksčiau pateiktas skelbimo pavyzdys.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
