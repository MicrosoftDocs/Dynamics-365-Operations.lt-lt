---
title: Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą
description: Šioje temoje paaiškinama, kaip naudodami tiekėjo portalą pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais vykstant pirkimo užsakymų patvirtinimo procesui. Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. gegužės mėn. „Dynamics AX“ versijoms.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07fbc5fea1fd44769a29bcc40297ffd02812a1e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "339883"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudodami tiekėjo portalą pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais vykstant pirkimo užsakymų patvirtinimo procesui. Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. gegužės mėn. „Dynamics AX“ versijoms.

Šios temos informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. gegužės mėn. „Dynamics AX“ versijoms. Tiekėjo portalo funkcija buvo pakeistą išplėstine tiekėjo bendradarbiavimo funkcija 1611 „Dynamics 365 for Operations“ versija. Daugiau informacijos apie naująją tiekėjo bendradarbiavimo funkciją ieškokite puslapyje [Tiekėjų bendradarbiavimo sąsajos naudojimas veiklai su išoriniais tiekėjais vykdyti](vendor-collaboration-work-external-vendors.md).  

Tiekėjo portalas skirtas tiekėjams, kurie neturi elektroninių duomenų mainų (EDI) integracijos su „Microsoft Dynamics AX“, skirtos mainytis pirkimo užsakymų (PU) informacija. Portale pirkimo agentai gali tiekėjui siųsti PU ir tada tiesiai programoje „Dynamics AX“ gauti atsakymą Patvirtinta arba Atmesta.  

Procesą galima sukonfigūruoti taip, kad tiekėjo patvirtinimas automatiškai patvirtintų užsakymą. Tokiu atveju užsakymą neautomatiškai vykdyti reikia tik kai užsakymas yra atmetamas arba kai tiekėjo patvirtinimas yra užregistruojamas kaip atsakymas, bet PU būsena neatnaujinama kaip **Patvirtinta** dėl patvirtinimo proceso problemos.

## <a name="po-confirmation-and-rejection"></a>PU patvirtinimas ir atmetimas
PU rengiami programoje „Dynamics AX“. Kai turite PU, kurio būsena yra **Patvirtinta**, jį siųsti tiekėjui galite generuodami patvirtinimo užklausą. Jei norite atkreipti tiekėjo dėmesį į naują PU, taip pat galite jį siųsti el. paštu, naudodami spausdinimo valdymo sistemą. PU rodomas Tiekėjo portale su galimybe tiekėjui jį patvirtinti arba atmesti. Tiekėjas taip pat gali įtraukti komentarų ir taip paskelbti informaciją, pvz., PO keitimus.  

Tiekėjo portale tiekėjas gali matyti užsakymų eilutes. Šios eilutės apima tokią informaciją kaip išorinis produkto numeris, dimensijos, kainos informacija, kiekis, pristatymo data ir pristatymo adresas. Tiekėjas gali generuoti ataskaitą, kurioje būtų rodoma PU informacija bei bendra kaina. Tiekėjui aktualios išlaidos rodomos tiekėjui antraštėje arba eilutėse spustelėjus mygtuką **Išlaidos**. Tiekėjai gali importuoti pirkimo užsakymo informaciją į savo sistemą naudodami funkciją **Eksportuoti į „Excel“**.  

Toliau pateikiamoje lentelėje parodomas įprastas keitimasis informacija, atsižvelgiant į tai, kaip tiekėjas atsako, kai siunčiate patvirtinti PU.

