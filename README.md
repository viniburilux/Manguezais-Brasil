# Manguezais-Brasil

Repositório muito enxuto que contém uma página HTML estática (manguezais-sp/index.html) com um design visual para monitoramento territorial de manguezais (título: "Manguezais SP · Monitoramento Territorial 2018–2024"). Não há código servidor, dados geoespaciais separados, documentação técnica (README), testes, CI/CD ou arquivos de configuração v...

## Auditoria e Potencial (Manus AI)

Este repositório foi auditado e possui um dossiê completo em `docs/AUDITORIA_E_POTENCIAL_MANUS.md`.

### Próximos Passos Sugeridos
- Adicionar README detalhado no nível de repositório: objetivo, escopo geográfico (ex.: SP), período temporal (2018–2024), público-alvo, instruções de reprodução local e plano de manutenção.
- Incluir LICENSE apropriada (ex.: CC-BY/ODbL para dados e MIT/Apache para código) para esclarecer permissões de uso; documentar fontes de dados e atribuições (INPE, IBGE etc.) — se aplicável, registrar como evidência de origem.
- Extrair e versionar dados geoespaciais em um diretório /data com formatos interoperáveis (GeoJSON para visualização, MBTiles/vector tiles para mapas grandes); se os arquivos forem grandes, usar LFS ou armazenamento externo (S3/Cloud Storage) e referenciar links no README.
- Adicionar scripts/notebooks (ex.: scripts Python, Jupyter) para o pipeline ETL com documentação passo a passo para geração dos artefatos de mapa a partir dos dados brutos — melhora reprodutibilidade e auditabilidade.
- Criar uma pipeline de CI/CD (GitHub Actions) que valide HTML/CSS, execute linting, gere/otimize assets e publique automaticamente em GitHub Pages ou outro host (automatizar deploy).
- Se houver mapas interativos planejados: incorporar biblioteca de mapas (Leaflet, MapLibre), documentar fontes de tiles e chaves (não comitar chaves), e validar performance e acessibilidade — adicionar testes básicos de smoke para a camada de visualização.
- Adicionar metadados formais para os datasets (README no /data, metadados ISO/JSON-LD/schema.org), e um arquivo PROVENANCE.md com descrição da origem, data de aquisição, transformações e contato do responsável.
- Implementar práticas básicas de segurança ao publicar: definir Content Security Policy, evitar incluir segredos no repositório, usar SRI para recursos externos quando possível e revisar dependências externas.
- Definir um roadmap mínimo: (1) estabilizar fonte de dados e processamento, (2) automatizar deploy, (3) publicar dataset com metadados e licença, (4) evoluir para API/serviço para suportar integração com LuxVerso/GhostWorks e fluxos de IA.
- Iniciar um pequeno conjunto de exemplos analíticos (notebook) que mostre uso dos dados para detecção de alteração (time series/NDVI), para demonstrar valor para iniciativas IA/dados e atrair colaboradores.