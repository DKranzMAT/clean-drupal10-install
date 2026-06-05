Key files:

- `fa_demo.info.yml` – Declares the theme, base theme, and libraries
- `fa_demo.libraries.yml` – Registers `global-styling` and attaches `css/style.css`
- `templates/html.html.twig` – Full HTML document wrapper
- `templates/page.html.twig` – Implements the one-page layout (hero, impact strip, three pillars)
- `css/style.css` – Design tokens, layout, and component styles

### Layout Highlights

- **Hero** – Deep navy background, Playfair Display headline, gold rule lines, red + outlined CTAs
- **Impact Strip** – 250 years · 50 states · 27 amendments · 330M Americans
- **Three Pillars** – Liberty / Unity / Legacy
- **Typography** – Playfair Display (headlines), EB Garamond (body), Cinzel (labels)

---

## Local Setup

1. Install dependencies:

```bash
   composer install
```

2. Add MAMP's PHP to your PATH:

```bash
   export PATH="/Applications/MAMP/bin/php/php8.3.30/bin:$PATH"
```

3. Update your database connection in `web/sites/default/settings.php`:

```php
   $databases['default']['default'] = [
     'database' => 'drupal_simple',
     'username' => 'root',
     'password' => 'root',
     'host' => 'localhost',
     'port' => '8889',
     'driver' => 'mysql',
   ];
```

4. Rebuild caches:

```bash
   DRUSH_NO_MIN_PHP=1 ./vendor/bin/drush cr
```

5. Enable and set the theme as default:

```bash
   DRUSH_NO_MIN_PHP=1 ./vendor/bin/drush theme:enable fa_demo
   DRUSH_NO_MIN_PHP=1 ./vendor/bin/drush config:set system.theme default fa_demo -y
```

6. Visit `http://localhost:8888` to preview.

---

## 🎨 Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--a250-navy` | `#0A1628` | Hero background |
| `--a250-blue` | `#002868` | Impact strip |
| `--a250-red` | `#BF0A30` | Accent buttons, rules |
| `--a250-gold` | `#C9A84C` | Headlines, labels, borders |
| `--a250-cream` | `#F8F4EC` | Page background |

---

## Notes

- Easily extendable: add blocks, views, or content types as needed.
- Drush requires `DRUSH_NO_MIN_PHP=1` prefix when running on MAMP PHP 8.2/8.3.

---

**Author:** [David Kranz](https://github.com/DKranzMAT)  
**Repo:** [clean-drupal10-install](https://github.com/DKranzMAT/clean-drupal10-install)