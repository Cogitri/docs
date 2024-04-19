---
title: "Wie lösche ich eine DNS-Zone?"
excerpt: "Diese Anleitung erklärt, wie Sie eine DNS-Zone für Ihre Domain über Ihr OVHcloud Kundencenter"
updated: 2024-02-19
---

> [!primary]
> Diese Übersetzung wurde durch unseren Partner SYSTRAN automatisch erstellt. In manchen Fällen können ungenaue Formulierungen verwendet worden sein, z.B. bei der Beschriftung von Schaltflächen oder technischen Details. Bitte ziehen Sie im Zweifelsfall die englische oder französische Fassung der Anleitung zu Rate. Möchten Sie mithelfen, diese Übersetzung zu verbessern? Dann nutzen Sie dazu bitte den Button "Beitragen" auf dieser Seite.
>

## Ziel

Die **DNS**-Zone (**D**omain **N**ame **S**ystem) ist die Konfigurationsdatei eines Domainnamens. Sie besteht aus **DNS-Einträgen**, Datensätzen die dem Domainnamen verschiedenen Diensten und Funktionen zuordnen.

Weitere Informationen zu DNS-Zonen und DNS-Servern finden Sie in den folgenden Anleitungen: 

- [OVHcloud DNS-Zone für eine Domainnamen erstellen](/pages/web_cloud/domains/dns_zone_create)
- [Bearbeiten der OVHcloud DNS-Zone](/pages/web_cloud/domains/dns_zone_edit)
- [DNS-Server eines OVHcloud Domainnamens ändern](/pages/web_cloud/domains/dns_server_general_information)

So kann es beispielsweise vorkommen, dass Sie eine DNS-Zone für Ihren Domainnamen bei OVHcloud löschen müssen (nicht abschließende Liste):

- Sie verwenden eine aktive DNS-Zone für Ihre Domain bei einem anderen Anbieter als OVHcloud.
- Sie verwenden den Domainnamen nicht mehr, der mit der bei OVHcloud vorhandenen DNS-Zone verbunden ist.
- Sie haben Ihre Dienste zu einem anderen Anbieter migriert und möchten Ihre Dienste bei OVHcloud kündigen.

> [!primary]
>
> Die Erstellung / Änderung / Löschung einer DNS-Zone in Ihrem [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de) ist kostenlos.
>

**Diese Anleitung erklärt, wie Sie im OVHcloud Kundencenter eine OVHcloud DNS-Zone für Ihren Domainnamen löschen.**

## Voraussetzungen

- Sie haben Zugriff auf Ihr [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de).
- Sie haben eine DNS-Zone in Ihrem OVHcloud Kundencenter.
- Sie verfügen über ausreichende Rechte für die zu löschende DNS-Zone. Weitere Informationen finden Sie in unserer Anleitung „[Verwaltung der Kontakte](/pages/account_and_service_management/account_information/managing_contacts)“.

## In der praktischen Anwendung

