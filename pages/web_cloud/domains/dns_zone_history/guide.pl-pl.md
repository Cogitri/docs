---
title: "Zarządzanie historią strefy DNS"
excerpt: "Dowiedz się, jak sprawdzać, porównywać, pobierać i przywracać kopie zapasowe strefy DNS"
updated: 2023-12-11
---

> [!primary]
> Tłumaczenie zostało wygenerowane automatycznie przez system naszego partnera SYSTRAN. W niektórych przypadkach mogą wystąpić nieprecyzyjne sformułowania, na przykład w tłumaczeniu nazw przycisków lub szczegółów technicznych. W przypadku jakichkolwiek wątpliwości zalecamy zapoznanie się z angielską/francuską wersją przewodnika. Jeśli chcesz przyczynić się do ulepszenia tłumaczenia, kliknij przycisk “Zgłoś propozycję modyfikacji” na tej stronie.
>

## Wprowadzenie

Strefa **D**omain **N**ame **S**ystem (**DNS**) jest plikiem konfiguracyjnym domeny. Zawiera on informacje techniczne nazywane *rekordami DNS*. Strefa DNS jest w pewnym sensie ośrodkiem prowadzącym.

Możesz na przykład w nim określić:

- Adres IP (rekordy DNS typu *A* i *AAAA*) Twojego hostingu, aby wyświetlał Twoją stronę WWW wraz z domeną.
- Serwery email (rekordy DNS typu *MX*), na które Twoja domena powinna przekierowywać wiadomości e-mail. Możesz wyświetlić je na Twoim (Twoich) spersonalizowanym(ych) adresie(ach) e-mail(ów) wraz z nazwą domeny.
- Informacje związane z bezpieczeństwem / uwierzytelnianie Twoich usług (hosting, serwer www, serwer e-mail, etc.) przypisane do Twojej domeny (rekordy DNS typu *SPF*, *DKIM*, *DMARC*, etc.).

Zapoznaj się z naszą dokumentacją dotyczącą [wpisów DNS i edycji strefy DNS](/pages/web_cloud/domains/dns_zone_edit) dostępną w [Panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl), jeśli chcesz dowiedzieć się więcej na ten temat.
Może zajść konieczność zastosowania poprzedniej konfiguracji DNS dla Twojej domeny.

Dzięki historii stref DNS zarządzanie serwerami DNS stało się łatwiejsze.

**Dowiedz się, jak sprawdzać, porównać, pobrać i przywrócić kopie zapasowe strefy DNS**

## Wymagania początkowe

- Strefa DNS dla Twojej domeny w [Panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl)
- Dostęp do [panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl)
- Dostęp do interfejsu zarządzania domeną

## W praktyce

Aby uzyskać dostęp do tej funkcji, zaloguj się do [Panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl) i przejdź do sekcji `Web Cloud`{.action} w górnej części interfejsu. W kolumnie po lewej stronie przejdź do zakładki `Domeny`{.action}, następnie wybierz domenę powiązaną ze strefą DNS, którą chcesz zarządzać.

Na stronie, która się wyświetli i jeśli jeszcze nie zostałeś przekierowany do tej zakładki, kliknij zakładkę `Strefa DNS`{.action}.

Pojawi się tabela, która przedstawia strefę DNS Twojej domeny. Znajduje się na niej lista rekordów DNS. Po prawej stronie tabeli znajduje się kilka przycisków umożliwiających wykonywanie operacji w strefie DNS. 

![DNS history tool](images/dns-zone-history.png){.thumbnail}

Kliknij przycisk 'Wyświetl historię strefy DNS`{.action}. 

Na nowej stronie, która się wyświetli, pojawi się tabela z historią kopii zapasowych strefy DNS, posortowana od najnowszej do najstarszej daty. Na górze tej tabeli znajduje się aktualna wersja Twojej strefy DNS. Na tej stronie możesz wykonać następujące czynności:

