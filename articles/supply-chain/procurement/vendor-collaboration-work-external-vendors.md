---
title: "Tiekėjo bendradarbiavimas su išoriniais tiekėjais"
description: "Šioje temoje paaiškinama, kaip naudodami pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais, norėdami apsikeisti informacija apie pirkimo užsakymus ir konsignacijos atsargas."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: abff906bcdf31c91ce696afbcd651a1d7a87ea8a
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Tiekėjo bendradarbiavimas su išoriniais tiekėjais

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip naudodami pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais, norėdami apsikeisti informacija apie pirkimo užsakymus ir konsignacijos atsargas.

Modulis **Tiekėjų bendradarbiavimas** skirtas tiekėjams, kurie neturi elektroninių duomenų mainų (EDI) integracijos su „Microsoft Dynamics 365 for Finance and Operations‟. Jis suteikia tiekėjams galimybę dirbti su pirkimo užsakymo, SF ir konsignacijos atsargų informacija. Šioje temoje aprašoma, kaip galite bendradarbiauti su išoriniais tiekėjais, kurie naudoja tiekėjo bendradarbiavimo sąsają, norėdami dirbti su PU ir konsignacijos atsargomis. Joje taip pat aprašoma, kaip tiekėjo bendradarbiavimo funkciją įjungti konkrečiam tiekėjui ir kaip nurodyti informaciją, kurią matys visi tiekėjai, atsakydami į PU. Daugiau informacijos apie tai, ką išoriniai tiekėjai gali atlikti tiekėjo bendradarbiavimo sąsajoje, ieškokite puslapyje [Tiekėjo bendradarbiavimas su klientais](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Šioje temoje pateikiama informacija apie tiekėjo bendradarbiavimą taikoma tik dabartinei „Dynamics 365 for Finance and Operations“ versijai. 2016 m. vasario mėn. ir 2016 m. gegužės mėn. „Microsoft Dynamics AX“ versijose bendradarbiauti su tiekėju galite naudodami tiekėjo portalo modulį. Norėdami gauti daugiau informacijos apie tiekėjo portalo modulį, žr. [Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą](collaborate-vendors-vendor-portal.md).

Daugiau informacijos apie tai, kaip tiekėjai gali tiekėjo bendradarbiavimą naudoti sąskaitų išrašymo procesuose, ieškokite puslapyje [Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Informacijos apie tai, kaip konfigūruoti naujus tiekėjo bendradarbiavimo vartotojus, ieškokite puslapyje [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md).

Daugiau informacijos apie tai, kaip tiekėjai gali tiekėjo bendradarbiavimą naudoti sąskaitų išrašymo procesuose, ieškokite puslapyje [Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). 

Informacijos apie tai, kaip konfigūruoti naujus tiekėjo bendradarbiavimo vartotojus, ieškokite puslapyje [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Nustatykite informaciją, kuri rodoma tiekėjams, atsakantiems į PU
Kai tiekėjai atsako į jiems siunčiamą PU, jie mato pranešimo langą, kuriame turi patvirtinti, kad nori priimti, atmesti arba priimti PU su keitimais. Informacija, kuri tuo metu turi būti rodoma tiekėjui, gali būti konkrečiai susijusi su jūsų verslu, todėl galite nurodyti tekstą, kuris bus rodomas kiekviename iš trijų patvirtinimo pranešimų. Pvz., tekstas tiekėją gali informuoti apie kitus proceso veiksmus arba apie sąlygas.  

Norėdami nurodyti tekstą, kuris rodomas PU atsakyme, atlikite tolesnius veiksmus.

1.  Atidarykite puslapį **Informacija tiekėjams, atsakantiems į PU**.
2.  Pasirinkite vieną iš atsakymų tipų.
3.  Spustelėkite **Redaguoti**.
4.  Įveskite informaciją, kurią tiekėjai turėtų matyti lauke **informacinis pranešimas**.

Jei turite įtraukti pranešimų daugiau nei viena kalba, kurkite atskirus pranešimus ir nurodykite kiekvieno tinkamus kalbų kodus. Tiekėjui pranešimas bus rodomas tiekėjo vartojama kalba.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Tiekėjo bendradarbiavimo parinkčių nustatymas konkrečiam tiekėjui
„Finance and Operations“ tiekėjo bendradarbiavimo bendruosius parametrus konfigūruoja administratorius. Pvz., administratorius nustatys, kuriuos saugos vaidmenis gali naudoti visi tiekėjai, su kuriais bendradarbiaujate. Taip pat yra parametrų, kurie kiekvieno tiekėjo paskyroje gali būti rodomi skirtingai; juos reikia nustatyti:
-   Įjunkite tiekėjo bendradarbiavimą.
-   Nuspręskite, ar norite, kad tiekėjas matytų kainų informaciją.

### <a name="enable-vendor-collaboration"></a>Tiekėjo bendradarbiavimo įjungimas

Prieš kuriant vartotojų paskyras išoriniam tiekėjui, reikia sukonfigūruoti tiekėjo kodą, kad jis galėtų naudoti tiekėjo bendradarbiavimą. Norėdami tai atlikti, puslapio **Tiekėjai** skirtuke **Bendra** nustatykite lauką **Bendradarbiavimo aktyvinimas** kaip aktyvų. Galima naudoti dvi parinktis.

-   **Aktyvus (PU yra automatiškai patvirtinamas)**– pirkimo užsakymai automatiškai patvirtinami, kai tiekėjas priima juos be keitimų.
-   **Aktyvus (PU automatiškai netvirtinamas)**– pirkimo užsakymus jūsų organizacija turi patvirtinti pati po to, kai tiekėjas juos priima.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Nuspręskite, ar norite, kad tiekėjas matytų kainų informaciją

Jei bendradarbiavimo sąsajoje norite bendrinti kainų informaciją, pvz., vieneto kainą, nuolaidas ir išlaidas, tiekėjo kode jums reikia nustatyti parinktį **Pirkimo užsakymo kainos / suma** į **Taip**. Ši parinktis pateikiama skirtuke **Pirkimo užsakymo numatytosios reikšmės**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Darbas su PU naudojant tiekėjo bendradarbiavimą
### <a name="sending-a-po-to-the-vendor"></a>PU siuntimas tiekėjui

Pirkimo užsakymai ruošiami programoje „Finance and Operations“. Kai PU būsena yra **Patvirtintas**, jis tiekėjui siunčiamas naudojant puslapio **Pirkimo užsakymas** veiksmą **Siųsti patvirtinti**. PU būsena pasikeičia į **Peržiūrima išorėje**. Išsiuntus PU tiekėjas gali matyti jį puslapyje **Pirkimo užsakymai, kuriuos galima peržiūrėti** tiekėjo bendradarbiavimo sąsajoje. Tada tiekėjas gali priimti užsakymą, jį atmesti arba pasiūlyti pakeitimų. Tiekėjas taip pat gali įtraukti komentarų ir taip paskelbti informaciją, pvz., PO keitimus. Jei norite atkreipti tiekėjo dėmesį į naują PU, taip pat galite jį siųsti el. paštu, naudodami spausdinimo valdymo sistemą.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Tiekėjo PU patvirtinimas ir priėmimas

Kai tiekėjas priima pirkimo užsakymą, PU gali būti patvirtintas automatiškai arba neautomatiškai. Tai priklauso nuo to, ar tiekėjo laukas **Tiekėjo aktyvinimas** nustatytas į parinktį **Aktyvus (PU yra automatiškai patvirtinamas)**, ar į **Aktyvus (PU automatiškai netvirtinamas)**.  

Toliau pateikiamoje lentelėje parodomas įprastas keitimasis informacija, atsižvelgiant į tai, kaip tiekėjas atsako, kai siunčiate jam patvirtinti PU.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Tiekėjo atsakymas</strong></td>
<td><strong>Rezultatas</strong></td>
</tr>
<tr class="even">
<td>Tiekėjas <strong>priima</strong> užsakymą. „Finance and Operations‟ sukonfigūruota automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>

<td>Užsakymo būsena atnaujinama į <strong>Patvirtinta</strong>. Jei dėl kokios nors priežasties užsakymo patvirtinti nepavyksta, tiekėjo atsakymas vis tiek įrašomas kaip <strong>Priimta</strong>, tačiau PU būsena lieka <strong>Peržiūrima išorėje</strong>. 

PU, kuris buvo išsiųstas tiekėjui ir kurio būsena **Peržiūrima išorėje**, atnaujinamas eilutėse patvirtintomis pristatymo datomis. Naujinimas inicijuoja naują versiją, kuri automatiškai atnaujinama į būseną **Patvirtinta**. Kai PU patvirtinamas, jis pasirodys tiekėjo bendradarbiavimo sąsajoje.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima</strong> užsakymą. „Finance and Operations‟ nesukonfigūruota automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Priimta</strong>, bet PU būsena lieka <strong>Peržiūrima išorėje</strong>.

PU, kuris buvo išsiųstas tiekėjui ir kurio būsena **Peržiūrima išorėje**, atnaujinamas eilutėse patvirtintomis pristatymo datomis. Naujinimas inicijuoja naują versiją, kuri bus nustatyta į **Peržiūrima išorėje**. Tada galėsite rankiniu būdu patvirtinti PU.</td>

</tr>
<tr class="even">
<td>Tiekėjas <strong>atmeta</strong> užsakymą.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Atmesta</strong> ir PU būsena lieka <strong>Peržiūrima išorėje</strong>. Atmetimas gaunamas kartu su tiekėjo pastaba.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima užsakymą su pakeitimais</strong>. Pakeitimai siūlomi eilutės lygiu. Galima priimti arba atmesti atskiras eilutes. Toliau pateikti kiti galimi keitimai.
<ul>
<li>Datų arba kiekių keitimas.</li>
<li>Eilučių skaldymas naudojant skirtingas pristatymo datas arba kiekius.</li>
<li>Prekės pakeitimas.</li>
</ul>
Tiekėjas negali keisti kainų informacijos ir išlaidų. Tokių keitimų pasiūlymus galima pateikti naudojant pastabas.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Priimtas su pakeitimais</strong>, o PU būsena lieka <strong>Peržiūrima išorėje</strong>. Būsenos rodo, kokių tipų pakeitimus tiekėjas pasiūlė. Informacijos apie automatinį pakeitimų naudojimą rasite tolesniame skyriuje, kaip atnaujinti PU, kai tiekėjas pasiūlo pakeitimų. </td>
</tr>
</tbody>
</table>

Naudodami darbo sritį **Pirkimo užsakymų** **paruošimas** galite stebėti PU, kurių atžvilgiu tiekėjas atliko veiksmus. Šioje darbo srityje yra du toliau nurodyti sąrašai, kuriuose pateikiami būsenos **Peržiūrimas išorėje** pirkimo užsakymai.

-   Būtina peržiūrėti išorinėje sistemoje.
-   Išorinėje peržiūroje laukiama tiekėjo atsakymo.

### <a name="changing-a-po"></a>PU keitimas

Norėdami pakeisti PU, į kurį jau atsakyta, turite nusiųsti tiekėjui naują PU versiją. Naujasis PU turės versijos priedėlį, kuris nurodys, kad PU yra modifikuota anksčiau paskelbto PU versija. Puslapyje **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** jūs ir jūsų tiekėjai galite sekti kiekvieno užsakymo retrospektyvą. Anksčiau patvirtinta PU versija patvirtintų PU sąraše liks tol, kol bus patvirtintas naujasis PU.

### <a name="cancelling-a-po"></a>PU atšaukimas

Kai atšaukiate PU, jo būsena vėl pakeičiama į **Patvirtinta**. PU turite siųsti atgal tiekėjui, kad jis galėtų atšaukimą patvirtinti arba atmesti. Patvirtinus atšaukimą, PU tiekėjo patvirtintų PU sąraše rodomas kaip **Atšaukta**.

### <a name="adding-attachments-to-a-po"></a>Priedų pridėjimas prie PU

Prie PU galite pridėti priedų, pvz., failų, vaizdų ir pastabų, naudodami dokumentų tvarkymo sistemą. **Išorinio** tipo priedai bus matomi tiekėjui, kai siunčiate PU.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Atnaujinti PU, kai tiekėjas pasiūlo pakeitimų
Kai tiekėjas atsako į PU ir pasiūlo pakeitimų, tolesnis veiksmas yra apdoroti atsakymą.
**Pirkimo užsakymo paruošimo darbo srityje** išorinė peržiūra reikalauja veiksmų sąrašo; galite nustatyti PU, į kurį tiekėjas atsakė priimdamas su pakeitimais. Išorinė peržiūra reikalauja veiksmų sąrašo, be to, galite pasiekti tiekėjo atsakymą. Atsakydamas tiekėjas gali pakeisti pateiktą antraštės informaciją.
 
-   Tiekėjo dokumento nuoroda
-   Pristatymo būdas
-   Pristatymo sąlygos
-   Patvirtinto pristatymo data

Be to, tiekėjas gali įtraukti pastabą arba priedą

Eilutėse tiekėjas gali pakeisti kiekį ir pristatymo datas, įtraukti pastabų ir priedų, atmesti eilutę, pakeisti eilutę kitu produktu, kuris įvestas kaip tekstas, bei išskaidyti eilutę į keletą pristatymų. Priklausomai nuo to, kokius pakeitimus tiekėjas siūlo, eilutės būsena gali būti skirtinga:
    
-   **Priimta su pakeitimais**
-   **Atmesta**
-   **Pakeista** šiuo atveju įtraukiama papildoma eilutė, kurios būsena **Pakaitas**.
-   **Patvirtinta** Išskaidyti grafike. Šiuo atveju bus įtrauktos papildomos eilutės, kurių būsena **Grafiko eilutės**.

Jei eilutėje nėra pakeitimų, jos būsena yra **Priimta**.

Atsakyme galite pamatyti anksčiau paminėtas eilučių būsenas, kurios rodo tiekėjo atliktų pakeitimų tipus. Be to, visi pakeisti laukai rodomi paryškintai, kad galėtumėte matyti pakeitimus.

PU galite atnaujinti vienu metu spustelėdami atsakymo veiksmą **Apdoroti PU naujinimą** arba vieną eilutę. Indikatorius **Ar PU naujinimas apdorotas?** antraštėje ir eilutėse leidžia matyti, ar sistema apdorojo antraštę arba eilutes, kad PU būtų atnaujintas galimais atsakymo pakeitimais. Procesą **Apdoroti PU naujinimą** galima paleisti tik kartą vienai antraštei arba eilutei.

Ne visi siūlomi pakeitimai gali būti atnaujinti PU. PU automatiškai galima atnaujinti tik antraštę ir eilučių datas bei kiekius. Kiti PU pakeitimai atliekami neautomatiškai. Tokiu atveju indikatorius **Ar PU naujinimas apdorotas?** rodo **Rankinis naujinimas**. Pakeitimo, kuris turi būti tvarkomas neautomatiškai, pavyzdys: tiekėjas pasiūlo išskaidyti eilutę grafike.

Eilutė, kurios būsena yra **Priimta**, turės patvirtintą pristatymo datą, kuri bus atnaujinta PU, kai vykdysite **Apdoroti PU naujinimą**. Pastabos ir priedai nebus automatiškai perkeliamas į dabartinį PU. Atkreipkite dėmesį, kad kai atnaujinate dabartinį PU naudodami veiksmą **Apdoroti PU naujinimą**, prekybos sutartys nebus iš naujo įvertintos PU eilutėse.


## <a name="po-statuses-and-versions"></a>PU būsenos ir versijos
Šiame skyriuje aprašomos įvairios būsenos, kurias PU gali turėti iki patvirtinimo. Be to, aprašoma, kada naujos PU versijos buvo pateiktos tiekėjui. Veikimas gali būti įvairus, jis priklauso nuo to, ar naudojate PU pakeitimų valdymą. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijos ir būsenos, jei nenaudojate pakeitimų valdymo funkcijos

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veiksmas**                                                               | **Būsena ir versija**                                                                                                                                       |
| Programoje „Finance and Operations‟ sukuriama pradinė PU versija. | Jo būsena yra **Patvirtinta**.                                                                                                                                  |
| PU išsiųstas tiekėjui.                                            | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                          |
| Tiekėjas išsiunčia atsakymą **Priimta su keitimais**.                  | Būsena vis dar yra **Peržiūrima išorėje**.                                                                                                                  |
| Atliekate keitimus, kurių prašė tiekėjas.                  | Būsena grąžinama į **Patvirtinta**.                                                                                                                        |
| Naująją PU versiją nusiunčiate tiekėjui.                        | Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                      |
| Tiekėjas priima naująją PU versiją.                            | Būsena vis dar yra **Peržiūrima išorėje**, jei tiekėjo kodas nėra sukonfigūruotas automatiškai nustatyti būseną **Patvirtinta**, kai tiekėjas priima užsakymą. |


Tiekėjams nereikia patvirtinti PU naudojant tiekėjų bendradarbiavimo sąsają. Jie taip pat gali nusiųsti el. laišką arba apie PU patvirtinimą paskelbti kitais kanalais. Galite patvirtinti užsakymą neautomatiškai programoje „Finance and Operations“. Tokiu atveju gausite įspėjimą, kad užsakymas patvirtinamas, nors nėra jokio atsakymo iš tiekėjo. Tada PU rodomas patvirtinimo istorijoje kaip atviras patvirtintas užsakymas, neturintis jokių atsakymų. Tiekėjas nebegali PU patvirtinti arba atmesti.  


>[!NOTE]
>PU versija, kurią gali naudoti kiti „Dynamics 365 for Finance and Operations“ procesai, visada yra naujausia, net jei ta versija tiekėjų bendradarbiavimo sąsajoje dar neužregistruota.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijos ir būsenos, jei naudojate pakeitimų valdymo funkcijos

Jei esate įjungę PU keitimų valdymą, prieš pasiekdamas būseną **Patvirtinta** PU pereina patvirtinimo darbo eigą. Šio proceso tiekėjas nemato.  

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai, kai įjungtas keitimų valdymas. Versija registruojama PU patvirtinus, o ne PU nusiuntus tiekėjui ar patvirtinus.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veiksmas**                                                               | **Būsena ir versija**                                                                                                                                       |
| Programoje „Finance and Operations‟ sukuriama pradinė PU versija.      | Jo būsena yra **Juodraštis**.  |
| PU teikiamas patvirtinti. (Patvirtinimo procesas yra vidinis procesas, kuriame tiekėjas nedalyvauja.)                                                           | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Patvirtintas PU užregistruojamas kaip versija.           | 
| PU išsiųstas tiekėjui.                                                            | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.      |
| Kai kuriuos tiekėjo pageidaujamus pakeitimus atliekate neautomatiniu būdu arba naudodami atsakymo veiksmą, kad atnaujintumėte PU.                                                            | Būsena grąžinama į **Juodraštis**.     |
|PU vėl teikiamas patvirtinti.                                                |  Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Taip pat galima sukonfigūruoti sistemą taip, kad atlikus konkrečius laukų keitimus nereikėtų patvirtinti iš naujo. Tokiu atveju būsena pirmiausia pakeičiama į **Juodraštis** ir tada automatiškai atnaujinama į **Patvirtinta**. Patvirtintas PU užregistruojamas kaip nauja versija.                                         |
|Naująją PU versiją nusiunčiate tiekėjui.                                                |  Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                         |
|Tiekėjas patvirtina naująją PU versiją.                                                |  Būsena pakeičiama į **Patvirtinta** automatiškai arba kai gaunate tiekėjo atsakymą ir patvirtinate PU. |

## <a name="share-information-about-consignment-inventory"></a>Informacijos apie konsignacijos atsargas bendrinimas
Jei naudojate konsignacijos atsargas, tiekėjai gali naudoti tiekėjo bendradarbiavimo sąsają, norėdami peržiūrėti informaciją tolesniuose puslapiuose.

-   **Pirkimo užsakymų naudojamos konsignacijos atsargos** -konsignacijos atsargų pirkimo užsakymai generuojami, kai jūsų įmonė perima atsargų nuosavybės teises iš tiekėjo. Tuo pat metu registruojamas produkto gavimas. Šie konsignacijos pirkimo užsakymai rodomi tik puslapyje **Pirkimo užsakymų naudojamos konsignacijos atsargos**. Jie nėra įtraukti į modulio **Tiekėjo bendradarbiavimas** puslapį **Visi patvirtinti pirkimo užsakymai**.
-   **Produktai, gauti iš konsignacijos atsargų** – šiame puslapyje pateikiamos visos operacijos, kuriose produktų nuosavybės teisės buvo iš tiekėjo perduotos jūsų įmonei. Tiekėjai gali naudoti šią informaciją kliento SF išrašyti.
-   **Turimos konsignacijos atsargos** – šiame puslapyje rodomos turimos, tiekėjui priklausančios konsignacijos atsargos, pristatytos į jūsų sandėlį.





