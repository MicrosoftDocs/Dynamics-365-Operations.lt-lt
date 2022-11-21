---
title: „Inventory Visibility“ viešos API
description: Šiame straipsnyje aprašomi vieši API, kurie pateikiami pagal atsargų matomumą.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762840"
---
# <a name="inventory-visibility-public-apis"></a>„Inventory Visibility“ viešos API

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi vieši API, kurie pateikiami pagal atsargų matomumą.

Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus. Jis palaiko keturis pagrindines sąveikos rūšis:

- Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas
- Turimų atsargų kiekių nustatymas arba nepaisimas prie išorinės sistemos priedo
- Publikavimas rezervavimo įvykių į papildinio formą išorės sistemoje
- Dabartinių turimų kiekių užklausos iš išorės sistemos

Toliau pateiktoje lentelėje nurodytos API esamos parinktys:

| Kelias | Metodas | Aprašas |
|---|---|---|
| /api/aplinka/{environmentId}/turi būti | Skelbti | [Kurti vieną turimos informacijos pakeitimo įvykį](#create-one-onhand-change-event)|
| /api/aplinka/{environmentId}/turi būti/bendras | Skelbti | [Kurti kelis pakeitimo įvykius](#create-multiple-onhand-change-events) |
| /api/aplinka/{environmentId}/stovintis/{inventorySystem}/bendras | Skelbti | [Nustatyti/nepaisyti turimos informacijos kiekių](#set-onhand-quantities) |
| /api/aplinka/{environmentId}/turi būti/rezervavimas | Registruoti | [Kurti vieną soft reservation event](#create-one-reservation-event) |
| /api/aplinka/{environmentId}/turi būti/rezervavimas/bendras | Registruoti | [Kelių soft rezervavimų įvykių kūrimas](#create-multiple-reservation-events) |
| / API / aplinka /{environmentId} turi būti / nereservis | Registruoti | [Atšaukti vieną soft reservation event](#reverse-one-reservation-event) |
| / API / aplinka / turi{environmentId} būti / rezervuoti / buferinė dalis | Registruoti | [Atšaukti kelis soft rezervavimo įvykius](#reverse-multiple-reservation-events) |
| / API / aplinka /{environmentId} turimi / pakeisti | Registruoti | [Kurti vieną suplanuotą turimos informacijos pakeitimą](inventory-visibility-available-to-promise.md) |
| / API / aplinka /{environmentId} turimi / perplanuotas / masinis pardavimas | Registruoti | [Kurti kelis turimos informacijos pakeitimus su datomis](inventory-visibility-available-to-promise.md) |
| /api/aplinka/{environmentId}/turi būti/indekso užklausa | Registruoti | [Užklausa naudojant skelbimo metodą](#query-with-post-method) (rekomenduojama) |
| /api/aplinka/{environmentId}/turi būti | Gauti | [Užklausa naudojant gavimo metodą](#query-with-get-method) |
| / API / aplinka /{environmentId} turi būti / tiksli užklausa | Registruoti | [Tiksli užklausa naudojant skelbimo metodą](#exact-query-with-post-method) |
| / API / aplinka /{environmentId} paskirstymas /<wbr> paskirstymas | Registruoti | [Sukurti vieną paskirstyti įvykį](inventory-visibility-allocation.md#using-allocation-api) |
| / API / aplinka /{environmentId} paskirstymas<wbr> / nepaskirstytas | Registruoti | [Sukurti vieną neišskirstyti įvykį](inventory-visibility-allocation.md#using-allocation-api) |
| / API / aplinka /{environmentId} paskirstymas /<wbr> realus paskirstymas | Registruoti | [Sukurti vieną iš naujo išskirstyto įvykio](inventory-visibility-allocation.md#using-allocation-api) |
| / API / aplinka /{environmentId} paskirstymas<wbr> / naudojimas | Registruoti | [Kurti vieną naudojimo įvykį](inventory-visibility-allocation.md#using-allocation-api) |
| / API / aplinka /{environmentId} paskirstymas /<wbr> užklausa | Registruoti | [Užklausos paskirstymo rezultatas](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Maršruto {environmentId} dalis yra aplinkos ID ciklo Microsoft Dynamics tarnybose.
> 
> Masinis API gali pateikti ne daugiau kaip 512 kiekvienos užklausos įrašų.

„Microsoft" pateikė "out-of-box *Paštininko* užklausų rinkinį. Šį rinkinį galite importuoti į savo *paštininko* rango programinę įrangą naudodami šį bendrai naudojamą saitą: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Rasti galinį punktą pagal „Lifecycle Services“ aplinką

Atsargų matomumo mikrotara įdiegta „Microsoft Azure Service Fabric“ regionams ir keliuose regionuose. Šiuo metu nėra centrinio galinio punkto, kuris gali automatiškai nukreipti jūsų prašymą į atitinkamą geografijos ir regiono informaciją. Todėl informacijos dalis turite sus sudaro į URL naudodami šį šabloną:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Trumpą regiono pavadinimą galima rasti ciklo tarnybų aplinkoje. Toliau pateiktoje lentelėje regioniniai API esamos parinktys.

| „Azure“ regionas        | Trumpas regiono pavadinimas |
| ------------------- | ----------------- |
| Rytų Australija      | eau               |
| Pietryčių Australija | seau              |
| Centrinė Kanada      | cca               |
| Rytų Kanada         | eca               |
| Šiaurės Europa        | neu               |
| Vakarų Europa         | weu               |
| Rytų JAV             | eus               |
| Vakarų JAV             | wus               |
| Pietų UK            | Suk               |
| Vakarų JK             | sąrašas               |
| Rytų Japonija          | ejp               |
| Vakarų Japonija          | wjp               |
| Centrinė Indija       | Cin               |
| Pietų Indija         | Nuodėmė               |
| Šveicarijos Šiaurės   | nch               |
| Šveicarijos West    | Iš 10               |
| Pietų Prancūzija        | Sfr               |
| Rytų Azija           | Eas               |
| Pietų Azijos     | Jūros              |
| Jae Šiaurės           | nae               |
| Norvegijos Rytų         | Eno               |
| Norvegija West         | wno               |
| Pietų Afrika West   | wza               |
| Pietų Afrika Šiaurės  | sąs.               |

Salos numeris yra ten, kur jūsų ciklo tarnybų aplinka įdiegta paslaugų medžiaga. Šiuo metu nėra būdo gauti šią informaciją iš vartotojo pusės.

„Microsoft“ sukūrė vartotojo sąsają (UI) tam, kad gautumėte „Power Apps“ visą mikroservice galinį punktą. Daugiau informacijos žr. [Surasti paslaugų galinį tašką](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikavimas

Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo viešui API iškviesti. Todėl turite sugeneruoti *„Azure Active Directory“ („Azure AD“) atpažinimo ženklą*, naudodami savo „Azure AD“ programą. Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte *prieigos atpažinimo ženklą*.

„Microsoft" teikia "out-of-box *Paštininko* užklausų rinkinį. Šį rinkinį galite importuoti į savo *paštininko* rango programinę įrangą naudodami šį bendrai naudojamą saitą: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Gaukite saugos paslaugų žymą atlikdami taip.

1. Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` vertes Jūsų „Dynamics 365 Supply Chain Management“ programa.
1. Iškvieskite „Azure AD” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:

    - **URL:**`https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Metodas:** `GET`
    - **Teksto turinys (formos duomenys):**

        | Raktas           | Reikšmė                                            |
        | ------------- | -------------------------------------------------|
        | „client_id”     | „${aadAppId}“                                      |
        | „client_secret” | „${aadAppSecret}“                                  |
        | „grant_type”    | „client_credentials”                               |
        | Taikymo sritis         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.Numatytasis    |

    Kaip atsakymą turėtumėte „Azure AD“ gauti (`aadToken`) atpažinimo ženklą. Ji turi atitikti šį pavyzdį.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
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
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Atkreipkite dėmesį į toliau nurodytus punktus.

    - Vertė `client_assertion` turi būti „Azure AD“ žetonas (`aadToken`) kurį gavote ankstesniame veiksme.
    - Reikšmė `context` turi būti ciklo tarnybų aplinkos ID, kur norite įdiegti papildinį.
    - Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.

1. Iškvieskite (`access_token`) atpažinimo ženklą pateikdami HTTP užklausą su šiomis ypatybes:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Metodas:** `POST`
    - **HTTP antraštė:** įtraukite API versiją. (Raktas `Api-Version`yra, o vertė yra `1.0` .)
    - **Teksto turinys:** įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.

    Kaip atsakymą turėtumėte (`access_token`) atsakymas. Turite naudoti šį žetoną dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API. Čia pateikiamas pavyzdys.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Kai naudojate pašto *reikalauti* rinkinį iškviesti atsargų matomumo viešus API, kiekvienai užklausai turite pridėti panaudos priemonės atpažinimo ženklą. Norėdami rasti savo išdėstojo atpažinimo ženklą, po užklausos URL pasirinkite skirtuką **Autorizavimo** pasirinkite **Bearer ženklas** tipą ir kopijuokite prieigos atpažinimo ženklą, kuris buvo rastos paskutiniame veiksme. Vėlesniuose šio straipsnio skyriuose bus `$access_token` naudojamas atpažinimo ženklui, kuris rastas paskutiniame veiksme, pateikti.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Kurti vieną turimos informacijos pakeitimo įvykius

Yra du API, skirti turimos informacijos keitimo įvykiams kurti:

- Vieno įrašo kūrimas: `/api/environment/{environmentId}/onhand`
- Kurti kelis įrašus: `/api/environment/{environmentId}/onhand/bulk`

Šioje lentelėje apibendrinama kiekvieno JSON turinio lauko reikšmė.

| Lauko ID | Aprašymas |
|---|---|
| `id` | Unikalus ID konkrečiam keitimo įvykiui. Jei dėl aptarnavimo trikties įvyksta pakartotinis pranešimas, šis ID naudojamas norint užtikrinti, kad sistemoje to paties įvykio nebus du kartus suskaičiuota. |
| `organizationId` | Organizacijos identifikatorius susietas su įvykiu. Ši vertė patalpina „Supply Chain Management“ organizacijas ar duomenų srities. |
| `productId` | Produkto identifikatorius. |
| `quantities` | Kiekis turi būti pakeistas pagal turimą kiekį. Pavyzdžiui, jei į lentyną įtraukiama 10 naujų knygų, ši vertė bus `quantities:{ shelf:{ received: 10 }}`. Jei iš lentynos arba parduodamos pašalinamos trys knygos, ši vertė bus `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje. Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio. Atsargų matomumas su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas. Jei ne `dimensionDataSource` vertė yra nurodyta, galite naudoti tik bendrą [pagrindines dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension) jūsų užklausose. |
| `dimensions` | Dinaminis rakto verčių poros. Vertės yra susietos su kai kurioms „Supply Chain Management“ dimensijoms. Tačiau galite įtraukti ir pasirinktines dimensijas (pvz.,, *Šaltinis*) ad nurodydami, ar įvykis įvyko iš „Supply Chain Management“ ar iš išorinės sistemos. |

> [!NOTE]
> Skaidinio `siteId` ir `locationId` konfigūraciją [konstruktorius ir parametrai](inventory-visibility-configuration.md#partition-configuration). Todėl kurdami turimos prekės pakeitimo įvykius, nustatytą ar perrašydami turimus kiekius arba kurdami rezervavimo įvykius, turite juos nurodyti dimensijose.

Toliau pateikti poskyriai pateikia pavyzdžius, kaip naudoti šiuos API.

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

Šiame pavyzdyje rodomas turinio pavyzdžio turinys. Šiame pavyzdyje įmonė turi point-sale (EKA) sistemą, kuri apdoroja parduotuvės operacijas ir todėl pakeičia atsargas. Klientas grąžino raudonus marškinėlius į parduotuvę. Tam, kad atsispindėtų pakeitimas, užregistruokite vieną marškinėlių *produkto pakeitimo įvykį*. Dėl šio įvykio marškinėlių *produkto* kiekis bus padidintas 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys `dimensionDataSource`. Šiuo atveju `dimensions` bus [pagrindinės dimensijos](inventory-visibility-configuration.md#data-source-configuration-dimension). Jei `dimensionDataSource` nustatyta, gali  `dimensions` būti duomenų šaltinio dimensijos arba pagrindinės dimensijos.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Kurti kelis pakeitimo įvykius

API gali kurti pakeitimo įvykius kaip ir [vieno įvykio API](#create-one-onhand-change-event). Vienintelis skirtumas yra tai, kad ši API gali sukurti kelis įrašus tuo pačiu metu. Todėl skiriasi `Path` vertės `Body` ir vertės. Šiai API `Body` pateikiamas įrašų masyvas. Maksimalus įrašų skaičius yra 512. Todėl turimos atsargų pakeitimo buferinės API gali palaikyti iki 512 pakeitimų įvykių vienu metu. 

Pavyzdžiui, parduotuvės EKA įrenginys apdorojo šias dvi operacijas:

- Vienas grąžinimo užsakymas su vienu raudonu marškinėlių
- Viena trijų juodų marškinėlių pardavimo operacija

Tokiu atveju į vieną API iškvietimą galite įtraukti abiejų atsargų atnaujinimus.

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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Nustatyti/nepaisyti turimos informacijos kiekių

Rinkinys *turimos* API nepaiso dabartinių nurodyto produkto duomenų. Ši funkcija paprastai naudojama atsargų inventorizacijos atnaujinimui atlikti. Pavyzdžiui, vykdant kasdienę atsargų skaičiavimą, parduotuvė gali rasti, kad faktinės turimos raudonų marškinėlių atsargos yra 100. Todėl EKA gaunamas kiekis turi būti atnaujintas į 100, neatsižvelgiant į tai, koks buvo ankstesnis kiekis. Šią API galite naudoti norėdami nepaisyti esamos vertės.

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

Šiame pavyzdyje rodomas turinio pavyzdžio turinys. Šios API veikimo būdas skiriasi nuo [API, kurie aprašyti anksčiau šiame straipsnyje skyriuje Kurti turimos](#create-onhand-change-event) medžiagos įvykius, veikimo. Šiame pavyzdyje, dėl šio įvykio marškinėlių *produkto* kiekis bus 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Kurti vieną rezervavimo įvykiai

Norėdami naudoti rezervo *API*, turite įjungti rezervavimo funkciją ir baigti konfigūruoti rezervavimą. Daugiau informacijos (įskaitant duomenų srauto ir pavyzdžio scenarijų) ieškokite Rezervavimo [konfigūracija (pasirinktinai)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Kurti vieną rezervavimo įvykį

Rezervuoti galima pagal skirtingus duomenų šaltinio parametrus. Norėdami konfigūruoti šio tipo rezervavimą, pirmiausia parametre nurodykite duomenų `dimensionDataSource` šaltinį. Tada parametre `dimensions` nurodykite dimensijas pagal dimensijų parametrus paskirties duomenų šaltinyje.

Kai iškiesite rezervavimo API, galite valdyti rezervavimo tikrinimą nurodydami parametrą Boolean `ifCheckAvailForReserv` užklausos body. Vertė, `True` kuri reiškia, kad būtinas tikrinimas, o `False` vertė reiškia, kad tikrinimas nebūtinas. Numatytoji vertė yra `True`.

Jei norite atšaukti rezervavimą ar nereservuoti nurodytų atsargų kiekių, `ifCheckAvailForReserv``False` nustatykite neigiamą kiekio vertę ir nustatykite parametrą praleisti tikrinimą. Taip pat yra skirtoji nerealizuoto API, norint tai padaryti. Skirtumas yra tik toks pat, kaip du API iškvie čiami. Lengviau atšaukti konkretų rezervavimo įvykį naudojant `reservationId` nereserve *API*. Daugiau informacijos rasite vieno rezervavimo [įvykio skyriaus nereserve](#reverse-reservation-events).

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Šiame pavyzdyje pateikiamas sėkmingas atsakymas.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Kurti kelis rezervuoti įvykius

Api yra masinis vieno [įvykio API variantas](#create-reservation-events).

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

## <a name="reverse-reservation-events"></a>Atšaukti rezervavimo įvykius

Nereserve *API* naudojama kaip rezervavimo įvykių atvirkštinė [*·*](#create-reservation-events) operacija. Tai leidžia atšaukti rezervavimo įvykį, kuris nurodytas pagal rezervavimo `reservationId` kiekį arba sumažinti.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a> Atšaukti vieną rezervavimo įvykį

Kai sukuriamas rezervavimas `reservationId`, jis bus įtrauktas į atsakymo tekstas. Norėdami atšaukti rezervavimą, `reservationId` turite pateikti tą patį ir tą patį ir `organizationId``dimensions` naudoti rezervavimo API iškvietimui. Galiausiai nurodykite `OffsetQty` vertę, kuri nurodo prekių skaičių, kuris bus atlaisvinęs nuo ankstesnio rezervavimo. Rezervavimas gali būti visiškai arba iš dalies atšauktas, priklausomai nuo nurodytos.`OffsetQty` Pavyzdžiui, jei rezervuota *100* prekių vienetų, `OffsetQty: 10` galite nurodyti nereservuoti *10* pradinės rezervuotos sumos vienetų.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Šis kodas rodo turinio pavyzdį.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Šis kodas rodo sėkmingo atsakymo kūno pavyzdį.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Atsakymo body, kai `OffsetQty` ji mažesnė arba lygi rezervavimo kiekiui, `processingStatus` bus "*sėkminga*" `totalInvalidOffsetQtyByReservId` ir bus *0*.
>
> Jei `OffsetQty` ji didesnė nei rezervuota suma, `processingStatus` bus "*partialSuccess*" `totalInvalidOffsetQtyByReservId` ir bus skirtumas tarp `OffsetQty` rezervuotos sumos ir.
>
>Pavyzdžiui, jei rezervavimo kiekis yra *10*, o `OffsetQty` vertė – *12*, `totalInvalidOffsetQtyByReservId` būtų *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a> Atšaukti kelis rezervavimo įvykius

Api yra masinis vieno [įvykio API variantas](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Turimos užklausos

Norėdami surasti *dabartinius* savo produktų turimų atsargų duomenis, naudokite turimų atsargų API užklausą. Šią API galima naudoti, kai tik reikia žinoti atsargas, pvz., kai norite peržiūrėti produktų atsargų lygius savo el. komercijos svetainėje arba kai norite patikrinti produkto prieinamumą regionuose arba artimiausiose parduotuvėse ir sandėliuose. API šiuo metu palaiko užklausas iki 5000 atskirų prekių pagal `productID` vertę. Šioje `siteID` užklausoje `locationID` dar galima nurodyti keletą verčių. Maksimali riba apibrėžiama šioje lygtyje:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

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
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Šioje užklausos dalyje vis dar `dimensionDataSource` yra pasirinktinis parametras. Jei jo nėra, ji bus `filters` laikoma *bazinėmis dimensijomis*. Yra keturi privalomi `filters` laukai: `organizationId`, `productId` ir `siteId`, `locationId`.

- `organizationId` turi būti tik viena vertė, bet ji vis dar masyve.
- `productId` gali būti viena arba daugiau verčių. Jei yra tuščias masyvas, bus pateiktos visų produktų grąžintos.
- `siteId` ir `locationId` yra naudojami atsargų matomumui skaldyti. Galite nurodyti daugiau nei vieną `siteId` ir `locationId` vertę *turimos užklausos* užklausoje. Dabartiniame leidime turite nurodyti ir vertes, `siteId` ir `locationId` vertes.

Rekomenduojame naudoti parametrą indeksavimo `groupByValues` konfigūracijai sekti. Daugiau informacijos, žr. [Produkto indekso hierarchijos konfigūracija](./inventory-visibility-configuration.md#index-configuration).

Parametras `returnNegative` kontroliuoja, ar rezultatuose yra neigiamų įrašų.

> [!NOTE]
> Jei įgalinote turimo keitimo grafiko ir prieinamų atsargų (ATP) priemones, `QueryATP` jūsų užklausoje taip pat gali būti Būlio logikos parametras, kuris kontroliuoja, ar užklausos rezultatuose yra ATP informacija. Daugiau informacijos ir pavyzdžių ieškokite atsargų [matomumo turimų atsargų pakeitimo grafikuose ir prieinamose atsargose](inventory-visibility-available-to-promise.md).

Šiame pavyzdyje rodomas turinio pavyzdžio turinys. Tai rodo, kad jūs galite pateikti užklausą apie turimos atsargos iš kelių vietų (sandėlių).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Toliau pateikiamas pavyzdys rodo, kaip pateikti užklausą apie visus produktus tam tikroje teritorijoje ir vietoje.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Užklausa naudojant gavimo metodą

```txt
Path:
    /api/environment/{environmentId}/onhand
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

Čia pavyzdys gauti URL. Ši gavimo užklausa yra lygiai tokia pati, kaip ir anksčiau pateiktas skelbimo pavyzdys.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a> Tiksli turimų atsargų užklausa

Turimos turimos užklausos yra panašios į įprastas turimos užklausos, bet jos leidžia nurodyti svetainės ir vietos susiejimo hierarchiją. Pavyzdžiui, turite šias dvi vietas:

- 1 svetainė, susietas su A vieta
- 2 vieta, susietas su B vieta

Jei nurodote ir, jei nurodote reguliarią turimų atsargų užklausą, `"siteId": ["1","2"]``"locationId": ["A","B"]` atsargų matomumas automatiškai ieškos rezultatų šioms svetainėms ir vietų:

- 1 vieta, A vieta
- 1 vieta, B vieta
- 2 vieta, A vieta
- 2 vieta, B vieta

Kaip matote, įprasta turimos informacijos užklausa neatpažįsta, kad A vieta yra tik 1 teritorijoje, o B vieta yra tik 2 teritorijoje. Todėl dėl to atlieka perteklines užklausas. Norėdami talpinti šį hierarchinį susiejimą, galite naudoti tikslią turimos informacijos užklausą ir nurodyti vietos susiejimus užklausos body. Šiuo atveju gausite užklausą ir gausite tik 1 vietos, A vietos ir 2 vietos B, rezultatus.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a> Tiksli užklausa naudojant skelbimo metodą

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Šios užklausos dalyje yra pasirinktinis `dimensionDataSource` parametras. Jei jos nėra, jos bus `dimensions``filters` laikomos bazinėmis *dimensijomis*. Yra keturi privalomi `filters` laukai: `organizationId`, `productId` ir `dimensions`, `values`.

- `organizationId` turi būti tik viena vertė, bet ji vis dar masyve.
- `productId` gali būti viena arba daugiau verčių. Jei yra tuščias masyvas, bus pateiktos visų produktų grąžintos.
- Masyve `dimensions` ir yra `siteId` būtini `locationId`, bet gali būti rodomi su kitais elementais bet kokia tvarka.
- `values` gali būti vienas arba daugiau atskirų verčių, atitinkančių `dimensions`.

`dimensions` į `filters` bus automatiškai pridėta prie `groupByValues`.

Parametras `returnNegative` kontroliuoja, ar rezultatuose yra neigiamų įrašų.

Šiame pavyzdyje rodomas turinio pavyzdžio turinys.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Toliau pateikiamas pavyzdys rodo, kaip pateikti užklausą visiems produktams keliose svetainėse ir vietose.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Prieinamos atsargos

Galite nustatyti atsargų matomumą, kad leisite suplanuoti būsimus turimų atsargų keitimus ir skaičiuoti ATP kiekius. ATP – tai turimos prekės kiekis, kurį galima žadėti klientui kitą laikotarpį. AtP skaičiavimo naudojimas gali labai padidinti jūsų užsakymo įvykdymo galimybes. Informacijos apie tai, kaip įgalinti šią funkciją ir kaip sąveikauti su atsargų matomumu, naudojant API, kai funkcija įgalinta, [žr. atsargų matomumo turimų atsargų keitimo grafikus ir prieinamus pasižadėti](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Paskirstymas

Su paskirstymu susiję API yra atsargų [matomumo paskirstyme](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
