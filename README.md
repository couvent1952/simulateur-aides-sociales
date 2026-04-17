# Vous y avez droit
### Simulateur officieux d'aides sociales françaises

> Outil indicatif de simulation des droits sociaux — APL calculée selon la formule officielle CAF, autres aides via OpenFisca-France, courriers de demande générés par IA.

🔗 **[Accéder au simulateur](https://couvent1952.github.io/simulateur-aides-sociales/)**

---

## Fonctionnalités

- **APL calculée avec la formule officielle CAF** — barèmes 2025 (arrêté du 30/12/2024), zonage géographique (zones 1, 2, 3), détail ligne à ligne du calcul
- **Connexion OpenFisca-France** — RSA et prime d'activité calculés en temps réel via `api.fr.openfisca.org`
- **22 aides référencées** — minima sociaux, logement, famille, emploi, santé, retraite
- **5 profils types** — Sophie (mère isolée), Mohamed (salarié modeste), Claire (étudiante), Jacques (retraité), Amira (en reconversion)
- **Génération de courriers par IA** — lettre formelle personnalisée pour chaque aide éligible, avec pièces justificatives à joindre
- **Application autonome** — un seul fichier HTML, aucune installation, fonctionne dans tout navigateur

---

## Aides couvertes

| Catégorie | Aides |
|-----------|-------|
| Minima sociaux | RSA, Prime d'activité, AAH, ASS, ASPA |
| Logement | APL, ALS/ALF, FSL, Visale |
| Famille | Allocations familiales, Complément familial, ASF, PAJE, AEEH |
| Emploi | ARCE, ACRE |
| Santé | CSS, AJPA, PCH |
| Retraite | ASPA, APA |
| Situations précaires | Aide violences conjugales, ATA (réfugiés) |

---

## Utilisation

### En local
```bash
# Cloner le dépôt
git clone https://github.com/couvent1952/simulateur-aides-sociales.git

# Ouvrir dans le navigateur
open index.html
```

### En ligne
Le simulateur est hébergé via **GitHub Pages** à l'adresse :
`https://couvent1952.github.io/simulateur-aides-sociales/`

---

## Sources & références

| Source | Usage |
|--------|-------|
| [Arrêté du 30/12/2024 (JO)](https://www.legifrance.gouv.fr) | Barèmes APL 2025 |
| [OpenFisca-France](https://api.fr.openfisca.org) | Calcul RSA, prime d'activité |
| [API Anthropic Claude](https://api.anthropic.com) | Génération des courriers |
| [CAF](https://www.caf.fr/allocataires/aides-et-demarches/mes-demarches) | Simulateur officiel (lien) |

---

## Limites & avertissements

> **Cet outil est indicatif et sans valeur juridique.**

- Les montants affichés sont des estimations basées sur les barèmes 2025
- La génération des courriers et le calcul OpenFisca nécessitent une connexion internet
- La génération des courriers utilise l'API Anthropic (Claude) — une clé API est nécessaire pour cet usage en production
- Seule une demande officielle auprès de la CAF, CPAM ou France Travail a valeur de droit
- L'API CAF (données réelles de l'allocataire) est réservée aux acteurs publics habilités

---

## Stack technique

- **HTML/CSS/JS vanilla** — aucun framework, aucune dépendance npm
- **Google Fonts** — Syne + DM Sans
- **OpenFisca-France API** — `https://api.fr.openfisca.org/calculate`
- **Anthropic API** — `claude-sonnet-4-20250514` pour la génération des courriers

---

## Contribuer

Les barèmes évoluent chaque année (janvier et octobre). Pour mettre à jour :

1. Modifier les constantes `APL_PL`, `APL_FC`, `APL_R0` dans `index.html`
2. Mettre à jour les montants des aides dans le tableau `AIDES`
3. Ouvrir une Pull Request avec les sources officielles (arrêtés au JO)

---

## Licence

MIT — libre d'utilisation, de modification et de redistribution.

---

*Construit avec Claude (Anthropic) · Barèmes : arrêté du 30/12/2024 · OpenFisca-France*
