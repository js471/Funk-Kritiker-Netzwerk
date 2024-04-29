# Codebuch Funk Kritiker Netzwerk

## Inhalt
- edgelist.csv (Edgelist)
- nodelist.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Forschungsinteresse, Ursprung und Datenerhebung
In unserem Netzwerkforschungprojekt wollen wir die Verbindungen und Verknüpfungen des Funk Netzwerks, STRG+F und seinen Kritikern darstellen und analysieren. Wir beobachteten dabei den Zeitraum vom 1. Januar 2023 bis 29. Februar 2024. Die Daten wurden individuell erfasst und eingetragen von den jeweiligen YouTube Kanälen.

Das Netzwerk ist ein *gerichtetes one-mode Netzwerk*. 

# EDGE-Attribute

**from**
Die Werte in der Spalte "from" definieren Sender in gerichteten Netzwerken, beziehungsweise generell einen Ausgangspunkt einer Beziehung. Da wir ein ungerichtetes Netzwerk erhoben haben, ist die Richtung der Beziehung nicht relevant. Der eingetragene Wert entspricht einer ID in der Nodelist und enthält keine Sonderzeichen, sondern nur ein Wort.

**to**
Die Werte in der Spalte "to" definieren Empfänger in ungerichteten Netzwerken. Der eingetragene Wert entspricht einer ID in der Nodelist und enthält keine Sonderzeichen, sondern nur ein Wort.

**relationship**  
Das Edge-Attribut "relationship" definiert die Art der Beziehung zwischen den Knoten, da es sich um ein multiplexes Netzwerk mit verschiedenen Beziehungsarten handelt. 

1 = Teil des Funk Netzwerks | Kantenattribut welches zwischen Funk und den jeweiligen Funk Kanälen und Partnern besteht.

2 = Reaction | Ein Knoten hat "Reaction" Videos über Inhalte eines anderen Knotens erstellt.

3 = Positive Erwähnung | Ein Knoten erwähnte den anderen Knoten positiv in seinen Videos.

4 = Kritik | Ein Knoten erstellte Kritikvideos über den Knoten.

5 = Ehemaliges Funknetzwerk | Der Knoten war in einem Geschäftsverhältniss mit dem Funk Knoten.

6 = Kollaboration | Zwischen zwei Knoten fand eine Kollaboration statt.

**weight**   
Das Edge-Attribut "weight" definiert die Gewichtung, welche wir anhand der Nummer von erstellten Videos zwischen zwei Knoten festlegen.

1 = 0 Video
2 = 1 Video
3 = 2 Videos
4 = ab 3 Videos 

# NODE-Attribute  

Die Knoten im Netzwerk bestehen hauptsächlich aus YouTube Kanälen. Ausnahme ist hier der "Funk" Knoten welcher sowohl den YouTube Kanal von Funk als auch das Content-Netzwerk meint. 

**id**  
(eindeutige Codierung des Knoten)   
codiert anhand der Initialen der YouTube Kanäle (bspw. "yk" für Y-Kollektiv).

**name**  
Gibt den Namen des YouTube Kanals des Knotens an. 

**creator**  
Nennt die jeweilige Person, Gruppe oder Institution die den Kanal leitet.

**funk**    
Definiert ob der Kanal zu Funk gehört, nicht zu Funk gehört oder ehemalig zu Funk gehörte. 
1 = Ja
2 = Nein
3 = Ehemalig
  
**Wohnsitz/Produktionsort**  
Nennt woher der jeweilige YouTuber kommt oder der Hauptsitz des Kanals ist.

**veröffentlichungsdatum**   
definiert an welchem Datum das erste Kritikvideo zur STRG+F vs Rezo Thematik veröffentlicht wurde.  
tt/mm/jj

**upload**  
Zählt wie viele Videos im genannten Zeitraum auf dem Kanal hochgeladen wurden. Kann wichtig sein wenn man den prozentualen Anteil anschauen will zwischen Kritikvideos und gesamt Uploads zu der Zeit.

**austrittsdatum**  
Zeigt an zu welchem Zeitpunkt der jeweilige Kanal aus Funk ausgetreten ist, wenn dieser zuvor bei Funk war.
tt/mm/jj

**kritik**  
Zählt wie viele Kritikvideos gegenüber STRG+F und Funk im genannten Zeitraum erstellt wurden.  

**reaktion_kritik**  
Zählt wie viele Videos von Funk Kanälen als Antwort auf Kritikvideos erschienen sind.

# Fehlende Werte
99 = fehlende Werte  
(etwa wenn diese nicht verfügbar waren oder wenn das Attribut nur auf Personen bezogen ist, wurde bei Knoten des Typs 2 (Aktion) dieser Wert vergeben)  
Eine vorherige Codierung mit "NA" hat zu Problemen bei der Netzwerkgenerierung geführt, was mit Vergabe des Werts "99" stattdessen behoben werden konnte.

##