> [!warning]
>
> Stellen Sie sicher, dass die DNS-Zone, die Sie löschen möchten, nicht mehr von Ihrer Domain verwendet wird, bevor Sie fortfahren.
>
> Wenn Sie die aktive DNS-Zone für Ihre Domain löschen, werden Ihre Online-Dienste (Website, E-Mail-Adressen usw.) unterbrochen.
>
> Überprüfen Sie mithilfe einer [WHOIS](https://www.ovhcloud.com/de/domains/whois/)-Abfrage, ob die aktive DNS-Zone Ihrer Domain bei OVHcloud liegt.
>
> Wenn die aktive DNS-Zone für Ihre Domain bei OVHcloud liegt und Sie diese durch eine an einem anderen Standort gehostete DNS-Zone ersetzen möchten, lesen Sie unsere Anleitung „[DNS-Server einer OVHcloud Domain bearbeiten](/pages/web_cloud/domains/dns_server_general_information)“, bevor Sie die Löschung der DNS-Zone vornehmen.
>

### Schritt 1 - Löschen einer OVHcloud DNS-Zone initiieren

So starten Sie die Löschung einer OVHcloud DNS-Zone: 

1. Verbinden Sie sich mit Ihrem [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de).
2. Klicken Sie oben im Kundencenter auf den Tab `Web Cloud`{.action}.
3. Klicken Sie in der linken Spalte auf das Dropdown-Menü `Domainnamen`{.action}.
4. Wählen Sie die betreffende Domain oder DNS-Zone aus.
5. Klicken Sie auf den Tab `DNS-Zone`{.action}, um auf die Tabelle zuzugreifen, in der alle DNS-Einträge der DNS-Zone aufgeführt sind.
6. Klicken Sie auf der rechten Seite (oder unter der Tabelle je nach Bildschirmauflösung) auf die Schaltfläche `Die DNS-Zone löschen`{.action}.

![delete the DNS zone](images/delete-the-dns-zone.png){.thumbnail}

Überprüfen Sie im angezeigten Fenster die darin enthaltenen Meldungen.

![delete the DNS zone validation](images/delete-the-dns-zone-confirmation.png){.thumbnail}

Klicken Sie auf `Bestätigen`{.action}, um den ersten Löschschritt der DNS-Zone abzuschließen.

### Schritt 2 - Löschen einer OVHcloud DNS-Zone bestätigen

Im vorherigen Schritt erhalten Sie eine E-Mail zur Bestätigung der Löschung der DNS-Zone an die E-Mail-Adresse des „[Administrator-Kontakts](/pages/account_and_service_management/account_information/managing_contacts)“.

> [!success]
>
> Wenn Sie die E-Mail nicht erhalten, überprüfen Sie Ihre Spam-Mails.
>

Diese E-Mail enthält zwei Links, die **72** Stunden ab dem Zeitpunkt gültig sind, an dem Sie Schritt 1 dieser Anleitung abgeschlossen haben.

Klicken Sie auf den **Validierung-Link**, um mit der Löschung der OVHcloud DNS-Zone fortzufahren, oder auf den **Stornierung-Link**, um die Löschung der OVHcloud DNS-Zone abzubrechen.

> [!primary]
>
> Wenn die Weiterleitung der Links nicht funktioniert, **kopieren** Sie den Link in die Adresszeile Ihres Browsers. Verbinden Sie sich bei Bedarf erneut mit Ihrem [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de).
>

Wenn Sie auf den Link zur Validierung klicken, werden Sie auf eine neue Seite weitergeleitet, auf der Sie nach den Gründen für die Löschung der OVHcloud DNS-Zone gefragt werden.

![cancel the service](images/cancel-my-service.png){.thumbnail}

Wenn Sie sicher sind, dass Sie die OVHcloud DNS-Zone dauerhaft löschen möchten, klicken Sie nach Ausfüllen des Formulars unten auf den Button `Bestätigen`{.action}.

Eine E-Mail wird an die E-Mail-Adresse des „[Administrator-Kontakts](/pages/account_and_service_management/account_information/managing_contacts)“
der OVHcloud DNS-Zone gesendet, um die Löschung zu bestätigen.

## Weiterführende Informationen

[Verwaltung der Kontakte](/pages/account_and_service_management/account_information/managing_contacts)

[Bearbeiten einer OVHcloud DNS-Zone](/pages/web_cloud/domains/dns_zone_edit)

[DNS-Server einer OVHcloud Domain bearbeiten](/pages/web_cloud/domains/dns_server_general_information)

[OVHcloud DNS-Zone erstellen](/pages/web_cloud/domains/dns_zone_create)
 
Kontaktieren Sie für spezialisierte Dienstleistungen (SEO, Web-Entwicklung etc.) die [OVHcloud Partner](https://partner.ovhcloud.com/de/directory/).
 
Wenn Sie Hilfe bei der Nutzung und Konfiguration Ihrer OVHcloud Lösungen benötigen, beachten Sie unsere [Support-Angebote](https://www.ovhcloud.com/de/support-levels/).
 
Für den Austausch mit unserer User Community gehen Sie auf <https://community.ovh.com/en/>.
