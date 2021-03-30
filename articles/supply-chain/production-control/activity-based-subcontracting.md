---
title: Veikla pagrįsta subranga
description: Šioje temoje išsamiai paaiškinama, kaip naudoti subrangos veiklas „lean manufacturing“ gamybos eigoje.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule, PlanActivityServiceDetails, PlanActivityServiceWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4217b78d53529572f1ae5e99fbd1ed5c233569f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246530"
---
# <a name="activity-based-subcontracting"></a>Veikla pagrįsta subranga

[!include [banner](../includes/banner.md)]

Šioje temoje išsamiai paaiškinama, kaip naudoti subrangos veiklas „lean manufacturing“ gamybos eigoje.

„Microsoft Dynamics 365 Supply Chain Management“ naudojami du subrangos metodai: gamybos užsakymai ir „lean manufacturing“. „Lean manufacturing“ metodas subrangos darbą modeliuoją kaip paslaugą, kuri susijusi su gamybos eigos veikla. Pristatytas specialus išlaidų grupės tipas, kuris vadinasi **Tiesioginė subranga**, ir subrangos paslaugos nebėra KS dalis. Subrangos darbo išlaidų apskaita yra visiškai integruota į „lean manufacturing“ įkainojimo sprendimą.

## <a name="production-flows-that-involve-subcontractors"></a>Gamybos eigos, apimančios subrangą
Pagrindinis gamybos eigos principas nesikeičia, kai veiklą vykdo subrangovai. Medžiagų srautas tarp vietų vis dar vykdomas, proceso veiklos konvertuoja medžiagas į produktus, o perkėlimo veiklos perkelia medžiagas arba produktus iš vienos vietos į kitą. Vietas ir darbo elementus galite modeliuoti kaip tiekėjo valdomus elementus, priskirdami tiekėjo sąskaitą sandėliui arba išteklių grupės ištekliui.  

Atsižvelgiant į šiuos pajėgumus, „lean manufacturing“ nereikia jokių specialių funkcijų, kad būtų palaikomas medžiagų ir produktų srautas. Visus galimus scenarijus, kurie apima tiekėjus kaip gamybos arba transporto paslaugų tiekėjus, galima modeliuoti pagal gamybos eigos ir veiklų architektūrą.  

Pvz., subrangovas dirba subrangovo vietoje esančiame prekybos centre. Kai subrangovo vietoje ištuštinami sandėliavimo vienetai, „kanban“ kortelės yra grąžinamos į rinkinio langelį kartu su kita siunta. Tada subrangovo prekybos centras yra papildomas. Perkėlimus subrangovui ir iš jo galima modeliuoti kaip tiesiogines perkėlimo veiklas, norint palaikyti paėmimo ir siuntimo procesą. Jei tiesioginė registracija nėra reikalinga, kad būtų palaikytas faktinis transportas, perkėlimo veiklų galima neįtraukti.  

Subrangovą galima naudoti norint subalansuoti bendrą gamybos eigos pajėgumą. Pvz., gamybos eiga modeliuojama naudojant suplanuotas „kanban“ taisykles. Planavimo priemonė naudoja „kanban“ planavimo lentą, kad suplanuotų ir paskirstytų poreikio apkrovą abiejuose darbo elementuose. Planavimo priemonė taip pat stebi prekybos centro konsoliduotą tiekimo grafiką puslapyje **Tiekimo grafikas**. Vienoje arba keliose gamybos eigose galima modeliuoti kelis subrangovus ir galima nustatyti kelias „kanban“ taisykles, kurios būtų naudojamos tam pačiam produktui į tą pačią vietą tiekti per skirtingas veiklas. Planavimo priemonė gali konvertuoti „kanban“ į alternatyvią „kanban“ taisyklę, kad perplanuotų pradžioje sukurtą vidinės gamybos „kanban“ alternatyviame procese. Tiesa sakant, darbo elemento subrangos savybės gamybos eigai įtakos neturi. Tas pats darbo principas taikomas dviem paraleliems vidiniams darbo elementams arba dviem subrangos elementams.   

