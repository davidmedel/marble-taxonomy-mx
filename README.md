# Marble Taxonomy MX 🇲🇽

Extensión mexicana de [Marble Skill Taxonomy](https://github.com/withmarbleapp/os-taxonomy) para **Grupo Educativo Banting (GEB)** y [Brighting AI Engine](https://github.com/davidmedel/brighting-ai-editorial).

## ¿Qué es esto?

Este fork extiende la taxonomía original de Marble (1,590 micro-topics, estándares US/UK) con:

- 🌐 **Traducción al español mexicano** de topics, evidence criteria y assessment prompts
- 🇲🇽 **Mapeo a estándares SEP** (Programa de Desarrollo de Aprendizaje — PDA)
- 📚 **Nuevos topics** específicos del currículo mexicano
- 👨‍👩‍👧 **Clusters para padres** en español

## Licencia

Este fork mantiene la licencia original:

| Capa | Licencia |
|---|---|
| Base de datos (topics, dependencias, relaciones) | [ODbL 1.0](LICENSE) |
| Contenido textual (descripciones, traducciones) | [CC BY-SA 4.0](LICENSE-CONTENT) |
| Estándares curriculares originales | Ver [PROVENANCE.md](PROVENANCE.md) |

## Upstream

- **Original:** [withmarbleapp/os-taxonomy](https://github.com/withmarbleapp/os-taxonomy)
- **Sincronización:** `git fetch upstream && git merge upstream/main`

## Estructura

```
data/
├── topics.json              ← Original + traducciones ES
├── topics_es.json           ← Mapeo rápido: id → nombre, descripción ES
├── dependencies.json        ← Original + nuevos edges
├── curriculum-standards.json ← Original + SEP México
├── clusters.json            ← Clusters originales
├── clusters_es.json         ← Clusters traducidos al español
└── manifest.json            ← Checksums actualizados

scripts/
├── validate.mjs             ← Validación extendida (incluye integridad .json ES)
└── translate.mjs            ← Pipeline de traducción DeepSeek
```
