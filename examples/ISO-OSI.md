---
marp: "true"
theme: mischok-academy
paginate: "true"
dark:
  - "true"
---

# Vortrag: Das ISO/OSI-Schichtenmodell
## Prüfungsvorbereitungskurs – Fachinformatiker Systemintegration
### Dauer: 45 Minuten

---

# 📋 Gliederung

1. Einleitung & Lernziele (3 Min.)
2. Was ist das ISO/OSI-Modell? (5 Min.)
3. Die 7 Schichten im Detail (20 Min.)
4. Merkhilfen & Prüfungstipps (5 Min.)
5. Praxisbezug & Protokollbeispiele (7 Min.)
6. Wiederholung & Prüfungsfragen (5 Min.)

---

# 1️⃣ EINLEITUNG & LERNZIELE
## ⏱️ ~3 Minuten

---

## Warum ist das OSI-Modell wichtig?

> **In der IHK-Prüfung ist das OSI-Modell eines der am häufigsten abgefragten Themen!**

- Es bildet die **Grundlage** für das Verständnis von Netzwerken
- Es hilft bei der **Fehlerdiagnose** im Berufsalltag
- Es erklärt, **wie Protokolle zusammenarbeiten**
- Es ist Basis für Themen wie **TCP/IP, Switching, Routing**

---

## 🎯 Lernziele

Nach diesem Vortrag könnt ihr:

✅ Das OSI-Modell mit allen 7 Schichten benennen
✅ Die Aufgaben jeder Schicht erklären
✅ Protokolle und Geräte den richtigen Schichten zuordnen
✅ Typische Prüfungsfragen zum OSI-Modell beantworten

---

# 2️⃣ WAS IST DAS ISO/OSI-MODELL?
## ⏱️ ~5 Minuten

---

## Geschichte & Hintergrund

| Merkmal | Details |
|--------|---------|
| **Vollständiger Name** | ISO/OSI-Referenzmodell |
| **ISO** | International Organization for Standardization |
| **OSI** | Open Systems Interconnection |
| **Entwickelt** | Ende der 1970er Jahre |
| **Veröffentlicht** | 1984 als ISO 7498 |
| **Zweck** | Standardisierung der Netzwerkkommunikation |

---

## Das Problem vor dem OSI-Modell

**Stellt euch vor:**
- Hersteller A baut Netzwerkgeräte nach eigenen Regeln
- Hersteller B baut Netzwerkgeräte nach anderen Regeln
- ❌ Geräte verschiedener Hersteller können **nicht miteinander kommunizieren**

**Die Lösung:**
> Ein einheitliches **Referenzmodell**, das festlegt, wie Kommunikation strukturiert sein soll

---

## Grundprinzip des OSI-Modells

```
┌─────────────────────────────────┐
│  Kommunikation wird in          │
│  7 Schichten aufgeteilt         │
│                                 │
│  Jede Schicht hat:              │
│  • Definierte Aufgaben          │
│  • Schnittstellen zur           │
│    nächsten Schicht             │
│  • Eigene Protokolle            │
└─────────────────────────────────┘
```

### Wichtige Grundsätze:
- Jede Schicht kommuniziert **logisch** mit der gleichen Schicht des anderen Systems
- **Physisch** läuft die Kommunikation immer über alle Schichten nach unten/oben
- Schichten sind **gekapselt** (Encapsulation)

---

## Das Schichtenmodell – Überblick

```
┌──────┬──────────────────────────┬──────────────┐
│  Nr. │ Schicht                  │ Englisch     │
├──────┼──────────────────────────┼──────────────┤
│  7   │ Anwendungsschicht        │ Application  │
│  6   │ Darstellungsschicht      │ Presentation │
│  5   │ Sitzungsschicht          │ Session      │
│  4   │ Transportschicht         │ Transport    │
│  3   │ Vermittlungsschicht      │ Network      │
│  2   │ Sicherungsschicht        │ Data Link    │
│  1   │ Bitübertragungsschicht   │ Physical     │
└──────┴──────────────────────────┴──────────────┘
```

---

## Zwei Gruppen von Schichten

```
┌─────────────────────────────────────────┐
│  SCHICHTEN 5-7: Anwendungsorientiert    │
│  (Application Layers)                   │
│  → Zuständig für die Anwendung          │
├─────────────────────────────────────────┤
│  SCHICHTEN 1-4: Transportorientiert     │
│  (Transport Layers)                     │
│  → Zuständig für die Übertragung        │
└─────────────────────────────────────────┘
```

