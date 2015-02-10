Übertragen von Dateien
==============


Übertragen von Dateien in eine Linux-Instanz und von einer Linux-Instanz (mitsamt des hinzugefügten Volumes)
------------------------------------------------------------------------------------------------------------

Dateien können in eine Linux-Instanz und von einer solchen mit scp und sftp übertragen werden. Versichern Sie sich jedoch zuerst, dass der öffentliche Schlüssel der Instanz hinzugefügt wurde und Port 22 offen ist.

Übertragen von Dateien mit scp (secure remote copy)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wie Dateien in eine Instanz und von einer solchen übertragen werden, hängt im Wesentlichen vom lokalen Betriebssystem ab.

scp zwischen einem lokalen Linux-Client und einer Linux-Instanz
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

**Um Dateien von einem lokalen Rechner in eine Instanz in der Cloud zu verschieben, gehen Sie folgendermassen vor:**

1. Wenn Sie OpenSSH noch nicht installiert haben, installieren Sie es jetzt.
2. Fügen Sie dem ssh agent Ihren privaten Schlüssel hinzu.
3. Führen Sie im Terminal folgenden Befehl aus:

     scp <source file> <username of instance>@<instance IP>:<destination file>
     
Ersetzen Sie <source file> durch den Pfad, der zu der zu kopierenden Datei führt, und <destination file> durch den gewünschten Zielort. Die IP der Instanz entspricht der Floating IP, die über das Internet erreichbar ist.

**Um eine Datei aus der Instanz in der Cloud zu ihrem lokalen Dateisystem zu verschieben, gehen Sie folgendermassen vor:**

1. Führen Sie im Terminal folgenden Befehl aus:

     scp <username of instance>@<instance IP>:<source file> <destination file>
     
Hier entspricht <destination file> der Datei auf Ihrem lokalen Rechner.


.. note::
   Mit scp können Sie auch Dateien von einer Instanzen in der Cloud in eine andere kopieren. 


scp zwischen einem lokalen Windows-Rechner und einer Linux-Instanz
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""" 

Mit WinSCP können Sie Dateien von einem Windows-Rechner in eine Linux-Instanz kopieren und umgekehrt. Sie können auf Ihrem lokalen Windows-Rechner pageant laufen lassen. Wenn Sie PuTTY zur SSH-Verbindung benutzen, fügen Sie zur bequemeren Verwaltung Ihren privaten Schlüssel hinzu.

1. Starten Sie WinSCP und klicken Sie auf die Schaltfläche **New Site**.
2. Klicken Sie rechts auf die Schaltfläche **Advanced**. Ein neues Fenster erscheint.
3. Klicken Sie danach auf **SSH** und dann links auf **Authentication**.
4. Aktivieren Sie das Kontrollkästchen **Allow agent forwarding** unter **Authentication parameters**.
5. Geben Sie den Ablageort des privaten Schlüssels in das Feld **Private key file** ein. Dies sollte im Format .ppk sein. 
6. Klicken Sie auf die Schaltfläche **OK**, um das Fenster **Advanced Site Settings** zu schliessen.
7. Als Protokoll wählen Sie scp aus dem **File protocol**-Dropdown-Menü aus. 
8. Geben Sie in das Feld **Host name** die Floating-IP-Adresse der Instanz ein, zu der eine Verbindung hergestellt werden soll. 
9. Im Feld **User name** geben Sie den Benutzer der Instanz ein. 
10. Klicken Sie auf die Schaltfläche **Save**, um die Einstellungen zu sichern.
11. Klicken Sie auf die Schaltfläche **Login**, damit sich die Verbindung zur Instanz über scp aufbaut. Nun erscheint ein Fenster mit einer graphischen Benutzerschnittstelle, über die Sie die Dateien zwischen Ihrem lokalen Rechner und der Instanz verschieben können.

.. note::
   Sollten Sie keine Verbindung herstellen können, vergewissern Sie sich bitte, dass Pageant ausgeführt wird und den privaten Schlüssel .ppk enthält.


Verwalten von Dateien in Object Storage
----------------------------------------

Dieser Abschnitt betrifft nur Windows! Für Linux empfehlen wir die Benutzung des CLI Client (SWIFT).
Sie können Object Storage auch mit einem SWIFT/S3 Browser benutzen. In unserem Beispielfall benutzen wir Cyberduck. Andere mögen auch funktionieren. 

1. Loggen Sie sich in das Cloudlynx-Dashboard ein. 

2. Klicken Sie auf den Menüunterpunkt **Access & Security**, den Sie unter **Manage Compute** finden.

3. Öffnen Sie den Reiter **API Access**.

4. Klicken Sie auf die Schaltfläche **Download EC2 Credentials**.

5. Laden Sie die Zip-Datei herunter und öffnen Sie sie. 

6. Starten Sie Cyberduck.

7. Klicken Sie auf die Schaltfläche.

8. Wählen Sie S3 (Amazon Simple Storage Service) aus dem Dropdown-Menü. 

9. Geben Sie in das Feld Server api.preview.cloudlynx.ch ein

10. Öffnen Sie die heruntergeladene Zip-Datei aus dem Dashboard, und öffnen Sie dann die ec2rc-Datei in Notepad oder einem anderen Text-Editor.

11. Suchen Sie die Angaben zu EC2_ACCESS_KEY und kopieren Sie sie in das Feld **Access Key ID** in Cyberduck.

12. Suchen Sie die Angaben zu EC2_ACCESS_KEY und kopieren Sie sie in den **Secret Access Key** in Cyberduck.

13. Klicken Sie auf die Schaltfläche **Connect**.

14. Vielleicht werden Sie aufgefordert, den Schlüssel Ihrem lokalen Schlüsselspeicher hinzuzufügen. 
