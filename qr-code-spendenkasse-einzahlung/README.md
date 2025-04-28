# QR Code für die Einzahlung aus der Spendenkasse

Dieser Code kann genutzt werden, um eine Bareinzahlung mit dem richtigen Betreff etc. auf das Konto zu machen.

Dafür einfach mit der Bank-App einscannen und den Betrag angeben.

Der entsprechende Standard:
https://de.wikipedia.org/wiki/EPC-QR-Code

Bilddaten von .txt updaten: `ninja` ausführen (benötigt: `qrencode(1)`, `ninja(1)`)

Wichtig: Wenn die `.txt` geändert wird, darf *kein* `\n` (`0x0a`) am Ende der letzten Zeile sein.
Viele Editoren (z.B. vim) machen das automatisch beim Speichern, aber dann ist der generierte QR-Code kaputt.
Dafür mit `hexdump -C qr-code-spendenkasse-einzahlung.txt` schauen, und falls das letzte byte `0x0a` ist
`truncate -s -1 qr-code-spendenkasse-einzahlung.txt` ausführen um es zu entfernen.