---

# 3️⃣ DIE 7 SCHICHTEN IM DETAIL
## ⏱️ ~20 Minuten

---

# 🔵 SCHICHT 1
## Bitübertragungsschicht (Physical Layer)

---

## Aufgaben der Schicht 1

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Übertragung von Bits als physikalische Signale |
| **Einheit** | **Bit** |
| **Frage** | Wie werden Nullen und Einsen übertragen? |

### Was wird hier definiert?
- ⚡ **Elektrische Spannungen** (z.B. 0V = 0, 5V = 1)
- 💡 **Lichtsignale** (Glasfaser)
- 📡 **Funksignale** (WLAN, Bluetooth)
- 🔌 **Stecker und Kabel** (RJ45, USB, Koaxial)
- ⏱️ **Übertragungsrate** (Bit/s)

---

## Geräte & Protokolle – Schicht 1

### Geräte:
| Gerät | Funktion |
|-------|----------|
| **Hub** | Verteilt Signale an alle Ports |
| **Repeater** | Verstärkt Signale |
| **Kabel** | Kupfer, Glasfaser, Koaxial |
| **WLAN-Antenne** | Funksignale |

### Standards/Protokolle:
- **Ethernet** (IEEE 802.3) – physikalische Ebene
- **DSL** – Digital Subscriber Line
- **USB** – Universal Serial Bus
- **Bluetooth** (IEEE 802.15)

---

## 💡 Prüfungstipp – Schicht 1

> **Merke:** Schicht 1 kennt **keine Adressen**!
> Sie überträgt nur rohe Bits – ohne zu wissen, was sie bedeuten.

**Typische Prüfungsfrage:**
> *"Auf welcher Schicht arbeitet ein Hub?"*
> ✅ **Schicht 1 – Bitübertragungsschicht**

---

# 🟢 SCHICHT 2
## Sicherungsschicht (Data Link Layer)

---

## Aufgaben der Schicht 2

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Gesicherte Übertragung zwischen direkt verbundenen Geräten |
| **Einheit** | **Frame (Rahmen)** |
| **Adresse** | **MAC-Adresse** (48 Bit, z.B. `00:1A:2B:3C:4D:5E`) |

### Hauptaufgaben:
- 📦 **Framing** – Daten in Rahmen verpacken
- 🔍 **Fehlererkennung** – CRC-Prüfsummen
- 🔄 **Flusskontrolle** – Übertragungsgeschwindigkeit anpassen
- 🔀 **MAC-Adressierung** – Geräte im lokalen Netz identifizieren

---

## MAC-Adresse – Wichtig für die Prüfung!

```
00:1A:2B:3C:4D:5E
└──────┘ └──────┘
   OUI    Geräte-ID
(Hersteller) (eindeutig)
```

| Merkmal | Details |
|---------|---------|
| **Länge** | 48 Bit = 6 Byte |
| **Schreibweise** | Hexadezimal, z.B. `00:1A:2B:3C:4D:5E` |
| **Eindeutigkeit** | Weltweit eindeutig (theoretisch) |
| **Typ** | Hardware-Adresse (in NIC eingebrannt) |

---

## Geräte & Protokolle – Schicht 2

### Geräte:
| Gerät | Funktion |
|-------|----------|
| **Switch** | Leitet Frames anhand von MAC-Adressen weiter |
| **Bridge** | Verbindet zwei Netzsegmente |
| **WLAN Access Point** | Drahtlose Verbindung |

### Protokolle:
- **Ethernet** (IEEE 802.3)
- **WLAN** (IEEE 802.11)
- **PPP** – Point-to-Point Protocol
- **ARP** – Address Resolution Protocol *(Schicht 2/3)*

---

## 💡 Prüfungstipp – Schicht 2

> **Merke:** Ein Switch arbeitet auf **Schicht 2** und nutzt die **MAC-Adresstabelle** (CAM-Table)

**Vergleich Hub vs. Switch:**

| | Hub (Schicht 1) | Switch (Schicht 2) |
|--|----------------|-------------------|
| Weiterleitung | An alle Ports | Nur an Zielport |
| Intelligenz | Keine | MAC-Tabelle |
| Kollisionen | Möglich | Keine |

---

# 🟡 SCHICHT 3
## Vermittlungsschicht (Network Layer)

