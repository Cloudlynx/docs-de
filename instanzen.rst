Instanzen erstellen
===================

Einführung
----------

Vielen Dank, dass Sie sich für Cloudlynx entschieden haben. Mit dieser Website möchten wir Cloud-Administratoren oder Systemoperatoren beim ersten Einstieg in unsere Cloud behilflich sein. Wir hoffen, dass hier auch alle Fragen, die im täglichen Betrieb auftauchen, beantwortet werden.

Folgende Themen sind behandelt:

* Compute Instanzen (Erstellen, in Betrieb nehmen und Verwalten der Instanzen)
* Speicheroptionen (Block- und Object-Storage)
* Einführung in das Thema API und CLI
* Orchestration (Automatisierung der Cloud-Infrastruktur)

Bitte lesen Sie diese Dokumentation aufmerksam durch bevor Sie unsere Cloud-Umgebung benutzen. So können Sie sich langsam mit dem System vertraut machen.

Sollten Sie zusätzliche Unterstützung benötigen, empfehlen wir Ihnen unsere Schulungen. Informationen dazu finden Sie auf unserer Website unter https://www.cloudlynx.ch/de/Training.

.. note::

Bitte beachten Sie:
Damit Sie die Anweisungen und Erklärungen in dieser Dokumentation erfolgreich umsetzen können, benötigen Sie einen aktiven Cloudlnyx-Zugang.

Grundlegendes zum Erstellen von Instanzen
-----------------------------------------

Um sicher zu gehen, dass neue Instanzen von Anfang an korrekt laufen, ist es sehr wichtig, 

1. dass Sie sie in der richtigen Reihenfolge erstellen.
2. dass Sie alle nötigen Konfigurationen vorgenommen haben.

Gehen Sie nach folgender Reihenfolge vor:

1. Erstellen des Netzwerks
2. Erstellen eines Keypairs
3. Erstellen einer Security Group
4. Erstellen der Instanz mit Hilfe des Netzwerks, der Keypairs und der Security Group

Nachdem Sie all diese Schritte vollzogen haben, können Sie Ihre Instanz in Betrieb nehmen und mit SSH darauf zugreifen.
