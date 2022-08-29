---
title: EKA kainos funkcijos
description: Šiame straipsnyje aprašomos įvairios kainos ir nuolaidos funkcijos point Microsoft Dynamics 365 Commerce point of sale (EKA) programoje.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293655"
---
# <a name="pricing-functions-in-pos"></a>EKA kainos funkcijos

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomos įvairios kainos ir nuolaidos funkcijos point Microsoft Dynamics 365 Commerce point of sale (EKA) programoje.

Dynamics 365 Commerce EKA programa suteikia gausių galimybių, kurios leidžia pirmos eilutės darbuotojams vykdyti parduotuvės "Commerce" operacijas. Šioje lentelėje rodomos kainų ir nuolaidų funkcijos, kurias šiuo metu galima naudoti programoje.

| Funkcija                       | EKA operacijos |
|--------------------------------|----------------|
| Peržiūrėti kainas                    | [Kainos tikrinimas](#price-check) |
| Peržiūrėti nuolaidas                 | [Peržiūrėti visas nuolaidas](#view-all-discounts)<br>[Rodyti pasiekiamas nuolaidas](#view-available-discounts) |
| Perrašyti kainas                | [Kainos perrašymas](#price-override) |
| Taikyti arba pašalinti nuolaidas      | [Eilutės nuolaidos suma](#line-discount-amount)<br>[Eilutės nuolaida procentais](#line-discount-percent)<br>[Bendroji nuolaidos suma](#total-discount-amount)<br>[Bendra nuolaida procentais](#total-discount-percent)<br>[Pašalinti sistemos nuolaidas iš operacijos](#remove-system-discounts-from-transaction)<br>[Dar kartą taikyti sistemos nuolaidas](#reapply-system-discounts) |
| Taikyti arba pašalinti kuponus        | [Įtraukti kupono kodą](#add-coupon-code)<br>[Pašalinti kupono kodą](#remove-coupon-code) |
| Skaičiuoti kainas ir nuolaidas | [Perskaičiuoti](#recalculate) |

Informacijos apie tai, kaip EKA programoje galima konfigūruoti pirmiau skirtas operacijas ir ar jos palaiko atjungties režimą, [žr. interneto ir autonominio pardavimo (EKA) operacijas](pos-operations.md).

## <a name="price-check"></a>Kainos tikrinimas

Kainos **tikrinimo operacija** įgalina EKA vartotojus ieškoti iš anksto sukonfigūruotų konkretaus produkto kainų.

## <a name="view-all-discounts"></a>Peržiūrėti visas nuolaidas

" **View all discounts** " operacija įgalina EKA vartotojus ieškoti visų veiksmingų akcijų, kurios šiuo metu vykdomos parduotuvės kanale. Tiksliau sakant, šioje operacijoje išvardijamos visos nuolaidos, kurios atitinka bet kurią iš šių sąlygų:

- Nuolaidos kainų grupė atitinka parduotuvės kainų grupę.
- Nuolaidos kainų grupė susieta su priskyrimo ar lojalumo programa.
- Nuolaidos kainų grupė yra susieta su katalogu, kuris susietas su parduotuve.

Visų **nuolaidų peržiūros** operacija rodo tik tas nuolaidas, kurios nekonkuruoja jokios jau taikomos nuolaidos. Taip užtikrinama, kad, jei pardavimų darbuotojas informuos klientą apie nuolaidą, o klientas imsis reikalaujamo veiksmo (pvz., klientas nusiperka dar vieną prekę, kad gautų 10 procentų nuolaidą), nuolaida taikoma operacijai. Kuponu pagrįstos nuolaidos rodomos tik tada, jei įjungtas **parametras** Taikyti be kupono kodo.

EKA **vartotojai gali ieškoti nuolaidų pagal pavadinimą ir aprašymą, o peržiūros operacijoje jie gali filtruoti nuolaidas** pagal tai, ar jiems reikia kupono.

## <a name="view-available-discounts"></a>Rodyti pasiekiamas nuolaidas

**Galimų nuolaidų peržiūros** operacija įgalina EKA vartotojus peržiūrėti visas nuolaidas, kurios taikomos pasirinktoms operacijos eilutėms arba visai operacijai. Į pasirinktą eilutę taikomos nuolaidos apima nuolaidas, kurios jau taikomos, ir nuolaidas, kurios nebuvo taikomos, bet gali būti taikomos (pvz., nuolaidas prekiųmams, kurioms reikia papildomų prekių). **Jei** taikoma nuolaida yra susieta su kuponu, kuriame įjungtas **kupono** kodo parametras Taikyti be kupono, EKA vartotojas taip pat gali naudoti kupono funkcijos taikymą šios operacijos viduje, tiesiogiai neįvesdami ir neskaitę jokių kupono kodų ar kupono brūkšninių kodų.

## <a name="price-override"></a>Kainos perrašymas

Kainos **perrašymo** operacija įgalina EKA vartotojus perrašyti operacijos produkto pardavimo kainą. Ši operacija veikia tik su produktais, kurie sukonfigūruoti taip, kad leistų perrašymus.

## <a name="line-discount-amount"></a>Eilutės nuolaidos suma

Eilutės **nuolaidos sumos** operacija įgalina EKA vartotojus įvesti operacijos eilutės prekės nuolaidos sumą. Ši operacija taikoma tik **prekėms**, kurių nuolaida leidžiama, ir atsižvelgiant į vartotojo EKA teisių grupėje nurodytą maksimalią eilutės nuolaidos sumos vertę.

## <a name="line-discount-percent"></a>Eilutės nuolaida procentais

Eilutės **nuolaidos procentų** operacija įgalina EKA vartotojus įvesti operacijos eilutės prekės nuolaidos procentą. Ši operacija taikoma tik **prekėms**, kurių nuolaida leidžiama, ir atsižvelgiant į vartotojo EKA teisių grupėje nurodytą maksimalią eilutės nuolaidos procentinę vertę.

## <a name="total-discount-amount"></a>Bendroji nuolaidos suma

Bendrosios **nuolaidos sumos operacija** leidžia EKA vartotojams įvesti operacijos nuolaidos sumą. Ši operacija taikoma tik **prekėms**, kurių nuolaida leidžiama, ir atsižvelgiant į vartotojo EKA teisių grupėje nurodytą maksimalią bendrosios nuolaidos sumos vertę. Jei įvesta nuolaidos suma viršija maksimalią bendrą nuolaidos sumą, operacija blokuojama ir joks teisių perrašymo srautas neįjunguojamas. Šiuo metu bendra nuolaidos suma negali būti taikoma krepšelyje, kuriame yra pardavimo ir grąžinamų prekių derinys.

## <a name="total-discount-percent"></a>Bendra nuolaida procentais

Bendrosios **nuolaidos procentinės vertės** operacija leidžia EKA vartotojams įvesti operacijos nuolaidos procentą. Ši operacija taikoma tik **prekėms**, kurių nuolaida leidžiama, ir atsižvelgiant į maksimalią bendrosios nuolaidos procento vertę, kuri nurodyta vartotojo EKA teisių grupėje. Jei įvestas nuolaidos procentas viršija didžiausią bendrosios nuolaidos procentą, operacija blokuojama ir teisių perrašymo srautas neįjunguojamas. Šiuo metu bendra nuolaidos procentinė dalis negali būti taikoma krepšelyje, kuriame yra pardavimo ir grąžinamų prekių derinys.

## <a name="remove-system-discounts-from-transaction"></a>Pašalinti sistemos nuolaidas iš operacijos

Sistemos **nuolaidų šalinimo iš operacijos** operacija įgalina EKA vartotojus išvalyti visas operacijos taikomas sistemos nuolaidas (įskaitant kuponu pagrįstas nuolaidas). Atlikus šią operaciją, kainos nustatymo variklis pradeda pašalinti sistemos nuolaidas iš nuolaidos skaičiavimo apimties. Sistemos **nuolaidų šalinimo iš operacijos** operacijos metu metu nėra pašalintos neautomatinės nuolaidos.

## <a name="reapply-system-discounts"></a>Dar kartą taikyti sistemos nuolaidas

Iš **naujo sistemos nuolaidų operacija įgalina EKA vartotojus iš naujo taikyti sistemos apskaičiuotas nuolaidas** operacijai, jei nuolaidos buvo pašalintos naudojant operacijos operaciją Pašalinti sistemos **nuolaidas**. Atlikus šią operaciją, kainos nustatymo variklis pradeda įtraukti visas sistemos nuolaidas į nuolaidos skaičiavimo aprėptį.

## <a name="add-coupon-code"></a>Įtraukti kupono kodą

Kupono **kodo pridėjimo** operacija leidžia EKA vartotojams įtraukti kuponą į operaciją įvedant kupono kodą. Arba EKA vartotojai gali nuskaityti kupono brūkšninius kodus arba įvesti jį naudodami skaitinę klaviatūrą operacijų **ekrane**.

## <a name="remove-coupon-code"></a>Pašalinti kupono kodą

Operacija **Pašalinti kupono kodą** leidžia EKA vartotojams pasirinkti ir pašalinti vieną ar daugiau kuponų, kurie šiuo metu taikomi operacijai.

## <a name="recalculate"></a>Perskaičiuoti

Perskaičiavimo **operacija leidžia** EKA vartotojams atlikti kainos pagal poreikį skaičiavimą. Šią operaciją reikia atlikti, kai įgalintas kainos užrakinimas ir (arba) atidėtas kainų skaičiavimas, O EKA vartotojas nori perskaičiuoti kainas ir nuolaidas po krepšelio arba užsakymo pakeitimų. Skaičiavimo **iš naujo operacija** visada perskaičiuoja visą užsakymą. Jo negalima naudoti pasirinktoms pardavimo eilutėms perskaičiuoti. Norėdami taikyti rankinius nuolaidą užrakintai EKA pardavimo eilutei, **EKA** vartotojai pirmiausia turi naudoti skaičiavimo operaciją, kad atrakintų visas pardavimo eilutes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