---

## Aufgaben der Schicht 3

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Wegewahl (Routing) durch das Netzwerk |
| **Einheit** | **Paket (Packet)** |
| **Adresse** | **IP-Adresse** |

### Hauptaufgaben:
- 🗺️ **Routing** – Besten Weg durch das Netzwerk finden
- 📬 **Logische Adressierung** – IP-Adressen vergeben
- 🔀 **Fragmentierung** – Pakete aufteilen falls nötig
- 🌐 **Netzwerkübergreifende Kommunikation**

---

## IP-Adressen – Kurze Wiederholung

### IPv4:
```
192.168.1.100
└─┘ └─┘ └┘ └─┘
  4 Oktette à 8 Bit = 32 Bit gesamt
```

### IPv6:
```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
└──────────────────────────────────────┘
              128 Bit gesamt
```

---

## Geräte & Protokolle – Schicht 3

### Geräte:
| Gerät | Funktion |
|-------|----------|
| **Router** | Verbindet Netzwerke, wählt Routen |
| **Layer-3-Switch** | Switch mit Routing-Funktion |

### Protokolle:
| Protokoll | Funktion |
|-----------|----------|
| **IP** (v4/v6) | Logische Adressierung |
| **ICMP** | Fehlermeldungen (z.B. Ping) |
| **OSPF** | Routing-Protokoll |
| **BGP** | Internet-Routing |
| **ARP** | IP → MAC Auflösung |

---

## 💡 Prüfungstipp – Schicht 3

> **Merke:** Der Router arbeitet auf **Schicht 3** und nutzt **IP-Adressen** für die Weiterleitung

**Wichtige Unterscheidung:**
```
Schicht 2: MAC-Adresse → lokales Netz
Schicht 3: IP-Adresse  → netzwerkübergreifend
```

**Prüfungsfrage:**
> *"Welches Protokoll wird verwendet, um eine IP-Adresse in eine MAC-Adresse aufzulösen?"*
> ✅ **ARP – Address Resolution Protocol**

---

# 🟠 SCHICHT 4
## Transportschicht (Transport Layer)

---

## Aufgaben der Schicht 4

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Zuverlässige Ende-zu-Ende-Verbindung |
| **Einheit** | **Segment** (TCP) / **Datagramm** (UDP) |
| **Adresse** | **Port-Nummer** |

### Hauptaufgaben:
- 🔢 **Segmentierung** – Daten in Segmente aufteilen
- ✅ **Fehlerkorrektur** – Verlorene Pakete neu anfordern
- 🔄 **Flusskontrolle** – Datenmenge regulieren
- 🚪 **Ports** – Anwendungen unterscheiden

---

## TCP vs. UDP – Prüfungsrelevant!

| Merkmal | TCP | UDP |
|---------|-----|-----|
| **Verbindung** | Verbindungsorientiert | Verbindungslos |
| **Zuverlässigkeit** | Ja (ACK) | Nein |
| **Reihenfolge** | Garantiert | Nicht garantiert |
| **Geschwindigkeit** | Langsamer | Schneller |
| **Overhead** | Hoch | Gering |
| **Einsatz** | HTTP, FTP, E-Mail | DNS, VoIP, Streaming |

---

## Wichtige Port-Nummern – Auswendig lernen!

| Port | Protokoll | Beschreibung |
|------|-----------|-------------|
| **20/21** | FTP | Dateiübertragung |
| **22** | SSH | Sichere Fernwartung |
| **23** | Telnet | Fernwartung (unsicher) |
| **25** | SMTP | E-Mail senden |
| **53** | DNS | Namensauflösung |
| **67/68** | DHCP | IP-Adressvergabe |
| **80** | HTTP | Webseiten |
| **110** | POP3 | E-Mail empfangen |
| **143** | IMAP | E-Mail empfangen |
| **443** | HTTPS | Sichere Webseiten |

---

## Der TCP-Handshake

```
Client                    Server
  │                          │
  │──── SYN ────────────────>│
  │                          │
  │<─── SYN-ACK ────────────│
  │                          │
  │──── ACK ────────────────>│
  │                          │
  │   Verbindung aufgebaut   │
```

> **SYN** = Synchronize | **ACK** = Acknowledge

---

## 💡 Prüfungstipp – Schicht 4

> **Merke:** Schicht 4 ist für die **Ende-zu-Ende-Kommunikation** zuständig – unabhängig vom Netzwerkweg!

