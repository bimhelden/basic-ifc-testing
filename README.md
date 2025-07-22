## Unterstützung für die Prüfung von IFC-Modellen 

**Problem und Idee:**<br>
Der IFC-Standard definiert in seinem Schema bereits zahlreiche Prüfregeln, die beim Erzeugen der IFC-Modelle nicht immer eingehalten werden. 
Die Gründe dafür sind vielfältig und die Prüfung meist nur für den Experten verständlich. 
Auch wenn eine solche Prüfung primär für Softwareentwickler relevant ist, so kann sie auch für normaler Anwender wichtige Einblicke in die Qualität der ausgetauschten IFC-Modelle liefern.   
Wir wollen die Prüfung der IFC-Modelle so vereinfachen, dass auch der Laie die Prüfergebnisse besser einordnen kann. 

**Lösung:**<br>
Wir haben begonnen, die im IFC-Schema definierten Regeln in eine für den Anwender verständliche Sprache zu übersetzen. 
Alle Regeln sind in einer Tabelle mit weiteren Hinweisen zusammengefasst und können zur Erläuterung der Prüfergebnisse herangezogen werden.<br><br>
Die tabellarische Aufbereitung unter anderem mit der Benennung der Fehler (WR aus dem Schema), 
der Übersetzung der IFC-Dokumentation, einer Einschätzung zur Art (falsche Eingabe durch den Anwender oder Exportfehler durch die Software) 
sowie mögliche Schritte zur Behebung des Fehlers sind an einem Beispiel gezeigt.  
![Beispiel für die tabellarische Aufbereitung](https://github.com/bimhelden/basic-ifc-testing/blob/main/Beispiel.png)<br><br>
Die mögliche Nutzung der Übersetzungstabelle zeigt ein Programm, das die Prüfergebnisse des frei verfügbaren [ifcCheckingTool](www.iai.kit.edu/ifc) von KIT in eine Excel-Tabelle überträgt.

**Selbst ausprobieren:**<br>
Sie benötigen eine ChkXML-Datei mit Prüfergebnissen und das hier bereitgestellte Programm ChkXML2XLSX.<br>
Laden Sie dafür die im Verzeichnis [Fehlerdokumentation](https://github.com/bimhelden/basic-ifc-testing/tree/main/Fehlerdokumentation) bereitgestellte Dateien mit allen Unterordnern herunter.<br>  
Folgende Dateien sind verfügbar:
1. Ein Beispiel mit Prüfbericht als ChkXML-Datei sowie als konvertierte Tabelle
2. Das Programm *ChkXML2XLSX.exe* mit allen zugehörigen Programmdateien im Unterordner _internal
3. Die für das Konvertieren verwendeten Hinweise als *ChkXML-IFC4Add2TC1-DE.csv*

Das Programm wird als Konsolapplikation bereitgestellt und kann mit folgendem Kommando aus der Konsole aufgerufen werden:<br>
>`ChkXML2XLSX Beispiele/Input.chkxml Beispiele/Output.xlsx`

Mit der Option -u können Sie die neueste Version der Übersetzungsdatei direkt von Github herunterladen und geben uns gleichzeit ein Feedback über die aufgetretenen Fehler. 
>`ChkXML2XLSX Beispiele/Input.chkxml Beispiele/Output.xlsx -u`

*Es gelten die in Haftungsausschluss.md ausgewiesenen Nutzungsbedingungen.* 