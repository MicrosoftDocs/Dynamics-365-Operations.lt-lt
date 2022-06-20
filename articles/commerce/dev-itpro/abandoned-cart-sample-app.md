---
title: Aptikti paliktus krepšelius ir siųsti klientams pranešimus
description: Šiame straipsnyje aprašoma, kaip pritaikyti paliekamos krepšelio Microsoft Dynamics 365 Commerce jungties pavyzdį programą, kad būtų aptikti paliekami krepšeliai ir išsiųsti priminimo el. paštu pranešimus klientams.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 707640ca211e997533d0f5a0b4e6d52cb5be9db4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899215"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Aptikti paliktus krepšelius ir siųsti klientams pranešimus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pritaikyti paliekamos krepšelio Microsoft Dynamics 365 Commerce jungties pavyzdį programą, kad būtų aptikti paliekami krepšeliai ir išsiųsti priminimo el. paštu pranešimus klientams.

Gebėjimas atkurti įplaukas ir išlaikyti klientus per paliekant krepšelio pranešimus yra svarbus pajėgumas, kuris Dynamics 365 Commerce palaiko. Pritaikant "Commerce" paliktos krepšelio jungties pavyzdinę programą, mažmenininkai gali pasiekti "Retail Server" pirkimo krepšelius, kurie nebuvo modifikuoti per laiko langą, kurį nurodo mažmenininkai. Tada šiuos krepšelius galima nuskaityti, papildyti produkto ir kliento duomenimis ir perduoti trečiosios šalies rinkodaros el. paštu tiekėjui, kuris gali generuoti el. paštu siunčiamus pranešimus ir siųsti juos klientams.

Paliekamame krepšelio el. pranešime, kurį gauna klientai, gali būti ši informacija:

- Kliento vardas.
- Kliento pavardė.
- Kliento el. pašto adresas.
- URL, kuris grąžina klientą į krepšelį.
- Operacijos valiuta.
- Kliento krepšelyje galimų produktų sąrašas. Pateikiama ši kiekvieno produkto informacija:

    - Rodomas produkto pavadinimas
    - Produkto ID (naudojamas URL surinkti produkto aprašo puslapyje)
    - Produkto vaizdas, kurį galima automatiškai pakeisti, kad būtų galima talpinti skirtingus rodinio prievado dydžius
    - Alternatyvus produkto vaizdo tekstas
    - Produkto vieneto kaina

## <a name="abandoned-cart-connector-sample"></a>Paliekamas krepšelio jungties pavyzdys

Jungties modelis, kurį "Microsoft" pateikia per "Retail" programinės įrangos kūrimo rinkinį (SDK), leidžia nuskaityti ir siųsti informaciją apie krepšelį trečiosios šalies el. pašto rinkodaros teikėjui. Ši jungtis tvarko ryšį su "Retail Server", sauga naudoja "Azure Key Vault", tvarko krepšelio nuskaitymo nurodytam laiko langui planavimą ir nuskaito užsakymo bei produkto duomenis. Taip pat pateikiamas integravimo su trečiųjų šalių el. pašto rinkodaros paslaugų teikėju pavyzdžio diegimas. Jungtis sukurta palaikyti ryšį su " [Emarsys](https://emarsys.com) " iš dėžės. Tačiau jį galima lengvai pritaikyti, kad būtų integruojama su kitais sprendimais, pvz., pastovaus kontakto, Mailchmp ir SendGrid.

Šioje iliustracijoje parodyti paliekamos krepšelio jungties pavyzdinės programos komponentai.