**Eselsbrücke:**
> TCP = **T**otally **C**ertain **P**rotocol (zuverlässig)
> UDP = **U**nsafe **D**ata **P**rotocol (schnell, aber unsicher)

---

# 🔴 SCHICHT 5
## Sitzungsschicht (Session Layer)

---

## Aufgaben der Schicht 5

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Aufbau, Verwaltung und Abbau von Sitzungen |
| **Einheit** | **Daten** |

### Hauptaufgaben:
- 🤝 **Sitzungsaufbau** – Verbindung zwischen Anwendungen herstellen
- 🔄 **Synchronisation** – Checkpoints setzen
- 🔁 **Wiederherstellung** – Bei Unterbrechungen fortsetzen
- 👥 **Dialogsteuerung** – Halb- oder Vollduplex

### Beispiele:
- **NetBIOS** – Sitzungen im Windows-Netzwerk
- **RPC** – Remote Procedure Call
- **SQL-Sitzungen**

---

## 💡 Prüfungstipp – Schicht 5

> **Hinweis:** Schicht 5 ist in der Praxis weniger prominent – in TCP/IP ist sie im Anwendungsprotokoll integriert

> **Merke:** Schicht 5 = **Sitzungsverwaltung**
> Beispiel: Ein Videoanruf besteht aus Audio- und Videositzung – Schicht 5 hält diese zusammen

---

# 🟣 SCHICHT 6
## Darstellungsschicht (Presentation Layer)

---

## Aufgaben der Schicht 6

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Daten in einheitliches Format umwandeln |
| **Einheit** | **Daten** |

### Hauptaufgaben:
- 🔄 **Datentransformation** – Konvertierung zwischen Formaten
- 🔐 **Verschlüsselung/Entschlüsselung** – z.B. SSL/TLS
- 🗜️ **Komprimierung** – Daten komprimieren
- 📝 **Zeichenkodierung** – ASCII, Unicode, EBCDIC

### Beispiele:
| Format | Typ |
|--------|-----|
| **JPEG, PNG, GIF** | Bildformate |
| **MP3, MP4** | Medienformate |
| **ASCII, UTF-8** | Zeichenkodierung |
| **SSL/TLS** | Verschlüsselung |

---

## 💡 Prüfungstipp – Schicht 6

> **Merke:** Schicht 6 = **"Übersetzer"** des Netzwerks

> Wenn eine Windows-Anwendung mit einem Linux-Server kommuniziert, sorgt Schicht 6 dafür, dass die Daten korrekt interpretiert werden.

---

# 🔵 SCHICHT 7
## Anwendungsschicht (Application Layer)

---

## Aufgaben der Schicht 7

| Merkmal | Beschreibung |
|---------|-------------|
| **Aufgabe** | Schnittstelle zwischen Netzwerk und Anwendung |
| **Einheit** | **Daten** |

### Hauptaufgaben:
- 🖥️ **Netzwerkdienste** für Anwendungen bereitstellen
- 📧 **E-Mail, Web, Dateitransfer** ermöglichen
- 🔍 **Namensauflösung** (DNS)
- 📁 **Dateifreigaben** (SMB, NFS)

---

## Protokolle der Schicht 7

| Protokoll | Funktion |
|-----------|----------|
| **HTTP/HTTPS** | Webseiten übertragen |
| **FTP/SFTP** | Dateien übertragen |
| **SMTP** | E-Mails senden |
| **POP3/IMAP** | E-Mails empfangen |
| **DNS** | Namen in IP-Adressen auflösen |
| **DHCP** | IP-Adressen automatisch vergeben |
| **SNMP** | Netzwerkgeräte überwachen |
| **SSH** | Sichere Fernwartung |
| **Telnet** | Fernwartung (unsicher) |

---

# 4️⃣ MERKHILFEN & PRÜFUNGSTIPPS
## ⏱️ ~5 Minuten

---

## 🧠 Merkhilfen für die 7 Schichten

### Von oben nach unten (7→1):
**"Alle Deutschen Studenten Trinken Verschiedene Sorten Bier"**
```
A lle         → Anwendungsschicht    (7)
D eutschen    → Darstellungsschicht  (6)
S tudenten    → Sitzungsschicht      (5)
T rinken      → Transportschicht     (4)
V erschiedene → Vermittlungsschicht  (3)
S orten       → Sicherungsschicht    (2)
B ier         → Bitübertragung       (1)
```