Kaip ir kiekvieną kitą gamybos eigos veiklą, subrangos veiklas galima vartoti ir tiekti kaip inventorizuotas, neinventorizuotas (nebaigtos gamybos \[NG\]) ir pusiau baigtas medžiagas bei produktus. Visais atvejais subrangos veiklų planavimas ir vykdymas atliekami taip pat. Be to, šie procesai atitinka vidinio darbo procesus.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Subrangos veiklų pirkimo procesas (paslaugos)
Subrangos veiklų pirkimo procesas paremtas faktinių medžiagų srautu, kuris užregistruotas „kanban“ taisyklės eigoje, pvz., Pradėti arba Baigti. Pvz., finansų srauto išlaidos už subrangos darbą yra antrinis srautas, kuris seka faktinį srautą. Tuo pat metu pirkimo procesas yra atskiras procesas, suteikiantis galimybę atliekant kiekvieną veiksmą neautomatiškai koreguoti pirkimo dokumentus. Toliau nurodomas subrangos veiklų pirkimo procesas.

1.  Pirkimo sutarties kūrimas. Sukuriama paslaugos pirkimo sutartis ir prijungiama prie gamybos srauto veiklos.
2.  Kurti pirkimo užsakymą. Galima kurti paslaugos išleistą pirkimo užsakymą pagal suplanuotas „kanban“ užduotis. Tos pačios paslaugos užduotis galima sugrupuoti pirkimo užsakyme pagal dieną, savaitę arba mėnesį. Pirkimo užsakymo eilutes galima kurti bet kada po to, kai sukuriamos „kanban“ užduotys. Pirkimo užsakymo eilutes galima kurti net atgaline data. Ši parinktis paprastai pasirenkama, jei subrangovas paslaugas suteikia be papildomo įspėjimo pagal „kanban“ arba „kanban“ korteles, kurias subrangovas gauna. Šiuo atveju nuokrypius tarp pirkimo užsakymo ir SF galima sumažinti.
3.  Generuokite „kanban“ korteles, medžiagas ir išrinkimo dokumentą, kad nusiųstumėte subrangovui ir jis galėtų pasiruošti gamybai. Atsižvelgiant į išsamų gamybos eigos modeliavimą, pasiruošimas atliekamas proceso veiklų „kanban“ srityje naudojant išrinkimo dokumentą ir pasiruošimo funkciją. Arba pasiruošimas atliekamas perkėlimo užduočių „kanban“ srityje naudojant išrinkimo dokumentą ir paleidimo arba baigimo funkciją. Naudojant inventorizuojamas medžiagas, abu procesus gali palaikyti WMS paėmimo ir siuntimo procesai. Važtaraštį galima kurti pagal poreikį.
4.  Generuokite „kanban“ sandėliavimo vienetus ir „kanban“ korteles. Apdorojus kortelės iš subrangovo perkeliamos atgal. Paprastai į korteles įtraukiama pristatymo pažyma, kuri nurodo išsiųstas faktines medžiagas. Suteiktų paslaugų nuoroda nėra būtina. Medžiagos arba produkto pristatymas klientui yra užregistruojamas „kanban“ srityje atsižvelgiant į „kanban“ korteles. (Naudojama proceso veiklų „kanban“ sritis arba perkėlimo užduočių „kanban“ sritis, atsižvelgiant į modeliuojamas veiklas.)
5.  Sukurkite gavimo patariamąjį dokumentą. Patariamąjį dokumentą galima naudoti norint pakeisti gautos paslaugos važtaraščio dokumentą. Gavimo patariamuosius dokumentus galima generuoti pagal pasirinkto laikotarpio subrangos veiklos baigtas „kanban“ taisykles. Kuriami kiekvieno užduoties gavimo pirkimo užsakymo eilutės patariamieji dokumentai. Gavimo patariamąjį dokumentą galima atspausdinti ir išsiųsti subrangovui kaip gavimo patvirtinimą.
6.  Generuokite SF.

Procesas baigiamas, kai subrangovui išrašoma SF už laikotarpį. SF gretinimas atliekamas pagal sukurtus gavimo patariamuosius dokumentus. Kadangi gavimo patariamieji dokumentai nurodo tikslų faktinį medžiagos gavimą, trišalis atitikimas yra supaprastintas.

