# SNA_Musiklabels

# Datensatz Musiklabels Deutschland und USA#
Codebuch Stand 2023-03
erstellt von Alicia Becht (ab297), Marie Pütter (mp172) und Sophia Rapp (sr187)

## Inhalt
- DE_nodes5.csv (Nodelist DE)
- DE_edge2.csv (Edgelist DE)
- USA_nodes.csv (Nodelist USA)
- USA_edges.csv (Edgelist USA)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Ich habe den Datensatz unter den Studierenden des dritten Semesters im Kurs Netzwerkanalyse erhoben. Die Daten sind nach der Erhebung nach einem Zufallsprinzip anonymisiert worden.

Das Netzwerk ist ein gerichtetes two-mode Akteursnetzwerk.

*Umgang mit fehlgenden Werten*
Fehlende Werte werden nicht erfasst.

# EDGE-Attribute

*id*  
(eindeutige Codierung des Knoten)   
codiert von 1 bis 38, jede ID entspricht einem Studenten

*from*
initiierender Knoten, in diesem Fall: Student/in fragt um Rat oder zeigt präferierte Zusammenarbeit

*to*
erhaltender Knoten, in diesem Fall: Student/in wird um Rat gefragt oder für Zusammenarbeit präferiert

*weight*  
Beziehungsstärke aufgrund der Nennung in den Fragen)  
3 = sehr starke Beziehung (erste Nennung),   
1 = starke Beziehung vorhanden (zweite Nennung)

*relation*
Beziehungsart zwischen den Personen  
1 = work Projektbasierte Beziehung: Bei einem gerichteten Netzwerk präferiert der Sender (erste Spalte) die Zusammenarbeit mit der genannten Zielperson (zweite Spalte).  
2 = help Unterstützungsbeziehung: Bei einem gerichteten Netzwerk fragt der Sender (erste Spalte) die genannte Person (zweite Spalte) um Rat.  
3 = love Liebesbeziehung zwischen Akteuren, codiert nach dem Attribut complicated

*complicated*  
1 = Beziehung (typische Paarbeziehung, d.h. reziprok zwischen beiden PartnerInnen),      
2 = Tinder-Like (hat die person rechts geswiped, muss aber nicht gegenseitig sein)     
3 = Crush (einseitig verliebt, ohne dass die Person etwas davon weiss).  


# NODE-Attribute  
  
*id*  
Identische ID wie aus der edgelist zur Identifikation der Knoten. In diesem Fall sind alle personenbezogenen Daten anonymisiert von 1 bis 38.

*name*
numerische ID

*name_first*
Vorname abgekürzt, z.B. für Visualisierung, falls der Name zu lange ist

*sex*    
Bitte geben Sie ihr Geschlecht an:  
1 = weiblich  
2 = männlich  
3 = divers
  
*crpr**    
Welche Studienrichtung haben Sie vertieft?  
1 = CR  
2 = PR

*height*  
Größe in cm   

*weight*  
Gewicht in kg  

*age_real*   
Alter in natürlichen Zahlen.  

*age*   
Bitte geben Sie Ihr Alter an:  
1 = bis 20 Jahre    
2 = 21 bis 22 Jahre    
3 = 23 bis 24 Jahre  
4 = 25 und älter  

*smoke*    
Rauchen Sie mindestens ein Mal pro Woche?  
1 = nein   
2 = ja  
  
*tatoo*    
Tatoo vorhanden?   
1 = nein  
2 = ja  

*phone*  
1 = android  
2 = iOS/iphone  
  
*eyes*    
Welche Augenfarbe?    
1 = grün,   
2 = blau,   
3 = braun,   
4 = blau.     

*hair*  
Welche Haarfarbe?  
1 = braun,      
2 = schwarz,   
3 = blond,    
4 = rot.    

*location* 
Wohnort, als string/characters codiert  

*county*  
Bundesland, als string/characters codiert  


##