![Paliktos krepšelio jungties pavyzdžio programos komponentai](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Kai kuriuose regionuose būtina, kad klientai galėtų pasirinkti, kad jų krepšelio duomenys būtų perduoti el. pašto rinkodaros teikėjui, arba prašyti, kad jų duomenys būtų pašalinti. Tačiau "Microsoft" neleidžia pateikti šių parinkčių klientams. Todėl, jei planuojate imtis verslo regionuose, kurie juos įgalios, turite pateikti reikiamą infrastruktūrą ir pritaikymus, kad būtų galima stebėti klientų nuostatas ir, atsižvelgiant į jas, neleisti kliento duomenis perduoti jūsų el. pašto platformai. Kliento pageidavimu taip pat turite nustatyti kliento duomenų išvalymo iš el. pašto rinkodaros teikėjo procesą.

## <a name="obtain-the-code-sample"></a>Gauti kodo pavyzdį

Paliekama krepšelio jungties pavyzdžio programa įtraukiama į "Retail" SDK versijoje 10.0.16. Kodą galima rasti kode **\\ RetailSDK\\ Code\\ SampleExtensions\\ RetailServer\\ plėtiniai.UžduotasCartSample**. Daugiau informacijos apie "Retail SDK" ir jo gavimo vietą ieškokite "Retail" programinės [įrangos kūrimo rinkinyje (SDK).](retail-sdk/retail-sdk-overview.md)

> [!NOTE]
> Nors pavyzdžio kodas pirmą kartą buvo pasiekiamas naudojant 10.0.16 versiją, jis suderinamas su 10.0.13 versija ir vėlesnėmis "Retail Server" versijomis.

## <a name="prerequisites-and-dependencies"></a>Būtinos sąlygos ir priklausomybės

Prieš diegiant ir konfigūruojamas paliekamos krepšelio jungties pavyzdžio kodas, turi būti laikomasi šių būtinųjų komponentų.

### <a name="access-to-commerce-resources"></a>Prieiga prie "Commerce" išteklių

Norėdami konfigūruoti ir diegti paliekamas krepšelio jungties programą, turite turėti prieigą prie šių "Commerce" išteklių:

- Administratoriaus prieiga prie jūsų aplinkos "Commerce Headquarters"
- Jūsų aplinkoje Microsoft Dynamics prieiga prie ciklo tarnybų (LCS) projekto

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Paliekama krepšelio jungties programa naudoja "Azure Cosmos DB " anksčiau nuskaitytiems krepšelių ID ir laiko žymoms sekti. Galite naudoti "Azure" Cosmos DB šių duomenų išlaikyme arba pritaikyti kodo pavyzdį, kad jis būtų integruotas su kita duomenų saugojimo pasirinktimi. Norėdami gauti daugiau informacijos apie "Azure Cosmos DB", žr. " [Sveiki! Čia "Azure"Cosmos DB](/azure/cosmos-db/introduction).

Jei naudojate "Azure Cosmos DB", prieš paleisdami pavyzdį turite įvykdyti šias būtinąsias sąlygas:

- Turite turėti aktyvią "Azure" Cosmos DB sąskaitą. Jei neturite abonemento, žr. Duomenų [bazės abonemento kūrimas](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Turite nuskaityti **URI ir pirminio** **rakto (arba** **ANTRINIo** rakto) **vertes** iš "Azure" abonemento "Azure Cosmos DB" portalo raktų funkcijos. Norėdami gauti daugiau informacijos apie tai, kaip nuskaityti galinį punktą ir pagrindinė jūsų "Azure Cosmos DB " abonemento informaciją, [žr. Rodinį, kopijavimą ir iš naujo generuoti prieigos raktus ir slaptažodžius](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Paliekama krepšelio jungties programa naudoja "Key Vault", kad saugo skirtingų komponentų, prie kurių reikia saugios prieigos, pavadinimus ir slaptus pavadinimus.

Norėdami nustatyti rakto saugyklą, atlikite šiuos veiksmus.

1. Vadovaukitės instrukcijomis, pateiktomis " [Azure" dėklo centro valdymo portale, naudodami portalą](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Sukurti šios informacijos slapymetes:

    - Emarsys programos programavimo sąsajos (API) vartotojo vardas ir API slaptos
    - Paliekamas krepšelio programos ID ir slaptasis

Paliekamas krepšelio jungties pavyzdys naudoja "Azure" numatytuosius kredencialus, kad būtų galima pasiekti "Key Vault". Turite pateikti sąrašo **ir** **skaitymo** teises prie tapatybės, kurią planuojate naudoti norėdami pasiekti "Key Vault".

Norėdami gauti daugiau informacijos apie "Azure" numatytuosius kredencialus [, žr. DefaultAzureCredential klasę](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Kurti nuomininkui skirtą paliktos krepšelio jungties programos programos Azure AD ID

Turite sukurti paliekamos krepšelio jungties programos pavyzdžio Azure Active Directory (AD) nuomininkui ID. Informacijos apie tai, kaip sukurti programos ID, [ieškokite portalo naudojimas, norėdami sukurti programą Azure AD ir aptarnavimo pagrindinį puslapį, kuris gali pasiekti išteklius](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Įtraukti paliekamos krepšelio jungties programos egzemplioriaus programos ID į "Retail Server" API sąrašą

Po to turite įtraukti paliekamos krepšelio jungties programos egzemplioriaus programos ID į "Retail Server" API leidžia sąrašą. Norėdami gauti daugiau informacijos apie tai, kaip įtraukti programos ID į leidžiamų sąrašą "Azure", žr [. "Retail Server" paslaugos autentifikavimo palaikymą](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigūruoti paliekamos krepšelio jungties pavyzdžio programą

Norėdami sukonfigūruoti paliktą krepšelio jungties pavyzdžio programą, modifikuokite appSettings.json **konfigūracijos** failą, **kuris yra kataloge (Kurį paliekamaCartDetectionSample) šakniniame** kataloge. Šiose lentelėse aprašomos konfigūracijos failo ypatybės.

### <a name="keyvaultoptions"></a>"KeyVaultOptions"

| Ypatybė    | Aprašymas |
| ----------- | ----------- |
| RaktoVaultURI | Kodo saugyklos, kurią naudojate "Azure" portale, domeno vardų sistemos (DNS) pavadinimas. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Ypatybė                                      | Aprašymas |
| --------------------------------------------- | ----------- |
| Nuomininko ID                                      | " Azure AD Azure" nuomininko ID. |
| RetailServerAudienceId                        | "Retail Server" auditorijos ID. Galite palikti numatytąją vertę. |
| AppIdKeyVaultSecretName                       | Slapto, kurį sukūrėte paliekamos krepšelio jungties programos programos ID pavyzdyje, pavadinimas. |
| AppSecretKeyVaultSecretName                   | Slapto failo, kuriame saugomas programos palikto krepšelio jungties programos prašymo ID pavyzdys, pavadinimas. |
| RetailServerUrl                               | "Retail Server" egzemplioriaus URL. Šią vertę galima rasti LCS. |
| OperatingUnitNumber                           | Valdymo vieneto numeris (OUN). Šią vertę galima rasti "Commerce Headquarters". |
| ĮtrauktiAbandonedCartsModifiedSinceLastMinutes | Laiko lango pradžia, kai paliekami krepšeliai, kuriuos norite nuskaityti. Vertė išreiškiama minučių skaičiumi prieš dabartinį laiką. Pvz., nustatykite šią ypatybę 120 **, kad būtų nuskaityti visi krepšeliai, kurie paskutinį kartą buvo modifikuoti nuo 120 minučių** iki laiko lango, **kurį nustatė ypatybė ExcludeAbandonedCartsModifiedSinceLastMinutes**. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Laiko lango, kurį norite nuskaityti, paliekami krepšeliai, pabaiga. Vertė išreiškiama minučių skaičiumi prieš dabartinį laiką. Pavyzdžiui, **jei ypatybė IncludeAbandonedCartsModifiedSinceLastMinutes** **nustatyta kaip 120, nustatykite šią ypatybę kaip 30** **,** kad būtų nuskaityti visi krepšeliai, kurie buvo modifikuoti prieš 120 minučių ir po 30 minučių. Paprastai ši ypatybė apibrėžia laiką, kurį norite laukti, kol krepšelis paliekamas paliekamas. |
| ReturnToCartUrl                               | Krepšelio URL jūsų el. komercijos svetainėje formatu, kuris naudojamas **faile app.config**. |

### <a name="azurecosmosoptions"></a>"AzureCosmosOptions"

"Azure" saugomi paliekami krepšelio nuskaitymi užduočių būsenos, krepšelio ID ir modifikuotos laiko žymos Cosmos DB. Pagal numatytuosius nustatymus konfigūracijos rinkmenos parametrai pereis į vietinį "Azure" emuliatoriaus egzempliorių Cosmos DB. Kai diegiate jungtį į gamybą, turite atnaujinti šiuos parametrus, kad jie nurodyti "Azure" egzemplioriui "Azure Cosmos DB " abonemente. Norėdami patikrinti vietinę arba šlifavimo dėžę, galite naudoti "Azure" iuliatorių [Cosmos DB](/azure/cosmos-db/local-emulator).

| Ypatybė    | Aprašymas |
| ----------- | ----------- |
| EndPointUri | Galinio punkto URI, kurį teikia "Azure" arba iuliatorius. |
| Pirminis raktas  | Pirminis raktas, kurį teikia "Azure" arba iasuliatorius. |
| Duomenų bazės ID  | Duomenų bazės ID. Galite palikti numatytąją vertę arba pateikti savo. |
| Konteinerio ID | Konteinerio ID. Galite palikti numatytąją vertę arba pateikti savo. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Jei integruojate su el. pašto rinkodaros teikėju, kuris nėra "Emarsys", **turite išplėsti IEmailProvider** sąsają, kad būtų galima palaikyti ryšį su tuo tiekėju.

| Ypatybė                      | Aprašymas |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Išorinio įvykio įrašo, sukurto "Emarsys", ID. Vertę pagal paleidiklio parametrus galite **rasti kampanijoje**, kurią sukūrėte išsiųsti pranešimais apie krepšelį el. paštu. |
| ApiUserNameKeyVaultSecretName | Rakto, kuriame saugomas "Emarsys API" vartotojo vardas, pavadinimas. |
| ApiSecretKeyVaultSecretName   | Rakto, kuriame saugomas Emarsys API secret, pavadinimas. |
| EmarsysContactKeyId           | El. pašto stulpelio ID Emarsys kontaktų duomenų bazėje. Numatytoji vertė **yra 3**, todėl jos keisti nereikia. |

### <a name="mediaoptions"></a>MediaOptions

Jei naudojatės el. prekybos galimybėmis "Commerce", produktų vaizdams nuskaityti galite naudoti "Commerce" skaitmeninio turto valdymą. Daugiau informacijos apie vaizdo dydžio keitimo priemonės galimybes skaitmeninio turto valdymui žr. [ImageSettings viewport konfigūracija](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Ypatybė                             | Aprašymas |
| ------------------------------------ | ----------- |
| Vaizdoserveriourl                       | Jūsų svetainės skaitmeninio turto tvarkytuvo šakninis URL. Vertę galite rasti "**Commerce Headquarters" ypatybės "Media Server" pagrindinio URL** **ypatybės rakte "Retail" ir "Commerce \> Channel" \> nustatymo kanalo** šablonuose. |
| ImageViewPorts                       | Konteinerio mazgas atskiroms viewport konfigūracijų. |
| ImageViewPorts / viewport              | Rodinio prievado apibrėžimas. Naudokite šią ypatybę, jei norite nurodyti rodinio pločio diapazonus pikseliais. Pavyzdžiui, kaip naudojama ši ypatybė, žr. **appSettings.json** konfigūracijos failą. |
| ImageViewPorts/imageWidth            | Rodinio vaizdo plotis pikseliais. |
| imageViewPorts/imageHe dk           | Rodinio vaizdo aukštis pikseliais. |
| imageViewPorts/useForDefaultImageTag | Teisinga **klaidinga**/**vertė**, kuri nurodo, ar vaizdo dimensijos, kurias apibrėžia viewport `<picture>`, turi būti naudojamos, jei HTML žymė nepalaikoma žiniatinklio naršyklėje ar el. pašto kliento programoje. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