## <a name="configuring-activities-for-subcontracting"></a>Subrangos veiklų konfigūravimas
Toliau pateikiamuose skyriuose aprašoma, kaip konfigūruoti subrangos veiklas.

### <a name="subcontracted-services"></a>Subrangos paslaugos

Veikla pagrįstoje subrangoje naudojama mokėjimo prekė turi būti produktas, turintis toliau nurodytas savybes.

-   **Produkto tipas:** paslauga
-   **Atsargų modelių grupė:** nelaikomas

Dėl šio reikalavimo reikia naudoti „pirmasis į, pirmasis iš“ (FIFO) atsargų modelį. **Pastaba.** Produktų išlaidų skaičiavimui atlikti reikia nurodyt standartinę paslaugos savikainą. Reikia sudaryti pirkimo sutartį su tiekėju. Kitaip paslaugos negalima naudoti veikla pagrįstoje subrangoje.

### <a name="subcontracted-process-activities"></a>Subrangos proceso veiklos

Norėdami proceso veiklą sukonfigūruoti kaip subrangos veiklą, atlikite toliau nurodytus veiksmus.

1.  Sukonfigūruokite subrangos darbo elementą. Norėdami darbo elementą sukonfigūruoti kaip subrangos darbo elementą, turite sukurti tipo **Tiekėjas** išteklių ir jį susieti su darbo elementu (išteklių grupe). Darbo elementu reikia priskirti išlaidų grupės tipo **Tiesioginė subranga** apdorojimo laiko išlaidų kategoriją. Sąrankos ir kiekio išlaidų kategorijos nėra būtinos.
2.  Sukūrus proceso veiklą ir susiejus ją su subrangos darbo elementu, prieš aktyvinant gamybos eigos versiją reikia sukonfigūruoti veiklos paslaugą. Šis veiksmas atliekamas puslapyje **Veiklos** **informacija**. Jei veiklos yra susietos su subrangos darbo elementu, rodomas „FastTab“ **Paslaugos sąlygos**. Šiame „FastTab“įtraukite numatytąją paslaugą, kuri galioja visoms išeigos prekėms. Jei konkrečioms išeigos prekėms reikalingos kitos paslaugos arba kiti paslaugos skaičiavimo parametrai (pvz., kitas paslaugos koeficientas), į veiklą galite įtraukti kitų paslaugų.

## <a name="subcontracted-transfer-activities"></a>Subrangos perkėlimo veiklos
Perkėlimo veikla konfigūruojama kaip subrangos veikla, atsižvelgiant į perkėlimo veiklos nustatymą **Transportuoja**. Galimos toliau nurodytos pasirinktys:

-   **Siuntėjas** – veikla yra subrangos veikla, jei perkėlimą iš sandėlio valdo tiekėjas (kaip nurodyta sandėlio nuosavybėje). Visoms pasirinktoms paslaugų pirkimo sutartims kaip sandėlis turi būti priskirtas tas pats tiekėjo ID.
-   **Gavėjas** – veikla yra subrangos veikla, jei perkėlimą į sandėlį valdo tiekėjas (kaip nurodyta sandėlio nuosavybėje). Visoms pasirinktoms paslaugų pirkimo sutartims kaip sandėlis turi būti priskirtas tas pats tiekėjo ID.
-   **Vežėjas** veikla yra bet kurio tiekėjo, teikiančio paslaugą, subrangos veikla. Tam, kad ši parinktis galiotų, reikia sukurti sandėlio valdymo vežėją ir priskirti tiekėjo sąskaitą.

O proceso veiklų subrangos perkėlimo veiklų numatytąją paslaugą reikia sukonfigūruoti puslapio **Veiklos** **informacija** „FastTab“ **Paslaugos sąlygos**.

## <a name="service-quantity-calculation"></a>Paslaugų kiekio skaičiavimas
Visas pirkimo procesas yra pagrįstas paslaugos prekės nuoroda. Ši prekės nuoroda apskaičiuojama naudojant paslaugos matavimo vienetą. Paslaugos paprastai skaičiuojamos pagal paslaugų (vienetų) skaičių arba laiką. Norėdami pagal užregistruotą „kanban“ taisyklių gavimą apskaičiuoti paslaugos kiekį, galite naudoti tolesnius būdus.