| Atsakymo tipas                                                                                                  | Rezultatas                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tiekėjas patvirtina užsakymą. Sistema sukonfigūruota automatiškai patvirtinti PU, kai juos patvirtina tiekėjas.    | Užsakymo būsena atnaujinama į **Patvirtinta**. Jei dėl kokios nors priežasties užsakymo patvirtinti nepavyksta, tiekėjo atsakymas vis tiek įrašomas kaip **Patvirtinta**, tačiau PU būsena lieka **Peržiūrima išorėje**.                                                                       |
| Tiekėjas patvirtina užsakymą. Sistema nesukonfigūruota automatiškai patvirtinti PU, kai juos patvirtina tiekėjas. | Tiekėjo atsakymas įrašomas kaip **Patvirtinta**, bet PU būsena lieka **Peržiūrima išorėje**.                                                                                                                                                                                      |
| Tiekėjas atmeta užsakymą.                                                                                     | Tiekėjo atsakymas įrašomas kaip **Atmesta** ir PU būsena lieka **Peržiūrima išorėje**. Atmetimas gaunamas kartu su priežastimi ir keitimo siūlymu, pvz., alternatyvia pristatymo data. Atnaujinate PU ir siunčiate patvirtinti naują versiją. |

## <a name="changes-to-a-po"></a>PU keitimai
Kai reikia pakeisti PU, kuris jau buvo patvirtintas, naują PU tiekėjui galite siųsti naudodami Tiekėjo portalą. Naujasis PU turės versijos priedėlį, kuris nurodys, kad PU yra modifikuota anksčiau paskelbto PU versija. Tiekėjo portale tiekėjai gali sekti kiekvieno užsakymo istoriją. Anksčiau patvirtinta PU versija patvirtintų PU sąraše liks tol, kol bus patvirtintas naujasis PU.  

Kai atšaukiate PU, jo būsena vėl pakeičiama į **Patvirtinta**. PU turite siųsti atgal tiekėjui naudodami Tiekėjo portalą, kad tiekėjas galėtų atšaukimą patvirtinti arba atmesti. Patvirtinus atšaukimą, PU tiekėjo patvirtintų PU sąraše rodomas kaip **Atšaukta**.

## <a name="versions-status-transitions-and-change-management"></a>Versijos, būsenų pasikeitimai ir keitimų valdymas
Kai PU išsiunčiamas tiekėjui, sistemoje jis užregistruojamas kaip konkreti PU versija ir jo būsena iš **Patvirtinta** pakeičiama į **Peržiūrima išorėje**. Jei PU pakeičiamas vėliau, sukuriama nauja PU versija, o būsena grąžinama į **Patvirtinta** (arba **Juodraštis**, jei įjungtas keitimų valdymas).  

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai.

| Veiksmas                                                   | Būsena ir versija                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Programoje „Dynamics AX“ sukuriama pradinė PU versija. | Jo būsena yra **Patvirtinta**.                                                                           |
| PU siunčiamas į Tiekėjo portalą.                     | Versija yra užregistruojama Tiekėjo portale ir būsena pakeičiama į **Peržiūrima išorėje**.    |
| Atliekate keitimus, kurių prašė tiekėjas.  | Būsena grąžinama į **Patvirtinta**.                                                            |
| Naująją PU versiją nusiunčiate į Tiekėjo portalą. | Tiekėjo portale užregistruojama nauja versija ir būsena pakeičiama į **Peržiūrima išorėje**. |
| Tiekėjas patvirtina naująją PU versiją.           | Būsena pakeičiama į **Patvirtinta**.                                                                |

Norėdami pamatyti tiekėjui išsiųstų PU versijas ir tiekėjų atsakymus, pirkimo užsakyme spustelėkite **Žurnalai** &gt; **Patvirtinimo užklausos**.  

Užsakymai, kurie buvo išsiųsti tiekėjui patvirtinti ir kurių būsena yra **Peržiūrima išorėje**, rodomi sąraše **Į tiekėjo portalą išsiųsti pirkimo užsakymai; laukiama atsako** arba sąraše **Į tiekėjo portalą išsiųsti pirkimo užsakymai; kad būtų pateiktas atsakas, reikia atlikti veiksmą**. Kai užsakymą, kuris buvo išsiųstas tiekėjui, pakeičiate taip, kad jo būsena grąžinama į **Patvirtinta**, užsakymas šiuose sąrašuose neberodomas. Norėdami pamatyti, ar anksčiau būta tiekėjo pateiktų atsakymų dėl užsakymo, spustelėkite **Žurnalai** &gt; **Patvirtinimo užklausos**.  

