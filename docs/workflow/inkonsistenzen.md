# Inkonsistenzen in der Datenbank finden

Mit dem Befehl 

```bash
php artisan kb:doctor -vv
```

lassen sich Inkonsistenzen in der Datenbank auffinden.

Mit der Option `--clean` lassen sich die meisten Inkonsistenzen bereinigen. Bei den Autoren/Komponisten von Literatur- und Liedeinträgen (`bibls_contributors`, `songs_contributors`) sollte die Bereinigung manuell erfolgen.
