Să adăugăm plugin-ul în pom.xml. Trimite-mi conținutul actual al pom.xml (sau o poză cu el), ca să îl actualizez corect fără să stric nimic.
Sau dacă vrei rapid — deschide pom.xml în IntelliJ și înlocuiește secțiunea <build> cu aceasta:
xml<build>
    <plugins>
        <plugin>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-maven-plugin</artifactId>
            <version>0.0.8</version>
            <configuration>
                <mainClass>com.centru.MainApp</mainClass>
            </configuration>
        </plugin>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.11.0</version>
            <configuration>
                <source>17</source>
                <target>17</target>
            </configuration>
        </plugin>
    </plugins>
</build>
Dacă pom.xml nu are deloc secțiunea <build>, adaug-o înainte de </project> (ultima linie din fișier).
După ce salvezi, în IntelliJ:

Click dreapta pe pom.xml → Maven → Reload project
Configurație Run → Maven → javafx:run → OK → ▶️
