# RF DRIVE – Calculadora de Corridas

Aplicativo web para motoristas do grupo **RF DRIVE** calcularem corridas com base em rota real no mapa.

## Funcionalidades

### Etapa 1 – Cálculo por KM com Rota Real
- Campos de **Origem** e **Destino** com autocomplete via Nominatim (OpenStreetMap)
- Mapa interativo (Leaflet + CartoDB Dark) com rota traçada em dourado
- Distância real (km) e tempo estimado via OSRM
- Cálculo automático: `valor = max(R$10, km × R$2,10)`
- Clique no mapa para definir pontos diretamente

### Etapa 2 – Ferramentas para Motoristas
- **Compartilhar no WhatsApp** com origem, destino, distância e valor
- **Gerar orçamento** formatado (copiável para área de transferência)
- **Histórico de corridas** salvo em `localStorage` (últimas 30)

### Etapa 3 – Personalização
- **Corrida personalizada**: toggle para ajuste manual do valor final
- **Configurações editáveis**: valor por km e valor mínimo persistidos em `localStorage`
- Exibe cálculo original e ajustado simultaneamente

## Design
- Tema escuro premium — preto `#0b0b0b` · dourado `#D4AF37` · branco `#ffffff`
- Layout mapa (70 %) + painel lateral (30 %)
- Responsivo — prioridade mobile

## Tecnologias (sem instalação necessária)
| Lib | Uso |
|-----|-----|
| [Leaflet.js](https://leafletjs.com/) | Mapa interativo |
| [Nominatim](https://nominatim.openstreetmap.org/) | Autocomplete e geocodificação reversa |
| [OSRM](https://project-osrm.org/) | Cálculo de rota real |
| CartoDB Dark tiles | Tiles de mapa escuro |

## Como usar
Abra `index.html` em qualquer navegador moderno. Sem build, sem servidor necessário.
