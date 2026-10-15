# Timmeren met Willemsen

Statische versie van kees-willemsen.nl. Gebouwd met Jekyll, gehost op GitHub Pages en te bewerken via [Pages CMS](https://pagescms.org).

## Structuur

- `_posts/` – één markdown-bestand per klusproject (titel, datum, tekst en foto's)
- `assets/images/` – alle foto's
- `_layouts/`, `assets/css/style.css` – opmaak
- `.pages.yml` – configuratie voor Pages CMS

Staan er meerdere foto's direct onder elkaar (zonder lege regel ertussen), dan worden ze als galerij getoond.

## Live zetten

1. Maak een repo aan op GitHub en push deze map.
2. Ga naar **Settings → Pages**, kies *Deploy from a branch*, branch `main`, map `/ (root)`.
3. Vul bij **Custom domain** `kees-willemsen.nl` in (het `CNAME`-bestand staat al klaar) en vink daarna *Enforce HTTPS* aan.
4. Zet bij je domeinprovider de DNS om:
   - A-records voor `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - CNAME voor `www`: `<github-gebruikersnaam>.github.io`

## Bewerken met Pages CMS

1. Ga naar https://app.pagescms.org en log in met GitHub.
2. Geef Pages CMS toegang tot de repo en open hem.
3. Onder **Klusprojecten** kun je projecten toevoegen of aanpassen. Foto's upload je via **Media**.

Elke wijziging is een commit, en GitHub Pages publiceert de site binnen een minuut opnieuw.

## Lokaal bekijken (optioneel)

```bash
bundle install
bundle exec jekyll serve
```
