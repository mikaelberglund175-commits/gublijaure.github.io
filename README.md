# Gublijare Production – hemsida

Statisk sida (ingen byggprocess, inga externa typsnitt/skript). Filer:

- `index.html` – startsida: berättelsen, spel (Mosquito med skärmdumpar), husregler, Google-noter, Ko-fi-dricksburk. Språk sv/en/fi.
- `privacy.html` – integritetspolicy + ansvarsfriskrivning på sv/en/fi (krävs av Google Play).
- `img/` – skärmdumpar och ikon, `favicon.png`.

## Länkar som spelet använder
Domän: **gublijaure.com** (filen `CNAME`). Repo: github.com/gublijare/gublijare.github.io.
Spelet öppnar `https://gublijaure.com/?app=1&lang=xx` och `https://gublijaure.com/privacy.html?lang=xx`.
`?app=1` döljer Ko-fi-rutan (Google Play tillåter inte länkar till andra betalsätt från appen).

## Ladda upp ändringar
Dubbelklicka `publish_to_github.bat` – den committar och pushar allt till GitHub.

## DNS hos domänleverantören
A-poster för `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
CNAME `www` → `gublijare.github.io`

## Publicera på GitHub Pages (första gången)
1. Skapa ett GitHub-konto/organisation som heter **gublijare** (annars blir adressen en annan – ändra då
   `HomeUrl` i `MosquitoGame.cs` och URL:erna i `store/RELEASE.md` + listingtexterna).
2. Skapa repot **gublijare.github.io** (publikt).
3. I den här mappen:
   ```
   git init
   git add .
   git commit -m "Gublijare Production hemsida"
   git branch -M main
   git remote add origin https://github.com/gublijare/gublijare.github.io.git
   git push -u origin main
   ```
4. Settings ▸ Pages ▸ Source: *Deploy from a branch*, `main` / root. Sidan är uppe efter någon minut.

## Att fylla i innan release
- **Kontakt-e-post** i `privacy.html` (sök `[e-post`) – Google Play kräver en riktig adress.
- **Ko-fi**: skapa sidan på ko-fi.com och kontrollera att `https://ko-fi.com/gublijare` stämmer (sök `ko-fi.com` i `index.html`).
- **Google Play-knappen** pekar redan på `play.google.com/store/apps/details?id=com.gublijare.mosquito`;
  ta bort texten "kommer snart" (`playSoon` i alla tre språk) när appen är live.
- Tidslinjen: kontrollera årtalen (1996 = trettio år sedan) så att de stämmer med din historia.
