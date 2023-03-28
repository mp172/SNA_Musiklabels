# SNA_Musiklabels

# Datensatz Musiklabels Deutschland und USA
Codebuch Stand 2023-03
erstellt von Alicia Becht (ab297), Marie Pütter (mp172), Fritz Wirbitzky (fw067), Paulina Bahr (pb089), Anne Meister (am214) und Sophia Rapp (sr187)

## Inhalt
- DE_nodes5.csv (Nodelist DE)
- DE_edge2.csv (Edgelist DE)
- USA_nodes.csv (Nodelist USA)
- USA_edges.csv (Edgelist USA)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung

Wir untersuchen die Labelstruktur der erfolgrichsten Artist in Deutschland (https://www.chartsurfer.de/musik/single-charts-deutschland/jahrescharts/artist/2022/top-100/4) und den USA (https://www.chartsurfer.de/musik/single-charts-usa/jahrescharts/artist/2022/top-100/4) im Jahr 2022. 

Dabei interessiert uns, welche Rolle die unterschiedlichen Formen von Labels in der Musikbranche haben. 
Für das Netzwerk wurden zwei Datensätze, zusammengesetzt aus Labels und Artists, erhoben. Dabei wurden nur Artists berücksichtigt, die die Staatsbürgerschaft des jeweiligen Landes besitzen (Datensatz USA: inklusive Puerto Rico) oder deren Songs in der Landessprache verfasst sind. Die entsprechenden Labels wurden anhand der aktuell bestehenden Verträge erhoben.

Neben den Beziehungsstrukturen zwischen Artist und Label wurden 
Variablen (Typus, Art, Geschlecht, Lebendigkeit, Genre, Platzierung anhand Punkte (https://www.chartsurfer.de/auswertung-info)) erfasst. 

Auf der Beziehungsebene interessiert uns, wer wo unter Vertrag steht, welche Label wie miteinander verknüpft sind und welche Artists eigene Labels besitzen. 

Das Netzwerk ist ein gerichtetes two-mode Akteursnetzwerk.

*Umgang mit fehlgenden Werten*

Fehlende Werte werden mit 0 codiert.

# EDGE-Attribute

*id*  

(eindeutige Codierung des Knoten)   
Deutschland: 132 Knoten, USA: 266 Knoten

Die ID sind die ersten vier Buchstaben des Namens, Artikel wie "the" wurden weggelassen


*from*

initiierender Knoten

*to*

erhaltender Knoten

*relation*

Beziehungsart zwischen den Personen  


1 - Unter Vertrag (Artists zu Label)

2 - Vertrieb über (Label zu Majorlabel (Vertrieb)

3 - Vertrag + Vertrieb (Artist zu Label)

4 - Ist Sublabel von… (Sublabel zu Label)

5 - Beteiligung ohne Vertrag (Filmmusik, Artist zu Label) 

6 - Arbeitsgemeinschaft/gleichgewichtete Kooperation (Label zu Label)

7 - Label von (Künstler zu selbst gegründeten Label)


# NODE-Attribute  
  
*id*  

Identische ID wie aus der edgelist zur Identifikation der Knoten.


*name*

Name des Artists


*type*

1 - Mensch

2 - Orga


*sort*

1-Solokünstler:in

2-Band

3-Majorlabel

4-Sublabel

5-Independent-Label

6-Eigenvertrieb

7-reiner Vertrieb-Dienstleister

8 - Produzent:in


*ranking*

Rang auf der Chartliste

bei Label: 0

*points*

Punktezahl auf der Chartliste

bei Label: 0


*gender*

1 -female

2 -male

3 -divers

4 -Bands mit gemischten Geschlechtern

bei Label: 0

*alive*

1-yes

2-no

0 - Label


*genre*

1 - Pop/ Indie Pop 

2 - Schlager/Ballermann

3 - Rock/ Metal/ Indie Rock

4 - HipHop/Rap/RnB

5 - Klassik 

6 - Soul/Funk 

7 - House/Electro/Techno

8 - Country

9 - Jazz

10 - Reggaeton

bei Label: 0

##
