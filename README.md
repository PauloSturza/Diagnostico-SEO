# Diagnostico-SEO


[![Built with n8n](https://img.shields.io/badge/Powered%20by-n8n-213355?style=flat-square)](https://n8n.io/)

Solução automatizada para coleta e preenchimento de informações sobre o dominio do cliente e de concorrentes. Os indicadores  Autoridade de domínio, Tráfego geral e número de Backlinks são encontrados através da API DataForSEO e preenchidos em uma aba de uma planilha Google Sheets. Enquanto as principais keywords, a quantidade pode ser escolhida pelo usuário, são preenchidas em uma outra aba da mesma planilha onde também são preenchidos os dados Volume, Dificuldade, Rank Médio, a URL onde ela aparece e a intenção de busca de cada uma das keywords. O objetivo da automação é facilidar a análise SEO de um cliente e seus concorrentes de maneira rápida e eficiente.

##  Fluxo de Trabalho
1. **Busca Sites** que serão analisados
2. **Busca os dados sobres as principais Keywords dos sites** via DataForSEO API
3. **Preenche os dados das Keywords na planilha** tanto as keywords principais quanto as métricas.
4. **BVerifica as Keywords que aparecem em mais de um site** e preenche essas informações na aba Keywords Gaps da planilha
5. **Busca os Backlinks, DA e Tráfego geral de cada site** no e preenche na aba Cenário Geral da PLanilha
   
## Fluxo Principal
<img width="921" height="406" alt="Captura de tela 2025-08-12 164553" src="https://github.com/user-attachments/assets/31a171e5-981c-4f59-9479-92f0f8dc7e69" />

## Exemplo de preenchimento de uma execução

 Os dados iniciais dados foram preenchidos na coluna "Site"
 
<img width="1080" height="80" alt="Captura de tela 2025-08-12 165016" src="https://github.com/user-attachments/assets/b4918cbb-6252-4d5f-be53-c29abbbfac57" />

 Essas são as keywords extraídas dos domínios, para este exemplo foram buscadas as 10 principais keywords dos dominios dados

<img width="1230" height="443" alt="Captura de tela 2025-08-12 165244" src="https://github.com/user-attachments/assets/d61a46ee-d395-444a-8709-cad50bec5a20" />


##  Configuração
Variáveis obrigatórias:
| Parâmetro          | Descrição                             |
|--------------------|---------------------------------------|
| `Planilha Sheets`  | Link da planilha com os dados         |
| `username`         | ID da conta DataForSEO                 |
| `password` | Senha da conta DataForSEO   |
| `Sites a serem eanalisados`        | Na Planilha devem estar preenchidos os dominios que serão anlisados           |

##  Como Usar
1. Importe o fluxo JSON no n8n
2. Configure as variáveis distribuídas nos nós
4. Conecte sua planilha Google
5. Execute o Workflow


##  Pré-requisitos
- Conta DataForSEO com acesso API
- Planilha Google pré-configurada
- Instância n8n (v0.152.0+)