-   **Skaičiavimas, pagrįstas užduočių skaičiumi** – viena „kanban“ taisyklė lygi *n* paslaugos vienetų, neatsižvelgiant į tiekiamą produkto kiekį. “Lean manufacturing“ viena užduotis atitinka vieną sandėliavimo vienetą. Šis skaičiavimo metodas taikomas visoms paslaugoms su nustatyta fiksuota sandėliavimo vieneto kaina. Todėl šis metodas paprastai taikomas perkėlimo veikloms. Tačiau jis gali būti taikomas proceso veikloms, kurios apdoroja visus sandėliavimo vienetus.
-   **Skaičiavimas, pagrįstas produkto kiekiu** – paslaugos kiekis priklauso nuo produkto kiekio, kuris yra suplanuotas / tiekiamas. Kai skaičiuojamas tiekiamo produkto kiekis, klaidingus kiekius galima įtraukti arba neįtraukti. Šis skaičiavimo metodas taikomas visais atvejais, kai susitariama dėl paslaugos kainos už apdoroto produkto vienetą.
-   **Skaičiavimas, pagrįstas veiklos laiku** – apskaičiuojami teoriniai veiklos laikai, atsižvelgiant į veiklos apdorojimo laiką, bendrą apdorotą kiekį ir apdoroto produkto našumo koeficientą. Šis skaičiavimo metodas taikomas visoms paslaugoms, kurios apmokamos valandiniu įkainiu ir kurių produkto apdorojimo laikas gali skirtis.

## <a name="cost-accounting-of-subcontracted-services"></a>Subrangos paslaugų išlaidų apskaita
Kai užregistruojamas gavimo patariamasis dokumentas arba tiekėjo važtaraštis sukurtame gamybos eigos pirkimo užsakyme (kitaip tariant, pirkimo užsakyme, kuris buvo sugeneruotas pagal subrangos veiklų „kanban“ taisykles), gavimo vertė nurodoma gamybos eigos NG kodais. SF nuokrypiai taip pat priskiriami gamybos eigai. Pristatyta subrangos darbo išlaidų kategorija. Išlaidų kategorija suteikia galimybę skaidriai sekti NG paskirstyto ir per laikotarpį sunaudojamo subrangos darbo vertę.  

Įkainojimo laikotarpio pabaigoje “lean manufacturing“ įkainojimas atvirkštine tvarka apskaičiuoja gamybos eigoje gaminamų produktų faktinius nuokrypius per įkainojimo laikotarpį.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Perkėlimų kaip subrangos veiklų modeliavimas
Dažnai žmonės galvoja, kad transportas nėra produktyvus ir nekuria jokios vertės. Tačiau, lyginant subrangos išlaidas ir vidaus gamybos išlaidas, reikėtų apsvarstyti papildomų transporto veiklų išlaidas. Gamybos eigoje, kuri vykdoma keliose vietose ir kuriai atlikti reikalingos transporto pareigos, transporto kaina turėtų būti modeliuojama kaip produktų tiekimo klientui išlaidų dalis. 

“Lean manufacturing“ veikla pagrįsta subranga suteikia galimybę integruoti vežėjus ir transporto tiekėjus, kurie gabena medžiagas ir produktus iš vienos gamybos eigos vietos į kitą. Modeliuodami perkėlimo veiklą galite priskirti vežėją arba tiekėją. Perkėlimo veiklos / užduotis yra pagrįsta aptarnavimo bei pirkimo sutartimi ir jūs pirkimo užsakymus bei gavimo patariamuosius dokumentus galite kurti pagal faktines perkėlimo užduotis. Ši funkcija yra tokia pati kaip subrangos proceso veiklų funkcija.  

Todėl „Supply Chain Management“ dabar palaiko KS skaičiavimą, kuris apima transporto paslaugas, susijusių pirkimo užsakymų kūrimą, integruotą gavimo registravimą ir transporto paslaugų išlaidų integravimą į gamybos eigos išlaidas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]