---
title: Tiekėjo bendradarbiavimas su išoriniais tiekėjais
description: Šioje temoje aprašoma, kaip naudodami pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais, norėdami apsikeisti informacija apie pirkimo užsakymus ir konsignacijos atsargas.
author: kamaybac
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d8d2b1f98803bc159d3164d4a7c883e088ca7e56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837662"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Tiekėjo bendradarbiavimas su išoriniais tiekėjais

[!include [banner](../includes/banner.md)]

Modulis **Tiekėjo bendradarbiavimas** skirtas tiekėjams, kurie neturi elektroninių duomenų mainų (EDI) integracijos su „Microsoft“ „Dynamics 365 Supply Chain Management“. Jis tiekėjams suteikia galimybę dirbti su pirkimo užsakymais (PU), SF, konsignacijos atsargų informacija ir pasiūlymo užklausomis (RFQ), taip pat jis suteikia galimybę pasiekti savo tiekėjo bendrųjų duomenų dalis. Šioje temoje paaiškinama, kaip galite bendradarbiauti su išoriniais tiekėjais, kurie naudoja tiekėjo bendradarbiavimo sąsają, norėdami dirbti su PU, RFQ ir konsignacijos atsargomis. Joje taip pat paaiškinama, kaip tiekėjo bendradarbiavimo funkciją įjungti konkrečiam tiekėjui ir kaip nurodyti informaciją, kurią matys visi tiekėjai, atsakydami į PU.

