---
title: "Tiekėjo bendradarbiavimas su išoriniais tiekėjais"
description: "Šioje temoje paaiškinama, kaip naudodami pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais, norėdami apsikeisti informacija apie pirkimo užsakymus ir konsignacijos atsargas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c8947f9335b3a2de83ab00bad1043ee14d35f2c8
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Tiekėjo bendradarbiavimas su išoriniais tiekėjais

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip naudodami pirkimo agentai gali bendradarbiauti su išoriniais tiekėjais, norėdami apsikeisti informacija apie pirkimo užsakymus ir konsignacijos atsargas.

Modulis **Tiekėjo bendradarbiavimas** skirtas tiekėjams, kurie neturi elektroninių duomenų mainų (EDI) integracijos su „Microsoft Dynamics 365 for Operations‟. Jis suteikia tiekėjams galimybę dirbti su pirkimo užsakymo, SF ir konsignacijos atsargų informacija. Šioje temoje aprašoma, kaip galite bendradarbiauti su išoriniais tiekėjais, kurie naudoja tiekėjo bendradarbiavimo sąsają, norėdami dirbti su PU ir konsignacijos atsargomis. Joje taip pat aprašoma, kaip tiekėjo bendradarbiavimo funkciją įjungti konkrečiam tiekėjui ir kaip nurodyti informaciją, kurią matys visi tiekėjai, atsakydami į PU. Daugiau informacijos apie tai, ką išoriniai tiekėjai gali atlikti tiekėjo bendradarbiavimo sąsajoje, ieškokite puslapyje [Tiekėjo bendradarbiavimas su klientais](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Daugiau informacijos apie tai, kaip tiekėjai gali tiekėjo bendradarbiavimą naudoti sąskaitų išrašymo procesuose, ieškokite puslapyje [Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Informacijos apie tai, kaip konfigūruoti naujus tiekėjo bendradarbiavimo vartotojus, ieškokite puslapyje [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Į PU atsakantiems tiekėjams rodomos informacijos nustatymas
Kai tiekėjai atsako į jiems siunčiamą PU, jie mato dialogo langą, kuriame jie turi patvirtinti, kad nori priimti, atmesti arba priimti PU su keitimais. Informacija, kuri tuo metu turi būti rodoma tiekėjui, gali būti konkrečiai susijusi su jūsų verslu, todėl galite nurodyti tekstą, kuris bus rodomas kiekviename iš trijų patvirtinimo pranešimų. Pvz., tekstas tiekėją gali informuoti apie kitus proceso etapus arba apie sąlygas.  

Norėdami nurodyti tekstą, kuris rodomas PU atsakyme, atlikite tolesnius veiksmus.

1.  Atidarykite puslapį **Informacija tiekėjams, atsakantiems į PU**.
2.  Pasirinkite vieną iš atsakymų tipų.
3.  Spustelėkite **Redaguoti.**
4.  Įveskite informaciją, kurią tiekėjai turėtų matyti lauke **informacinis pranešimas**.

Jei norite įtraukti pranešimų daugiau nei viena kalba, kurkite atskirus pranešimus su atitinkamos kalbos kodais. Tiekėjas pranešimą matys ta kalba, kurią jis naudoja.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Tiekėjo bendradarbiavimo parinkčių nustatymas konkrečiam tiekėjui
„Dynamics 365 for Operations“ tiekėjo bendradarbiavimo bendruosius parametrus konfigūruoja administratorius. Pvz., jie nustato, kuriuos saugos vaidmenis gali naudoti visi tiekėjai, su kuriais bendradarbiaujate. Taip pat yra tam tikrų parametrų, kurie gali būti taikomi tiekėjams atskirai. Jums reikėtų nustatyti toliau pateiktus parametrus.

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

Pirkimo užsakymai rengiami programoje „Dynamics 365 for Operations“. Kai PU būsena – **Patvirtintas**, jis tiekėjui siunčiamas naudojant puslapio **Pirkimo užsakymas** veiksmą **Siųsti patvirtinti**. PU būsena pasikeičia į **Peržiūrima išorėje**. Išsiuntus PU tiekėjui, jis jį gali peržiūrėti tiekėjo bendradarbiavimo sąsajos puslapyje **Pirkimo užsakymai, kuriuos galima peržiūrėti**, kuriame jie gali užsakymą priimti, atmesti ar siūlyti keitimų. Tiekėjas taip pat gali įtraukti komentarų ir taip paskelbti informaciją, pvz., PO keitimus. Jei norite atkreipti tiekėjo dėmesį į naują PU, taip pat galite jį siųsti el. paštu, naudodami spausdinimo valdymo sistemą.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Tiekėjo PU patvirtinimas ir priėmimas

Kai tiekėjas priima pirkimo užsakymą, PU gali būti patvirtintas automatiškai arba neautomatiškai. Patvirtinimo būdą lemia tiekėjo lauko **Tiekėjo aktyvinimas** reikšmė, kuri gali būti nustatyta **Aktyvus (PU yra automatiškai patvirtinamas)** arba **Aktyvus (PU automatiškai netvirtinamas)**.  

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
<td>Tiekėjas <strong>priima</strong> užsakymą. „Dynamics 365 for Operations‟ sukonfigūruota automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>
<td>Užsakymo būsena atnaujinama į <strong>Patvirtinta</strong>. Jei dėl kokios nors priežasties užsakymo patvirtinti nepavyksta, tiekėjo atsakymas vis tiek įrašomas kaip <strong>Priimta</strong>, tačiau PU būsena lieka <strong>Peržiūrima išorėje</strong>.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima</strong> užsakymą. „Dynamics 365 for Operations‟ nėra sukonfigūruota automatiškai patvirtinti PU, kai juos priima tiekėjas.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Priimta</strong>, bet PU būsena lieka <strong>Peržiūrima išorėje</strong>.</td>
</tr>
<tr class="even">
<td>Tiekėjas <strong>atmeta</strong> užsakymą.</td>
<td>Tiekėjo atsakymas įrašomas kaip <strong>Atmesta</strong> ir PU būsena lieka <strong>Peržiūrima išorėje</strong>. Atmetimas gaunamas kartu su tiekėjų pastaba.</td>
</tr>
<tr class="odd">
<td>Tiekėjas <strong>priima užsakymą su pakeitimais</strong>. Pakeitimai siūlomi eilutės lygiu. Galima priimti arba atmesti atskiras eilutes. Toliau pateikti kiti galimi keitimai.
<ul>
<li>Datų arba kiekių keitimas.</li>
<li>Eilučių skaldymas naudojant skirtingas pristatymo datas arba kiekius.</li>
<li>Prekės pakeitimas.</li>
</ul>
Tiekėjas negali keisti kainų informacijos ir išlaidų. Tokių keitimų pasiūlymus galima pateikti naudojant pastabas.</td>
<td>Tiekėjo atliktas veiksmas įrašomas kaip <strong>Priimtas su pakeitimais</strong>, <strong></strong> o PU būsena lieka <strong>Peržiūrimas išorėje</strong>.</td>
</tr>
</tbody>
</table>

Naudodami darbo sritį **Pirkimo užsakymų** **paruošimas** galite stebėti PU, kurių atžvilgiu tiekėjas atliko veiksmus. Šioje darbo srityje yra du toliau nurodyti sąrašai, kuriuose pateikiami būsenos **Peržiūrimas išorėje** pirkimo užsakymai.

-   Būtina peržiūrėti išorinėje sistemoje.
-   Išorinėje peržiūroje laukiama tiekėjo atsakymo.

### <a name="changing-a-po"></a>PU keitimas

Jei jums reikia pakeisti PU, į kurį jau atsakyta, siųskite tiekėjui naują PU versiją. Naujasis PU turės versijos priedėlį, kuris nurodys, kad PU yra modifikuota anksčiau paskelbto PU versija. Puslapyje **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** jūs ir jūsų tiekėjai galite sekti kiekvieno užsakymo retrospektyvą. Anksčiau patvirtinta PU versija patvirtintų PU sąraše liks tol, kol bus patvirtintas naujasis PU.

### <a name="cancelling-a-po"></a>PU atšaukimas

Kai atšaukiate PU, jo būsena vėl pakeičiama į **Patvirtinta**. PU turite siųsti atgal tiekėjui naudodami Tiekėjo portalą, kad tiekėjas galėtų atšaukimą patvirtinti arba atmesti. Patvirtinus atšaukimą, PU tiekėjo patvirtintų PU sąraše rodomas kaip **Atšaukta**.

### <a name="adding-attachments-to-a-po"></a>Priedų pridėjimas prie PU

Prie PU galite pridėti priedų, pvz., failų, vaizdų ir pastabų, naudodami dokumentų valdymo sistemą. Įtrauktus priedus, kuriems priskirtas tipo **Išorinis** apribojimas, tiekėjas matys tada, kai jiems išsiųsite PU.

## <a name="purchase-order-statuses-and-versions"></a>Pirkimo užsakymo būsenos ir versijos
Šiame skyriuje aprašomos skirtingos PU būsenos, naudojamos, kol užsakymas nėra patvirtintas, ir nurodoma, kada tiekėjui pateikiamos naujos PU versijos. Tai gali skirtis priklausomai nuo to, ar naudojate pirkimo užsakymų pakeitimų valdymo funkciją. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versijos ir būsenos, jei nenaudojate pakeitimų valdymo funkcijos

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veiksmas**                                                               | **Būsena ir versija**                                                                                                                                       |
| Programoje „Dynamics 365 for Operations‟ sukuriama pradinė PU versija. | Jo būsena yra **Patvirtinta**.                                                                                                                                  |
| PU išsiųstas tiekėjui.                                            | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                          |
| Tiekėjas išsiunčia atsakymą **Priimta su keitimais**.                  | Būsena vis dar yra **Peržiūrima išorėje**.                                                                                                                  |
| Atliekate keitimus, kurių prašė tiekėjas.                  | Būsena grąžinama į **Patvirtinta**.                                                                                                                        |
| Naująją PU versiją nusiunčiate tiekėjui.                        | Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                      |
| Tiekėjas priima naująją PU versiją.                            | Būsena vis dar yra **Peržiūrima išorėje**, jei tiekėjo kodas nėra sukonfigūruotas automatiškai nustatyti būseną **Patvirtinta**, kai tiekėjas priima užsakymą. |

Tiekėjams PU patvirtinti naudojant tiekėjo bendradarbiavimo sąsają nereikia. Jie taip pat gali nusiųsti el. laišką arba apie PU patvirtinimą paskelbti kitais kanalais. Tada užsakymą rankiniu būdu galite patvirtinti programoje „Dynamics 365 for Operations‟. Tokiu atveju gaunate įspėjimą, kad užsakymas patvirtinamas, nors nėra jokio atsakymo iš tiekėjo. Tada PU rodomas patvirtinimo istorijoje kaip atviras patvirtintas užsakymas, neturintis jokių atsakymų. Tiekėjas nebegali PU patvirtinti arba atmesti.  

**Pastaba.** PO versija, kurią gali naudoti kiti „Dynamics 365 for Operations‟ procesai, visada yra naujausia, net jei ta versija tiekėjo bendradarbiavimo sąsajoje dar neužregistruota.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versijos ir būsenos, jei naudojate pakeitimų valdymo funkcijos

Jei esate įjungę PU keitimų valdymą, prieš pasiekdamas būseną **Patvirtinta** PU pereina patvirtinimo darbo eigą. Šio proceso tiekėjas nemato.  

Toliau pateikiamoje lentelėje rodomas pavyzdys, kaip gali būti vykdomi PU būsenos ir versijos keitimai, kai įjungtas keitimų valdymas. Versija registruojama PU patvirtinus, o ne PU nusiuntus tiekėjui ar patvirtinus.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veiksmas**                                                                                                    | **Būsena ir versija**                                                                                                                                                                                                                                                                                                                                                                      |
| Programoje „Dynamics 365 for Operations‟ sukuriama pradinė PU versija.                                      | Jo būsena yra **Juodraštis**.                                                                                                                                                                                                                                                                                                                                                                    |
| PU teikiamas patvirtinti. (Tai yra vidinis procesas, kuriame tiekėjas nedalyvauja.) | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Patvirtintas PU užregistruojamas kaip versija.                                                                                                                                                                                                                     |
| PU išsiųstas tiekėjui.                                                                                  | Versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                                                                                                                                                                                                                                                       |
| Atliekate keitimus, kurių prašė tiekėjas.                                                       | Būsena grąžinama į **Juodraštis**.                                                                                                                                                                                                                                                                                                                                                    |
| PU vėl teikiamas patvirtinti.                                                            | Jei, vykstant tvirtinimo procesui, PU neatmetamas, jo būsena iš **Juodraštis** pakeičiama į **Peržiūrima** ir tada į **Patvirtinimas**. Taip pat galima sukonfigūruoti sistemą taip, kad atlikus konkrečius laukų keitimus nereikėtų patvirtinti iš naujo. Tokiu atveju būsena pirmiausia pakeičiama į **Juodraštis** ir tada automatiškai atnaujinama į **Patvirtinta**. Patvirtintas PU užregistruojamas kaip nauja versija. |
| Naująją PU versiją nusiunčiate tiekėjui.                                                             | Nauja versija yra užregistruojama tiekėjo bendradarbiavimo sąsajoje ir būsena pakeičiama į **Peržiūrima išorėje**.                                                                                                                                                                                                                                                                   |
| Tiekėjas patvirtina naująją PU versiją.                                                                | Būsena pakeičiama į **Patvirtinta** automatiškai arba kai gaunate tiekėjo atsakymą ir patvirtinate PU.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Informacijos apie konsignacijos atsargas bendrinimas
Jei naudojate konsignacijos atsargas, tiekėjai gali naudoti tiekėjo bendradarbiavimo sąsają, norėdami peržiūrėti informaciją tolesniuose puslapiuose.

-   **Pirkimo užsakymų naudojamos konsignacijos atsargos** -konsignacijos atsargų pirkimo užsakymai generuojami, kai jūsų įmonė perima atsargų nuosavybės teises iš tiekėjo. Tuo pat metu registruojamas produkto gavimas. Šie konsignacijos pirkimo užsakymai rodomi tik puslapyje **Pirkimo užsakymų naudojamos konsignacijos atsargos**. Jie nėra įtraukti į modulio **Tiekėjo bendradarbiavimas** puslapį **Visi patvirtinti pirkimo užsakymai**.
-   **Produktai, gauti iš konsignacijos atsargų** – šiame puslapyje pateikiamos visos operacijos, kuriose produktų nuosavybės teisės buvo iš tiekėjo perduotos jūsų įmonei. Tiekėjai gali naudoti šią informaciją kliento SF išrašyti.
-   **Turimos konsignacijos atsargos** – šiame puslapyje rodomos turimos, tiekėjui priklausančios konsignacijos atsargos, pristatytos į jūsų sandėlį.