- [Wyświetl strefę DNS](#view)
- [Pobierz strefę DNS](#download)
- [Przywróć strefę DNS](#restore)
- [Porównaj dwie strefy DNS](#compare)

### Wyświetl strefę DNS <a name="view"></a>

Aby wyświetlić wybraną strefę DNS, zidentyfikuj odpowiedni wiersz w tabeli i kliknij na ikonę w kolumnie `Wyświetl`{.action}.

![Wyświetl strefę DNS](images/visualize-dns-eyes.png){.thumbnail}

Wyświetlą się dane odpowiedniej strefy DNS.

![Szczegóły strefy DNS](images/details-dns-zone.png){.thumbnail}

Kliknij przycisk `Zamknij`{.action}, aby wrócić do strony głównej "Historia strefy DNS".

### Pobierz strefę DNS <a name="download"></a>

Aby pobrać wybraną strefę DNS, zidentyfikuj jej wiersz w tabeli i kliknij na ikonę w kolumnie `Pobierz`{.action}.

![Pobierz strefę DNS](images/download-dns-zone.png){.thumbnail}

Strefa DNS zostanie pobrana w formacie .txt.

### Przywróć strefę DNS <a name="restore"></a>

Jeśli chcesz zastąpić aktualną strefę DNS inną, wystarczy przywrócić starszą strefę DNS. W tabeli zawierającej historię stref DNS wskaż wiersz odpowiadający strefie DNS, którą chcesz przywrócić (sprawdź datę po lewej stronie wiersza), następnie kliknij ikonę w kolumnie `Przywróć`{.action}.

![Przywróć strefę DNS](images/restore-dns-zone.png){.thumbnail}

Pojawi się następujące okno.

![Potwierdzenie przywrócenia strefy DNS](images/confirmation-restore-dns-zone.png){.thumbnail}

Sprawdź, czy data podana w wiadomości odpowiada strefie DNS, którą chcesz przywrócić. Pamiętaj, że bieżąca strefa DNS (znajdująca się na górze listy historii stref DNS) zostanie usunięta i zastąpiona strefą DNS, którą chcesz przywrócić.

Kliknij przycisk `Przywróć`{.action}, aby potwierdzić przywrócenie lub `Anuluj`{.action}.

> [!primary]
>
> Modyfikacja lub przywrócenie strefy DNS spowoduje opóźnienie propagacji z **4** do **24** godzin, aby zostało w pełni uwzględnione w sieci DNS.
>

### Porównanie dwóch stref DNS <a name="compare"></a>

Możesz porównać zawartość dwóch stref DNS. W tabeli zawierającej historię strefy DNS wskaż dwie linie odpowiadające dwóm strefom DNS, które chcesz porównać (sprawdź datę po lewej stronie każdej linii), a następnie zaznacz je. Aby porównać te dwie wersje strefy DNS, w lewym górnym rogu kliknij `Porównanie wersje`{.action}.

![Porównanie dwóch stref DNS](images/compare-two-dns-zone.png){.thumbnail}

Zostanie wyświetlona nowa strona z zawartością dwóch stref DNS. Nad każdą wersją wyświetlana jest odpowiednia data. Domyślnie najnowsza wersja strefy DNS znajduje się po lewej stronie, a najstarsza po prawej. Kolorowy kod pomaga zidentyfikować różnice w zawartości.<br>
Po lewej stronie zawartość podświetlona na czerwono została zmodyfikowana lub usunięta w nowszej wersji.<br>
Z prawej strony, zaznaczona na zielono treść została zmieniona lub dodana w porównaniu ze starszą wersją. 

Możesz również zaktualizować daty wersji, które chcesz porównać, korzystając z dwóch rozwijanych list.

![Porównanie dwóch stref DNS](images/compare-dns-zone-details.png){.thumbnail}

Dzięki niniejszemu przewodnikowi możesz teraz porównywać dwie strefy DNS oraz wyświetlać, pobierać, przywracać i usuwać strefę DNS.

## Sprawdź również

[Zaloguj się do Panelu klienta OVHcloud](/pages/account_and_service_management/account_information/ovhcloud-account-login)

[Utworzenie strefy DNS w OVHcloud](/pages/web_cloud/domains/dns_zone_create)

W przypadku wyspecjalizowanych usług (pozycjonowanie, rozwój, etc.) skontaktuj się z [partnerami OVHcloud](https://partner.ovhcloud.com/pl/directory/).

Jeśli chcesz otrzymywać wsparcie w zakresie konfiguracji i użytkowania Twoich rozwiązań OVHcloud, zapoznaj się z naszymi [ofertami pomocy](https://www.ovhcloud.com/pl/support-levels/).

Dołącz do społeczności naszych użytkowników na stronie <https://community.ovh.com/en/>.