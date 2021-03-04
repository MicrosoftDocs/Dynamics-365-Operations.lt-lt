---
title: Autentifikavimas
description: Šiame straipsnyje pateikiama peržiūros informacija apie tai, kaip autentifikuoti „Microsoft Dynamics 365 Human Resources“ duomenų taikomojo programavimo sąsają (API).
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a0509ce99205d49d516e180203ffb65a1dc09a7c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419652"
---
# <a name="authentication"></a>Autentifikavimas

Šiame straipsnyje pateikiama peržiūros informacija apie tai, kaip autentifikuoti „Microsoft Dynamics 365 Human Resources“ duomenų taikomojo programavimo sąsają (API).

## <a name="overview"></a>Peržiūrėti

„Human Resources“ skirta duomenų API yra „OData“ diegimas. Daugiau informacijos žr. [„Open Data Protocol“ („OData“)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Jūsų programą reikia autentifikuoti kaip įgaliotą kvietyklę, kad API galėtų atsakyti į užklausas, gautas iš jūsų programos.

## <a name="fundamentals"></a>Pagrindai

Siekiant iškviesti duomenų API, programa turi gauti „Microsoft“ tapatumo platformos prieigos atpažinimo ženklą. Prieigos atpažinimo ženkle yra informacija apie jūsų programą ir teisė iškviesti „Human Resources“ išteklius.

### <a name="access-token"></a>Prieigos atpažinimo ženklas

„Microsoft“ tapatumo platformos išduodami prieigos atpažinimo ženklai yra base64 užkoduoti „JavaScript Object Notation“ (JSON) žiniatinklio atpažinimo ženklai (JWT). Jose yra informacija (paraiškos), kad duomenų API (ir kitos žiniatinklio API, saugomos „Microsoft“ tapatumo platformos) yra naudojamos kvietyklei patvirtinti ir įsitikinti, kad kvietyklė turi tinkamas teises prašomai operacijai atlikti. Skambučių metu galite laikyti prieigos atpažinimo ženklus nepermatomais. Prieigos atpažinimo ženklus visada turite perduoti saugiais kanalais, tokiais kaip transportavimo lygmens sauga (TLS) ir Hypertext Transfer Protocol Secure (HTTPS).

Čia yra prieigos atpažinimo ženklo, kurį išdavė „Microsoft“ tapatumo platforma, pavyzdys.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Norėdami iškviesti duomenų API, pridėkite prieigos atpažinimo ženklą kaip pateikėjo atpažinimo ženklą prie autorizavimo antraštės savo HTTP užklausoje. Toliau pateikiamas pavyzdys.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Naudodami „Azure“ portalą, užregistruokite naują programą

1. Prisijunkite prie [„Microsoft Azure“ portalo](https://portal.azure.com) naudodami darbo ar mokyklos paskyrą arba asmeninę „Microsoft“ paskyrą.

2. Jeigu jūsų paskyra suteikia prieigą prie daugiau nei vieno nuomotojo, viršutiniame dešiniajame kampe pasirinkite savo paskyrą ir nustatykite portalo sesiją į norimą „Azure Active Directory“ („Azure AD“) nuomotoją.

3. Kairiojoje srityje pasirinkite paslaugą **„Azure Active Directory“**, tada pasirinkite **Programų registracijos \>Nauja registracija**.

4. Kai pasirodys puslapis **Registruoti programą**, įveskite programos registracijos informaciją:

    - **Pavadinimas**: įveskite prasmingą programos pavadinimą, kuris bus rodomas programos vartotojams.
    - **Palaikomi paskyrų tipai**: pasirinkite paskyrų tipus, kuriuos turi palaikyti programa.

        | Palaikomi sąskaitų tipai | Aprašymas |
        |-------------------------|-------------|
        | Paskyros tik šiame organizaciniame kataloge | Pasirinkite šią pasirinktį, jei kuriate verslui skirtą programą. Ši parinktis pasiekiama tik tuo atveju, jei registruojate programą kataloge.<p>Ši parinktis susieta tik su **vienu „Azure AD“ nuomotoju**.</p><p>Ši parinktis yra numatytoji parinktis, nebent registruojate programą ne kataloge. Tokiu atveju numatytoji parinktis yra kelių nuomotojų **„Azure AD“ ir asmeninės „Microsoft“ paskyros**.</p> |
        | Paskyros bet kokiame organizaciniame kataloge | Pasirinkite šią parinktį, norėdami tiksline auditorija pasirinkti visus verslo ir mokslo klientus.<p>Ši parinktis susieta tik su **keliais „Azure AD“ nuomotojais**.</p><p>Jei užregistravote programą kaip **tik vieno nuomotojo „Azure AD“**, galite naudoti mentę **Autentifikavimas**, kad atnaujintumėte ją į **tik kelių nuomotojų „Azure AD“**, o tada vėl į **tik vieno nuomotojo „Azure AD“**.</p> |
        | Bet kokio organizacinio katalogo paskyros ir asmeninės „Microsoft“ paskyros | Pasirinkite šia parinktį, kad tiksline auditorija pasirinktumėte didžiausią klientų grupę.<p>Ši parinktis yra susieta su **kelių nuomotojų „Azure AD“ ir asmeninėmis „Microsoft“ paskyromis**.</p><p>Jei užregistravę programą kaip **Kelių nuomotojų „Azure AD“ ir asmeninės „MIcrosoft“ paskyros**, negalite keisti šio parametro vartotojo sąsajoje (UI). Vietoj to, turite naudoti programos deklaracijos doroklį, kad pakeistumėte palaikomus paskyrų tipus.</p> |

    - **Nukreipimo URI (pasirinktinai)** – pasirinkite, kokio tipo programą kuriate: **Žiniatinklio** ar **Viešojo kliento (skirta mobiliesiems įrenginiams ir asmeniniams kompiuteriams)**. Tada įveskite programos nukreipimo URI (arba atsakymo URL).

        - Norėdami naudoti žiniatinklio programas, nurodykite pagrindinį programos URL. Pavyzdžiui, `http://localhost:31544`gali būti jūsų vietiniame kompiuteryje veikiančios žiniatinklio programos URL. Tada vartotojai naudoja šį URL, kad prisijungtų prie žiniatinklio kliento programos.
        - Norėdami naudoti viešojo kliento programas, nurodykite URI, kurį „Azure AD“ naudoja, kad atsilieptų į atpažinimo ženklų atsakymus. Įveskite savo programai būdingą vertę, pvz., `myapp://auth`.

        Norėdami pamatyti konkrečius pavyzdžius, susijusius su žiniatinklio programomis ir vietinėmis programomis, žr. greitąjį pasirengimą darbui[ „Microsoft“ tapatumo platformoje (anksčiau vadinamoje „Azure Active Directory“, skirta kūrėjams)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. Dalyje **API teisės** pasirinkite **Įtraukti teisę**. Tada skirtuke **Mano organizacijoje naudojamos API**, ieškokite **„Dynamics 365 Human Resources“** ir pridėkite teisę **vartotojas\_apsimetimas** prie savo programos. „Human Resources“ programos ID yra f9be0c49-aa22-4ec6-911a-c5da515226ff. Naudokite šį ID norėdami įsitikinti, kad pasirinkote tinkamą programą.

6. Pasirinkite **Registruotis**.

   [![Naujos programos registravimas „Azure“ portale](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

„Azure AD“ priskiria jūsų programai unikalų programos ID (kliento ID) ir perkelia jus į programos puslapį **Apžvalga**. Norėdami pridėti daugiau galimybių prie programos, galite pasirinkti kitas konfigūravimo parinktis, pvz., prekių ženklų, sertifikatų ir slaptųjų raktų parinktis.

## <a name="retrieving-an-access-token"></a>Prieigos atpažinimo ženklo nuskaitymas

Konkreti informacija apie tai, kaip nuskaityti prieigos atpažinimo ženklą, kad būtų galima iškviesti „Human Resources“ duomenų API, priklausys nuo to, kokiomis technologijomis naudojatės kurdami kliento programą. Pavyzdžiui, galbūt [bandote trečiosios šalies priemonę](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (pvz., „Postman“), kuriate C# konsolės programą ar žiniatinklio paslaugą arba kuriate javascript / TypeScript klientą.

C# kliento programos pavyzdys:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

Nuskaitę prieigos atpažinimo ženklą, perduosite šį ženklą autorizavimo antraštėje kaip pateikėjo atpažinimo ženklą kartu su kiekviena užklausa, kurią siunčiate duomenų API, kaip aprašyta anksčiau.


[!INCLUDE[footer-include](../includes/footer-banner.md)]