Văd că ești în IntelliJ IDEA și nu ai o configurație de rulare. Trebuie să adaugi una pentru JavaFX cu Maven. Iată pașii exact:
În fereastra "Run/Debug Configurations" care e deschisă:

Click pe + (Add New Configuration) din stânga sus
Selectează Maven
În câmpul "Run" scrie: javafx:run
Click OK
Apasă butonul ▶️ Run


Alternativ, mai simplu — direct din terminal IntelliJ:
Deschide terminalul din IntelliJ (Alt+F12) și rulează:
bashmvn javafx:run

Dacă apare eroare că Maven nu găsește JavaFX, asigură-te că pom.xml are plugin-ul corect — deschide pom.xml și verifică că există secțiunea:
xml<plugin>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-maven-plugin</artifactId>
    <version>0.0.8</version>
    <configuration>
        <mainClass>com.centru.MainApp</mainClass>
    </configuration>
</plugin>
Dacă e prezent, configurația Maven cu javafx:run va funcționa direct. Văd și că MySQL rulează pe portul 3306 în XAMPP — deci conexiunea BD ar trebui să meargă imediat.
