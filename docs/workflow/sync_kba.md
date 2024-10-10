# Synchronisieren der Vorlagen (sources) ins Karl Barth-Archiv (KBA)

## Quellen (Meta) / Verzeichnungseinträge (Anton)

Mit dem Antonbefehl

```bash 
php artisan kbga:update-edition-data --env kba
```

werden in Anton die Infos von der API https://meta.karl-barth.ch/api/anton-sources gespeichert und damit wird eine Ansicht der Edition in Anton angezeigt. 

https://meta.karl-barth.ch/api/anton-sources gibt die Quellen zurück die in der Produkivumgebung publiziert sind.

## Actors und Places

Anton: 

```bash
php artisan beacon:read --url http://kb.test/api/places\?format\=beacon\&provider\=kba --entity place --env kba --provider kbga --save

art beacon:read --url http://kb.test/api/actors\?format\=beacon\&provider\=kba --entity actor --env kba --provider kbga --save
```
