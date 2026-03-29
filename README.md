# RF DRIVE – Calculadora de Corridas

Aplicativo web para motoristas do grupo **RF DRIVE** calcularem corridas com base em rota real no mapa, usando **Google Maps**.

## Funcionalidades

### Etapa 1 – Cálculo por KM com Rota Real
- Campos de **Origem** e **Destino** com autocomplete via Google Places
- Mapa interativo (Google Maps com tema escuro) com rota traçada em dourado
- Distância real (km) e tempo estimado via Google Directions
- Cálculo automático: `valor = max(R$10, km × R$2,10)`
- Clique no mapa para definir pontos diretamente (geocodificação reversa via Google)

### Etapa 2 – Ferramentas para Motoristas
- **Compartilhar no WhatsApp** com origem, destino, distância e valor
- **Gerar orçamento** formatado (copiável para área de transferência)
- **Histórico de corridas** salvo em `localStorage` (últimas 30)
- **Rota no Google Maps** — abre a rota de origem a destino no Google Maps para navegação por voz

### Etapa 3 – Personalização
- **Corrida personalizada**: toggle para ajuste manual do valor final
- **Configurações editáveis**: valor por km, valor mínimo e API Key do Google Maps persistidos em `localStorage`
- Exibe cálculo original e ajustado simultaneamente

## Design
- Tema escuro premium — preto `#0b0b0b` · dourado `#D4AF37` · branco `#ffffff`
- Layout mapa (70 %) + painel lateral (30 %)
- Responsivo — prioridade mobile

## Tecnologias (sem instalação necessária)
| Serviço | Uso |
|---------|-----|
| [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript) | Mapa interativo com tema escuro |
| [Google Places API](https://developers.google.com/maps/documentation/places/web-service) | Autocomplete de endereços |
| [Google Directions API](https://developers.google.com/maps/documentation/directions) | Cálculo de rota real e tempo estimado |
| [Google Geocoding API](https://developers.google.com/maps/documentation/geocoding) | Geocodificação reversa (clique no mapa) |

## Como usar
1. Obtenha uma [chave da API do Google Maps](https://console.cloud.google.com/apis/credentials) com as APIs: Maps JavaScript, Places, Directions e Geocoding habilitadas.
2. Abra `index.html` em qualquer navegador moderno. Sem build, sem servidor necessário.
3. Na primeira vez, o sistema pedirá a chave da API. Ela também pode ser configurada em **Configurações**.
