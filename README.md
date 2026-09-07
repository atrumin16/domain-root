# trujillomingorance.com — Root Domain Edge Gateway & Wildcard 404

[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-Deployed-F38020?style=flat-square&logo=cloudflare&logoColor=white)](https://trujillomingorance.com)
[![Status](https://img.shields.io/badge/Status-Operational-107c41?style=flat-square)](#)
[![Design](https://img.shields.io/badge/Design_System-Mica_Corporate-0078d4?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-Proprietary-blue?style=flat-square)](#)

> **Root Gateway:** [trujillomingorance.com](https://trujillomingorance.com)  
> Enrutador perimetral de nivel raíz y manejador de diagnósticos wildcard 404 para todo el dominio apex `trujillomingorance.com`.

---

## 🧭 Funcionalidad

1. **Redirección Canónica Apex**: Reenvía automáticamente el tráfico entrante del dominio raíz hacia el portal central [labs.trujillomingorance.com](https://labs.trujillomingorance.com) de forma instantánea.
2. **Diagnóstico Perimetral Wildcard (404)**: Interfaz de fallback corporate mica cuando un usuario o bot consulta un subdominio inexistente o una ruta huérfana, con inspector dinámico de cabeceras Cloudflare Edge (Ray ID, IP, Datacenter, Protocolo HTTP/3).

---

## 🌿 Enterprise Branching Model

| Branch | Purpose | Deployment Target |
| :--- | :--- | :--- |
| `main` | **Production Release** | Deployed live to `trujillomingorance.com` apex |
| `develop` | **Staging & Route Testing** | Routing rules, redirect validations & 404 template testing |

---

## 📁 Repository Structure

```
domain-root/
├── _headers             # Security headers, HSTS, and edge caching rules
├── _redirects           # Apex root redirection rules to labs.trujillomingorance.com
├── 404.html             # Corporate mica diagnostic error page with Cloudflare Ray ID telemetry
├── index.html           # Edge fallback landing page
└── wrangler.toml        # Cloudflare Pages deployment configuration
```

---

## 🚀 Despliegue en Cloudflare Pages

```bash
npx wrangler pages deploy . --project-name domain-root --commit-dirty=true
```

---

## 👤 Autor

**Alberto Trujillo Mingorance**  
- Portfolio: [alberto.trujillomingorance.com](https://alberto.trujillomingorance.com)  
- GitHub: [@atrumin16](https://github.com/atrumin16)