Tiekėjams Tiekėjo portale PU patvirtinti nereikia. Jie taip pat gali nusiųsti el. laišką arba apie PU patvirtinimą paskelbti kitais kanalais. Tada užsakymą rankiniu būdu galite patvirtinti programoje „Dynamics AX“. Tokiu atveju gaunate įspėjimą, kad užsakymas patvirtinamas, nors nėra jokio atsakymo iš tiekėjo. PU tada rodomas Tiekėjo portalo patvirtinimo istorijoje, kaip atidarytas patvirtintas užsakymas, neturintis jokių atsakymų. Be to, tiekėjas nebegali PU patvirtinti arba atmesti.  

**Pastaba.** PO versija, kurią gali naudoti kiti „Dynamics AX“ procesai, visada yra naujausia, net jei ta versija dar neužregistruota.

### <a name="change-management"></a>Keitimų valdymas

Jei esate įjungę PU keitimų valdymą, prieš pasiekdamas būseną **Patvirtinta** PU pereina patvirtinimo darbo eigą. Šio proceso tiekėjas nemato.  

Kai įjungtas PU keitimų valdymas, versija registruojama PU patvirtinus, o ne PU nusiuntus tiekėjui ar patvirtinus.  

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai, kai įjungtas keitimų valdymas.


|                                                    Veiksmas                                                     |                                                                                                                                                                                                                      Būsena ir versija                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           Programoje „Dynamics AX“ sukuriama pradinė PU versija.                            |                                                                                                                                                                                                            Jo būsena yra <strong>Juodraštis</strong>.                                                                                                                                                                                                             |
| PU teikiamas patvirtinti. (Tai yra vidinis procesas, kuriame tiekėjas nedalyvauja.) |                                                                                                                        Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš <strong>Juodraštis</strong> pakeičiama į <strong>Peržiūrima</strong> ir tada į <strong>Patvirtinimas</strong>. Patvirtintas PU užregistruojamas kaip versija.                                                                                                                        |
|                                      PU siunčiamas į tiekėjo portalą                                      |                                                                                                                                                                      Versija yra užregistruojama Tiekėjo portale ir būsena pakeičiama į <strong>Peržiūrima išorėje</strong>.                                                                                                                                                                       |
|                            Atliekate keitimus, kurių prašė tiekėjas.                            |                                                                                                                                                                                                    Būsena grąžinama į <strong>Juodraštis</strong>.                                                                                                                                                                                                     |
|                              PU vėl teikiamas patvirtinti.                               | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš <strong>Juodraštis</strong> pakeičiama į <strong>Peržiūrima</strong> ir tada į <strong>Patvirtinimas</strong>. Taip pat galima sukonfigūruoti sistemą taip, kad atlikus konkrečius laukų keitimus nereikėtų patvirtinti iš naujo. Tokiu atveju būsena pirmiausia pakeičiama į <strong>Juodraštis</strong> ir tada automatiškai atnaujinama į <strong>Patvirtinta</strong>. Patvirtintas PU užregistruojamas kaip nauja versija. |
|                           Naująją PU versiją nusiunčiate į Tiekėjo portalą.                            |                                                                                                                                                                    Naujoji versija yra užregistruojama Tiekėjo portale ir būsena pakeičiama į <strong>Peržiūrima išorėje</strong>.                                                                                                                                                                     |
|                                Tiekėjas patvirtina naująją PU versiją.                                 |                                                                                                                                                     Būsena pakeičiama į <strong>Patvirtinta</strong> automatiškai arba kai gaunate tiekėjo atsakymą ir patvirtinate PU.                                                                                                                                                     |

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Tiekėjo bendradarbiavimo funkcijos vartotojų saugos konfigūracija](configure-security-vendor-portal-users.md)

[Tiekėjo bendradarbiavimo SF išrašymo darbo srities peržiūra](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)