---

### Von unten nach oben (1→7):
**"Bitte Sende Trotzdem Vernünftige Daten Anständig"**
```
B itte         → Bitübertragung       (1)
S ende         → Sicherungsschicht    (2)
T rotzdem      → Transportschicht... 
```
*(Wählt die Merkhilfe, die euch am besten gefällt!)*

---

## 📊 Komplette Übersichtstabelle

| Nr. | Schicht | PDU | Adresse | Gerät | Protokolle |
|-----|---------|-----|---------|-------|------------|
| 7 | Anwendung | Daten | – | – | HTTP, FTP, DNS, SMTP |
| 6 | Darstellung | Daten | – | – | SSL, JPEG, ASCII |
| 5 | Sitzung | Daten | – | – | NetBIOS, RPC |
| 4 | Transport | Segment | Port | – | TCP, UDP |
| 3 | Vermittlung | Paket | IP | Router | IP, ICMP, OSPF |
| 2 | Sicherung | Frame | MAC | Switch | Ethernet, ARP |
| 1 | Bitübertragung | Bit | – | Hub | DSL, USB |

> **PDU** = Protocol Data Unit (Bezeichnung der Dateneinheit)

---

## 🎯 Top 10 Prüfungsthemen zum OSI-Modell

1. ✅ Schichten benennen und nummerieren
2. ✅ Aufgaben jeder Schicht beschreiben
3. ✅ Geräte den Schichten zuordnen (Hub, Switch, Router)
4. ✅ Protokolle den Schichten zuordnen
5. ✅ TCP vs. UDP unterscheiden
6. ✅ Port-Nummern kennen
7. ✅ MAC vs. IP-Adresse unterscheiden
8. ✅ PDU-Bezeichnungen kennen (Bit, Frame, Paket, Segment)
9. ✅ Encapsulation erklären
10. ✅ OSI vs. TCP/IP-Modell vergleichen

---

# 5️⃣ PRAXISBEZUG & PROTOKOLLBEISPIELE
## ⏱️ ~7 Minuten

---

## Was passiert beim Aufrufen einer Webseite?

**Beispiel:** Browser ruft `www.beispiel.de` auf

```
Schicht 7 (Anwendung):  HTTP-Anfrage wird erstellt
         ↓
Schicht 6 (Darstellung): Daten werden kodiert (UTF-8)
         ↓
Schicht 5 (Sitzung):    Sitzung wird aufgebaut
         ↓
Schicht 4 (Transport):  TCP-Verbindung, Port 80/443
         ↓
Schicht 3 (Vermittlung): IP-Paket mit Ziel-IP
         ↓
Schicht 2 (Sicherung):  Ethernet-Frame mit MAC
         ↓
Schicht 1 (Physisch):   Bits über Kabel/WLAN
```

---

## Encapsulation – Datenkapselung

```
┌────────────────────────────────────────────────┐
│  Schicht 7-5: [ DATEN ]                        │
├────────────────────────────────────────────────┤
│  Schicht 4:   [ TCP-Header | DATEN ]           │
├────────────────────────────────────────────────┤
│  Schicht 3:   [ IP-Header | TCP | DATEN ]      │
├────────────────────────────────────────────────┤
│  Schicht 2:   [ ETH | IP | TCP | DATEN | FCS ] │
├────────────────────────────────────────────────┤
│  Schicht 1:   01001010110100101...             │
└────────────────────────────────────────────────┘
```

> **Beim Empfänger:** Jede Schicht entfernt ihren Header → **Decapsulation**

---

## OSI-Modell vs. TCP/IP-Modell

| OSI-Schicht | TCP/IP-Schicht |
|-------------|----------------|
| 7 – Anwendung | **Anwendung** |
| 6 – Darstellung | **Anwendung** |
| 5 – Sitzung | **Anwendung** |
| 4 – Transport | **Transport** |
| 3 – Vermittlung | **Internet** |
| 2 – Sicherung | **Netzzugang** |
| 1 – Bitübertragung | **Netzzugang** |

> **Merke:** TCP/IP hat nur **4 Schichten** – OSI hat **7 Schichten**
> In der Praxis wird **TCP/IP** verwendet, OSI dient als **Referenzmodell**

---

## Fehlerdiagnose mit dem OSI-Modell

**Im Berufsalltag:** Fehler systematisch von unten nach oben eingrenzen!