Daugiau informacijos apie tai, ką išoriniai tiekėjai gali atlikti tiekėjo bendradarbiavimo sąsajoje, ieškokite puslapyje [Tiekėjo bendradarbiavimas su klientais](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Šioje temoje pateikiama informacija apie tiekėjo bendradarbiavimą taikoma tik dabartinei Tiekimo grandinės valdymo versijai. „Microsoft Dynamics AX 7.0“ (2016 m. vasario mėn.) ir „Microsoft Dynamics AX“ 7.0.1 programos versijoje (2016 m. gegužės mėn.) su tiekėjais galite bendradarbiauti naudodami modulį **Tiekėjo portalas**. Norėdami gauti daugiau informacijos apie modulį **Tiekėjo portalas**, žr. [Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą](collaborate-vendors-vendor-portal.md).

Daugiau informacijos apie tai, kaip tiekėjai gali tiekėjo bendradarbiavimą naudoti sąskaitų išrašymo procesuose, ieškokite puslapyje [Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Informacijos apie tai, kaip konfigūruoti naujus tiekėjo bendradarbiavimo vartotojus, ieškokite puslapyje [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Informacijos, kuri rodoma tiekėjams, atsakantiems į PU, nustatymas

Kai tiekėjai atsako į jiems siunčiamą PU, jie mato vieną iš trijų pranešimų langų, kuriame turi patvirtinti, kad nori priimti, atmesti arba priimti PU su keitimais. Informacija, kuri tuo metu turi būti rodoma tiekėjui, gali būti konkrečiai susijusi su jūsų verslu, todėl galite nurodyti tekstą, kuris bus rodomas kiekviename patvirtinimo pranešime. Pvz., tekstas tiekėją gali informuoti apie kitus proceso veiksmus arba apie sąlygas.

Norėdami nurodyti tekstą, kuris rodomas PU atsakyme, atlikite tolesnius veiksmus

1. Puslapyje **Informacija tiekėjams, atsakantiems į PU** pasirinkite atsakymo tipą, tada pasirinkite **Redaguoti**.
2. Lauke **Informacinis pranešimas** įveskite informaciją, kuri turi būti rodoma tiekėjams pranešimo lange.

Jei turite įtraukti pranešimų daugiau nei viena kalba, kurkite atskirus pranešimus ir nurodykite kiekvieno atitinkamą kalbos kodą. Kiekvienam tiekėjui pranešimas bus rodomas tiekėjo vartojama kalba.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Konkretaus tiekėjo bendradarbiavimo parinkčių nustatymas

Administratorius konfigūruoja bendruosius tiekėjo bendradarbiavimo parametrus, pvz., saugos vaidmenis, skirtus visiems tiekėjams, su kuriais bendradarbiaujate. Tačiau taip pat yra parametrų, kurie kiekvieno tiekėjo paskyroje gali būti rodomi skirtingai. Turėtumėte šiuos parametrus sukonfigūruoti.

- Įjunkite tiekėjo bendradarbiavimą.
- Nurodykite, ar tiekėjas turėtų matyti informaciją apie kainas.

### <a name="enabling-vendor-collaboration"></a>Tiekėjo bendradarbiavimo įjungimas

Prieš kuriant vartotojų paskyras išoriniam tiekėjui, reikia sukonfigūruoti tiekėjo kodą, kad jis galėtų naudoti tiekėjo bendradarbiavimą. Puslapio **Tiekėjai** skirtuke **Bendra** nustatykite lauką **Bendradarbiavimo aktyvinimas**. Galimos toliau nurodytos parinktys.

- **Aktyvus (PU yra automatiškai patvirtinamas)**– PU automatiškai patvirtinami, jei tiekėjas priima juos be keitimų.
- **Aktyvus (PU automatiškai netvirtinamas)**– jūsų organizacija turi patvirtinti PU pati po to, kai tiekėjas juos priima.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Nurodymas, ar tiekėjas turėtų matyti informaciją apie kainas

Norėdami bendrinti PU kainų informaciją per tiekėjo bendradarbiavimo sąsają, tiekėjo kodo skirtuke **Pirkimo užsakymo numatytosios reikšmės** turite nustatyti parinktį **Pirkimo užsakymo kainos / suma** į **Taip**. Ši kainų informacija apima vieneto kainą, nuolaidas ir išlaidas.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Darbas su PU naudojant tiekėjo bendradarbiavimą

### <a name="sending-a-po-to-a-vendor"></a>PU siuntimas tiekėjui

EKA ruošiami Tiekimo grandinės valdyme. Kai PU būsena yra **Patvirtintas**, jis tiekėjui siunčiamas pasirenkant puslapio **Pirkimo užsakymas** veiksmą **Siųsti patvirtinti**. Tada PU būsena pasikeičia į **Peržiūrima išorėje**. Išsiuntus PU tiekėjas gali matyti jį puslapyje **Pirkimo užsakymai, kuriuos galima peržiūrėti** tiekėjo bendradarbiavimo sąsajoje. Tada tiekėjas gali priimti PU, jį atmesti arba pasiūlyti pakeitimų. Tiekėjas taip pat gali įtraukti komentarų ir taip paskelbti informaciją, pvz., PO keitimus. Jei norite atkreipti tiekėjo dėmesį į naują PU, taip pat galite jį siųsti el. paštu, naudodami spausdinimo valdymo sistemą.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Tiekėjo PU patvirtinimas ir priėmimas

Kai tiekėjas priima PU, PU gali būti patvirtintas automatiškai arba neautomatiškai. Tai priklauso nuo to, ar tiekėjo laukas **Bendradarbiavimo aktyvinimas** nustatytas į parinktį **Aktyvus (PU yra automatiškai patvirtinamas)**, ar į **Aktyvus (PU automatiškai netvirtinamas)**.

Toliau pateikiamoje lentelėje parodomas įprastas keitimasis informacija, atsižvelgiant į tai, kaip tiekėjas atsako, kai siunčiate jam patvirtinti PU.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Tiekėjo atsakymas</th>
<th>Rezultatas</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Tiekėjas <strong>priima</strong> užsakymą ir Tiekimo grandinės valdymas sukonfigūruotas automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>
<td>Užsakymo būsena atnaujinama į <strong>Patvirtinta</strong>. Jei dėl kokios nors priežasties užsakymo atnaujinti&#39;nepavyksta, tiekėjo atsakymas vis tiek įrašomas kaip <strong>Priimta</strong>, tačiau PU būsena lieka <strong>Peržiūrima išorėje</strong>. 

PU, kuris buvo išsiųstas tiekėjui ir kurio būsena <strong>Peržiūrima išorėje</strong>, atnaujinamas eilutėse patvirtintomis pristatymo datomis. Šis naujinimas inicijuoja naują versiją, kuri automatiškai nustatoma į būseną <strong>Patvirtinta</strong>. Kai PU patvirtinamas, jis pasirodys tiekėjo bendradarbiavimo sąsajoje.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima</strong> užsakymą, tačiau Tiekimo grandinės valdymas ne&#39;sukonfigūruotas automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Priimta</strong>, bet PU būsena lieka <strong>Peržiūrima išorėje</strong>.

PU, kuris buvo išsiųstas tiekėjui ir kurio būsena <strong>Peržiūrima išorėje</strong>, atnaujinamas eilutėse patvirtintomis pristatymo datomis. Šis naujinimas inicijuoja naują versiją, kuri automatiškai nustatoma į būseną <strong>Peržiūrima išorėje</strong>. Tada galite neautomatiškai patvirtinti PU.</td>
</tr>
<tr class="even">
<td>Tiekėjas <strong>atmeta</strong> užsakymą.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Atmesta</strong> ir PU būsena lieka <strong>Peržiūrima išorėje</strong>. Atmetimas gaunamas kartu su tiekėjo&#39;pastaba.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima</strong> užsakymą <strong>su pakeitimais</strong>. Pakeitimai siūlomi eilutės lygiu. Tiekėjas gali priimti arba atmesti atskiras eilutes. Toliau nurodyti kai kurie kiti pakeitimai, kuriuos tiekėjas gali pasiūlyti.
<ul>
<li>Keisti datas arba kiekius.</li>
<li>Suskaldykite eilutes naudodami skirtingas pristatymo datas arba kiekius.</li>
<li>Pakeisti prekę.</li>
</ul>
Tiekėjas negali&#39;keisti kainų informacijos ir išlaidų. Tačiau tiekėjas gali pasiūlyti šiuos pakeitimus naudodamas pažymas.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Priimtas su pakeitimais</strong>, o PU būsena lieka <strong>Peržiūrima išorėje</strong>. Būsenos rodo, kokių tipų pakeitimus tiekėjas pasiūlė. Informacijos apie automatinį pakeitimų naudojimą rasite tolesniame šios temos skyriuje &quot;PU naujinimas, kai tiekėjas pasiūlo pakeitimų&quot;. </td>
</tr>
</tbody>
</table>

Naudodami darbo sritį **Pirkimo užsakymų paruošimas** galite stebėti PU, kurių atžvilgiu tiekėjas atliko veiksmus. Šioje darbo srityje yra du toliau nurodyti sąrašai, kuriuose pateikiami būsenos **Peržiūrimas išorėje** PU.

- Būtina peržiūrėti išorinėje sistemoje
- Išorinėje peržiūroje laukiama tiekėjo atsakymo

### <a name="changing-a-po"></a>PU keitimas

Norėdami pakeisti PU, į kurį tiekėjas jau atsakė, turite nusiųsti tiekėjui naują PU versiją. Naujasis PU turės versijos priedėlį, kuris nurodys, kad PU yra modifikuota anksčiau išsiųsto PU versija. Puslapyje **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** jūs ir jūsų tiekėjai galite sekti kiekvieno užsakymo retrospektyvą. Anksčiau patvirtinta PU versija patvirtintų PU sąraše liks tol, kol bus patvirtintas naujasis PU.

### <a name="canceling-a-po"></a>PU atšaukimas

Kai atšaukiate PU, jo būsena vėl pakeičiama į **Patvirtinta**. PU turite siųsti atgal tiekėjui, kad jis galėtų atšaukimą patvirtinti arba atmesti. Patvirtinus atšaukimą, PU tiekėjo patvirtintų PU sąraše rodomas kaip **Atšaukta**.

### <a name="adding-attachments-to-a-po"></a>Priedų pridėjimas prie PU

Prie PU galite pridėti priedų, pvz., failų, vaizdų ir pastabų, naudodami dokumentų tvarkymo sistemą. **Išorinio** tipo priedai bus matomi tiekėjui, kai siunčiate PU.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>PU naujinimas, kai tiekėjas pasiūlo pakeitimų

Jei tiekėjas atsako į PU ir pasiūlo pakeitimų, tolesnis veiksmas yra apdoroti atsakymą.

Darbo srityje **Pirkimo užsakymo paruošimas**, sąraše **Išorinė peržiūra reikalauja veiksmų sąrašo** galite nustatyti PU, kurį tiekėjas priėmė su pakeitimais. Iš šio sąrašo taip pat galite pereiti į tiekėjo atsakymas.

Atsakydamas tiekėjas gali pakeisti pateiktą antraštės informaciją.
 
- Tiekėjo dokumento nuoroda
- Pristatymo būdas
- Pristatymo sąlygos
- Patvirtinto pristatymo data

Be to, tiekėjas gali įtraukti pastabą arba priedą.

Eilutėse tiekėjas gali pakeisti kiekį ir pristatymo datas, įtraukti pastabų ir priedų, atmesti eilutę, pakeisti eilutę kitu produktu, kuris įvestas kaip tekstas, bei išskaidyti eilutę į keletą pristatymų. Eilutės būsena priklauso nuo tiekėjo siūlomų pakeitimų.
    
- **Priimta su pakeitimais**
- **Atmestas**
- **Pakeista** – šiuo atveju įtraukiama papildoma eilutė, kurios būsena **Pakaitas**.
- **Pritarta**
- **Išskaidyti grafike** – šiuo atveju bus įtrauktos papildomos eilutės, kurių būsena **Grafiko eilutės**.

Jei eilutėje nėra pakeitimų, jos būsena yra **Priimta**.

Atsakyme galite pamatyti eilučių būsenas, kurios rodo tiekėjo atliktų pakeitimų tipus. Be to, visi pakeisti laukai rodomi paryškintai, kad galėtumėte matyti pakeitimus.

PU galite atnaujinti pasirinkdami atsakymo arba vienos eilutės veiksmą **Apdoroti PU naujinimą**. Laukas **Ar PU naujinimas apdorotas?** antraštėje ir eilutėse nurodo, ar sistema apdorojo antraštę arba eilutes, kad PU būtų atnaujintas galimais atsakymo pakeitimais. Veiksmą **Apdoroti PU naujinimą** galima paleisti tik kartą vienai antraštei arba eilutei.

Ne visi siūlomi pakeitimai gali būti atnaujinti PU. PU automatiškai galima atnaujinti tik antraštę ir eilučių datas bei kiekius. Kiti PU pakeitimai atliekami neautomatiškai. Tokiu atveju lauko **Ar PU naujinimas apdorotas?** reikšmė yra **Rankinis naujinimas**. Pavyzdžiui, jei tiekėjas pasiūlo, kad eilutė būtų suskaidyta į grafiką, šis pakeitimas turi būti atliktas neautomatiškai.

Kiekvienai eilutei, kurios būsena **Priimta**, bus priskirta patvirtinta pristatymo data. Kai vykdote veiksmą **Apdoroti PU naujinimą**, ši data atnaujinama PU. Pastabos ir priedai nėra automatiškai perkeliami į dabartinį PU. Kai atnaujinate dabartinį PU naudodami veiksmą **Apdoroti PU naujinimą**, prekybos sutartys nebus iš naujo įvertintos PU eilutėse.

## <a name="po-statuses-and-versions"></a>PU būsenos ir versijos

Šiame skyriuje aprašomos įvairios būsenos, kurias PU gali turėti iki patvirtinimo. Be to, aprašoma, kada naujos PU versijos buvo pateiktos tiekėjui. Veikimas gali būti įvairus, jis priklauso nuo to, ar naudojate PU pakeitimų valdymą. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijos ir būsenos, jei nenaudojate pakeitimų valdymo funkcijos

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai.

| Veiksmas | Būsena ir versija |
|--------|--------------------|
| Tiekimo grandinės valdyme sukuriama pradinė PU versija. | Jo būsena yra **Patvirtinta**. |
| PU išsiųstas tiekėjui. | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**. |
| Tiekėjas išsiunčia atsakymą **Priimta su keitimais**. | Būsena vis dar yra **Peržiūrima išorėje**. |
| Atliekate keitimus, kurių prašė tiekėjas. | Būsena grąžinama į **Patvirtinta**. |
| Naująją PU versiją nusiunčiate tiekėjui. | Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**. |
| Tiekėjas priima naująją PU versiją. | Būsena vis dar yra **Peržiūrima išorėje**, jei tiekėjo kodas nėra sukonfigūruotas automatiškai nustatyti būseną **Patvirtinta**, kai tiekėjas priima užsakymą. |

Tiekėjams nereikia patvirtinti PU naudojant tiekėjų bendradarbiavimo sąsają. Jie taip pat gali nusiųsti el. laišką arba apie PU patvirtinimą paskelbti kitais kanalais. Tada galite neautomatiškai patvirtinti užsakymą. Tokiu atveju gausite įspėjimą, kad užsakymas patvirtinamas, nors nėra jokio atsakymo iš tiekėjo. Tada PU rodomas patvirtinimo istorijoje kaip atviras patvirtintas užsakymas, neturintis jokių atsakymų. Šiuo metu tiekėjas nebegali PU patvirtinti arba atmesti.

> [!NOTE]
> PU versija, kurią gali naudoti kiti „Supply Chain Management“ procesai, visada yra naujausia, net jei ta versija tiekėjų bendradarbiavimo sąsajoje dar neužregistruota.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijos ir būsenos, jei naudojate pakeitimų valdymo funkcijos

Jei esate įjungę PU keitimų valdymą, prieš pasiekdami būseną **Patvirtinta** PU pereina patvirtinimo darbo eigą. Šio proceso tiekėjas nemato.

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai, kai įjungtas keitimų valdymas. Versija registruojama PU patvirtinus, o ne PU nusiuntus tiekėjui ar patvirtinus.

| Veiksmas | Būsena ir versija |
|--------|--------------------|
| Tiekimo grandinės valdyme sukuriama pradinė PU versija. | Jo būsena yra **Juodraštis**. |
| PU teikiamas patvirtinti. (Patvirtinimo procesas yra vidinis procesas, kuriame tiekėjas nedalyvauja.) | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Patvirtintas PU užregistruojamas kaip versija. | 
| PU išsiųstas tiekėjui. | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**. |
| Kai kuriuos tiekėjo pageidaujamus pakeitimus atliekate neautomatiniu būdu arba naudodami atsakymo veiksmą **Apdoroti PU naujinimą**, kad atnaujintumėte PU. | Būsena grąžinama į **Juodraštis**. |
| PU vėl teikiamas patvirtinti. | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Taip pat galima sukonfigūruoti sistemą taip, kad atlikus konkrečius laukų keitimus nereikėtų patvirtinti iš naujo. Tokiu atveju būsena pirmiausia pakeičiama į **Juodraštis** ir tada automatiškai atnaujinama į **Patvirtinta**. Patvirtintas PU užregistruojamas kaip nauja versija. |
| Naująją PU versiją nusiunčiate tiekėjui. | Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**. |
| Tiekėjas patvirtina naująją PU versiją. | Būsena pakeičiama į **Patvirtinta** automatiškai arba kai gaunate tiekėjo atsakymą ir patvirtinate PU. |

## <a name="sharing-information-about-consignment-inventory"></a>Informacijos apie konsignacijos atsargas bendrinimas

Jei naudojate konsignacijos atsargas, tiekėjai gali naudoti tiekėjo bendradarbiavimo sąsają, norėdami peržiūrėti informaciją tolesniuose puslapiuose.

- **Pirkimo užsakymų naudojamos konsignacijos atsargos** -konsignacijos atsargų PU generuojami, kai jūsų įmonė perima atsargų nuosavybės teises iš tiekėjo. Tuo pat metu registruojamas produkto gavimas. Šie konsignacijos PU rodomi tik puslapyje **Pirkimo užsakymų naudojamos konsignacijos atsargos**. Jie nėra įtraukti į modulio **Tiekėjo bendradarbiavimas** puslapį **Visi patvirtinti pirkimo užsakymai**.
- **Produktai, gauti iš konsignacijos atsargų** – šiame puslapyje pateikiamos visos operacijos, kuriose produktų nuosavybės teisės buvo iš tiekėjo perduotos jūsų įmonei. Tiekėjai gali naudoti šią informaciją kliento SF išrašyti.
- **Turimos konsignacijos atsargos** – šiame puslapyje rodomos turimos, tiekėjui priklausančios konsignacijos atsargos, pristatytos į jūsų sandėlį.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Darbas su RFQ naudojant tiekėjo bendradarbiavimą

Šiame skyriuje aprašoma sąveika tarp klientų ir tiekėjų RFQ proceso metu. Jame taip pat paaiškinama, kaip informacija perduodama tiekėjams. RFQ proceso palaikymo pagrindinę apžvalgą žr. [Pasiūlymo patvirtinimų (RFQ) apžvalga](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Pakaitai, priedai, pakeitimai ir grąžinimai

- **Pakaitai** – RFQ atvejo antraštėje galite nurodyti, kad leidžiami ne katalogo prekių eilučių pakaitai. Įjungus pakaitus, tiekėjai gali įtraukti kiekvienos pageidaujamos eilutės alternatyvią eilutę.
- **Priedai** – priedus galima pridėti RFQ atvejo antraštės lygyje ir eilutės lygyje. Priedus galima klasifikuoti kaip vidinius arba išorinius. Vidinius priedus galima peržiūrėti tik kliento pusėje, o išorinius priedus gali peržiūrėti tiekėjai, kai priedai išsiųsti.

    Tiekėjai taip pat gali pridėti priedų prie savo kainos siūlymo atsakymo. Šiuos priedus galima peržiūrėti kliento pusėje, kai tiekėjas pateikia kainos siūlymo atsakymą. Priedai, kuriuos pridėjo tiekėjai, visada klasifikuojami kaip išoriniai. Norėdami atidaryti priedą, kurį tiekėjas pateikė kartu su pasiūlymu, pasirinkite **Kainos siūlymų priedai** arba **Kainos siūlymo eilutės priedai**.
    
    Norėdami atidaryti priedus, kurie buvo išsiųsti kartu su RFQ atveju, naudokite dokumentų tvarkymo sąvaržėlės simbolį, pateiktą atsakyme.

- **Pakeitimai** – kai pakeitimas baigtas, esami kainos siūlymo atsakymai pašalinami, kad būtų galima atnaujinti reikšmes. RFQ atvejo žurnaluose galima peržiūrėti informaciją, pvz., ankstesnių kainos siūlymo atsakymų eilutės kainos ir kiekio informaciją.

    Norėdami taikyti pakeitimo apdorojimą, puslapio **Paraiškų parametrai** „FastTab“ **Pasiūlymo patvirtinimas** nustatykite parinktį **Užrakinti išsiųstus RFQ** į **Taip**. (Ši parinktis yra nustatyta ir būtina viešajame sektoriuje).

- **Grąžinimas** – jei tiekėjas pateikė kainos siūlymą, bet reikia daugiau arba modifikuotos informacijos apie RFQ atvejį, klientas gali grąžinti kainos siūlymą tiekėjui. Duomenys iš anksčiau pateikto kainos siūlymo yra išsaugomi ir tiekėjas gali atlikti pageidaujamus keitimus nepradėdamas kainos siūlymo proceso iš naujo.

## <a name="public-sector-extensions"></a>Viešojo sektoriaus plėtiniai

Viešajame sektoriuje išplėstinės funkcijos suteikia galimybę RFQ atvejį išsiųsti tiekėjams ir publikuoti. Publikavus RFQ, bet kas reikalaujantis informacijos gali peržiūrėti darbą, kuris atitinka daugumą viešojo sektoriaus reglamentų. Visas galimas darbas parodomas sąrašo puslapyje **Atviri paskelbti pasiūlymų patvirtinimai**, o atšauktas, laukiančias arba skirtas RFQ galima peržiūrėti sąrašo puslapyje **Uždaryti paskelbti pasiūlymų patvirtinimai**. Šiuos dokumentus taip pat galima peržiūrėti ne Tiekimo grandinės valdyme esančioje svetainėje, naudojant integravimą su toliau nurodytais duomenų objektais.

- Paskelbti pasiūlymų patvirtinimai
- Paskelbtų pasiūlymų patvirtinimų eilutė
- Paskelbtų pasiūlymų patvirtinimų antraščių priedai

Šie objektai suteikia galimybę žmonėms, kurie nėra Tiekimo grandinės valdymo sukonfigūruoti vartotojai, bet turi anoniminės prieigos prie išorinės svetainės teises, peržiūrėti galimą ir uždarytą darbą. Be to, išplėstinės funkcijos dalyje **Siųsti ir publikuoti** suteikia galimybę vartotojui, kuris nustato RFQ proceso parametrus, nustatyti el. laiško šabloną. Tada, kai įsigijimo specialistas sukuria RFQ atvejį, jis turi pasirinkti el. laiško šabloną, kad tiekėjams išsiųstų reikiamą informaciją apie RFQ atvejį. 

Vartotojas, kuris nustato RFQ proceso parametrus, gali kurti kelis el. laiškų šablonus. Šie el. laiškų šablonai gali apimti statinį tekstą ir toliau nurodytus pakeitimo atpažinimo ženklus. Atpažinimo ženklai bus pakeisti kontekstinėmis reikšmėmis, kai el. laiškas bus sukurtas.

- „%RFQCase%“
- „%RFQCaseName%“
- „%bidType%“
- „%inviteOnly%“
- „%expiryDateTime%“
- „%requester%“
- „%requestingDepartment%“
- „%accountnum%“
- „%todaysdate%“
- „%createddate%“

Jei pakeitimas yra būtinas ir yra išsiunčiamas po to, kai išsiunčiama RFQ, RFQ bus pakartotinai išsiųsta visiems pakviestiems tiekėjams. Publikuotas dokumentas taip pat bus atnaujinamas puslapyje **Atviri paskelbti pasiūlymų patvirtinimai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]