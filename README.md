# attendo.hailo.mx

Página de diagnóstico pitch construida específicamente para Attendo.

**Tipo:** landing estática single-page (HTML + CSS embebido, sin build, sin backend).
**Stack:** HTML5 + CSS3 puro + Tailwind-like utility classes inline · Google Fonts (Inter + JetBrains Mono).
**Tamaño:** ~50 KB de HTML, 2 PNGs.

## Estructura

```
attendo.hailo.mx/
├── index.html              # Página completa, todo embebido
├── README.md               # Este archivo
└── assets/
    ├── attendo-logo.png    # Wordmark Attendo (top bar + email signature)
    └── favicon.png         # Isotipo Attendo (browser tab)
```

## Secciones

1. **Hero** — Stat strip con 7 datos clave + CTA
2. **01 · Contexto** — Quiénes son (SOFOM, modelo, productos, liderazgo)
3. **02 · Stack** — Las 8 capas técnicas verificadas
4. **03 · Operaciones** — Las 5 lanes operativas reales
5. **04 · Brechas** — 8 brechas críticas con su fuente
6. **05 · Oportunidades** — 9 iniciativas en 3 tiers
7. **06 · Wedge** — Por qué empezar con Agente WhatsApp
8. **07 · Roadmap** — Plan 6 meses en 4 fases
9. **08 · Impacto** — KPIs esperados
10. **CTA final** — Agendar diagnóstico

## Ver en local

```bash
open index.html
```

O servir en puerto local:

```bash
cd "attendo.hailo.mx"
python3 -m http.server 8080
# abrir http://localhost:8080
```

## Deploy a `attendo.hailo.mx`

Pasos estándar HAILO:

1. **Repo en GitHub** (organización `hailomx`):
   ```bash
   cd attendo.hailo.mx
   git init && git add . && git commit -m "Initial: diagnostic pitch page"
   gh repo create hailomx/attendo --public --source=. --push
   ```

2. **Vercel** — importar repo `hailomx/attendo` como proyecto estático (sin framework).

3. **Custom domain en Vercel** — agregar `attendo.hailo.mx`.

4. **DNS en Cloudflare** (zona `hailo.mx`):
   ```
   CNAME  attendo  →  cname.vercel-dns.com  (Proxied OFF)
   ```

5. **Esperar SSL** (~1 min) y verificar.

## Iteración

La página es 100% estática y no tiene dependencias de build. Cualquier cambio se hace editando `index.html` directamente y empujando al repo — Vercel re-despliega automático.

## Notas de uso

- **Confidencialidad:** la página se hizo con inteligencia 100% pública. Nada filtrado o privado. Es safe enviarla por correo a Attendo.
- **Branding:** sigue el estándar visual HAILO (dark, mono accents, premium). Si HAILO tiene un logo SVG/PNG más adelante, sustituir el wordmark CSS por `<img>` en el top bar.
- **Personalización:** las cifras son fijas (las verificadas). Si en la junta surge dato nuevo, editar `index.html`.

---

*Generada 2026-05-22 · HAILO design+intel desk.*
