# 🏥 VisitaSaúde

Aplicativo mobile desenvolvido em **Flutter** para apoiar **Agentes Comunitários de Saúde (ACS)** durante visitas domiciliares, centralizando consultas essenciais de rotina em uma única interface.

> **Contexto Acadêmico:** Disciplina de Programação para Dispositivos Móveis – Universidade Municipal de São Caetano do Sul (USCS)  
> **Professor:** Prof. Me. Raphael Lopes de Souza  
> **Entrega:** 02/12/2026

---

## 📋 Sobre o Projeto

Agentes Comunitários de Saúde realizam dezenas de atendimentos externos diariamente, lidando com conferência de endereços, variações climáticas e dúvidas frequentes sobre medicamentos. Na prática, essas informações costumam ficar dispersas em anotações de papel, conversas de WhatsApp ou dependem apenas da memória do profissional.

O **VisitaSaúde** surge como uma ferramenta de apoio operacional (não recreativa) para otimizar o tempo em campo e reduzir falhas de consulta durante o atendimento à população.

---

## 📊 Pesquisa de Campo

Para validar a proposta e definir o escopo funcional do aplicativo, foi aplicado um questionário estruturado com **15 Agentes Comunitários de Saúde**. Os dados brutos e gráficos consolidados estão disponíveis na planilha [`pesquisa_campo_visitasaude.xlsx`](./pesquisa_campo_visitasaude.xlsx) (abas *Respostas* e *Resumo*).

### Principais Resultados
* **Volume de atendimento:** Média de **12,8 visitas/dia** (mínimo de 7 e máximo de 20).
* **Uso de tecnologia:** **100%** dos entrevistados já utilizam o celular como ferramenta de trabalho.
* **Métodos atuais de registro:** **33%** utilizam papel, **27%** WhatsApp, **27%** sistemas institucionais e **13%** dependem apenas da memória.
* **Gargalos identificados:** Dificuldade média de **3,6 / 5,0** tanto para localizar endereços quanto para consultar informações de medicamentos.
* **Impacto climático:** **87%** afirmam que condições climáticas interferem diretamente no planejamento das visitas.
* **Aceitação da solução:** Utilidade percebida avaliada em **4,6 / 5,0**, com destaque para pedidos de consulta de CEP, previsão do tempo/chuva, bulário rápido e checklist de visitas.

### Questionário Aplicado
O levantamento contemplou os seguintes indicadores:
1. Profissão e tempo de experiência na área;
2. Média de visitas realizadas por dia;
3. Método atual de registro das visitas;
4. Grau de dificuldade com endereços (escala 1–5);
5. Grau de dificuldade na consulta de medicamentos (escala 1–5);
6. Impacto do clima na rotina de trabalho;
7. Uso de smartphone durante o expediente;
8. Percepção de utilidade do aplicativo (escala 1–5) e funcionalidades desejadas.

---

## 📱 Protótipo e Funcionalidades

Com base nas dores mapeadas na pesquisa, o protótipo de baixa fidelidade foi estruturado em **3 telas principais** conectadas a APIs públicas e acessíveis por meio de uma barra de navegação inferior (*Bottom Navigation Bar*):

| Tela | API Integrada | Funcionalidade |
| :--- | :--- | :--- |
| **Endereço** | [ViaCEP](https://viacep.com.br/) | Consulta rápida por CEP para confirmação de logradouro, bairro e município. |
| **Clima** | [Open-Meteo](https://open-meteo.com/) | Exibe temperatura, umidade, previsão de chuva e alertas de calor com base na localização (geocoding). |
| **Medicamentos** | [openFDA](https://open.fda.gov/) | Busca de indicações por princípio ativo (com tradução automática PT → EN para termos comuns) e aviso de validação em fontes oficiais. |

### Wireframes
Os fluxos e a estrutura visual das três telas podem ser visualizados no arquivo [`docs/Wireframes_do_app_VisitaSaude.png`](./docs/Wireframes_do_app_VisitaSaude.png).

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
* [Flutter SDK](https://docs.flutter.dev/get-started/install) instalado e configurado;
* Emulador Android/iOS ou dispositivo físico com depuração USB ativada.

### Passo a Passo
1. **Clone o repositório e acesse a pasta do projeto:**
   ```bash
   git clone <url-do-repositorio>
   cd visitasaude
   ```

2. **Gere os arquivos nativos das plataformas (caso necessário):**
   ```bash
   flutter create .
   ```

3. **Instale as dependências:**
   ```bash
   flutter pub get
   ```

4. **Verifique a permissão de internet (Android):**
> Certifique-se de que a tag abaixo esteja presente em `android/app/src/main/AndroidManifest.xml` para permitir o consumo das APIs:
   ```XML
   <uses-permission android:name="android.permission.INTERNET" />
   ```

5. **Execute a aplicação:**
   ```Bash
   flutter run
   ```

---
## 👩‍💻 Integrantes
- Verônica Santos Salgado
- Yasmin Silva Santos Galazo
