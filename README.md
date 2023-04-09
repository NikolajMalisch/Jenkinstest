# Jenkinstest
Maven-Test-Pipeline
Dieses Repository enthält eine Beispiel-Jenkins-Pipeline, die eine Maven-basierte Anwendung erstellt, testet und bereitstellt.

Anforderungen
Um diese Pipeline auszuführen, benötigen Sie:

Jenkins-Server mit dem "Pipeline" Plugin installiert
Docker installiert
Verwendung
Klonen Sie dieses Repository auf Ihrem Jenkins-Server.
Erstellen Sie eine neue Pipeline in Jenkins und wählen Sie "Pipeline aus SCM" als Definitionsmethode aus.
Geben Sie die Git-Repository-URL und die Branch-Name-Details ein und speichern Sie die Pipeline.
Sobald die Pipeline erfolgreich gespeichert wurde, sollte sie automatisch gestartet werden, um Ihre Anwendung zu erstellen, zu testen und bereitzustellen.

Pipeline-Schritte
Build
Dieser Schritt kompiliert die Quellcode-Dateien und erstellt ein ausführbares JAR-Archiv.

Test
Dieser Schritt führt alle Unit-Tests in der Anwendung aus und generiert einen Testbericht.

Deliver
Dieser Schritt ist verantwortlich für die Bereitstellung der Anwendung. Es verwendet ein benutzerdefiniertes Shell-Skript, um die Anwendung in einer Docker-Containerumgebung bereitzustellen.

Hinweise
Stellen Sie sicher, dass Ihre Jenkins-Umgebung die notwendigen Berechtigungen hat, um Docker-Befehle auszuführen.
Passen Sie die "Deliver" Schritt entsprechend an, um Ihre eigene Bereitstellungslogik zu implementieren.