```
Schicht 1: Kabel kaputt? LED leuchtet?
    ↓
Schicht 2: Switch-Port aktiv? VLAN korrekt?
    ↓
Schicht 3: IP-Adresse korrekt? Route vorhanden? (ping)
    ↓
Schicht 4: Port erreichbar? Firewall-Regel?
    ↓
Schicht 7: Anwendung funktioniert?
```

---

# 6️⃣ WIEDERHOLUNG & PRÜFUNGSFRAGEN
## ⏱️ ~5 Minuten

---

## ❓ Prüfungsfragen – Beantwortet selbst!

**Frage 1:**
> Auf welcher Schicht des OSI-Modells arbeitet ein Switch?

**Frage 2:**
> Welche PDU-Bezeichnung hat die Transportschicht bei TCP?

**Frage 3:**
> Welches Protokoll löst IP-Adressen in MAC-Adressen auf?

**Frage 4:**
> Nennen Sie zwei Unterschiede zwischen TCP und UDP!

**Frage 5:**
> Auf welchem Port läuft HTTPS?

---

## ✅ Antworten

**Frage 1:** → **Schicht 2** (Sicherungsschicht)

**Frage 2:** → **Segment**

**Frage 3:** → **ARP** (Address Resolution Protocol)

**Frage 4:** → TCP: verbindungsorientiert, zuverlässig / UDP: verbindungslos, schnell

**Frage 5:** → **Port 443**

---

## 🎯 Zusammenfassung – Das Wichtigste

```
┌──────────────────────────────────────────────┐
│  7 SCHICHTEN – MERKE DIR:                    │
│                                              │
│  7 - Anwendung   → HTTP, FTP, DNS            │
│  6 - Darstellung → SSL, Kodierung            │
│  5 - Sitzung     → Verbindungsverwaltung     │
│  4 - Transport   → TCP/UDP, Ports            │
│  3 - Vermittlung → IP, Router                │
│  2 - Sicherung   → MAC, Switch, Ethernet     │
│  1 - Bitübertrag → Kabel, Hub, Bits          │
└──────────────────────────────────────────────┘
```

---

## 📚 Empfehlungen zur Vorbereitung

### Für die Prüfung üben:
1. **Schichten auswendig lernen** – Nummer + Name + Aufgabe
2. **Port-Tabelle auswendig lernen** – mind. 10 wichtige Ports
3. **Geräte zuordnen** – Hub, Switch, Router, Bridge
4. **TCP vs. UDP** – Unterschiede erklären können
5. **Alte Prüfungsaufgaben** lösen (IHK-Prüfungsarchiv)

### Nützliche Ressourcen:
- 📖 IT-Handbuch für Fachinformatiker (Westermann)
- 🌐 IHK-Prüfungsarchiv online
- 📝 Eigene Karteikarten erstellen

---

## 🏁 Abschluss

> ### "Das OSI-Modell ist kein trockenes Theoriekonstrukt –
> ### es ist euer tägliches Werkzeug als Fachinformatiker!"

---

**Habt ihr noch Fragen?** 🙋

---

*Viel Erfolg bei der Prüfung!* 🎓

---

## 📎 ANHANG – Spickzettel für die Prüfung

### Alle Schichten auf einen Blick:

| # | Schicht | Aufgabe | PDU | Gerät | Protokolle |
|---|---------|---------|-----|-------|------------|
| 7 | Anwendung | Dienste für Anwendungen | Daten | – | HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS, DHCP, SSH |
| 6 | Darstellung | Formatierung, Verschlüsselung | Daten | – | SSL/TLS, JPEG, ASCII, MPEG |
| 5 | Sitzung | Sitzungsmanagement | Daten | – | NetBIOS, RPC, NFS |
| 4 | Transport | Ende-zu-Ende, Ports | Segment/Datagramm | – | TCP, UDP |
| 3 | Vermittlung | Routing, IP-Adressierung | Paket | Router, L3-Switch | IP, ICMP, OSPF, BGP, ARP |
| 2 | Sicherung | MAC-Adressierung, Framing | Frame | Switch, Bridge | Ethernet, WLAN, PPP |
| 1 | Bitübertragung | Physische Übertragung | Bit | Hub, Repeater | DSL, USB, Bluetooth |

---

*Ende des Vortrags*
*Prüfungsvorbereitungskurs Fachinformatiker Systemintegration*