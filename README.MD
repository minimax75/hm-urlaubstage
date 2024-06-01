Script-Source: https://homematic-forum.de/forum/viewtopic.php?f=31&t=4058&hilit=feiertag#p23994

# Einrichtung Skript Urlaubstage (ab Version 4)

1. Gehe in der CCU unter "Programme und Verknüpfungen" -> "Programme und Zentralenverknüpfungen" und erstelle ein neues Programm mit der Bedingung, dass dieses 1x täglich (z.B. um 0:01Uhr) ausgeführt wird.
2. Unter Aktivität füge das **Urlaubstage-Complete** Skript ein und setze in den Zeilen 89 und 91 die Systemvariablen **b_debug** und **b_CheckSVs** jeweils auf true und klicke dann einmal auf "Ausführen". Im Ausgabefenster erhälst du nun die Bestätigung, dass die benötigten Systemvariablen automatisch angelegt wurden.
3. Wenn du das **Urlaubstage-Complete** Skript verwenden möchtest, dann setze in den Zeilen 89 und 91 die Systemvariablen **b_debug** und **b_CheckSVs** wieder zurück auf false und klicke dann auf "OK".

__Alternativ__ kannst du aber auch das **Complete-Skript** löschen und durch das identische **Compact-Skript** ersetzen.

**Ergänzender Hinweis**: Die Systemvariable "Urlaubstage" wird vom Complete-Skript automatisch als "Zeichenkette" deklariert. Dadurch wird ermöglicht, dass man die Urlaubsdaten in Apps, wie z.B. PocketControl, direkt eingeben kann. Für den Fall, dass man - wie beim alten Skript V3.01 - die Urlaubsdaten in der WebUI der CCU eingeben möchte, muss man den Typ der Systemvariablen "Urlaubstage" auf "Werteliste" ändern.