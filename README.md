# 📚 Librolandia (Arcana)

Biblioteca abierta: **un solo buscador para libros de acceso libre**, sin registro y sin API key.

**▶ En vivo:** https://jpm70.github.io/Librolandia/

Parte del proyecto [Un Fantasma en el Sistema](https://www.unfantasmaenelsistema.com).

## Qué hace
- Busca a la vez en dos colecciones y muestra los resultados juntos, con portada, autor, año e idioma.
- Filtra por idioma (español, inglés, francés, alemán, italiano, portugués, ruso, chino, japonés, árabe y latín) y por fuente.
- Ofrece descarga directa (EPUB, MOBI, TXT, HTML, PDF) cuando el libro es de dominio público o de acceso libre.

## Fuentes
| Fuente | Qué aporta |
|---|---|
| [Project Gutenberg](https://www.gutenberg.org) (vía [Gutendex](https://gutendex.com)) | Dominio público, descarga directa |
| [Open Library](https://openlibrary.org) / [Internet Archive](https://archive.org) | Catálogo enorme; solo se ofrece EPUB/PDF cuando el libro es de acceso público (los de préstamo llevan únicamente el enlace a Open Library) |

Todo se consulta desde el navegador con `fetch`; no hay servidor ni claves.

## Limitaciones
- Gutendex es un servicio comunitario y a veces tarda o no responde. Cada consulta tiene un límite de 10 s con un reintento, y si una fuente cae, la otra sigue mostrando resultados.
- Los resultados dependen de lo que devuelvan esas APIs en cada momento.
- Se retiró Standard Ebooks: su catálogo OPDS ahora exige una cuenta de Patrons Circle y ya no se puede consultar desde una web pública.

## Desarrollo local
Es un único `index.html` estático:

```bash
python -m http.server 8000
```

## Aviso
Solo se enlaza a obras de dominio público o de acceso libre alojadas por sus colecciones. Proyecto educativo y sin ánimo de lucro.
