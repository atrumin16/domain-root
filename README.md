# trujillomingorance.com — Root Domain Edge Gateway & Wildcard 404

[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-Deployed-F38020?logo=cloudflare&logoColor=white)](https://trujillomingorance.com)
[![Status](https://img.shields.io/badge/Status-Operational-107c41)](#)
[![Design](https://img.shields.io/badge/Design_System-Mica_Corporate-0078d4)](#)

> **Root Gateway:** [trujillomingorance.com](https://trujillomingorance.com)

Enrutador perimetral de nivel raíz y manejador de diagnósticos wildcard 404 para todo el dominio apex `trujillomingorance.com`.

---

## 🧭 Funcionalidad

1. **Redirección Canónica Apex**: Reenvía automáticamente el tráfico entrante del dominio raíz hacia el portal central [labs.trujillomingorance.com](https://labs.trujillomingorance.com) de forma instantánea.
2. **Diagnóstico Perimetral Wildcard (404)**: Interfaz de fallback corporate mica cuando un usuario o bot consulta un subdominio inexistente o una ruta huérfana, con inspector dinámico de cabeceras Cloudflare Edge (Ray ID, IP, Datacenter, Protocolo HTTP/3).

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
